## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:4bd9252d46c1fb1ec1a1884db15a0d020d13ff6a30f4aae0770120e57c6b5c83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:d2f1707e713698e0663f1aea4b5e756c8a67b52efa8cd0af355e9e2e2ee7d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288357019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea98edd58b76c8a19c69bf832735ce1e7eca26f6ea1c073f7503514a21e00c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 22:13:52 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Mar 2026 22:13:52 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Mar 2026 22:13:52 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Mar 2026 22:13:52 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 24 Mar 2026 22:13:52 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 24 Mar 2026 22:13:52 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 24 Mar 2026 22:13:52 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:52 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:52 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d369d06b24abfce8bf1921caa0734dc4a2f28340f898b0978fc14407c3b238`  
		Last Modified: Tue, 24 Mar 2026 22:14:21 GMT  
		Size: 225.4 MB (225400509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:16d060b48caba41666a5bb059b4543536e94c91a1d9619732c54e454d300e1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ca7b99df94e21a094f4ad896ab9a098443ddc8b7ec9f690ef8ddfa3a1c6be6`

```dockerfile
```

-	Layers:
	-	`sha256:999c1f144e1c31454bdd1ce179e25b5cede46077d39511da514986f072c959e0`  
		Last Modified: Tue, 24 Mar 2026 22:14:16 GMT  
		Size: 5.1 MB (5082197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83babe06d8a7799fb5afcee77147d7222f684252fa667e90adc6da146a1c630b`  
		Last Modified: Tue, 24 Mar 2026 22:14:15 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:89939b0583094a2ece7284d7ccc468aacb6ffdf781ee7ecefb3feabb1bd09048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265185298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80644db06679490ea93f5cb8b557173e6459fd76c284ef9caa9a29a6dad13877`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 22:13:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Mar 2026 22:13:15 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Mar 2026 22:13:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Mar 2026 22:13:15 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 24 Mar 2026 22:13:15 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 24 Mar 2026 22:13:15 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 24 Mar 2026 22:13:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb700324fbde11225b3e23f4dae428b5843941fab3e0893721a3020a607b63d`  
		Last Modified: Tue, 24 Mar 2026 22:13:44 GMT  
		Size: 200.4 MB (200382149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:fd7d9d05fa75aadefa136c6dcdc9f1ca49f005c3c94c5bd774a33d1bb16dc264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc49da92f57daad3bfb61c1e54ea135d43ebb61a8029c0f1c4ab305d6b886c`

```dockerfile
```

-	Layers:
	-	`sha256:8f439db8a8301b409b8b328c9eaa0ee114e7b96c4ea7a9ce151c9fe38146ac88`  
		Last Modified: Tue, 24 Mar 2026 22:13:39 GMT  
		Size: 5.1 MB (5081631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362639e691aece9173925fba4e8f56227733bdec3a18e0e14fc24e2dd2acb738`  
		Last Modified: Tue, 24 Mar 2026 22:13:39 GMT  
		Size: 11.9 KB (11934 bytes)  
		MIME: application/vnd.in-toto+json
