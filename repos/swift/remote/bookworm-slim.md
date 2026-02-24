## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:ffad7c09851696019d16d2e31f529bdf5d896583ed4a9dfbf0c8b5aa935592d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:7b346c3e8a8ebaf44f7eefb376a0db3a2939d4ada5cca77399aeb3ee156b6293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122180545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c266e61f51e051cd3bb699f6ecff3480fea03962e96f542f92a2f686570389e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:25 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Feb 2026 19:50:25 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Feb 2026 19:50:25 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:50:25 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Feb 2026 19:50:25 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 24 Feb 2026 19:50:25 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Tue, 24 Feb 2026 19:50:25 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Tue, 24 Feb 2026 19:50:25 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Feb 2026 19:50:25 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Feb 2026 19:50:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb0a34b67e32f9bfce6aae370403fe84be8352c68842f5dcf361b0be27f2ad5`  
		Last Modified: Tue, 24 Feb 2026 19:51:13 GMT  
		Size: 23.6 MB (23633703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8038e4fd8ca268dbec6c274a491ce0b739f73907562c26050ceeef7121d221bf`  
		Last Modified: Tue, 24 Feb 2026 19:51:13 GMT  
		Size: 50.1 MB (50058065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:0f7e0e12d44d236b5529d5d1713e26ee5e5190c62f4be21a49ea938bba1ac13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2469d9eb0012766cba6187f0cc133b90b9d1b88fd987a32c76c7f043523a36b`

```dockerfile
```

-	Layers:
	-	`sha256:d7bbfe6b1bff70103cf9bfea189bd19e53f81cdd7a880f70325384eb9c40863f`  
		Last Modified: Tue, 24 Feb 2026 19:51:12 GMT  
		Size: 4.2 MB (4156972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f451b407f6bfdde89457ecc5902a68584723336abe0f0a06c9e1831772cb6e2`  
		Last Modified: Tue, 24 Feb 2026 19:51:11 GMT  
		Size: 13.9 KB (13926 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:be69760e4148a754d5dc3f0ef76ee5106d1754ad2b4242c070b416d8e9d90bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121289219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6bfbc8351424af150de9c6506aa8d9de294b46b9377c3337f226c77d9a970d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Feb 2026 20:01:15 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Feb 2026 20:01:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:01:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Feb 2026 20:01:15 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 24 Feb 2026 20:01:15 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Tue, 24 Feb 2026 20:01:15 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Tue, 24 Feb 2026 20:01:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Feb 2026 20:01:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Feb 2026 20:01:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a6327f572bda69d667f6ecef3b9a08724b045da27d6fa60550186562140752`  
		Last Modified: Tue, 24 Feb 2026 20:02:09 GMT  
		Size: 23.5 MB (23453407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52361347ae5a3332f7688e64deae3e0987631d56411de7b583628db59a69b729`  
		Last Modified: Tue, 24 Feb 2026 20:02:10 GMT  
		Size: 49.5 MB (49462602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:7da767e46d3105ca5696547db9d2cb9d99333ba8b7aa79c2f1f7f2ef28da5ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b94acbd297e7c2181205c6f9004ef56f6718b2b4332891d10a7fc93b649afe5`

```dockerfile
```

-	Layers:
	-	`sha256:83f1144af4c50a7bac7ebcc3dd7201b7613ce8c65d15866d131b76532ab6d41f`  
		Last Modified: Tue, 24 Feb 2026 20:02:08 GMT  
		Size: 4.2 MB (4157249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3262747b52bba43e5ef52634cc6e15c64fa20260211f8121459f988c920c0f96`  
		Last Modified: Tue, 24 Feb 2026 20:02:08 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
