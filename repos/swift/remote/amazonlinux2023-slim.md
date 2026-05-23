## `swift:amazonlinux2023-slim`

```console
$ docker pull swift@sha256:931a553390c2f4501e4e6deb1b1af4e2588c99054bf652294fbc41bc16890e13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023-slim` - linux; amd64

```console
$ docker pull swift@sha256:6d2374abb09fb7a55b1a09aa1e7179ece289ac242e8335b043fc81bac70dd8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256231697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4297b222b5e310c393b4119aa2e5b79a80dc5dfb9d8823860211c9b5f0a29e4f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:13:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 22 May 2026 21:13:09 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 22 May 2026 21:13:09 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 22 May 2026 21:13:09 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Fri, 22 May 2026 21:13:09 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Fri, 22 May 2026 21:13:09 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Fri, 22 May 2026 21:13:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 May 2026 21:13:09 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 May 2026 21:13:09 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Fri, 22 May 2026 21:13:51 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39cbf98f49d898d35edc3009bc909405f6aebe4cdc16e3c852638fcc1c2dfc5`  
		Last Modified: Fri, 22 May 2026 21:14:13 GMT  
		Size: 146.9 MB (146930554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf262af2511f0a2496d8a3d0fb17e699475feccca741ca63612348f7ad0b0d78`  
		Last Modified: Fri, 22 May 2026 21:14:11 GMT  
		Size: 54.7 MB (54728703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:9977420bdc027b7f03f37679dcbdbe7d5c469f932aaeab7d6a3ad59992dc4de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c431aa4f7bf5bf5f60ee19d7d0e1d6be4def26e921ff09e46ea84dd84f5deb`

```dockerfile
```

-	Layers:
	-	`sha256:a8877aa7f53661111cf71807e8a9c95523ba75b2432233bd563a3290d76ba1e3`  
		Last Modified: Fri, 22 May 2026 21:14:09 GMT  
		Size: 6.5 MB (6452556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:351189f854263679d6891679e5ae394425a753c6cc38a004caa430df86fece18`  
		Last Modified: Fri, 22 May 2026 21:14:08 GMT  
		Size: 13.1 KB (13129 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:8b790b06d2ed61e4a73bf5f482435c7cd54c39aff3646bf83dcd85f2677bb4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253230122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d88882183d6ea89247c26ac461af21fb8b904d9df26216d9ca2360abd286eb3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:56 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 22 May 2026 21:12:56 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 22 May 2026 21:12:56 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 22 May 2026 21:12:56 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Fri, 22 May 2026 21:12:56 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Fri, 22 May 2026 21:12:56 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Fri, 22 May 2026 21:12:56 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 May 2026 21:12:56 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 22 May 2026 21:12:56 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Fri, 22 May 2026 21:13:36 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5352c9fac7db5df7f7525078cd837ceb70ccee025ff01bf15326a7554f2a94bc`  
		Last Modified: Fri, 22 May 2026 21:13:58 GMT  
		Size: 145.6 MB (145638760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43b00c44867a4b55e288af83005dc0d7cfac0259f6b5ecd46670f9dd39df2ba`  
		Last Modified: Fri, 22 May 2026 21:13:57 GMT  
		Size: 54.1 MB (54136947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:62fd55b2cb4397cfb516c3623d618fd5cc8c2343c4ac72ec82e425cc1a4c469a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc9e3cf890c751258f6bb9387ad7e286436b290de785def9c5549fadf3eb70c`

```dockerfile
```

-	Layers:
	-	`sha256:57aaf26c3573701137924643af6c899d3015895f40ed746dff0105fa9b70465e`  
		Last Modified: Fri, 22 May 2026 21:13:54 GMT  
		Size: 6.5 MB (6452063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d0fa8e40fff154e34d25e81eece5f5c68b5020845f2808d4a15c0efdee966e7`  
		Last Modified: Fri, 22 May 2026 21:13:54 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json
