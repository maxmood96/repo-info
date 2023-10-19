## `swift:slim`

```console
$ docker pull swift@sha256:9809396932ec79fd891d3d7beb37c666b76bf9b4e3319142dcb5eed4b19629e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:f2368a00ea9385ac16422f6bbf564ef62e8fc3e8e503cf85a6f12fb26f9a3e6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90448168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5caa6a5869be3e0180659e90c99334eece3c615a36bba2dbefa5bff548e3e2b1`
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
# Fri, 13 Oct 2023 06:24:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 06:24:01 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 06:24:01 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 19 Oct 2023 19:37:55 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Thu, 19 Oct 2023 19:37:55 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Thu, 19 Oct 2023 19:37:56 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 19:37:56 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 19:38:27 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadc893cce371897a8c525ab6746986ca0a550231ca98c07f67a88fa9a658e2c`  
		Last Modified: Fri, 13 Oct 2023 06:47:31 GMT  
		Size: 19.2 MB (19192893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c71ba90632de6631de70556d0e9926186ff8203ff38e9185d6ced3a84019d7`  
		Last Modified: Thu, 19 Oct 2023 20:03:40 GMT  
		Size: 40.8 MB (40816164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:8c65b5475583385ef29d39860ac73f8be8352d4f01b2cef1b6e15886fd68da94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87616058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5e9dd733e24ab722c6841c9c42ec2d2c6688a8f883411cbe631961444f69f6`
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
# Fri, 13 Oct 2023 03:13:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 03:13:37 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 03:13:37 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 19 Oct 2023 20:05:26 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Thu, 19 Oct 2023 20:05:26 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Thu, 19 Oct 2023 20:05:26 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 20:05:26 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 20:06:01 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cb0413ea4af52712a026c020a1edd0454ad243985a249db921e73e0d498d12`  
		Last Modified: Fri, 13 Oct 2023 03:27:15 GMT  
		Size: 19.1 MB (19087954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb03450b1dcdc49826a17f357787f142c8b5a3aaf326546558012070f3a9dc8`  
		Last Modified: Thu, 19 Oct 2023 20:18:44 GMT  
		Size: 40.1 MB (40136165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
