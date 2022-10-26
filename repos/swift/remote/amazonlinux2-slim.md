## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:af60f3483cbe7e25908f65eac6be4c896755c254326bf1e390fa10af2c3e31eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:02a5da3acc1e8083833b0066274a335d5a6bd3aed87cf7dc5441e8e4fbd6b14f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288436122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fb352a2c3085ef01b1358a1447ff007cb7a768307bb756e3a86442201243f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Oct 2022 00:19:49 GMT
ADD file:33ce740675602f8911c110c617b08d74ebe9c26c82226b4815019d8c2d0a2263 in / 
# Fri, 21 Oct 2022 00:19:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 00:37:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 21 Oct 2022 00:37:44 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 21 Oct 2022 00:39:22 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 21 Oct 2022 00:39:22 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 21 Oct 2022 00:39:22 GMT
ARG SWIFT_BRANCH=swift-5.7-release
# Fri, 21 Oct 2022 00:39:22 GMT
ARG SWIFT_VERSION=swift-5.7-RELEASE
# Fri, 21 Oct 2022 00:39:23 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 21 Oct 2022 00:39:23 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7-release SWIFT_VERSION=swift-5.7-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 21 Oct 2022 00:40:14 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:e3cfe889ce0a44ace07ec174bd2a7e9022e493956fba0069812a53f81a6040e2`  
		Last Modified: Wed, 19 Oct 2022 18:11:43 GMT  
		Size: 62.3 MB (62306642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a54ea0238fac508ba60c079a2dba4957100d46de467de896e2a751c7577b394`  
		Last Modified: Fri, 21 Oct 2022 00:58:34 GMT  
		Size: 226.1 MB (226129480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:0eaaa6bb3edec967161e129604d73a5ebb412f4f74c53243a06c618139c5b3ea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252809526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0b4e8aeff81fdcd8b6b84a3a09bb597e50e0c9b14e3d3b83e2e0df8d9c5bd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Oct 2022 15:27:06 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Wed, 26 Oct 2022 15:27:06 GMT
CMD ["/bin/bash"]
# Wed, 26 Oct 2022 19:27:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 26 Oct 2022 19:27:42 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 26 Oct 2022 19:29:04 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 26 Oct 2022 19:29:04 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 26 Oct 2022 19:29:04 GMT
ARG SWIFT_BRANCH=swift-5.7-release
# Wed, 26 Oct 2022 19:29:04 GMT
ARG SWIFT_VERSION=swift-5.7-RELEASE
# Wed, 26 Oct 2022 19:29:04 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 26 Oct 2022 19:29:05 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7-release SWIFT_VERSION=swift-5.7-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 26 Oct 2022 19:29:38 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b96aa24639fe965498e8341946b5e24895ccc2ff20b31241bc79d0e6f6017e`  
		Last Modified: Wed, 26 Oct 2022 19:33:21 GMT  
		Size: 188.9 MB (188889657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
