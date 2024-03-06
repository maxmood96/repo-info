## `swift:focal`

```console
$ docker pull swift@sha256:1ad100b916322812a272d3de421cefbcdb3a5d2efbd05966208eb99bb6c279b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:8b2370dd5ba18d45c175325c4dc8a8d3c16346fe39ab4e1b94ee27960c7b8ba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.1 MB (771125951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687cf19537eef426b6e865b13aba62ecc1a4890e6253774c4ae5bbbac6088c31`
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
# Wed, 06 Mar 2024 03:19:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:19:36 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 06 Mar 2024 03:19:36 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 06 Mar 2024 20:59:52 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Wed, 06 Mar 2024 20:59:53 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Wed, 06 Mar 2024 20:59:53 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 20:59:53 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:00:43 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Wed, 06 Mar 2024 21:00:49 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb98fe932cb77db15803ff214702979b2ad0ab36c4f7ae2e9aa394eebe05df6`  
		Last Modified: Wed, 06 Mar 2024 03:41:44 GMT  
		Size: 120.5 MB (120523359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62ab55bd9f7e97027d0af372a39f705a8b1314f3d5b054dd4bc8b7b05b89131`  
		Last Modified: Wed, 06 Mar 2024 21:14:34 GMT  
		Size: 622.0 MB (622018076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7236124232d37d05532c2357ca631e0ac905b4a3849360208f5540de2926df`  
		Last Modified: Wed, 06 Mar 2024 21:13:10 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:cc21180e3858b0b2183febcf5d1f2cb529470a40253375fc1597d90ad19898d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.5 MB (760540389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeecac3ff0b60ff317a7ddcc7b4f6aaa57b4896e6d9e2f6e5d5e741520c9ab92`
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
# Wed, 06 Mar 2024 05:18:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:18:17 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 06 Mar 2024 05:18:17 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 06 Mar 2024 21:23:17 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Wed, 06 Mar 2024 21:23:17 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Wed, 06 Mar 2024 21:23:18 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:23:18 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:24:00 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Wed, 06 Mar 2024 21:24:12 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8e12c181d3740e90f44b2dea3700e70be763023b250fbe83ba2a5901fa7127`  
		Last Modified: Wed, 06 Mar 2024 05:30:14 GMT  
		Size: 117.3 MB (117287304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0855f7d66980f2a5d0b0a590fb04b0553e6b705de3036af0a3d153566e478ee`  
		Last Modified: Wed, 06 Mar 2024 21:32:06 GMT  
		Size: 616.0 MB (616048599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd205a671aafa5826a886913d8c4c513e2bd15dd690fbfed9a9ed1f7b2eae1c0`  
		Last Modified: Wed, 06 Mar 2024 21:31:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
