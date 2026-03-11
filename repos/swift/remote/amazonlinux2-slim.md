## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:89777377a79b5052f418ad569fdff1d561318bd4f5dedc0fd9b19fa19e96df5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:c47f77dc935d07f279ec3aa73e13dc4897590fd525b372ea70006ec77a7a641d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286403326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1f9f293a83d7d20709c083c340f43d7c82d180e419d0ff63c2321a9d9b338f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:40:34 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 11 Mar 2026 18:40:34 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 11 Mar 2026 18:40:34 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 11 Mar 2026 18:40:34 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 11 Mar 2026 18:40:34 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Wed, 11 Mar 2026 18:40:34 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Wed, 11 Mar 2026 18:40:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 11 Mar 2026 18:40:34 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 11 Mar 2026 18:40:34 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d280eb2dc319ebbffd374f63494bf6dbc33585a0beaa2d503bfd9838ad76c620`  
		Last Modified: Wed, 11 Mar 2026 18:41:04 GMT  
		Size: 223.4 MB (223446816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:42dc85137c9fd03ea44b2a4d4849c9eb3da7e18a1071e7d12bf4e8bde9e32d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e918985db8ba34d43de61c117cf3a4cc5cea4e0356f4780fbb017ab1394ebee`

```dockerfile
```

-	Layers:
	-	`sha256:2fa6e6475453c43d6bc6291b9efbb2c1c9892f41fa669b9ea27cd098a083bb42`  
		Last Modified: Wed, 11 Mar 2026 18:40:59 GMT  
		Size: 5.1 MB (5082197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b9e594db8bf4dd9c2af92e8212e800775c4c357f9330f50110f776d0be437c`  
		Last Modified: Wed, 11 Mar 2026 18:40:59 GMT  
		Size: 11.9 KB (11854 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:68d40b72eddd5656442eec27c1ecca42c91c12dbd55167d4de371d3dac22b7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.4 MB (263414381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ddd4eeabd1b13eb4561b11f5d9c5a6cea69853222343ccc387e6c5160ed1ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:40:31 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 11 Mar 2026 18:40:31 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 11 Mar 2026 18:40:31 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 11 Mar 2026 18:40:31 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 11 Mar 2026 18:40:31 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Wed, 11 Mar 2026 18:40:31 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Wed, 11 Mar 2026 18:40:31 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 11 Mar 2026 18:40:31 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 11 Mar 2026 18:40:31 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a09ffdb1fd2d948d7eccedd4a18cfb752ab6e92c812ad67ff050c563ec52c3`  
		Last Modified: Wed, 11 Mar 2026 18:41:01 GMT  
		Size: 198.6 MB (198611232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:0bc526f77f661cb550e547c19459ac53e3c954058231fdcd1473f45a9e6da845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc543d5ec34befd1790ce8b64a0d0378271785078ee270eeba716ef911cd583`

```dockerfile
```

-	Layers:
	-	`sha256:834b93dcd26a94d1bc1e06ef5032aab97eb670d69e36b641872327a5d959ddfa`  
		Last Modified: Wed, 11 Mar 2026 18:40:57 GMT  
		Size: 5.1 MB (5081631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f0b94491fca9f75e85cf497a3a88425bd882e7950415fb81e8175a75fa19f6`  
		Last Modified: Wed, 11 Mar 2026 18:40:57 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.in-toto+json
