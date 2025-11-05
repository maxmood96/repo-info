## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:ca4ef8b505c805b061127931f849775f33d206199a85d3e9034363148ffd5500
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:b049edd0e2f1e9fa34b4198d3e994b5f64ce688af72ac82d83eda73ef2ef195b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122168528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad6d3f4195d55a64da6cf36823603512c8f529f9c1b3cece196c11c30b0298d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 22:26:03 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 22:26:03 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 22:26:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 22:26:03 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 22:26:03 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 04 Nov 2025 22:26:03 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 22:26:03 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 22:26:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:26:03 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:26:40 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc2dc1fa51a077d1c9666c50d67cd57424b327e9e37392c6e46429aa7215b0`  
		Last Modified: Tue, 04 Nov 2025 22:27:05 GMT  
		Size: 23.6 MB (23630675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c04b8462b1dd1388a1166042bb687f130c79f6bec4bc377bf26100596bc2b6`  
		Last Modified: Tue, 04 Nov 2025 22:27:06 GMT  
		Size: 50.1 MB (50056797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:12c09d36bad47350912f557616228a0eebff894e896adb169cfab5fccda5ee63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ff33b47b7efe1e1320c18daa99c63f93823b50a33bbb786c6ff9e8110a47b`

```dockerfile
```

-	Layers:
	-	`sha256:cf8a1556663646e74ed6b87318922b40370edec7eafeb278fd3b22d2a1592e47`  
		Last Modified: Tue, 04 Nov 2025 23:48:05 GMT  
		Size: 4.2 MB (4156329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:585493f767d8f24ccd63c93da62f76d498118e094ecc453bf86c9f63c3a6fcbc`  
		Last Modified: Tue, 04 Nov 2025 23:48:06 GMT  
		Size: 13.9 KB (13926 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:69afa8156e807749badb3c614266fd50a6344eb382008eaa3ea31de66c91ac9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121274082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130d28c0d0aa871109a888a9d8a77098cfa3310064564d6b2058456bd46e1d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 19:23:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 19:23:59 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 19:23:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 19:23:59 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 19:23:59 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 04 Nov 2025 19:23:59 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 19:23:59 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 19:23:59 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:23:59 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:43 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4500acc02f374ecf570327cc85ad3a817e5c08b3cbea30f16c57833ecb9bb4d`  
		Last Modified: Tue, 04 Nov 2025 19:25:05 GMT  
		Size: 23.4 MB (23449882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dfd60feca2dc6a8a57c0967a3fb1689c04bbfa28882d183694b1237cb3d74f`  
		Last Modified: Tue, 04 Nov 2025 19:25:07 GMT  
		Size: 49.5 MB (49464722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:2c4f0a6e6938c3bc177ee407a997e9816b019e3242598e9e65c8ffb187015583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccff4f1d3cf082d8aeaa46b495f23051eb7c420b97f8f81c6454b09283ce39ea`

```dockerfile
```

-	Layers:
	-	`sha256:4bbb8f736d4c6bfd987a7e9b68d66f2c42b714e65e867af9b410a2a3d866f7db`  
		Last Modified: Tue, 04 Nov 2025 20:48:08 GMT  
		Size: 4.2 MB (4156606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcbe8094fa3a9f572f577cb52a143c14d5acdf40482274da0c5231934cc239c3`  
		Last Modified: Tue, 04 Nov 2025 20:48:09 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
