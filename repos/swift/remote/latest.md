## `swift:latest`

```console
$ docker pull swift@sha256:2351780014bad244d1867e03ef282508aedbc438b0a722ea126eac5c6d104131
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:54a65362b4bca1071cd723b94c32c509e441e83abe1df97bd85e7a4dd01379e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.1 MB (828053707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9fb51c815c2097ac8e31f9178615a81ee044103ab0f34843225edfd707b302`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ARG RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f64d2f4fa00135b3f09f05b68dd2b5bbe4808a607200b8016895fa47445176c`  
		Last Modified: Tue, 17 Sep 2024 01:02:51 GMT  
		Size: 175.4 MB (175400935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd617bcafe581e3219213061d40d07ad0251a007b40a21bbd6011494df04d5f`  
		Last Modified: Tue, 17 Sep 2024 01:03:02 GMT  
		Size: 623.1 MB (623116910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c3d50cbaf494380f49efd2917e9fedeb0ee5a1f9f4494c842acdcf93092572`  
		Last Modified: Tue, 17 Sep 2024 01:02:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:8138ad2e773c22c6b7e726b53ef9a695221b163d2d57eece22c69dc6459bb73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8210499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73061fb04c78cab64793607dd03d86b1218a813dc509323600a0c3e76dd7d63a`

```dockerfile
```

-	Layers:
	-	`sha256:b319dc00a3f6fafabd9fa39df2b2ce4dcdedf251f3cf736d0738318b34a94522`  
		Last Modified: Tue, 17 Sep 2024 01:02:48 GMT  
		Size: 8.2 MB (8193862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a940a3693e35e4bac66c97b832dcc810bea1863d5143e47602065724c66d0df`  
		Last Modified: Tue, 17 Sep 2024 01:02:47 GMT  
		Size: 16.6 KB (16637 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3e0e94b3bf21ef036b489c08208cdf988217f092514a2476c1e720f3739512c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **816.3 MB (816284864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03473e054dcccb4ca4c187016d758f49ebcc5dc250188b746478614c7f0995fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ARG RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4cf0ffc78fea97df6b548d2b1104922a293f96c7f5f7d489275ff7c46a8ff9`  
		Last Modified: Tue, 17 Sep 2024 03:45:52 GMT  
		Size: 171.7 MB (171663262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7c2c0fe6d897311bd00e47351f56a8a537bf90b6c4f302271599264d4f2166`  
		Last Modified: Tue, 17 Sep 2024 03:46:00 GMT  
		Size: 617.3 MB (617263099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604b3be1524aa69702db88493e231c8a9709fcb56ab3cce3b75e08cca79b9557`  
		Last Modified: Tue, 17 Sep 2024 03:45:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:49dca6ca5ccc29bfa99ebb2798f4125acbeef92fc8d8472632ba2f0da481e0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77cc3feb7f9b4e74629309933fcdb52e2bc3628b8c58fabf00512bcfd5eaf8b`

```dockerfile
```

-	Layers:
	-	`sha256:c2a6b39a76d2211b59397e91d6d4fe0ad5c8516ade5a42c8cd40775b82212a33`  
		Last Modified: Tue, 17 Sep 2024 03:45:48 GMT  
		Size: 8.2 MB (8189574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1038f77447e189bb0bdfbd116e522e59d1263f8333ccd6e727397b3f4278db`  
		Last Modified: Tue, 17 Sep 2024 03:45:48 GMT  
		Size: 17.0 KB (16962 bytes)  
		MIME: application/vnd.in-toto+json
