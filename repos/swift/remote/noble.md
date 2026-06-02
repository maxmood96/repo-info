## `swift:noble`

```console
$ docker pull swift@sha256:c4336909a71b2e69b884f4078cdf98c0cd081911632cb349ef72abc4cbed69fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble` - linux; amd64

```console
$ docker pull swift@sha256:d02671b53bebdf3be9dd82f51d2912d462fc9a017535272a266480c016e27f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1251844044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e1671882b89f0690ca4c69cd2982cd868b6f3ce4b34301fe8434eba997add9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:25:12 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 02 Jun 2026 08:25:12 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 02 Jun 2026 08:25:12 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:25:12 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 02 Jun 2026 08:25:12 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 02 Jun 2026 08:25:12 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 02 Jun 2026 08:25:12 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 02 Jun 2026 08:25:12 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jun 2026 08:25:12 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jun 2026 08:25:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 02 Jun 2026 08:25:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ad342fd9c7d4ad500b7abb8d343f058d137dcb549f34633c9201b6249ef898`  
		Last Modified: Tue, 02 Jun 2026 08:28:21 GMT  
		Size: 129.7 MB (129725745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d599776af84e68a741f2e36b67fbf9a6723483a531d0a6bfa9ce29564bf9df`  
		Last Modified: Tue, 02 Jun 2026 08:28:44 GMT  
		Size: 1.1 GB (1092385320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67058f643eddc1b0bd93603991a4a51e87cd51f561d8848020a5d764a602b70f`  
		Last Modified: Tue, 02 Jun 2026 08:28:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:2315ed077472542db6645d4310d870981830c94f9447cfdb6721e7d11bea17dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7883252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007ae868c19df30a78e2eae0dfda8e4ca0b3c531a947423bb4fbac4bfa38fb23`

```dockerfile
```

-	Layers:
	-	`sha256:af9eeb248c04f23b4e8f9e1e82156576156697eedc64306d5bf1668958fd24b1`  
		Last Modified: Tue, 02 Jun 2026 08:28:12 GMT  
		Size: 7.9 MB (7866453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a83b03cf14747ebba504085056eaee7b075bb4ba54f494c28f60d978a1c3f1`  
		Last Modified: Tue, 02 Jun 2026 08:28:11 GMT  
		Size: 16.8 KB (16799 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b39f89a4f14b7bbb135dfb54df95b88c027e1190d366ed437d46d9560dcde3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1244125296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba67eccb41e43c848b5bea33615f72828c7977ae08785d85599c995bf97155`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:25:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 02 Jun 2026 08:25:44 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 02 Jun 2026 08:25:44 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:25:44 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 02 Jun 2026 08:25:44 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 02 Jun 2026 08:25:44 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 02 Jun 2026 08:25:44 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 02 Jun 2026 08:25:44 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jun 2026 08:25:44 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jun 2026 08:26:25 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 02 Jun 2026 08:26:25 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e8159c69fef4db88eaa354e61463d078189e1dea08f9343086aee715e985a9`  
		Last Modified: Tue, 02 Jun 2026 08:28:36 GMT  
		Size: 128.8 MB (128830883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdab1e96d6591e5de0ea8bb1d8bdeb33e99746f1ec68da1907d277665a57e38c`  
		Last Modified: Tue, 02 Jun 2026 08:29:05 GMT  
		Size: 1.1 GB (1086417834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b190a16a17e47dcf4742837e36c5d40dc10c0d332bdf41cabd07e90dba3dd0e`  
		Last Modified: Tue, 02 Jun 2026 08:28:32 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:3e8f3fce0508a3c337a3c3cc68a9d2b7b54a42d5a307c45c6c9a33fce22a771e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7905891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05aaebddd8ad4aa3bd061b5b5be8cc72703e3093ec4d69510292cb5167d7298d`

```dockerfile
```

-	Layers:
	-	`sha256:d80dca63aed3ca221478fc34cc96b00ab110a25c641955afc279b9ea1fd71f5d`  
		Last Modified: Tue, 02 Jun 2026 08:28:32 GMT  
		Size: 7.9 MB (7888934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f39e55cd07f5c0804069f0856a8bf83b93ad4b659c4f3ca865c7e1c86bbc69`  
		Last Modified: Tue, 02 Jun 2026 08:28:32 GMT  
		Size: 17.0 KB (16957 bytes)  
		MIME: application/vnd.in-toto+json
