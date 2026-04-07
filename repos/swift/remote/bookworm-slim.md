## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:0eb11b09cfb96a4aa585b749712772360f8f9f394f7f1f12ac2281e9b702bcda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:b08bbc69b909ab954d6c0ebde25b7af747cd971e7b97fdd4582f2cba99ed274f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123433885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feec05297443684f622500c6173b79c546d2ab8e267a1ee623af65bc64fde34d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:33:45 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 Apr 2026 02:33:45 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 07 Apr 2026 02:33:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:45 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 07 Apr 2026 02:33:45 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 07 Apr 2026 02:33:45 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 07 Apr 2026 02:33:45 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 07 Apr 2026 02:33:45 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:33:45 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:34:20 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0b6f1514009d2570683b6aab588391f827bc1cf0ef5d0cb5a7acc77319f4f3`  
		Last Modified: Tue, 07 Apr 2026 02:34:35 GMT  
		Size: 23.6 MB (23633620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75b8d395d6d15c0e025624a28a22aafae6c8817c1779a44bbf0273caa662d8`  
		Last Modified: Tue, 07 Apr 2026 02:34:36 GMT  
		Size: 51.3 MB (51311442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:48e64fe82228982f7884a7ea678d2c0c402ebdd72c30dc85545025498e827e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d99132c0f680a3ae7110286362843f81c93efd617b29ddf5f1fa66652c7cf5`

```dockerfile
```

-	Layers:
	-	`sha256:a0e2b3c3444285099a6df849664c77a6e49a5e527e9e3295702713c9ba63266a`  
		Last Modified: Tue, 07 Apr 2026 02:34:34 GMT  
		Size: 4.2 MB (4156972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80e76f944a4d75b61e64f24ecd5d5fcfe8af6e79c71a30632aa814eb4779d98`  
		Last Modified: Tue, 07 Apr 2026 02:34:34 GMT  
		Size: 13.9 KB (13918 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b4033e70ba4d2fd292835a917572b53162d5d7fabfa8599821450d8f197793cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122428484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43098ddac19c0664fe8d1899edd309bbfaac4bf37d001e8261b37175a435addb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:39:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 Apr 2026 02:39:59 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 07 Apr 2026 02:39:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:59 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 07 Apr 2026 02:39:59 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 07 Apr 2026 02:39:59 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 07 Apr 2026 02:39:59 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 07 Apr 2026 02:39:59 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:39:59 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:40:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc0bf4651c4c888d954f3f9759d3b5d391bb70eea4ef47976990ef7dd75be9`  
		Last Modified: Tue, 07 Apr 2026 02:41:00 GMT  
		Size: 23.5 MB (23453369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dadb02a4bcaea0e317c3cf5cd16b7ef97a3d415643582825f0d7d1cf341e06`  
		Last Modified: Tue, 07 Apr 2026 02:41:00 GMT  
		Size: 50.6 MB (50601853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:e31f5b66ecf2ca9866c25d04c811cb658c288ffe30ae99174d794b9c416aaed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9e14ede5309814e1d68f0b3a79cb3bc4d41a9e52ab6708038844385f556db0`

```dockerfile
```

-	Layers:
	-	`sha256:8c58bb74ed45780d47a4c49259de94834107922b523653fff084990c10727a1a`  
		Last Modified: Tue, 07 Apr 2026 02:40:59 GMT  
		Size: 4.2 MB (4157249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28fb484ef50092d02179f55001b700d93d48df91213629f891be45f5af104163`  
		Last Modified: Tue, 07 Apr 2026 02:40:59 GMT  
		Size: 14.0 KB (14024 bytes)  
		MIME: application/vnd.in-toto+json
