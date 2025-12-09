## `swift:bookworm`

```console
$ docker pull swift@sha256:73f569f5536fe3c9ad5109eb4622c5560af7424d55304955190e5fbccc047b86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:6271bab49b3df0c33610653c3282eba358e40318a29f2a0918004d08e0d6d70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276383505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a617ea4e392e457d0a31861fdad4801c0978eaebd597e6d96437b52742889c8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:45:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 08 Dec 2025 23:45:22 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 08 Dec 2025 23:45:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:45:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 08 Dec 2025 23:45:22 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 08 Dec 2025 23:45:22 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Mon, 08 Dec 2025 23:45:22 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Mon, 08 Dec 2025 23:45:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 08 Dec 2025 23:45:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 08 Dec 2025 23:46:05 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 08 Dec 2025 23:46:05 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46ce461134aa35e8cd0b992a05f2c9a1f0c100dc3bb6b5d1f058347a7030903`  
		Last Modified: Tue, 09 Dec 2025 01:39:23 GMT  
		Size: 198.4 MB (198409241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39be9132c2a3f7d93d917b3f133f74dcb4b67af465eb9e3d2322eae23d2c7a0`  
		Last Modified: Mon, 08 Dec 2025 23:50:58 GMT  
		Size: 1.0 GB (1029493354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9887adb3efc4d2ac8b168e3435816177b3b8f05f173abc132bf92e24f2054e96`  
		Last Modified: Mon, 08 Dec 2025 23:48:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:2e70a7f013525dfbe847cc7de5075590e4ed010f1a263be84b31921cc27661f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11330044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add6f80ae62968a60742013567d3acdf7d5744c9dfe93a1317eeb10273fa2f77`

```dockerfile
```

-	Layers:
	-	`sha256:3fc20348a30949a87fc00e6be7267443a22bc465b3474a8af37c211e233d343e`  
		Last Modified: Tue, 09 Dec 2025 02:48:30 GMT  
		Size: 11.3 MB (11314322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e55c9b9c7931868ad0bb0cc8970b0320f9fdce04a76759bbe70f115ee54fba8a`  
		Last Modified: Tue, 09 Dec 2025 02:48:38 GMT  
		Size: 15.7 KB (15722 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:fd33e2a8111302258a7970e7489af93e15577f2e27e0009385a6483ffac11b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1262470147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a30c4b00a7979af9389061e120187b064de90e3d5b6eedbac5f3d47cac51a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:29 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 08 Dec 2025 23:53:29 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 08 Dec 2025 23:53:29 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:53:29 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 08 Dec 2025 23:53:29 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 08 Dec 2025 23:53:29 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Mon, 08 Dec 2025 23:53:29 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Mon, 08 Dec 2025 23:53:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 08 Dec 2025 23:53:29 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 08 Dec 2025 23:54:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 08 Dec 2025 23:54:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63773517bddac37eb8a57bc7e10a6ca1ffb12ee5965fbe66508dd8f272cf5d8`  
		Last Modified: Mon, 08 Dec 2025 23:57:08 GMT  
		Size: 190.3 MB (190315435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d9bdcb551fa2b2d1e3acdd399214802bc58165971c55eb2c9008f1d30bb596`  
		Last Modified: Mon, 08 Dec 2025 23:57:44 GMT  
		Size: 1.0 GB (1023795467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66856f8eadbe0763873dd154c482aa043134a4e79436b575dad452222a7d820b`  
		Last Modified: Mon, 08 Dec 2025 23:56:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:083c836994a346570d8eac0adb8112c05f68e6d5212d622728f38c2d3400d551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad63eac3d37fa2885cd992539f7c5ab224147919179db68ff70d784df1ee57f6`

```dockerfile
```

-	Layers:
	-	`sha256:e89c4f821b7db37f05b2f6cfdbb29abcd2cff4d16b543754653f118d19520591`  
		Last Modified: Tue, 09 Dec 2025 02:48:47 GMT  
		Size: 11.3 MB (11342327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3dc82bb531e2181d93fd0070e045146ef4cb3f86600163fd3aa3cfbc411d30`  
		Last Modified: Tue, 09 Dec 2025 02:48:48 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json
