## `swift:slim`

```console
$ docker pull swift@sha256:d9078f3b8b8661957658d2fc3eeb90122d89d2b6084f965ef9db7094c059c211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:0adc0bfbe9d27650aa33ebcf9515f8f53a195ef89a4cf7eb23a8e6c00ffd53b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90428119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaefe31ba677b455f50b02dcd7aef836e3b4005125e52c01f71cdb357dabd36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:14:25 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 06 Mar 2024 03:14:25 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 06 Mar 2024 03:16:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:16:42 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 06 Mar 2024 03:16:42 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 06 Mar 2024 20:58:22 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Wed, 06 Mar 2024 20:58:22 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Wed, 06 Mar 2024 20:58:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 20:58:22 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 20:58:57 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d75ec9855ca39d7d640a88c41ac636b0cf2e257fad0f9b42cad3581418fe4c7`  
		Last Modified: Wed, 06 Mar 2024 03:40:46 GMT  
		Size: 19.2 MB (19193647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f40143a6230b7276ce1b8d32123f049e39edcdc0bbd509eeaa211f0131173f`  
		Last Modified: Wed, 06 Mar 2024 21:12:36 GMT  
		Size: 40.8 MB (40783170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:1ea53ea2f79baaa72c6162bff80172299f70f7801eb9f1cc7481a36f98e56c6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87582656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1842b8d29e23fc931cb51680dfa69a4fdb22be57d849eb21d0be6eadab841c7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:12:40 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 06 Mar 2024 05:12:40 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 06 Mar 2024 05:14:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:14:39 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 06 Mar 2024 05:14:39 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 06 Mar 2024 21:21:20 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Wed, 06 Mar 2024 21:21:20 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Wed, 06 Mar 2024 21:21:20 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:21:20 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:22:19 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92666babbc3ae26c9405adbf4864be66af5f2eb2648af6618ce80b2de94edf5a`  
		Last Modified: Wed, 06 Mar 2024 05:29:26 GMT  
		Size: 19.1 MB (19088217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7e3474899152ceaff4b6ce79feca75afafe91f9eecf7183714fe6360e62caf`  
		Last Modified: Wed, 06 Mar 2024 21:30:32 GMT  
		Size: 40.1 MB (40093801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
