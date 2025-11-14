## `swift:noble-slim`

```console
$ docker pull swift@sha256:8bdf537a52c351a18fcf2a4b814220b522c0f8bb83a6dfca59e24320d2946cd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble-slim` - linux; amd64

```console
$ docker pull swift@sha256:54fba28ba44b8a611cac30334fd9d166b55d24fd2ad0fa19860fdbcb0197b114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99857907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227f6e52cb89d35c566db3a61d8b5343415bf5eaf1a406b0ca7be6485c85416`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:40:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 13 Nov 2025 23:40:37 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 13 Nov 2025 23:40:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:40:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 13 Nov 2025 23:40:37 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Thu, 13 Nov 2025 23:40:37 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Thu, 13 Nov 2025 23:40:37 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Thu, 13 Nov 2025 23:40:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Nov 2025 23:40:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Nov 2025 23:41:12 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40e141b6543359f5fd364524877dddbd9093bd06c6f3b2adfb8913b276275c6`  
		Last Modified: Thu, 13 Nov 2025 23:41:35 GMT  
		Size: 20.0 MB (20019040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210d65f572deff9bbbfed15953c52336375482b07175aa9dc1998ed8da8d0cf0`  
		Last Modified: Thu, 13 Nov 2025 23:41:37 GMT  
		Size: 50.1 MB (50114179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:830fa83a43931f396570a7c8f9d8d720cfc0010dcf2bb89ac83ba737e03cc2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a23fe98a46cff35197a7301846542c6bd5a7ed4f47907c82d1bd0738a51bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:4a981064bd17f927ceea58909f5f20255979b8a7f41ec42e0ba35bf7e4202d12`  
		Last Modified: Fri, 14 Nov 2025 02:51:37 GMT  
		Size: 2.5 MB (2497218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd51c07438d0de9588e10ae6032a61364c8ca17bd1298e2b89d76b7b83e662a1`  
		Last Modified: Fri, 14 Nov 2025 02:51:38 GMT  
		Size: 14.8 KB (14838 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:19521123b706f5bd221ed43a4ea0b2cbd1aa80417155b0c04f0d40853f16b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98421849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b40d8c2dd4eb359cd000e33b3895bb9a25578e9505bdc0ce12f2e3847077859`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:08 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 13 Nov 2025 23:39:08 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 13 Nov 2025 23:39:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:08 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 13 Nov 2025 23:39:08 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Thu, 13 Nov 2025 23:39:08 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Thu, 13 Nov 2025 23:39:08 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Thu, 13 Nov 2025 23:39:08 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Nov 2025 23:39:08 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Nov 2025 23:39:45 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e20e21867d409a6e82b0844b75e40baaf0d33c0b2ffed6c542c12b39b1a119c`  
		Last Modified: Thu, 13 Nov 2025 23:40:09 GMT  
		Size: 20.0 MB (20029504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054aac7556cfa7e7a9d0f3b5f1cd8df156298b8cb1c8a5a3e78433692ab3fcc3`  
		Last Modified: Thu, 13 Nov 2025 23:40:13 GMT  
		Size: 49.5 MB (49530388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:5815757cbc087993d498c44d1101211b544891455281f23e0688242043a02775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2102fb524da7331b2d9647afd7f229d022706559cc8b54cc2c5d7bb20aea2505`

```dockerfile
```

-	Layers:
	-	`sha256:1bf58e8b1305b3e610e3472a84f59e7cf7c6dd135adb7c207b5d99d60ffc0dcb`  
		Last Modified: Fri, 14 Nov 2025 02:51:42 GMT  
		Size: 2.5 MB (2498334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f3efb5511660cbe6c937ce3c1e7c02c8ba121cf2f6481eb57b1b1dc819aed7`  
		Last Modified: Fri, 14 Nov 2025 02:51:44 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json
