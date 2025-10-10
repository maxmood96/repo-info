## `swift:noble`

```console
$ docker pull swift@sha256:471acf16d3ce9b270d2f15ea177b0e150bdf1595ae2acfcc4932d1a03f43c3fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble` - linux; amd64

```console
$ docker pull swift@sha256:ff6b4a90306fb98099c55f0e89cb913a705924e8f51a322758122f113be02e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1189090345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f32808c594afc0623c221baf40f381dfe30d00000a96f70d63228e0d158ff0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Sep 2025 22:15:37 GMT
ARG RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Sep 2025 22:15:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Mon, 15 Sep 2025 22:15:37 GMT
CMD ["/bin/bash"]
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Sep 2025 22:15:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabaacd4bf0b9f4a46ec1edb35816e955e45710d5d10148ab4a64988940f91ff`  
		Last Modified: Thu, 09 Oct 2025 22:50:43 GMT  
		Size: 130.4 MB (130384990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ee3a3c98c6876bd26c08b739d3a0135ebb7efc786d3ddd3d637ecb997f363a`  
		Last Modified: Thu, 09 Oct 2025 22:51:40 GMT  
		Size: 1.0 GB (1028982035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998b7d86b81182f4334cb9f2d8dd70aad441e94e710ea69468d129fe0988871c`  
		Last Modified: Thu, 09 Oct 2025 21:30:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:3750f72a55ab510d0b2e0a0355b96326b946eed51cbccedcc4efb795ac13b88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7894793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3163e8a3f17c29cd3192523cf12e09a3c170f5faaa47b2b02d42e1728034cc`

```dockerfile
```

-	Layers:
	-	`sha256:f82d93bb7da2cfaf6fb4288abb21839cecd34d1138562356d840110b19d2d831`  
		Last Modified: Thu, 09 Oct 2025 22:49:50 GMT  
		Size: 7.9 MB (7877963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7cca42298dd01dfb378f7735b996ff7c2bf4d4160f44dfb1622a64b5334f069`  
		Last Modified: Thu, 09 Oct 2025 22:49:54 GMT  
		Size: 16.8 KB (16830 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:cac1cfbd2b66bb47aecde197efee5f409c88e53ea2efb8d00d7667b1e74fa524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1181582822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db0c5112c183ac574f5f5269a7c9ed95b391af429f831470c396eb3e48d94d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Sep 2025 22:15:37 GMT
ARG RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Sep 2025 22:15:37 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Mon, 15 Sep 2025 22:15:37 GMT
CMD ["/bin/bash"]
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Sep 2025 22:15:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdcfa73562450457d4c27b390ff88dba247c252cc67a2e3d58c6207f6d479c7`  
		Last Modified: Thu, 09 Oct 2025 22:53:59 GMT  
		Size: 129.5 MB (129468165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa051495599d4b829fbd96c766e281f61fae5a8547bb56439fcef2d5ea03fc0`  
		Last Modified: Thu, 09 Oct 2025 22:54:22 GMT  
		Size: 1.0 GB (1023252771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9200fa4103448ed1a9479645baf895798d6babd6da34a3c793f4aa66b614334c`  
		Last Modified: Thu, 09 Oct 2025 21:31:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:d5adc27a38a41e6fc6aa422160cc0324eb61e83241d4d759db1396936fedb2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d82e03851d2fa5dc799a46c412f52b0b215438d703bdb570d7f486315499d3e`

```dockerfile
```

-	Layers:
	-	`sha256:106887a267c6b0447902475a97c8b8fd69ae134752aac60fc42463ec7a4922d7`  
		Last Modified: Thu, 09 Oct 2025 22:50:19 GMT  
		Size: 7.9 MB (7900450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4f56de58648aefca5f11c08622cf72d1ba1ae496e8e1798efaaac06e87b48c`  
		Last Modified: Thu, 09 Oct 2025 22:50:23 GMT  
		Size: 17.0 KB (16988 bytes)  
		MIME: application/vnd.in-toto+json
