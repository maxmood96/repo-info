## `swift:jammy-slim`

```console
$ docker pull swift@sha256:950aeb9b11dd83f81e9ee38a461412c3de29bb85b7b8323146bb17377175495b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:2e0429843573edd49165c4f04cf27fac2f45cacd3a3a45a32eee053070c3bed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98832563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0875c2283e3d7db67808aa896b861d150188e043fa699b0d494589f1d13dabc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Fri, 12 Dec 2025 22:42:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Dec 2025 22:42:15 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Dec 2025 22:42:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 12 Dec 2025 22:42:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 12 Dec 2025 22:42:15 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 12 Dec 2025 22:42:15 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Fri, 12 Dec 2025 22:42:15 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Fri, 12 Dec 2025 22:42:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:42:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:42:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b447a7f9201f6795701efaf0e679bfc9d75a8f5ecbdeeaa2cf2536379dd28`  
		Last Modified: Fri, 12 Dec 2025 22:43:14 GMT  
		Size: 19.2 MB (19223571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb11df38b68e3b059bd9a2f647323b163b11b5467c8801d95dfe78d32ee8f53d`  
		Last Modified: Fri, 12 Dec 2025 22:43:19 GMT  
		Size: 50.1 MB (50072194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:4cccd9105312dd3977b80e793ff3a7c7b7041ba14b74c19c24af6ef6c30fe965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb93163f0c5df55723681f2615ccb8b319710afe5550ef7c24e2319591451aab`

```dockerfile
```

-	Layers:
	-	`sha256:f7a3c444c3a949ca663badcdbda1b3d99e897bbefdec86ed73bec6e53dcc7d30`  
		Last Modified: Fri, 12 Dec 2025 23:48:31 GMT  
		Size: 3.1 MB (3055481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1994053c246d094ce29c7785faac1aa10be4f20ad1f2b1d80a649bd7f0c14f30`  
		Last Modified: Fri, 12 Dec 2025 23:48:32 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d00c9d42fa3f4a0a5c05a145edc7ef717b2b085085b9ccbb0ac4816f98507aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ac8bfaaff0346a8d31877ebe60371c76b5a6a33edc02a4db9640ca42d6a20f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Fri, 12 Dec 2025 22:42:26 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Dec 2025 22:42:26 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Dec 2025 22:42:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 12 Dec 2025 22:42:26 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 12 Dec 2025 22:42:26 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 12 Dec 2025 22:42:26 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Fri, 12 Dec 2025 22:42:26 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Fri, 12 Dec 2025 22:42:26 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:42:26 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:43:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338fd831d3e1a6a168a84e019e4412368c776c1c366f081c76ff583420d798e8`  
		Last Modified: Fri, 12 Dec 2025 22:43:37 GMT  
		Size: 19.1 MB (19100041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5891ade0034b38e10657f95d2355fed03db7a8fb44aa93f809a5b6cfcdff003b`  
		Last Modified: Fri, 12 Dec 2025 22:43:35 GMT  
		Size: 49.5 MB (49476962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d4d0cefdbf13a8dcf0bd8dade9461468eab64d59f572a83f968d164a2a9eb310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6996bbfca1d0d4d0f6143b8a4b6aea0b574818c8be536e2a365a8330b75f6d47`

```dockerfile
```

-	Layers:
	-	`sha256:7a57c3dcc9f8ce23ea2a1ea857e57c7f694369b5c71972fd00aa3b62f6d2f9b7`  
		Last Modified: Fri, 12 Dec 2025 23:48:36 GMT  
		Size: 3.1 MB (3055768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e30eb74419685712da7db2a604537377c68b9687b5959be97450e9fc24d6dc2b`  
		Last Modified: Fri, 12 Dec 2025 23:48:37 GMT  
		Size: 14.0 KB (14044 bytes)  
		MIME: application/vnd.in-toto+json
