## `swift:slim`

```console
$ docker pull swift@sha256:bbca2680dba01e47f97abbdde32d8e759138eeb23bc4d137c079b6e6bc904a6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:526f6cdd63c1d9363b49cd1e31009846e891ff03ab9318fbcb5b3d92c9e91375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101136609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9c61909609def5ff847026914077fb04c8e9ce999149ca858d671fc17d8cbd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:33:23 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 Apr 2026 02:33:23 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 07 Apr 2026 02:33:23 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:23 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 07 Apr 2026 02:33:23 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 07 Apr 2026 02:33:23 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 07 Apr 2026 02:33:23 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 07 Apr 2026 02:33:23 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:33:23 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:34:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf28c3c7cb1547dbbe59b6b9075c671154f085d20ec69bbed5649a443a3264de`  
		Last Modified: Tue, 07 Apr 2026 02:34:16 GMT  
		Size: 20.0 MB (20023989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f623bbd8de42a3b8445fa4428747173eee96e42ad31d3eaea3668d495645bbc7`  
		Last Modified: Tue, 07 Apr 2026 02:34:17 GMT  
		Size: 51.4 MB (51379161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:d3f920dabd1ceeef20bf9271638bd5081f872f1a48bcfa95b6d6e10f5027e67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc18a2ddc3745c3da819d4f9d895d5cdd1959fc4367fdb8e1fd1615e429bbd4`

```dockerfile
```

-	Layers:
	-	`sha256:6bb053ba4169ed3a7a5413c4911b98d0083f61880afc924af2aa89cef16409e8`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 2.5 MB (2497246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7240c940198acc8dea7518bfcb7a5d7cb4afd2c12535b4ec763623a818939d9c`  
		Last Modified: Tue, 07 Apr 2026 02:34:15 GMT  
		Size: 14.8 KB (14830 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:e1a187d4a3b0d677af9b9fcf2d1fa3cfb0d32b8b593240b3a86ffd1a901295a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99582604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785126f9c7999dfd6fa5a4811c5dfc8ec986c56234b996218f84931cbb2293f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:39:57 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 Apr 2026 02:39:57 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 07 Apr 2026 02:39:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:57 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 07 Apr 2026 02:39:57 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 07 Apr 2026 02:39:57 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 07 Apr 2026 02:39:57 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 07 Apr 2026 02:39:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:39:57 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:40:35 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7fc5db10a6b6b64b1c0d113a3cd62463036cfc64b36a6922ccd41cca9774c4`  
		Last Modified: Tue, 07 Apr 2026 02:40:48 GMT  
		Size: 20.0 MB (20037073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267776938d09ab4297be0e8dcd1e90777c2af6fb679f3efeb93c8233f4c854bf`  
		Last Modified: Tue, 07 Apr 2026 02:40:49 GMT  
		Size: 50.7 MB (50671456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:8a3f6c13c13a5aeff748c62bd6452836623161567714b0120af226f9f454f8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1df834a1be504d84f6a3c788828df43fd479b90aa977834ca42a6de97b9698`

```dockerfile
```

-	Layers:
	-	`sha256:63b96563b936b13aaae99d364ee9cf7356fd8b12684dd3066f74ebe20da444bc`  
		Last Modified: Tue, 07 Apr 2026 02:40:48 GMT  
		Size: 2.5 MB (2498362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71be86c34f607ad2e7d3f72b167bb50a334aad3cfc6874b6a0b773b6d2b55dc0`  
		Last Modified: Tue, 07 Apr 2026 02:40:48 GMT  
		Size: 15.0 KB (14972 bytes)  
		MIME: application/vnd.in-toto+json
