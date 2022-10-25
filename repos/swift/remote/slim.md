## `swift:slim`

```console
$ docker pull swift@sha256:6203846e3371bef65fd3ee881717d50914c683342b743bafd6aebe4262b2984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:4b8f906a47c33704ef3679996790e0ac53eaa4311bd7b7a87dc041d8ea59ed55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138989670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a10cfea8944d474072991a08019c5d6df4880fac9f939a90f5673311ec8172`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:32:36 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 25 Oct 2022 18:32:36 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 25 Oct 2022 18:35:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:35:22 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 25 Oct 2022 18:35:22 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 25 Oct 2022 18:35:22 GMT
ARG SWIFT_BRANCH=swift-5.7-release
# Tue, 25 Oct 2022 18:35:22 GMT
ARG SWIFT_VERSION=swift-5.7-RELEASE
# Tue, 25 Oct 2022 18:35:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 25 Oct 2022 18:35:22 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7-release SWIFT_VERSION=swift-5.7-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 25 Oct 2022 18:35:53 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63be0a80d4b1546bdcd0f4b0806e6817af7162ce5da44c287dd1f025ee099f9f`  
		Last Modified: Tue, 25 Oct 2022 19:13:37 GMT  
		Size: 19.1 MB (19142346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0a1bd833f67fb7484ba6540f4601b940fba2fe624f7a2a5b9bbc41b8a5229`  
		Last Modified: Tue, 25 Oct 2022 19:13:47 GMT  
		Size: 89.4 MB (89420950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:365e402542010f5a661f0990f2d9dbd354283458f8a5a597f6cc6fb2fe83b8cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135406011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2ee5ae6412e0424df82e06194152f6c44f338ca6c705e3e0789f1b46816887`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:06:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 05 Oct 2022 00:06:28 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 05 Oct 2022 00:08:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:08:06 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 05 Oct 2022 00:08:07 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 05 Oct 2022 00:08:08 GMT
ARG SWIFT_BRANCH=swift-5.7-release
# Wed, 05 Oct 2022 00:08:09 GMT
ARG SWIFT_VERSION=swift-5.7-RELEASE
# Wed, 05 Oct 2022 00:08:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 05 Oct 2022 00:08:11 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7-release SWIFT_VERSION=swift-5.7-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 05 Oct 2022 00:08:54 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d28a3b1a157a466b8634ccf6f98c5e36a5e6f7b77b51689f74ab5ae323a93ee`  
		Last Modified: Wed, 05 Oct 2022 00:16:30 GMT  
		Size: 19.0 MB (19010004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c859a0ca9145d73e7a97f9fcb1ba5bc37d2233c3b3298bf6357908a0e70c7e`  
		Last Modified: Wed, 05 Oct 2022 00:16:40 GMT  
		Size: 88.0 MB (88013752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
