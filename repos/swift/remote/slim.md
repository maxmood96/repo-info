## `swift:slim`

```console
$ docker pull swift@sha256:e0d758dd44f38434896abc60f7efa85863a5256b32d1cf853210063d61477a75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:94c110a9d9a19bcccd48e1ac6c0ad576c985f70a5061547dca143ea5e1b17547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101081205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306688966cc24e3a3ede4bb79433429f594f9abafa6f6b4f7875a39bca34012b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:13:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:13:06 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:13:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 18:13:06 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:13:06 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 13 May 2026 18:13:06 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:13:06 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:13:06 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:13:06 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:13:43 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafa7226ac50108bd13f342a143e97b6305b91aa5c4db6fb5aa2fdfa59e6914b`  
		Last Modified: Wed, 13 May 2026 18:13:56 GMT  
		Size: 20.0 MB (20023641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc55b9e09d1c6fbd70ddabee27aa4a2d75b9a4900c0ce6eec50011b15e634a96`  
		Last Modified: Wed, 13 May 2026 18:14:00 GMT  
		Size: 51.3 MB (51324586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:2c1f2d9558725807f93806b1a104335980dec30ac3ecd10d12976553f1bfb99f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4051bdab9dc5c283679fcabff2f5f5e15d32969834f2fc12b9c580601ca835`

```dockerfile
```

-	Layers:
	-	`sha256:1d3e74b1453003233a42a33407fdc7b3c359226c4ef92925f764c08868919590`  
		Last Modified: Wed, 13 May 2026 18:13:55 GMT  
		Size: 2.5 MB (2497246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f630c8eeadd6dab38147f0db1abf2bfe332fa2cdbd9644c004a8060e75ad64b3`  
		Last Modified: Wed, 13 May 2026 18:13:55 GMT  
		Size: 14.8 KB (14838 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:57f08e28fa9b90599e3537259a609bd4f3d2bed806a18af20765d5700dec1672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99530079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0a8b949189e9af3c584571a28078d44281b5bf9e606ec9518339c5d882726`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:03:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:03:22 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:03:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 18:03:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:03:22 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 13 May 2026 18:03:22 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:03:22 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:03:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:03:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:04:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2df7ee40a76cd927427f239e0c8b24c75bc0160f73d9c35d04a931bd177c6b`  
		Last Modified: Wed, 13 May 2026 18:04:24 GMT  
		Size: 20.0 MB (20038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545b327279813635d5f119403bcc59763178f1d16c867f6fc404bf8eac5a085c`  
		Last Modified: Wed, 13 May 2026 18:04:25 GMT  
		Size: 50.6 MB (50615848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:f0a5328c7699cc1763499c2d1486c435fd809e8993ce3ff7f05f6e6bca3eb52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731025ad8e8af0178477ba2f04b9eb00ad258e4cde6991db6fa4974811d4678f`

```dockerfile
```

-	Layers:
	-	`sha256:88ce3f31df5db3077abcbd270f3dc67dd665c35264bd2bb9994397c911b64df7`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 2.5 MB (2498362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5facdbda01a2752be89db4a98414d2d7ce126e60b17dab17bf2f917dd594998b`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json
