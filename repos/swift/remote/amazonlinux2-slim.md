## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:c2913790dddb36b3ef15f7bb2904f9e26ad9e3860fb24a423682c2906fb0b4e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:731279f5b3d157b59f49cc3f8207d4161a988939045f49e73a916f607d18f85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283374484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d597a24aba784a466ca8c89da291b629881f7c145c3fa348e3cf6f5117be4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:25:26 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 03 Dec 2025 20:25:26 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 03 Dec 2025 20:25:26 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 03 Dec 2025 20:25:26 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 03 Dec 2025 20:25:26 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Wed, 03 Dec 2025 20:25:26 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Wed, 03 Dec 2025 20:25:26 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 03 Dec 2025 20:25:26 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 03 Dec 2025 20:25:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bde80767285ae08ffbcda577549a10c7590c42e9c5e140db883d08e80352b0d`  
		Last Modified: Wed, 03 Dec 2025 22:34:07 GMT  
		Size: 220.4 MB (220443912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:c4d5c89b263a83cfb81959035f42e95b98532db9362839628bd0187b37d7aac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d5da4c6d22890e7fbdfb94457e600130a667a3e419bfcb73cf63df4bb4a6cc`

```dockerfile
```

-	Layers:
	-	`sha256:ad690fceead05d40a9ac36e1c0c1ef85b2f26197219281494df00d2c4e7685d5`  
		Last Modified: Wed, 03 Dec 2025 23:48:45 GMT  
		Size: 5.1 MB (5082197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be026c8b9164cf6694ccff6f32e5f7ab1ddfb16996bfd69bc16c2d2ae9140d0`  
		Last Modified: Wed, 03 Dec 2025 23:48:47 GMT  
		Size: 11.9 KB (11853 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3bc367a0c58809a24d92de37c566d0c11e4f30c314f17601231ce7eb6b2a7762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260670944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8b077aecb0b98e680eae80cc85d35c908a3537df2934c38246a9fce5178792`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:29:24 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 03 Dec 2025 20:29:24 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 03 Dec 2025 20:29:24 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 03 Dec 2025 20:29:24 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 03 Dec 2025 20:29:24 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Wed, 03 Dec 2025 20:29:24 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Wed, 03 Dec 2025 20:29:24 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 03 Dec 2025 20:29:24 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 03 Dec 2025 20:29:24 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c175a307ad6090943a2bd4f0d8eda3e04babebba523de06a95ab5f24f6ac8f81`  
		Last Modified: Wed, 03 Dec 2025 22:31:07 GMT  
		Size: 195.9 MB (195878143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d03a319d028194d2f58ff8578ad3a8487a300824d6f5f85adc035a5f03a040a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d2428000f87b7ea585a570601930e39c8d611427d74767c40de1334a7177b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a09b9af8f9bee2697210258c96d640e9cf4e2f03294a5e16c78306d21fdd448`  
		Last Modified: Wed, 03 Dec 2025 23:48:52 GMT  
		Size: 5.1 MB (5081631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d98aa502c841aeabed484dcf41529f57e69e115753fe947ea0a5679662916040`  
		Last Modified: Wed, 03 Dec 2025 23:48:53 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.in-toto+json
