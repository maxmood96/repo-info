## `swift:jammy`

```console
$ docker pull swift@sha256:c6743c24d7c3cb1d04f357158fdc90032672860c8ddc728e6bea81fbd48cab0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:6e037e89d7dd5e657ce0714b18b90784caa4c8f531e45105b747f75bc411f188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1102733824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01f068bf1d9f0c34ed3e7a3e98594314350a3a73ce3de3e24401b87ee46a14d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
ARG RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 01 Apr 2025 00:12:10 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1772cf87542116acc6069f9af067c8acd0f7d1ae57ec71f6d6eccbc8359cb5`  
		Last Modified: Wed, 09 Apr 2025 01:24:53 GMT  
		Size: 175.4 MB (175449180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c20b67727f90f4d4abcd7e9049200b1854239fe0c79d5d7cd8ab6709c576bc`  
		Last Modified: Wed, 09 Apr 2025 01:25:08 GMT  
		Size: 897.8 MB (897752105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e30c34933c2298fa092da7adf25e0e2837212ee2472c19a4a903738d684aed`  
		Last Modified: Wed, 09 Apr 2025 01:24:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:90016e7f2cda866d33020cf05cbf37054b166ef6c9c98f7bb913a052687840cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8233815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdd5322658a1dbe241d274f84ac67f4f4aee104778988a67759a0e229f91b73`

```dockerfile
```

-	Layers:
	-	`sha256:1da8cba31f77d7ea2527ef3d4b9633f9d5b323927633a1244484755c7212a711`  
		Last Modified: Wed, 09 Apr 2025 01:24:51 GMT  
		Size: 8.2 MB (8217866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b552d5f81d6c7a032422455fe1402abcb2e9cf198ab37dd013df7f868fc4dfd7`  
		Last Modified: Wed, 09 Apr 2025 01:24:50 GMT  
		Size: 15.9 KB (15949 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3a00757c1db28aafd25faf8d6f44502286bee7c126b80827619b984382ed5487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1095928853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaddf357296192b729f616e178d42ba34d44430f1906aafefef61cd460265f95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e3d9eb6b2904c7479c08c8c6fe4f396dd7cdf0c1869b0bb5f304b8459f4cf1`  
		Last Modified: Tue, 01 Apr 2025 17:27:37 GMT  
		Size: 175.8 MB (175773191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61597c1805c0562756d13453366f189d1621b42e4b6a2b7ee7681391d6aa0c37`  
		Last Modified: Tue, 01 Apr 2025 17:27:57 GMT  
		Size: 892.8 MB (892797306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340c9c50195cd37cbb0f99c7c16a1a031010afa2b4ab250cbd2b777e885a9369`  
		Last Modified: Tue, 01 Apr 2025 17:27:32 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:3707e76b42dad506ef1b5f1fbe8195f1edb838bb9ce2adb7ad7fe2e54680d250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8230873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918c2cc0b3af00809628c2b1c6a945cb21f67b0bb6a5ca6bdfe765dc561f0781`

```dockerfile
```

-	Layers:
	-	`sha256:666765577140da182e5913f0f212fcb55c309bef7e9f03ecd100ff495f714adf`  
		Last Modified: Tue, 01 Apr 2025 17:27:33 GMT  
		Size: 8.2 MB (8214802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e27ab9930e3abbb7a8ce8002e805a0e9a0f8802c3baa6270d68f6d23e3b1d828`  
		Last Modified: Tue, 01 Apr 2025 17:27:32 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json
