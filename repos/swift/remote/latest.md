## `swift:latest`

```console
$ docker pull swift@sha256:7f969657c95bd7c2054e3aeda04e0ac97341e129588c952a547fb7009ee2fc44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:28535a3f003e5304557eb5b2b1cdbf2d050bf623b491cb04cceee7c1ef79bc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1252640888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a986e1a591ac08aacf46dc169b7704725a083df3171711919161e8ce784458`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 22:12:57 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Mar 2026 22:12:57 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Mar 2026 22:12:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 22:12:57 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Mar 2026 22:12:57 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 24 Mar 2026 22:12:57 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 24 Mar 2026 22:12:57 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 24 Mar 2026 22:12:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:12:57 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 24 Mar 2026 22:13:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a373a7e952bd99e8f3063c34ecc52bcb4282e0c8ebfe8d5438801ae468750e0`  
		Last Modified: Tue, 24 Mar 2026 22:16:03 GMT  
		Size: 130.6 MB (130580962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25712cfb75e76282e2b563798165947f026aa9670572e2ce370dae7cc50d0aab`  
		Last Modified: Tue, 24 Mar 2026 22:16:21 GMT  
		Size: 1.1 GB (1092327760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a875f2d0a4f688a8898c020a98d7d1447d0ec36e9b0bcd9c53006da985cf57`  
		Last Modified: Tue, 24 Mar 2026 22:15:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:0ca79e9dbb5e688dc2a048c5444ae660721dab354e46de604ae82f8e9df0b84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7894896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18664cf2d988f27ce8f55dce2deb314ebbcfca45b5f691ae83cd7f2374c39be`

```dockerfile
```

-	Layers:
	-	`sha256:3f7027d728d7589a048e0c7e79cface9ea034d534766487887c994d0d55a9de7`  
		Last Modified: Tue, 24 Mar 2026 22:15:59 GMT  
		Size: 7.9 MB (7878109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:312e156fca1b5ec962fe3ba9bf6c23acf923ec7a40ca928d7c56eade55654c48`  
		Last Modified: Tue, 24 Mar 2026 22:15:58 GMT  
		Size: 16.8 KB (16787 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:8f2b8d3e5211c264d5aa9d0d23f735cc4560acac09be5e8ffde02e195dcf883b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1244913108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afec785c8a098e24b2d7f086ff13a39e561c9f51f737b9068a612b82173cb89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 22:13:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Mar 2026 22:13:02 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Mar 2026 22:13:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:45 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 24 Mar 2026 22:13:45 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b54e22908e48b16e0ffa323419425c943a4df08e7a448fbf9234ffb48746e`  
		Last Modified: Tue, 24 Mar 2026 22:15:56 GMT  
		Size: 129.6 MB (129647751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb160b91c13d25072474d2d4661c04a4312f8fe1f1a5ebd90a3cfdb473691a9`  
		Last Modified: Tue, 24 Mar 2026 22:16:15 GMT  
		Size: 1.1 GB (1086395474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e751b4913d1bb7c891a601304d9387455d74d19e36d1a11e96e34d0bd6bc0293`  
		Last Modified: Tue, 24 Mar 2026 22:15:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:79227900e8ce50e0007b2af5a3c96f569c0e0f5466bdff4fab5531fe5b8b2602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec38ad6c7c968f24f286d5d6d723ebf58ab7f474d75c701b0a4841d5f340dd06`

```dockerfile
```

-	Layers:
	-	`sha256:4f2ea46eff08df6fe3f894f7543d08a91ae9f318eeb18139f38bf5ad316ec5a8`  
		Last Modified: Tue, 24 Mar 2026 22:15:52 GMT  
		Size: 7.9 MB (7900592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ec7c5305274d08719a2de7fe48459fce8a2fa95a7420a725c8aa262b742cfd`  
		Last Modified: Tue, 24 Mar 2026 22:15:52 GMT  
		Size: 16.9 KB (16944 bytes)  
		MIME: application/vnd.in-toto+json
