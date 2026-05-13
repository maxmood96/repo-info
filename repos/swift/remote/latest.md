## `swift:latest`

```console
$ docker pull swift@sha256:70680d9f3bfca824d7c1242d9fa35152513137531c6c2e98797877139b4bab28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:459f3f0674cf51e7098bdbd72e4c767de6f50d8decca837c9e1d69d0b352c10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1251987281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3ce2d94857acc93fe3864ab4137869a930dc2b6443c349894989a7084aae58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:13:01 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:13:01 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:13:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 18:13:01 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:13:01 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 13 May 2026 18:13:01 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:13:01 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:13:01 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:13:01 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:13:41 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 13 May 2026 18:13:41 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50b35117c63b46068dafbfbf5b258d47138bc9e35b390d1611d8cb621f2bef9`  
		Last Modified: Wed, 13 May 2026 18:16:04 GMT  
		Size: 129.9 MB (129868986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73613c1210eb525fdf0d4ab4e0c8767eccba25eac4dd50ce83f4d0e58be100`  
		Last Modified: Wed, 13 May 2026 18:16:28 GMT  
		Size: 1.1 GB (1092385143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5edb6cf1a2ac2579fba9082a2b0581655e8303189088a229fcfaeadecfd727a`  
		Last Modified: Wed, 13 May 2026 18:15:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:0782cb3a4050b7bebfadcb9e9208ea4ad002418d819ee8127c544f40501da22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7883234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919c7d2172e9c04bf4cecb0d1b19ec53296a30f6298231e1db7b0de10ac6dfb`

```dockerfile
```

-	Layers:
	-	`sha256:ffb4792c25789ae4f2480acbea06c1310fb3e5effc9d94efa22d2f02cd66b695`  
		Last Modified: Wed, 13 May 2026 18:15:59 GMT  
		Size: 7.9 MB (7866435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca22e29deae1073eb420709e9eed80d02ffeef57b4952151b08591fd9d2c3e1d`  
		Last Modified: Wed, 13 May 2026 18:15:59 GMT  
		Size: 16.8 KB (16799 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:8c679f18b755d5a3f87607a6257b0890b120840a28e0afd158efa465aedc55f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1244275767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f8c6e601b8c2d828957041fdc62ea6d8b8e7f88dabd38796f9d5c7118dbc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:03:40 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:03:40 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:03:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 18:03:40 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:03:40 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 13 May 2026 18:03:40 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:03:40 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:03:40 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:03:40 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:04:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 13 May 2026 18:04:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d323cc9019ba7ef4e601a4c242281caf2534fb027e48d1fd712a20bd4c86f6cd`  
		Last Modified: Wed, 13 May 2026 18:06:38 GMT  
		Size: 129.0 MB (128981928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e6442d99d2ad2af4fa1d0f86bd7f602e6cf566d296db779eb61d56c016d086`  
		Last Modified: Wed, 13 May 2026 18:06:59 GMT  
		Size: 1.1 GB (1086417880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f402571e96c02c316f80413a1c10713d4b02e4d6d6264fcc6313deeb8d9c49`  
		Last Modified: Wed, 13 May 2026 18:06:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:7806cd0a964b2d6de6cb8648f9ce41d8ec263a70cb8cc8986d64968ed1b7a589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7905873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e115e371d4946227bd271e15128bbb823176169b1ff319c70d2706efc289637`

```dockerfile
```

-	Layers:
	-	`sha256:37efd486ac08adc2278f731a0ac52301aa0aa68b8b72708527936bc507a13e26`  
		Last Modified: Wed, 13 May 2026 18:06:33 GMT  
		Size: 7.9 MB (7888916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b22c3674e98bec2e7ea3db18336ddb786d237ba506ae500966155fc57a73c30`  
		Last Modified: Wed, 13 May 2026 18:06:33 GMT  
		Size: 17.0 KB (16957 bytes)  
		MIME: application/vnd.in-toto+json
