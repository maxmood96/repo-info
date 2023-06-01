## `swift:jammy`

```console
$ docker pull swift@sha256:67f0eb3e7c1034d94325e1f3691c96caf7fa8d41511fe158df5b6c9021ca3464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:e7f136ae2898a06108d884651dc5712a98bc366cec8c0e12961939055f2f2bc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.4 MB (766439403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6cc52a88f5e16afcb3194c4d0434b8adbddf7ecc1079ecc4267fc8af3b448b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Apr 2023 17:30:47 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:30:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:30:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:30:49 GMT
ADD file:2fc6364d149eccc7f94ead482a0dcf24b0e44cc0d00ac6a2c1797776153e9608 in / 
# Tue, 25 Apr 2023 17:30:49 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 08:02:56 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 04 May 2023 08:02:56 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 04 May 2023 08:03:51 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3-dev     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Thu, 04 May 2023 08:03:52 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 04 May 2023 08:03:52 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 04 May 2023 08:03:52 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Thu, 04 May 2023 08:03:52 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Thu, 04 May 2023 08:03:52 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 May 2023 08:03:53 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 May 2023 08:04:27 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Thu, 04 May 2023 08:04:33 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:1bc677758ad7fa4503417ae5be18809c5a8679b5b36fcd1464d5a8e41cb13305`  
		Last Modified: Tue, 25 Apr 2023 22:54:44 GMT  
		Size: 30.4 MB (30430220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8961e425aecead266ba68a41d129fb91a20c82ee8b2651c21516ba6310d4b3f1`  
		Last Modified: Thu, 04 May 2023 08:12:14 GMT  
		Size: 176.3 MB (176254602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1249ee5d5c3e4fb59c27c4334d5985e4b98bc602116ea35ec05eb27230eb6d65`  
		Last Modified: Thu, 04 May 2023 08:13:07 GMT  
		Size: 559.8 MB (559754356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118369d72b8ee23ef7c8b2bb9f82e168b6af9c8caea0c45ada33df4fda58c704`  
		Last Modified: Thu, 04 May 2023 08:11:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a12efc6d835cfde83187f90a1abd7a749104669d97ed2a2a5aa895eed958cafc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.5 MB (749547709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99eee7aa616e319b4c5be9b6bd332cef46f6977676b5400b197e317b77a1c05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:05:54 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 01 Jun 2023 23:05:55 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 01 Jun 2023 23:07:52 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3-dev     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:07:55 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 01 Jun 2023 23:07:55 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 01 Jun 2023 23:07:55 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Thu, 01 Jun 2023 23:07:55 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Thu, 01 Jun 2023 23:07:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 01 Jun 2023 23:07:55 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 01 Jun 2023 23:08:35 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Thu, 01 Jun 2023 23:08:47 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:6c7698a779f6d8c45a39a6721fb5cce267d66ff8ab5181c55aa6d02c8ddacd01`  
		Last Modified: Tue, 23 May 2023 02:05:13 GMT  
		Size: 28.4 MB (28389044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e88fa81bf36df7228a7372bdfff9e697c89dbcd741dd328026e369fe404b07`  
		Last Modified: Thu, 01 Jun 2023 23:12:36 GMT  
		Size: 170.8 MB (170813695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d89c670953b093ba6c949121a425162bed214b5b1af018cba0fb83cd7006cc`  
		Last Modified: Thu, 01 Jun 2023 23:13:13 GMT  
		Size: 550.3 MB (550344743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3f0dd9c1227bce33617c0b25550e1a1b3741ac9107299317982e0374eed5fe`  
		Last Modified: Thu, 01 Jun 2023 23:12:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
