## `swift:latest`

```console
$ docker pull swift@sha256:081f70bfa456ed066e0a06b1959d4fbf490b2eca29e533b1448f8075058e62a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:9247890114d2c02b7b8e68763aa982e47e054dab713ff2a3792747e071a0cdfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **812.8 MB (812791670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac494d12480ed0ea57214b975957dea6555b505e3965be6305d86643a2a888e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 12:18:48 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 16 Dec 2023 12:18:48 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 16 Dec 2023 12:19:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Sat, 16 Dec 2023 12:19:41 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 16 Dec 2023 12:19:41 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Sat, 16 Dec 2023 12:19:41 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Sat, 16 Dec 2023 12:19:41 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Sat, 16 Dec 2023 12:19:41 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 16 Dec 2023 12:19:42 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 16 Dec 2023 12:20:30 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Sat, 16 Dec 2023 12:20:37 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca41c19834942f0a088d4f74851c090af44e570a1caa30fb50a658e133f18970`  
		Last Modified: Sat, 16 Dec 2023 12:42:19 GMT  
		Size: 175.4 MB (175394011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73168ed394c3e0b3413e50c55b91701bd308cd263180f4bcf73f6100c60e552`  
		Last Modified: Sat, 16 Dec 2023 12:43:12 GMT  
		Size: 607.0 MB (606950879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2bb3617183be8387ff76634d1da10ff95544cf118034090e21db2b6d9244d2`  
		Last Modified: Sat, 16 Dec 2023 12:41:51 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:6fcaf3dd14619421502aa7eb9057cff62c9e45b71a9d598c2b65f16f71abc630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **801.9 MB (801864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0148ff792b27a10251f94a0f9acaa818e934cbd7516b43038143d32042f12d61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:59:45 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 16 Dec 2023 11:59:45 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 16 Dec 2023 12:00:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Sat, 16 Dec 2023 12:00:44 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 16 Dec 2023 12:00:44 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Sat, 16 Dec 2023 12:00:44 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Sat, 16 Dec 2023 12:00:44 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Sat, 16 Dec 2023 12:00:44 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 16 Dec 2023 12:00:44 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 16 Dec 2023 12:01:29 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Sat, 16 Dec 2023 12:01:42 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ace5a253b82d52f5515b57b95d534bb1b60f109af65843cc045beedf349f5`  
		Last Modified: Sat, 16 Dec 2023 12:15:43 GMT  
		Size: 171.7 MB (171662262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e626083456fe2fd2bd959f660f6fc88a2364d6fc5468c67fbfe3fd743ad734`  
		Last Modified: Sat, 16 Dec 2023 12:16:22 GMT  
		Size: 601.8 MB (601801985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04365fecd14bfe10fb679f17d597c70b78565a0dcce7228454f72ce3c9a9a10`  
		Last Modified: Sat, 16 Dec 2023 12:15:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
