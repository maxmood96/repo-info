## `swift:slim`

```console
$ docker pull swift@sha256:932b8506bab22ff5697d5ca5e4590f0d15f15e22ff2cf286e5fac89e21882cca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:abc79490e0364baca77809aa1619af548c34e6a61bb0b0836d01a03c5dbd8494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98839381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f4419379bb5dd3d1e32aa2607978e0d6a7d186a76f4a22145923b975d0cb2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 06 Sep 2025 05:03:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_BRANCH=swift-6.1.3-release
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_VERSION=swift-6.1.3-RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de651a9b212cca0756906bc843cac518d03f04b27f516400a0ae044cb12979f0`  
		Last Modified: Mon, 08 Sep 2025 16:47:19 GMT  
		Size: 20.0 MB (20018211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b18d34d0c0d74b6dd8a5d0ec68634a7debf888ff8e71db3c41146de5db254be`  
		Last Modified: Mon, 08 Sep 2025 16:47:22 GMT  
		Size: 49.1 MB (49098106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:c4667bc6381c6e947ebfd4d265d8581faa9a7b432fbb162041b7d5a2ac2dcc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93227e7ebf891d6fdcf36f1fff10668a46b94a36e6e85a1d4bc5877d05a62778`

```dockerfile
```

-	Layers:
	-	`sha256:617d229bbfe4721cf4d7c42dada1194cfdfced9727fe5fdb846b849c94c6c1a2`  
		Last Modified: Mon, 08 Sep 2025 19:48:29 GMT  
		Size: 2.5 MB (2497214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a87bd9bb5d13cddf8f176f5e2f7322db84f348d53e46fb68862654f586354a2`  
		Last Modified: Mon, 08 Sep 2025 19:48:31 GMT  
		Size: 14.9 KB (14881 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:e9984de82fe8014b1a2dbfef7566548e64e5a07a689c671c3e21c7e6bd62b868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97345233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7724ea0f8648f972ac3e447331431f752c5a2d5614f7209913db25d6181dec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 06 Sep 2025 05:03:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_BRANCH=swift-6.1.3-release
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_VERSION=swift-6.1.3-RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42db643df7942f2712dab458b4319ca5ca0856acc70f89ec0e3bb57a2a291495`  
		Last Modified: Mon, 08 Sep 2025 16:49:01 GMT  
		Size: 20.0 MB (20027539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bf1e9c9dea889023dc6ddf87f6a793e0ead8a822d7049c04659689df9ed851`  
		Last Modified: Mon, 08 Sep 2025 16:49:02 GMT  
		Size: 48.5 MB (48457454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:3e822696011d2ac437e7924669d2eddd99bf84d0e1f06017f61e0f03948ec726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97d867efe5321fbe7ed055b4d09347c30f0b8a4e9c4458ae1be03433283d198`

```dockerfile
```

-	Layers:
	-	`sha256:fdd8794962da78f1e574b2fd86b34483d51fa955c60f56f08ede2bb3001be54e`  
		Last Modified: Mon, 08 Sep 2025 19:48:35 GMT  
		Size: 2.5 MB (2498330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6889fb8ba66ee2e1ecacb5d1343e658a75a9c7c04553f0f49dfaec99c34ecda0`  
		Last Modified: Mon, 08 Sep 2025 19:48:36 GMT  
		Size: 15.0 KB (15024 bytes)  
		MIME: application/vnd.in-toto+json
