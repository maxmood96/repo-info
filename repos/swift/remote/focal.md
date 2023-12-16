## `swift:focal`

```console
$ docker pull swift@sha256:12f2ac154ebfa4ca88463469af0f1a19a14bd966acdb0d2df1b50ccf3e642f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:2d7f6880bd79d2b025dec6d4bffd04cf40f3f4d52a0ce093df6139ed1cd378ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **755.8 MB (755769930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdc241aadd210f43348821f2f0dd0f7041f4073042b170b64a5aa409836de64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 03:18:41 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 02 Dec 2023 03:18:41 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 02 Dec 2023 03:20:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Sat, 02 Dec 2023 03:20:39 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 02 Dec 2023 03:20:39 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 12 Dec 2023 00:25:46 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Tue, 12 Dec 2023 00:25:46 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Tue, 12 Dec 2023 00:25:46 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 Dec 2023 00:25:46 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 Dec 2023 00:26:36 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Tue, 12 Dec 2023 00:26:42 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e0cce1dead2294bfc5a82cd6c634f5832a864d1155efeae7fab09fdf511ee`  
		Last Modified: Sat, 02 Dec 2023 03:42:30 GMT  
		Size: 120.5 MB (120499516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccd808560fa8a5f43bc769ffc82db217c058d3eff1b9b19b9a7b086b349bf4e`  
		Last Modified: Tue, 12 Dec 2023 00:39:59 GMT  
		Size: 606.7 MB (606686185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610407b756124994de44925530b7c4d397e2bab7653ebfd98a1ec3f779d2f725`  
		Last Modified: Tue, 12 Dec 2023 00:38:37 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:9ef8b3ebd8a6f95a3351a2997532abce341b2ab7dfdf956c6df6263947e58d01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.2 MB (745182766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130d9cb636f23bbb523d7a43a1a1b487b3b91e9c1e513ec951db4d026aced204`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 12:02:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 16 Dec 2023 12:02:33 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 16 Dec 2023 12:05:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Sat, 16 Dec 2023 12:05:31 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 16 Dec 2023 12:05:31 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Sat, 16 Dec 2023 12:05:31 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Sat, 16 Dec 2023 12:05:31 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Sat, 16 Dec 2023 12:05:31 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 16 Dec 2023 12:05:31 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 16 Dec 2023 12:06:08 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Sat, 16 Dec 2023 12:06:20 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7f393beba825f6d6e4b7b850be8de5ca1bf68e2e4a40d0031e68b7ca30c46d`  
		Last Modified: Sat, 16 Dec 2023 12:17:29 GMT  
		Size: 117.3 MB (117281537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698cd26a853dbcc1351619358ab8f7da97f62d1b9fd6c37d82f389e96191fc86`  
		Last Modified: Sat, 16 Dec 2023 12:18:14 GMT  
		Size: 600.7 MB (600697885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9b23e8f2a55de9cb21c2e022a432365c8b53c0e29d8c137eb0c5eed2adcfe7`  
		Last Modified: Sat, 16 Dec 2023 12:17:13 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
