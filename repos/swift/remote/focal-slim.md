## `swift:focal-slim`

```console
$ docker pull swift@sha256:0e39290c3600351d81f337129f42331ff8546b790b6557bf01f0aa3c16fba025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:a8e98e1149a276328c26884a62628366c45090aee1bc9db82962868c9ac285e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91639439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e176fa83edb583bf5afd4f285c8ab795693916586e356a5f394a894eaee381e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:17:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 06 Mar 2024 03:17:15 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 06 Mar 2024 03:17:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:17:31 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 06 Mar 2024 03:17:31 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 06 Mar 2024 20:59:03 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Wed, 06 Mar 2024 20:59:03 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Wed, 06 Mar 2024 20:59:04 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 20:59:04 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 20:59:47 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d848b5954c6d39c63ce2afafb337d19665b0bc2d21db526d0d6be49516d429`  
		Last Modified: Wed, 06 Mar 2024 03:41:09 GMT  
		Size: 22.3 MB (22277738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7d953360709df603b93d3eef40c75ff1de3a7a764489f55e4952b5e6553bbb`  
		Last Modified: Wed, 06 Mar 2024 21:12:58 GMT  
		Size: 40.8 MB (40777384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:17bb7d5bb523a76c2f1b19f284bad586c2d6ccfcf5792cd723f6aa5dee6cb242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89354892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d70a0b690af9078af00c7a4f7995f4a4f75dc90cfeb3f4318e7345b0100a3df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:15:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 06 Mar 2024 05:15:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 06 Mar 2024 05:15:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:15:58 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 06 Mar 2024 05:15:58 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 06 Mar 2024 21:22:29 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Wed, 06 Mar 2024 21:22:29 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Wed, 06 Mar 2024 21:22:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:22:30 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:23:13 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242ec1b365c214edde7f1d61113d3ff8354486fbaea85cdb61002c078323c9b5`  
		Last Modified: Wed, 06 Mar 2024 05:29:46 GMT  
		Size: 22.1 MB (22074971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0abed98397eb9fbcc3d529455b1c883985aec11de1755ac2dcadfe2825ac3`  
		Last Modified: Wed, 06 Mar 2024 21:30:52 GMT  
		Size: 40.1 MB (40075634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
