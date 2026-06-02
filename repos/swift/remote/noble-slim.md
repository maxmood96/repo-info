## `swift:noble-slim`

```console
$ docker pull swift@sha256:af652929184ac4a5a56b52caf514ce80d6db53f03bb010c572cfc7f0f916a374
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble-slim` - linux; amd64

```console
$ docker pull swift@sha256:8c02d330523a988ce5b720fa39bdba1af8e60075408cc0b8566f3f393b2f5471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101081166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33d17938db23860e2b2cf255900795b6b6442cae166841fce30afdc46909064`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:25:04 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 02 Jun 2026 08:25:04 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 02 Jun 2026 08:25:04 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:25:04 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 02 Jun 2026 08:25:04 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 02 Jun 2026 08:25:04 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 02 Jun 2026 08:25:04 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 02 Jun 2026 08:25:04 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jun 2026 08:25:04 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jun 2026 08:25:38 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2150321ca725899abf4a1c407d7744deecd1d10c9a5673f892596e722470f628`  
		Last Modified: Tue, 02 Jun 2026 08:25:51 GMT  
		Size: 20.0 MB (20023630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0527ef882a0024e3454e3294c46cd0f00f036090def5d2d42f50f27122188b85`  
		Last Modified: Tue, 02 Jun 2026 08:25:54 GMT  
		Size: 51.3 MB (51324731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:f2bed52dee4b8095f5f0aa3ca7451c66ae007e31afaeaac950235b3f058c05ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a2eb8d06321d71a2f0a40bdbb689495c1a9ab4510b70f20613c4f2f4264754`

```dockerfile
```

-	Layers:
	-	`sha256:47af8cc5f54649e72b669b870a5976760319eda15094f94f8a609dc67a7a09a5`  
		Last Modified: Tue, 02 Jun 2026 08:25:51 GMT  
		Size: 2.5 MB (2497264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1440dfecb208c245cfc84eb2005b114ec6feaf134c70cf5986bc4b82125d9682`  
		Last Modified: Tue, 02 Jun 2026 08:25:50 GMT  
		Size: 14.8 KB (14837 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b23695a1c00ecbe9a8d0c7ef2fd9f1f922b91116c4931fa9093f44206c27918a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99530714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0220255d0b0e5d93898f998269354bb8103e9975ee2aa033f91ea5358bc3768e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:25:31 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 02 Jun 2026 08:25:31 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 02 Jun 2026 08:25:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:25:31 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 02 Jun 2026 08:25:31 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 02 Jun 2026 08:25:31 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 02 Jun 2026 08:25:31 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 02 Jun 2026 08:25:31 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jun 2026 08:25:31 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jun 2026 08:26:06 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05685377a0089791f2fbf7e24ed5bf1b18767f1b95ec33cb7e1536cedfa98ed`  
		Last Modified: Tue, 02 Jun 2026 08:26:18 GMT  
		Size: 20.0 MB (20038445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64cdd6cfe4b6f66c38fb76c5a59ffa40b9c0573f95bcf05521c989b37b184a7`  
		Last Modified: Tue, 02 Jun 2026 08:26:19 GMT  
		Size: 50.6 MB (50615863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:c29a25d448797b2529d094e618fb91c501336bf468be2508fef9a92edcb24073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaf644b97f6e464f1d5b9bc74a3db639ba720bba899dc1ad7f57362b7797b42`

```dockerfile
```

-	Layers:
	-	`sha256:1d03139e81c327a3b8c24a2dd2227dc05033488ec0bee4aa31167185b57c9060`  
		Last Modified: Tue, 02 Jun 2026 08:26:17 GMT  
		Size: 2.5 MB (2498380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4fd95da75938381a61605210cbd5ce48a433e4baab728da8af9bd5b9e15b139`  
		Last Modified: Tue, 02 Jun 2026 08:26:17 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json
