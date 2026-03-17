## `swift:bookworm`

```console
$ docker pull swift@sha256:6ff0d2567e1a9ce6b2bb1212a8d7ade9dc90e6fb02bed349fc664b981c206858
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:02f1973eeb805f98f0c3e4490c72739961ddd077e678e6e906a092aba10d3f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276915418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092cc7addb34fbb8d5e87dce0c15ec0b9b296fa71a4ff7c2f9b5600fa9b57162`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:11:56 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 16 Mar 2026 23:11:56 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 16 Mar 2026 23:11:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:11:56 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 16 Mar 2026 23:11:56 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 16 Mar 2026 23:11:56 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Mon, 16 Mar 2026 23:11:56 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Mon, 16 Mar 2026 23:11:56 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 16 Mar 2026 23:11:56 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 16 Mar 2026 23:12:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 16 Mar 2026 23:12:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c681a61cfcc7e07b14affb33db3a66ab96a7b0f7a2e2a903e946771cf0dcc09e`  
		Last Modified: Mon, 16 Mar 2026 23:14:57 GMT  
		Size: 198.5 MB (198451984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1161315d21a05beda532e1c3f80d129dfc2bcc40dce099e771069b87169eb6b`  
		Last Modified: Mon, 16 Mar 2026 23:15:12 GMT  
		Size: 1.0 GB (1029974676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ee5bcaeca7ffda7b9a3955b8897d4d978c3c740cd4a9e2ef63b65745a6bcb`  
		Last Modified: Mon, 16 Mar 2026 23:14:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:9bcb5e308b25abbfaefd866eb105cc2da90f101a205b6286cb03cc8f64371418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11330724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0c6ad1179cd32a43489d8da20e8cf1e30ec743c085dcdddd0ac4585cf84536`

```dockerfile
```

-	Layers:
	-	`sha256:71e804d519977a34574ce2042755da63b432eb1d2a76223639336090605c0f9e`  
		Last Modified: Mon, 16 Mar 2026 23:14:51 GMT  
		Size: 11.3 MB (11315001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b897b7685fe5c3cc000759abed1cf647125d37fcbeb8942cc325a6c03155c8f9`  
		Last Modified: Mon, 16 Mar 2026 23:14:50 GMT  
		Size: 15.7 KB (15723 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:7238cdb0193b895b5be8138f7a86d1b34a7d880610d0f815ceb133c315fb0972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1263162724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ce7c3fe4e30dec4fb91e3e1a850f19685daea9ff7f6f2838c26351a22eaac1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:17:11 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 16 Mar 2026 23:17:11 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 16 Mar 2026 23:17:11 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:17:11 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 16 Mar 2026 23:17:11 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 16 Mar 2026 23:17:11 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Mon, 16 Mar 2026 23:17:11 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Mon, 16 Mar 2026 23:17:11 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 16 Mar 2026 23:17:11 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 16 Mar 2026 23:17:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 16 Mar 2026 23:17:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdbee508f029525febcf1c6631c1f03d281f1e4911c218ea9b3eeb0ea0c95fa`  
		Last Modified: Mon, 16 Mar 2026 23:20:27 GMT  
		Size: 190.5 MB (190472023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c956dc93416956fb66d0f069ec08f168c87f2de2a53c1a7da2c4deb0928584e`  
		Last Modified: Mon, 16 Mar 2026 23:20:44 GMT  
		Size: 1.0 GB (1024317497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000a63ae2d982deefd847653c6b46392d188d553085fe548adfb7a208d72d377`  
		Last Modified: Mon, 16 Mar 2026 23:20:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:bc51250cd190cc7b639f478867afee1538639529bbf1fe037f585f62960d0d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34519c4e05e768e3746c3fbaa81cae7522cea6aeed7d750e0d5b184be82a255`

```dockerfile
```

-	Layers:
	-	`sha256:e08a0e1390d8c980b08698f430e4a05f84e12754040c0edc1fe77319994d4987`  
		Last Modified: Mon, 16 Mar 2026 23:20:20 GMT  
		Size: 11.3 MB (11343006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1074c09a62e10e7180fb1ad7099902578172f522c0d2b721f8ef46bb8b75d84c`  
		Last Modified: Mon, 16 Mar 2026 23:20:20 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json
