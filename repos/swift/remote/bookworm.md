## `swift:bookworm`

```console
$ docker pull swift@sha256:5b36d0cbe21b24e22fb443abe7f0606e7ae05b7ecfd9479d058db9eebb3125cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:64cec474bfdaaed168dc510348c0f4c6ee17af425b97af298b7ef515a681f45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276582166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88d78eb47132db71e57e3e7d4e71807b493b1082354fddf648330fbc6094a78`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Feb 2026 19:50:28 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Feb 2026 19:50:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:50:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Feb 2026 19:50:28 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 24 Feb 2026 19:50:28 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Tue, 24 Feb 2026 19:50:28 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Tue, 24 Feb 2026 19:50:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Feb 2026 19:50:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Feb 2026 19:51:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 24 Feb 2026 19:51:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882d2f88ef7686069132325a1082a33467d6daa7918727c0254fc5c8330a9a6c`  
		Last Modified: Tue, 24 Feb 2026 19:53:17 GMT  
		Size: 198.4 MB (198448962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465336602d97d4d13df0822e806cf0ecad2f24ee20a43d863dbb38c82aae417d`  
		Last Modified: Tue, 24 Feb 2026 19:53:34 GMT  
		Size: 1.0 GB (1029644253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57488dca2760fd2af7d6a9d2dcca9bec8d48b279e95fa00769c9b5c3263cf778`  
		Last Modified: Tue, 24 Feb 2026 19:53:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:584013e1026de94d0259def7f201f59c7f91579d3d21fb023ab87133332756d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11330724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b058dbf0e4c5d37e3a07eb0dce931ff3e4fe77d4935da1a28cec94d4eb93e1`

```dockerfile
```

-	Layers:
	-	`sha256:36ada28e687e87ac3f8279cfc904ef253d0715b612e1df78949efa002eb99600`  
		Last Modified: Tue, 24 Feb 2026 19:53:11 GMT  
		Size: 11.3 MB (11315001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9041955adc2c8358e0579526adae5be3a378ccc6eeccb818786ad5c6c2d051e6`  
		Last Modified: Tue, 24 Feb 2026 19:53:10 GMT  
		Size: 15.7 KB (15723 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d67fc88f0be664fc53d37d7deca3fc205ce049ec30c7294f85d5cb67f29cf4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1262821317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08f07b883f9cd559a77d67cc74e933733aa1013797c28cc43d1490a40afc8ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:12 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Feb 2026 20:01:12 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Feb 2026 20:01:12 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:01:12 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Feb 2026 20:01:12 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 24 Feb 2026 20:01:12 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Tue, 24 Feb 2026 20:01:12 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Tue, 24 Feb 2026 20:01:12 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Feb 2026 20:01:12 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Feb 2026 20:02:01 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 24 Feb 2026 20:02:01 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7271307a8bcb13fa8a06da83f75127f86fbf6780d4a06c0fee401b7acb3d5c7`  
		Last Modified: Tue, 24 Feb 2026 20:04:15 GMT  
		Size: 190.5 MB (190470631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac9e7e34d4445d68fffee66fb9e5215b39c00f555fc8e58a67483e4573797bd`  
		Last Modified: Tue, 24 Feb 2026 20:04:32 GMT  
		Size: 1.0 GB (1023977303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03102739b2a1b4fad265fd68038cb2cf2a8ecdc6f2b53b56afdcdee8f395df3`  
		Last Modified: Tue, 24 Feb 2026 20:04:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:865a2965a0de147a7c08a5ff3efd420ac3e80f2acd9b1c568b05b4691f5acb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a66080d871184bd04e7bbd3006a0ad912ec5385ab982c516afe7dd47174b8e`

```dockerfile
```

-	Layers:
	-	`sha256:7c53e1276d0b2f9014aaa9be99930de01fab6b40ae21cfcb35d53b33be564c87`  
		Last Modified: Tue, 24 Feb 2026 20:04:09 GMT  
		Size: 11.3 MB (11343006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d018cecc0c99610bb251319da65d5f1d9e0f3ef2165bbc1f1f3867a187e92644`  
		Last Modified: Tue, 24 Feb 2026 20:04:09 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json
