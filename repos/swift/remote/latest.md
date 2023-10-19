## `swift:latest`

```console
$ docker pull swift@sha256:d1a20a7ca0272bc0313a443b313762e465bd657674e41fbd06a06740a389a84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:3fdc5ac4d86fdcf953e11aba87cd0b32e56c1d7a39d1b0db8e48839f87172382
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **812.8 MB (812806419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc638424d9f4bffdd90660496e9ad6ce5d4443b009f6fb339b45b50260ca69f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 06:21:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 13 Oct 2023 06:21:45 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 13 Oct 2023 06:22:51 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 06:22:52 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 06:22:52 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 19 Oct 2023 19:36:45 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Thu, 19 Oct 2023 19:36:45 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Thu, 19 Oct 2023 19:36:46 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 19:36:46 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 19:37:38 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Thu, 19 Oct 2023 19:37:45 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a36b75cc2e15afb22e2fdb9797195d738922a07a77e47913f085c78919c8f`  
		Last Modified: Fri, 13 Oct 2023 06:46:16 GMT  
		Size: 175.4 MB (175413804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a659dca10c17a69eb5726b276c2aaa86e114f56fc8ec4fe1ad817a179a1f8b2`  
		Last Modified: Thu, 19 Oct 2023 20:03:16 GMT  
		Size: 607.0 MB (606953303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601d71a7ecfb948583bd00c2b2869860b9078f7738082f51c6617c0bc9cf750b`  
		Last Modified: Thu, 19 Oct 2023 20:01:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:32e059335fd20fa2afe452d64f940129d6b6a99180265eb3212105d1e305270e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **801.6 MB (801571513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e629af8e87dc8a208dd59e5056ef6dbc0690b6706902044ba2926e514077de11`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 03:11:07 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 13 Oct 2023 03:11:07 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 13 Oct 2023 03:12:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 03:12:09 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 03:12:09 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 19 Oct 2023 20:04:17 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Thu, 19 Oct 2023 20:04:17 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Thu, 19 Oct 2023 20:04:17 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 20:04:17 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 20:05:12 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Thu, 19 Oct 2023 20:05:24 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97118e2e53f65985f7768cea5cbf82a7c20a83156add390f122f3fca7a537f88`  
		Last Modified: Fri, 13 Oct 2023 03:26:12 GMT  
		Size: 171.7 MB (171664690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a87ea149fb8f67320af3c912dea0f24e8fffe957143f449334785f10b2f9b22`  
		Last Modified: Thu, 19 Oct 2023 20:18:20 GMT  
		Size: 601.5 MB (601514682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dce387f39142b57e9d765cae72babb779be129cbbdb8b17c163ed3710b51b4`  
		Last Modified: Thu, 19 Oct 2023 20:17:19 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
