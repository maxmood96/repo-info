## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:2b2b1d0c5219d8c0854d5f686091f810254c71e34566eeafb8d9c4bf272f47d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:a60aa5866ecf961dcf48620cb30aafb32ae45ebe1bc23d99bbb2f1dff4fb3b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123410396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eebfc08c70227e7260ff441e038a9fceca65e68a4b1d6a9abc31f19d60cc3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Tue, 30 Jun 2026 18:55:46 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:55:46 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:55:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 18:55:46 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:55:46 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 30 Jun 2026 18:55:46 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:55:46 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:55:46 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:55:46 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:56:30 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568e5969764bf08948cde0b10e063c3dd1d72f631de2e8a9db280ba3c3f1e3ec`  
		Last Modified: Tue, 30 Jun 2026 18:56:44 GMT  
		Size: 23.6 MB (23647425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7a1c8dcef0db2047bba255449d3dd7fe4049884541dde4309e1a4b30a9b8b1`  
		Last Modified: Tue, 30 Jun 2026 18:56:45 GMT  
		Size: 51.3 MB (51260761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:897967b46be57198746dd7aa14775abcd8a4f6d1480549943c74f5c9d63280b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7faf2cecaac90ab6cc5c960d1321535db98c3545d651324cc72a287c8e3a682`

```dockerfile
```

-	Layers:
	-	`sha256:3f54ea5313b6f2ad11dd556e36441e53c40c577b9d44848696995321a630a3db`  
		Last Modified: Tue, 30 Jun 2026 18:56:43 GMT  
		Size: 4.2 MB (4157008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831fc23d90cce91c67a284e50791c0b13c233abe7068876c4dde183ecb6248be`  
		Last Modified: Tue, 30 Jun 2026 18:56:43 GMT  
		Size: 13.9 KB (13926 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3b63cd44352113cdfc6adf0ad24d35d5ee3596e0864b16d5cd1d5adce54fb87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122400360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1cc72761104c5cc6d12b4878f9967a21af4aec06af15dba56ebb69e2629f42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Tue, 30 Jun 2026 18:55:41 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:55:41 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:55:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 18:55:41 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:55:41 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 30 Jun 2026 18:55:41 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:55:41 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:55:41 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:55:41 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:56:25 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1572113a711fd7a53716cae08fe5f9df116ffc0a8beeedda82b2a9c8a773e7`  
		Last Modified: Tue, 30 Jun 2026 18:56:40 GMT  
		Size: 23.5 MB (23464482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f71c044922eda44d523da1b218c4be42d8898e7b1193c34f1d069042af02e93`  
		Last Modified: Tue, 30 Jun 2026 18:56:41 GMT  
		Size: 50.5 MB (50546677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:fe1f2d54d3804e546cf2a88eb57c3e90538db6a57a5f2ba2e98890d554de9d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630f4179ba6bf508b3db6af0055f5dd84b885d09a0c97efdf644a9128537648a`

```dockerfile
```

-	Layers:
	-	`sha256:ed44eedfb642d2ff48d23d3161907cb92d5ba4d92277af629a288518d861140d`  
		Last Modified: Tue, 30 Jun 2026 18:56:38 GMT  
		Size: 4.2 MB (4157285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942ed7b002c4291e0e5beeb89537ae050264ac0c6777b1bea5b601f1aa57436f`  
		Last Modified: Tue, 30 Jun 2026 18:56:38 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
