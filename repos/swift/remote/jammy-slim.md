## `swift:jammy-slim`

```console
$ docker pull swift@sha256:7d46734ba7da7763579d889583ba8024d26b443032e613e4a5d8522533dad868
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:678a4507ac67343524688710e2c82dd3e2944fc08de9ee59a61ef94285309931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97718741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df02f0fcf01fa4aa8d9d984b34821704ceb55399932229118af94b43f7bb8c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08ef5527b754988b204d196ede91b35a838be017e5bc66fc440047a48281469`  
		Last Modified: Wed, 28 May 2025 18:28:24 GMT  
		Size: 19.2 MB (19222830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d013a2ebc9dc8f460b8b1ba00f1ffc67d1495261a307c9c4eb0c7ac5ba673544`  
		Last Modified: Wed, 28 May 2025 18:28:31 GMT  
		Size: 49.0 MB (48963297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:37e2879e73b23ac21603f28a6ff980e4a636cd2aac407b698d874d9aec5d8b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2963675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082e707b9efbac7917e895b892f5cf67c078e1922b83d49dd8bf89458bde2581`

```dockerfile
```

-	Layers:
	-	`sha256:2f9923edb70a9daa343ad40bf90df84389e7ece1c043d0c22b0b653ecc9f3da0`  
		Last Modified: Wed, 28 May 2025 18:28:23 GMT  
		Size: 2.9 MB (2949693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e732546a7dc8ca090ccffef036f59f98ac3ca0476edff46af0151fdc105c7c90`  
		Last Modified: Wed, 28 May 2025 18:28:23 GMT  
		Size: 14.0 KB (13982 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b8495cf48631e4465f7a3501e29bed54a4252da7e46b28ed6f70f780ce71fac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94833187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17d82b7bce27408aa7a08ac41a5ca0c814ad1bb65b89fb443b70d3449a4c542`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd472a1dba7563c8b50af4dfac5665c4c39192bb6b1b8050dba08ef9f376677d`  
		Last Modified: Tue, 27 May 2025 21:19:51 GMT  
		Size: 19.1 MB (19087803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e89f0feeed0062779ea1fefed5511342cec1e6166be0b388f7806dd432e2d`  
		Last Modified: Wed, 28 May 2025 18:36:22 GMT  
		Size: 48.4 MB (48391173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:f358a047481e667d7612f47c64d5a5c52b3d472e83c5c05c91227f5863737a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2964066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196ae7ba9f11742de6655a16e77a35ee3d17d12fecd2f97ee0ed6a300d8e055a`

```dockerfile
```

-	Layers:
	-	`sha256:bebb93c54d063863e1377d854a5c799c750db23c5d27279d187c3e3a9c930c9c`  
		Last Modified: Wed, 28 May 2025 18:36:21 GMT  
		Size: 2.9 MB (2949976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7917e50a916b59256e17b07a88794844114d03d97ed1bb82ea3f02f00e634f36`  
		Last Modified: Wed, 28 May 2025 18:36:20 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json
