## `swift:bookworm`

```console
$ docker pull swift@sha256:94f35f7d73a6143288ca15780c3b467b7a5c81f4748fd3ba46dc34cef4dd44dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:1afc8e6680da0cfed7d0bd5544ebabad6263655ff7ede9544337a528b06fd33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276912429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddec9037176984eacaeac5020c79a6afa27c5339cac72083884887c218105d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Fri, 27 Feb 2026 22:43:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 27 Feb 2026 22:43:22 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 27 Feb 2026 22:43:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 27 Feb 2026 22:43:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 27 Feb 2026 22:43:22 GMT
ARG SWIFT_PLATFORM=debian12
# Fri, 27 Feb 2026 22:43:22 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Fri, 27 Feb 2026 22:43:22 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Fri, 27 Feb 2026 22:43:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:43:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:44:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Fri, 27 Feb 2026 22:44:09 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b268ca89902e32aa417c9a6cfaf6874f5fa629e636f17aebdb0bc4d6804ce15`  
		Last Modified: Fri, 27 Feb 2026 22:46:18 GMT  
		Size: 198.4 MB (198448840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5836d63de72d6f3274be3d6647b56c574072a9f70d545c4371dcf54c5dd71cb`  
		Last Modified: Fri, 27 Feb 2026 22:46:34 GMT  
		Size: 1.0 GB (1029974639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbbc0b63ee054899753740e6886048aad00a0c18c7494913d033f5e0ad2ab5d`  
		Last Modified: Fri, 27 Feb 2026 22:46:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:c607e4f2e90d7b16d074bbbfe81f3205239d619ed3a61d7b7abbfadef8d251bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11330724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0713ebc7864565ccfcaaaedd632db0910c6cfbb477980f8b0c9544abff3e1c63`

```dockerfile
```

-	Layers:
	-	`sha256:78f781725563b4f52792b75d1948d7d2622fc7c8c68df27319cf1f96c7c93095`  
		Last Modified: Fri, 27 Feb 2026 22:46:12 GMT  
		Size: 11.3 MB (11315001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a180b2959c8fb1486d93def9b524362e43b4ce94b027eedef66300ec8ecccad7`  
		Last Modified: Fri, 27 Feb 2026 22:46:12 GMT  
		Size: 15.7 KB (15723 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:26912030288b2121cf3f19ced06fc99acb8f54b623e5ffcf936bade90f991da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1263161773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8dae30f02b6b810b3cea0a7e37171c3c89ba6c05490d1cff881315bcd0a09`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Fri, 27 Feb 2026 22:42:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 27 Feb 2026 22:42:33 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 27 Feb 2026 22:42:33 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 27 Feb 2026 22:42:33 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 27 Feb 2026 22:42:33 GMT
ARG SWIFT_PLATFORM=debian12
# Fri, 27 Feb 2026 22:42:33 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Fri, 27 Feb 2026 22:42:33 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Fri, 27 Feb 2026 22:42:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:42:33 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:43:20 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Fri, 27 Feb 2026 22:43:20 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c378c4b26e7e51f0620f6d54abdc32d718cdc9fd7e3b0e32cbcae8277d6022a`  
		Last Modified: Fri, 27 Feb 2026 22:45:30 GMT  
		Size: 190.5 MB (190470757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ba48e6838a9a28ec2c31ddd1536314aa9b93919455da67555015a723827287`  
		Last Modified: Fri, 27 Feb 2026 22:45:45 GMT  
		Size: 1.0 GB (1024317633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61ecada0e7c09e42c59232aa6ce4d9708e6f1626c5cc34069fb4c70c9478ff`  
		Last Modified: Fri, 27 Feb 2026 22:45:23 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:955d8a09ea9e5891b89279c283ff4a298b8a49b32528c66d55db950f3a089e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c20886216a7de9ecae2bca10a99f794bd07da5fe126ec0db681fb131528ab2`

```dockerfile
```

-	Layers:
	-	`sha256:af2a0358c4833d3d2b73d050ffd7eb107219855916e2600e11274f6d67112ede`  
		Last Modified: Fri, 27 Feb 2026 22:45:24 GMT  
		Size: 11.3 MB (11343006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9021217e469a17cc91db8f4cc9c6118927d429934242fabbc0866eda37fa70c1`  
		Last Modified: Fri, 27 Feb 2026 22:45:24 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json
