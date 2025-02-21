## `swift:bookworm`

```console
$ docker pull swift@sha256:efc964f62a06526f987389c27817bcd44cd63a774254bd5fc2142e18acb3c891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:0a0b3ff4c787eae08ce2523a8364f021724c11cd0ecadde22472c3acd3ba3a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1045688107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb398b94db346995aaf039ae10257e39686db8ac9123fa80c01a6138189af1a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=debian12
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b231d953643d842c9b7b219de7bc755c6f0c430ad1ac5b884ae1db69a91376`  
		Last Modified: Tue, 04 Feb 2025 04:53:16 GMT  
		Size: 198.3 MB (198275864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086e155e5ac0645e62ee6436325b3798e90ab668135817805662d6244d96186`  
		Last Modified: Tue, 04 Feb 2025 04:53:29 GMT  
		Size: 798.9 MB (798932357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667a1bdc497256180ce8b24ee03d01a89a108a6fcff45c7bb01acfb4f9549c4a`  
		Last Modified: Tue, 04 Feb 2025 04:53:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:f743f91126f10cf85b455c8d7706ea6eb4a56f53b2811adc85488a3d10684f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11121693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb529e6d2cf160eed89bbd25b3c79e89d66de966495c47ea2801149ec7d7eba`

```dockerfile
```

-	Layers:
	-	`sha256:bcc5c3e7dcc77bb986a1e1d3c06695da74aa50f2fe096642981645d3f82a8f3a`  
		Last Modified: Tue, 04 Feb 2025 04:53:12 GMT  
		Size: 11.1 MB (11105916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb790a7c12ee911bb108cdbb053f2d1d2e70ebb39534588a7f788c0383e6e3b`  
		Last Modified: Tue, 04 Feb 2025 04:53:11 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:cdcfca461ea8c43fb730ecd7d7485bf3639e43582c990ffeb104d7231d206f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034818276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db812f11863761677dc043c22c39c8afdf0bc0a61ea064746f61c8a822f18b9b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=debian12
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed60f0d6427f97ef2a992fd1e390e36a1c3434a6f3a62c2efac530e477206602`  
		Last Modified: Tue, 04 Feb 2025 18:01:13 GMT  
		Size: 190.1 MB (190100165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e887e700f37a0a5c523e64f310fe1f7573e48b8ed4c7ed384004bdb7ae6020`  
		Last Modified: Tue, 04 Feb 2025 18:01:19 GMT  
		Size: 796.4 MB (796411357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4343f1f1502598dad5f044208d35c262ffafb93e4ff43e511e5436e055590a95`  
		Last Modified: Tue, 04 Feb 2025 18:01:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:d2c6210146272cc9b77ab70bd15cb6400745624737986b0fe13e11502d81615d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11149819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c2447e994ef7a29673a3a433bb5f021379973b48ff07ef13b499719979d738`

```dockerfile
```

-	Layers:
	-	`sha256:f013ca39cf19541360a3e96bbf3ae0654ace91d0b181a2b57123dbe7adc9539f`  
		Last Modified: Tue, 04 Feb 2025 18:01:05 GMT  
		Size: 11.1 MB (11133920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b69f75859e4b1805df39fabda184f44f3a0259aa955276d8eb49b53a90b0f9a`  
		Last Modified: Tue, 04 Feb 2025 18:01:04 GMT  
		Size: 15.9 KB (15899 bytes)  
		MIME: application/vnd.in-toto+json
