## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:9a83d2061260370318fc2134780730f7c2dfd7b9f65c46aaac0cf617dbd5ded9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:9fc47c0aa65e91fb5cdb8789e7776974712bc9778c0820b6b25c4ac45e51f4da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **966.2 MB (966171513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2707bba83742505084906f21ca2b89dcdd437eafdfc57c62cca0e43160e784ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:52 GMT
COPY dir:b97e45ed3c8a3f1b9f45748b11869cc647c58d36ef808547c8bfc5893d6bcdef in / 
# Fri, 12 Jan 2024 21:45:53 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:36:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Jan 2024 22:36:59 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Jan 2024 22:37:30 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 12 Jan 2024 22:37:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 12 Jan 2024 22:37:32 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 12 Jan 2024 22:37:33 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Fri, 12 Jan 2024 22:37:33 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Fri, 12 Jan 2024 22:37:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Jan 2024 22:37:33 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Jan 2024 22:38:23 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 12 Jan 2024 22:38:30 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:1243323cbbce9384c54ac7f8354a552ac222dc3ce5d0ece482a667a33fce339c`  
		Last Modified: Thu, 11 Jan 2024 06:58:33 GMT  
		Size: 62.7 MB (62661001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8765f141b6554e87238a35543b4243696fc052a3a03968b30d887fe571a3c`  
		Last Modified: Fri, 12 Jan 2024 22:55:48 GMT  
		Size: 295.2 MB (295225383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd4599e8defc9d654ea817e84ccb89f96a691cce116694bd33964f2656011de`  
		Last Modified: Fri, 12 Jan 2024 22:56:35 GMT  
		Size: 608.3 MB (608284931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebf1b8f7ed17bf359bc88ccfc6115220b6ef6115edd079a95f5d4b46bc6ff08`  
		Last Modified: Fri, 12 Jan 2024 22:55:12 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:305cae5c6a7a02d0407654a952c394eb07da9998802c0a1252e980e62fea4795
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **928.3 MB (928310386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd7d857e77fc9dcbbf79242a9b5d7fc2b8fb4d2db14ec364063c03fcca78d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:23 GMT
COPY dir:eb2de4474e28d9fde9bbe1ffb630978f47dae30856e760ca73ebb5d0cb75efd7 in / 
# Fri, 12 Jan 2024 21:49:24 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:46:25 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Jan 2024 22:46:26 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Jan 2024 22:46:50 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 12 Jan 2024 22:46:53 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 12 Jan 2024 22:46:53 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 12 Jan 2024 22:46:54 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Fri, 12 Jan 2024 22:46:54 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Fri, 12 Jan 2024 22:46:54 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Jan 2024 22:46:54 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Jan 2024 22:47:34 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 12 Jan 2024 22:47:45 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:9620bfd6832ce2ca50093b819c4f62fd86c4b96a997fd5da88afa856b28cb1a0`  
		Last Modified: Fri, 12 Jan 2024 19:03:15 GMT  
		Size: 64.5 MB (64462448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ceeafaf2d5c13dc8b15abd77f74652be589d6879b40db91627fc90e7763f8fa`  
		Last Modified: Fri, 12 Jan 2024 22:54:22 GMT  
		Size: 261.5 MB (261481860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997e480ec3e441248104b70a80f2a6a888434de3b85ac3f0d222a1ab4ac79fce`  
		Last Modified: Fri, 12 Jan 2024 22:54:57 GMT  
		Size: 602.4 MB (602365877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae312e4dbfbfa86f5c5fec59c074b5d5ffa2fb050ac19fad7d2618eb0457989`  
		Last Modified: Fri, 12 Jan 2024 22:53:56 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
