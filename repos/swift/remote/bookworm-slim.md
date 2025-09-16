## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:e8a28b273a215e6f5e0f4c8ded1cd4ebc703d86ff9f60d9142a6670d5b9f0d56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:f02de974f579e1fb8ef2322dfb533eb9cc4fc2314b267617ded47a9e888d1d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122165107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d2bb515c52ba5970d144e4557f0d1265d75e99cf4112c2aab315fbc4e13d58`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Sep 2025 22:15:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae0265054ea0125003bf765bb1c9b1e0620d43ccfc1f56004d6d55527dc88e7`  
		Last Modified: Tue, 16 Sep 2025 16:53:03 GMT  
		Size: 23.6 MB (23626915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d693bf5fddec7421071150327665bab6d0462556815a281793fac1295983e9`  
		Last Modified: Tue, 16 Sep 2025 16:53:04 GMT  
		Size: 50.1 MB (50057582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:10addf0fd894a652a634136b9b157c5e211abdd15adcae2bced78d6174e1b6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac2ac47a9fbfb42727e642902405c131d5ad284de388da944ed272fc805a5fc`

```dockerfile
```

-	Layers:
	-	`sha256:e37e256c583e1a1e81b0e2fb744e3860bcb0863606758fe784fbb7962dfb4104`  
		Last Modified: Tue, 16 Sep 2025 19:49:06 GMT  
		Size: 4.2 MB (4156329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd3dd2e8acc2a1b4f2fccbeb0516e1d0ed338912a6f6a539ad8257ab5484d80`  
		Last Modified: Tue, 16 Sep 2025 19:49:07 GMT  
		Size: 14.0 KB (13961 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a06e07f7f5e95e258d0d0e6fc5659e65624d04659e84a972c6f0492cbb4a946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121270316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf4f8494edcdeda560c77d2d2d66505eb4a816fa969db69903945954d4413eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Sep 2025 22:15:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da308d2d53a7f14a3312b4c120f3c76e5cb4522933b1fa965eb4d3f8063c245b`  
		Last Modified: Tue, 16 Sep 2025 16:53:48 GMT  
		Size: 23.4 MB (23446972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d64847ca72edb8f51582d545cc2d04667cd9517a7742253cc4afbc02edf1b2`  
		Last Modified: Tue, 16 Sep 2025 16:54:11 GMT  
		Size: 49.5 MB (49464325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:57ff6ae171a733b6febed479b46fa971aa3bd204691500a9cb1da45ac9ff171c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b073758096aba116793c0695fcdc35490cd665b2ec1036fcbe0ace898b02ce9`

```dockerfile
```

-	Layers:
	-	`sha256:5b697aa69914316323c08e01f753617b7aefd26200613fb0b873e44da4d32f70`  
		Last Modified: Tue, 16 Sep 2025 19:49:11 GMT  
		Size: 4.2 MB (4156606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126fa3d8fa1e4921cb07f919e4a539b15441238abfc885623f4f026fdd7a0111`  
		Last Modified: Tue, 16 Sep 2025 19:49:12 GMT  
		Size: 14.1 KB (14068 bytes)  
		MIME: application/vnd.in-toto+json
