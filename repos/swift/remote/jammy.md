## `swift:jammy`

```console
$ docker pull swift@sha256:d339e10abdbee683f26cf5a16b89036902e3af694311e00ec74caafe333ef2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:b95a368becafbf1758dc2ac6ed07cc63d3aa427416eb4e906fd2bb1fe4ae4451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1296295527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaabf4ca5db2f877b0eee6e1fcfdfec1b706ec7b45b11c789467aa3422e40e7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 15 Apr 2026 21:01:22 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Apr 2026 21:01:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 15 Apr 2026 21:01:22 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 15 Apr 2026 21:01:22 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 15 Apr 2026 21:01:22 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 15 Apr 2026 21:01:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:01:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:02:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 15 Apr 2026 21:02:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac50028c9e1b23606233f668a2bc8343de0f9b5deb54ada0bfe283483ec2f265`  
		Last Modified: Wed, 15 Apr 2026 21:04:22 GMT  
		Size: 175.7 MB (175664391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db48c5cf2647895b1afdf5e0ad605867866c9d70c72a9571c9f420d2a270878`  
		Last Modified: Wed, 15 Apr 2026 21:04:40 GMT  
		Size: 1.1 GB (1090894465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c753df78f226939845df810977b579a4582d0f47562d396df74749eaab44d09`  
		Last Modified: Wed, 15 Apr 2026 21:04:15 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:ab477ed14c8a558600558a38c07e1110d7ac18fdc3088660c799b8e3700509dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22480499c4478194cecf6c17cedde2eed8af3913939416bf7c7daa5ddba1e8f`

```dockerfile
```

-	Layers:
	-	`sha256:52f89f9672c4274ef41f849daea1ceb048d8e4a36b3665632361d335132458ac`  
		Last Modified: Wed, 15 Apr 2026 21:04:16 GMT  
		Size: 8.5 MB (8477479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfe6fb35c9c8ef82c2b836bbcac6c93adc2748fd0727c67074a5d06fb4dc485`  
		Last Modified: Wed, 15 Apr 2026 21:04:15 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f7899ae9c0973a449678033c1339a433f4605ffb7b8a1ed432eda6207c28a317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1284997384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c404e91de80c6dab695e856c1bb706e5f33b90d5a8b1c5fff204de9d1a434cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:12:12 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 15 Apr 2026 21:12:12 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Apr 2026 21:12:12 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:12:12 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 15 Apr 2026 21:12:12 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 15 Apr 2026 21:12:12 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 15 Apr 2026 21:12:12 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 15 Apr 2026 21:12:12 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:12:12 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:13:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 15 Apr 2026 21:13:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab2cc6de569035f563aa14d324d76193a332d6d823577a6aac1b6857f16087`  
		Last Modified: Wed, 15 Apr 2026 21:15:17 GMT  
		Size: 172.0 MB (172015960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59987193c44dea51366337a5d04f3fcdeb79381008702322020838e6a37f5ace`  
		Last Modified: Wed, 15 Apr 2026 21:15:36 GMT  
		Size: 1.1 GB (1085374710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f501105ef192d2eea028a32d1ad8ccc28c664f70005dd14b3ba8440789e8639`  
		Last Modified: Wed, 15 Apr 2026 21:15:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:4d793170d6a26afb7925cdfeb579ec3ad1f44eac4b9cb5061ccfbf3cafcac08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9440e989ebae2cf7292c87f50e6c7b9895ab54be7f515f1c1350002650ca1c01`

```dockerfile
```

-	Layers:
	-	`sha256:59058bfdb5814407e566b265348ee6b9667867c3b74d6616c805d93ec315d988`  
		Last Modified: Wed, 15 Apr 2026 21:15:11 GMT  
		Size: 8.5 MB (8473165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a78cb47842c71c5a015ea8ff4e986f489302456640e5c8f25a87893908863ae`  
		Last Modified: Wed, 15 Apr 2026 21:15:10 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json
