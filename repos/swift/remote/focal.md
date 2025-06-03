## `swift:focal`

```console
$ docker pull swift@sha256:90ae41d66825cb3d41610c1caac07a55728c29578254e086042ab458a9d09b70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:686873931ed469fa9b0d735401e033908ff613600975c7fd01ddf033c8e43951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1042296456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f47b4a14e80b0fddd7ec9be7f308ed525897791e6d64d66a7bfe8b8f674d71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7f1e6cd27183b0b37532a3d52f37db1cfaf2039b3cd65892ebafdb0d51e74`  
		Last Modified: Tue, 03 Jun 2025 20:30:33 GMT  
		Size: 125.7 MB (125666525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f830e02e71deeb0476d0d46d6316f975a70c9e2283fbc72200e3941bfe2adb`  
		Last Modified: Tue, 03 Jun 2025 20:31:16 GMT  
		Size: 889.1 MB (889119366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8032318a706b963a6ed598116fbc7f80f0a51eb6b138e00bbed0fda6767a6c7`  
		Last Modified: Tue, 03 Jun 2025 20:30:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal` - unknown; unknown

```console
$ docker pull swift@sha256:ec0f1481c0a7202123fa3d362100033f79a8aed85cfe18a5eeeeb5cefa0fc3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7752046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7809035409fdc19872f8e4ea4877ae85fcf18366c346eaaba5f18500e8e85e3`

```dockerfile
```

-	Layers:
	-	`sha256:403aff19d08c7549e6d2a97d7a109b850d3c9dd445823be9a56a38827bf7b91b`  
		Last Modified: Wed, 28 May 2025 18:31:00 GMT  
		Size: 7.7 MB (7736183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27061bf103af778355d5a38b415e5658c041aba432c046bc88983c592bfd3fc`  
		Last Modified: Wed, 28 May 2025 18:30:59 GMT  
		Size: 15.9 KB (15863 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:focal` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:24d9c9ca28c3e9c7da51aa45ef15d680a38a1b819581abe2a0113a277c637da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1029242567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674f808bc0e140c0c04b754c49f29513ab8a10eca4a30d97e8c0b716edf7f774`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1407075f057a568ec32a8dadbfe71d996e1b1948860362de9c124add263d1fd7`  
		Last Modified: Tue, 27 May 2025 21:25:07 GMT  
		Size: 117.3 MB (117288111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c6cfbb356733626ab4744970987a81be35205f286fea4ec6094412b695d728`  
		Last Modified: Wed, 28 May 2025 18:40:54 GMT  
		Size: 886.0 MB (885976621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae5e7f14a15954f2cb74d1c7636b25342a8219dcdc905c357ddd5750c486de9`  
		Last Modified: Wed, 28 May 2025 18:40:34 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal` - unknown; unknown

```console
$ docker pull swift@sha256:4c7a2fda80a32532d1ba887dcc960f4a4dc35592726d27c05d5f00f851c611ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53cc5e291b1eb57a39fdc32dfaac986677a8152e19a7187679137cf02ea6b9b`

```dockerfile
```

-	Layers:
	-	`sha256:2b25146b973fc9350d34cd9a444e8f582f7c673f0dab8c7dfe3772401f4b1dc4`  
		Last Modified: Wed, 28 May 2025 18:40:35 GMT  
		Size: 7.7 MB (7738477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8912caf3ae8bf5e353316041aee6dc0b5e075294bdb0cc247da8a2ac865aed6c`  
		Last Modified: Wed, 28 May 2025 18:40:34 GMT  
		Size: 16.0 KB (15987 bytes)  
		MIME: application/vnd.in-toto+json
