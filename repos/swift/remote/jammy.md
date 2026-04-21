## `swift:jammy`

```console
$ docker pull swift@sha256:98ced124a39751bef755522808683aa931516f39556909efac6c9f3c57be662b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:21c6c833e058b6355480858a91cb1f15990f23768a11cbccd864ca80ecf4f94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1296473690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0888aa8bcd8efad3360e5922e632c64f375d916335910f58cadb5fd1adb90547`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 21:52:57 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 20 Apr 2026 21:52:57 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 20 Apr 2026 21:52:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 21:52:57 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 20 Apr 2026 21:52:57 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Mon, 20 Apr 2026 21:52:57 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 20 Apr 2026 21:52:57 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 20 Apr 2026 21:52:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:52:57 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:53:44 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Mon, 20 Apr 2026 21:53:44 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3015d8cc1b3558ec1c87688f1ef079a6fdf7a79ca1319a5d16d63e20b3d7501e`  
		Last Modified: Mon, 20 Apr 2026 21:56:11 GMT  
		Size: 175.7 MB (175669009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ddff07307d861396ef087c688451fa1f8b74c610fe4beef33655864b2b2e58`  
		Last Modified: Mon, 20 Apr 2026 21:56:33 GMT  
		Size: 1.1 GB (1091068009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc1f776d31b6807fcbb0374aefe18eb6df78b68b658d7a703ddc0992be5eb59`  
		Last Modified: Mon, 20 Apr 2026 21:56:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:ce6d78c5763a22234496c5984b55868980a794d6257d5c08321f4ec9d22e6905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fc3cb45e30b8b4435e2047119b750c684fdd3f27870db9a2f3ab7183a391d5`

```dockerfile
```

-	Layers:
	-	`sha256:c45e8f750ecbba0906b6089660fb5d0e7c24518e7351befa6c535723e3fcdf97`  
		Last Modified: Mon, 20 Apr 2026 21:56:05 GMT  
		Size: 8.5 MB (8477483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6d84d6b6e2f266a08e9b528122f5c50f6651de37a2fc360da4a89f8f055ea5`  
		Last Modified: Mon, 20 Apr 2026 21:56:05 GMT  
		Size: 15.9 KB (15919 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:0b7f76a3c11e814dd6de3d674317408d98c2dab44f3f9952899cc70bba869ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1285177481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6499bfbeddff2fb4720691dffe1750066e2bd778aa0d0f0872920d7c7814a60`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 21:54:29 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 20 Apr 2026 21:54:29 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 20 Apr 2026 21:54:29 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 21:54:29 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 20 Apr 2026 21:54:29 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Mon, 20 Apr 2026 21:54:29 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 20 Apr 2026 21:54:29 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 20 Apr 2026 21:54:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:54:29 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:55:25 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Mon, 20 Apr 2026 21:55:25 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c19b52d460ac52596b3727c03edfc62cf33c1cd211e01963b922ca130ed2c`  
		Last Modified: Mon, 20 Apr 2026 21:57:39 GMT  
		Size: 172.0 MB (172017332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f307451700dbe7d28f1a7726b7ec6dd1372a65733de9fc8f3fb891e45c4666f`  
		Last Modified: Mon, 20 Apr 2026 21:57:59 GMT  
		Size: 1.1 GB (1085553433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ac166f6cce2c4162aadec8789b3cdc48c48ad57b300b92ed7c0345f89ad39`  
		Last Modified: Mon, 20 Apr 2026 21:57:33 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:88f692f251bb46bfce7cc28b60c968d48be092851a70aac2c53c7c5cdbce79c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f714326bbf46c78804130178c48e9fd373eb70111e6db7801ef8113fd2fa4639`

```dockerfile
```

-	Layers:
	-	`sha256:4d3f796a9df42cb1cb445650adf3f374a2fb30e5b2178706d3f6095af83f4c80`  
		Last Modified: Mon, 20 Apr 2026 21:57:34 GMT  
		Size: 8.5 MB (8473169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f452cc8e5389fc50d8f25eda06e3c09aa8102b2d966de6fbdd8e3b8e514b4c44`  
		Last Modified: Mon, 20 Apr 2026 21:57:33 GMT  
		Size: 16.0 KB (16042 bytes)  
		MIME: application/vnd.in-toto+json
