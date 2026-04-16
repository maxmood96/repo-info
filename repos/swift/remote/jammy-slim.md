## `swift:jammy-slim`

```console
$ docker pull swift@sha256:4bbe1d086dd09279ea2c753e58889b00a7e88cdfb84d444528a9c0f202be3ab4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:86b3b7e68c2e22f9ba1485df77e41067ffc5965ab662e713dd921275139f89b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100289878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f34d84bf9eb77d2d9999feeeae6279e6bcb6a0643b393bfea53816060816811`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:00:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 15 Apr 2026 21:00:55 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Apr 2026 21:00:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:00:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 15 Apr 2026 21:00:55 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 15 Apr 2026 21:00:55 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 15 Apr 2026 21:00:55 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 15 Apr 2026 21:00:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:00:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:01:31 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678e694bd7a1ee60f2f8b0f25b02abb7085b55719bb3e800d7afac875fed8b4`  
		Last Modified: Wed, 15 Apr 2026 21:01:45 GMT  
		Size: 19.2 MB (19226186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe9dd866f55a935f1a1903ea05284b3b25c32ee61ec5912924d2e99b4126f7`  
		Last Modified: Wed, 15 Apr 2026 21:01:46 GMT  
		Size: 51.3 MB (51327194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:a6ef862df1d3fca58c18c147d520ca065a85f281ab7b5da3211ebc0bb693b099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200a459537b1bfa6e504fdcdf5312421c961afc5ec24761446f87e58a3efd1dd`

```dockerfile
```

-	Layers:
	-	`sha256:891f2f37fdbee179b6e525bbdbd634d7ddd455c3a1b4a63ef0b11c23aba0e7d5`  
		Last Modified: Wed, 15 Apr 2026 21:01:44 GMT  
		Size: 3.1 MB (3055481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6683409bd018122d3823092934d1cb4277a3c3d79061bdedc3acb3e14eeb0642`  
		Last Modified: Wed, 15 Apr 2026 21:01:44 GMT  
		Size: 13.9 KB (13927 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:4df0c97397860099391dc8555e76b438ac67cb02acc12731dc3fd1371a6eec3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97334849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e86f9561e80fda66b63de32e6f2a4b0ba7d5eb43772876b07ff047ba11f365`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:52 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 01 Apr 2026 20:16:52 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 01 Apr 2026 20:16:52 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:52 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 01 Apr 2026 20:16:52 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 01 Apr 2026 20:16:52 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 01 Apr 2026 20:16:52 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 01 Apr 2026 20:16:52 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 01 Apr 2026 20:16:52 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 01 Apr 2026 20:17:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8864933e7b96cd6eb99ca2918c838b7c780b410c5bc4f8d40c38dfab5cb5b550`  
		Last Modified: Wed, 01 Apr 2026 20:17:55 GMT  
		Size: 19.1 MB (19104516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bbe19c6684752adcf188b5e4989d73bd57cf3b5fd3d08955d4ade5c28775ad`  
		Last Modified: Wed, 01 Apr 2026 20:17:56 GMT  
		Size: 50.6 MB (50623390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:ae64621fc5aa2a9e605fac1820d1e2035b556f75d84f398a99c159a6fa72d4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c8634f171b107e1680918cf6212eabf9c5681299eec7c7c541c5d01c5443d9`

```dockerfile
```

-	Layers:
	-	`sha256:5f4a98521b14109f5a4d134a2ab41bcb94ead46c8b77a29a52dab25aa1126399`  
		Last Modified: Wed, 01 Apr 2026 20:17:54 GMT  
		Size: 3.1 MB (3055768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff89fac3414f6617609e9cf0653dd3c9ed0b754238fe2b758243bbfa8512ce08`  
		Last Modified: Wed, 01 Apr 2026 20:17:54 GMT  
		Size: 14.0 KB (14035 bytes)  
		MIME: application/vnd.in-toto+json
