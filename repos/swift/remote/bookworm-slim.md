## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:5499415c3feb9491b4afd00c40b966426dfda2fbcfe31e3ed3dec785137ff60b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:d5b86b23b7e247d5e8ce0b3e5185facf84fdf3a84af7d929e1ed6c31f822a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122168359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4338df6a3cb35cc7323505aa4ed24645954439eada176aeca18a39c777608c93`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:45:03 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 08 Dec 2025 23:45:03 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 08 Dec 2025 23:45:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:45:03 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 08 Dec 2025 23:45:03 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 08 Dec 2025 23:45:03 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Mon, 08 Dec 2025 23:45:03 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Mon, 08 Dec 2025 23:45:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 08 Dec 2025 23:45:03 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 08 Dec 2025 23:45:36 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99c38e02004227414e4d8fc52b4b12e5a4d82a8a19a05527e583b017eaddf82`  
		Last Modified: Mon, 08 Dec 2025 23:46:04 GMT  
		Size: 23.6 MB (23630783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f69b687a6a2c6d4253fa3104660ec0fd80cda3a012abdb3b1b10924f495cb1`  
		Last Modified: Mon, 08 Dec 2025 23:46:05 GMT  
		Size: 50.1 MB (50056840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:20587b88b18e6ea2d2da00b823c8146da8f34ff8570b702202b3bdc5b5385313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29e7ba7845b2899b88f0eae0baeec81872d56feb9f10664bf176130f1c8f9c0`

```dockerfile
```

-	Layers:
	-	`sha256:79adc5b77cbc29d3faac2cde0dbcba8195b0f964c559bf3320c5d694058527ac`  
		Last Modified: Tue, 09 Dec 2025 02:48:37 GMT  
		Size: 4.2 MB (4156329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915dde8f4c6c47e66a642d6d9f2a059f22dd4a7bf01d1e5c3b38dc9b852fee90`  
		Last Modified: Tue, 09 Dec 2025 02:48:38 GMT  
		Size: 13.9 KB (13926 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:6af78059e2bd1653945e07f8ed36157c31b50116b784fa2720234eb4d969b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121273804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee8838952dccbbd1d52c83a58cccfb34fc7d71abf8f9d4e77faf87b50abd1f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:50 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 08 Dec 2025 23:53:50 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 08 Dec 2025 23:53:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:53:50 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 08 Dec 2025 23:53:50 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 08 Dec 2025 23:53:50 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Mon, 08 Dec 2025 23:53:50 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Mon, 08 Dec 2025 23:53:50 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 08 Dec 2025 23:53:50 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 08 Dec 2025 23:54:24 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6695b57a05d70413782f0ac409248bdea73b3cc4b7eff2e64f6934fccbeaf36`  
		Last Modified: Mon, 08 Dec 2025 23:54:47 GMT  
		Size: 23.4 MB (23449962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2fe917bbfdcda4a6cd010061a17ad24533d08e363838f9e63326b96cde02ab`  
		Last Modified: Mon, 08 Dec 2025 23:54:48 GMT  
		Size: 49.5 MB (49464771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:8fad3daf8c1572a5d55a7475161d16a2da3227aa3563708773da8edf2959f593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66980f0240c90a37c5eb349f51e086d8da58f9c0233a9c932dcd18615117fa1`

```dockerfile
```

-	Layers:
	-	`sha256:8343f4c2281faaf71a975a5c5f740275751ba1f27841df04f890f89962b9998e`  
		Last Modified: Tue, 09 Dec 2025 02:48:43 GMT  
		Size: 4.2 MB (4156606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75591d3ab31b22a216fa7e30ff1cd092dc3ccb3b81027d69c05070b882a51216`  
		Last Modified: Tue, 09 Dec 2025 02:48:44 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
