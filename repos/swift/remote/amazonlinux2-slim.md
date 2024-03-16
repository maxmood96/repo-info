## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:14155bcebf8b3c52ccf988af5253b853ac98ee2996aa88b0b61bf215158874d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:88c0e38822f30ae4dad90a4f6ac4ffd43e69b8d0b4ed14b401f42d83cfc12d00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252771562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f6e91294a2b3ab49ddd771399a42a1d77013834bcde8846eb0c8c750858e9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 23:50:32 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Mon, 11 Mar 2024 23:50:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Mar 2024 00:18:52 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 12 Mar 2024 00:18:52 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 12 Mar 2024 00:20:31 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 12 Mar 2024 00:20:31 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 12 Mar 2024 00:20:31 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Tue, 12 Mar 2024 00:20:31 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Tue, 12 Mar 2024 00:20:31 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 Mar 2024 00:20:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 Mar 2024 00:21:14 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ae666865150f892fc20fe2ed548f30fe407ada9f00846e4a225ac2988d30e2`  
		Last Modified: Tue, 12 Mar 2024 00:40:08 GMT  
		Size: 190.1 MB (190121009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:8453f71120d32cadb82a7572fa8af843b3a5cd47c5cf2f301bb2fc0e3c1b110e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224955925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985c486bade7fbed7f88878251a8bcd21dc4b70e3d8b8aae59d03fa29226b74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 00:06:05 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Sat, 16 Mar 2024 00:06:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 10:30:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 16 Mar 2024 10:30:37 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 16 Mar 2024 10:32:14 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 16 Mar 2024 10:32:14 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Sat, 16 Mar 2024 10:32:15 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Sat, 16 Mar 2024 10:32:15 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Sat, 16 Mar 2024 10:32:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 16 Mar 2024 10:32:15 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 16 Mar 2024 10:32:46 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1567484c1db5250c480c8c7970de73aaf900bb6920c166a40e13e986ac123e4`  
		Last Modified: Sat, 16 Mar 2024 10:41:04 GMT  
		Size: 160.4 MB (160379551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
