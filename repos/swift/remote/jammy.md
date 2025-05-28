## `swift:jammy`

```console
$ docker pull swift@sha256:1714176da6bafcf56f09c93c39867a19e42d775ae918d54008c85a01b4d155df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:e5e49e4da98bc01c295cbcebd1db6b6eb6c8d0cf51f6908c1ab47fa32bd43a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1105690185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977faba3c38adbdee5378d857f93dbb9238c08ffb878ede84c36364e64eeff7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02500674e4157f9e4f90f0b670741f40327205a30f51f251675737799629628`  
		Last Modified: Wed, 28 May 2025 18:30:50 GMT  
		Size: 180.6 MB (180605978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d11707195ae04bc3e364f48ef7f0c4a499e4ead921c1e293244463a5f93d06`  
		Last Modified: Wed, 28 May 2025 18:31:04 GMT  
		Size: 895.6 MB (895551419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef94df3e1ffc97efc33660ae13e799f5fbfc2acc5897d9a35188a500b94054bd`  
		Last Modified: Wed, 28 May 2025 18:30:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:8ea1704963b5546fbc1c55fbf7b2a00cd8988fa709cc9bfb9f58778799a01e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be0ad5fe0097804e2387cb0e2eb9656b7ad985915ba3afa3a707c9fdb13e6a9`

```dockerfile
```

-	Layers:
	-	`sha256:d1729ede45ade1c8db6e551ca76b65cf2d749ceb28aada69edbd154ce7332f1c`  
		Last Modified: Wed, 28 May 2025 18:30:44 GMT  
		Size: 8.3 MB (8268175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7a9b56d00622f3fbf02054f8148d7e9b1e0cde19444792d32260f3a42884d53`  
		Last Modified: Wed, 28 May 2025 18:30:43 GMT  
		Size: 16.0 KB (15960 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:4ce985844ecac6718238446fb80405bb9b2fa9588e53987458dbdac03e6e5a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089736088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb3cc9d784990a745b1c1fdb7585568789cdc47d291d9f73b250486aa3e0454`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d309deb5b090f8da1bfd8e8d6acac5e179a95ad333860a38bd4c056bbb95b5c`  
		Last Modified: Tue, 27 May 2025 21:18:37 GMT  
		Size: 171.7 MB (171677203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e994a5e545de1e11474203dcb349674a20a5f98c4810c96c85e6415f16eab4`  
		Last Modified: Wed, 28 May 2025 18:35:13 GMT  
		Size: 890.7 MB (890704500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054a701fa15bad889c3ae472aecc7964debdd47767c6ca2c4a9a19e14e4251b2`  
		Last Modified: Wed, 28 May 2025 18:34:57 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:d14ce1f4ec758c7142c2b05c6e6a0ff3b39762cb9612ae8093a09afc8a998b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8278665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a25adb6ddbd13c7471cf66bd233706979d1072f6a673abc9c8b101b9cb2162`

```dockerfile
```

-	Layers:
	-	`sha256:670ba3e40071f2b5dbd6fb8b6adc0b9b80b469f0fae5d4ed1e695830ea192719`  
		Last Modified: Wed, 28 May 2025 18:34:58 GMT  
		Size: 8.3 MB (8262582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5463ea5156167e78aa1694b6d1d978cb7418431b98add44d62820b98d97b0a`  
		Last Modified: Wed, 28 May 2025 18:34:57 GMT  
		Size: 16.1 KB (16083 bytes)  
		MIME: application/vnd.in-toto+json
