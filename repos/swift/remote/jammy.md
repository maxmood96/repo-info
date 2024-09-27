## `swift:jammy`

```console
$ docker pull swift@sha256:d2288ec36876c52ca28fef6852cff4e11b8f40517564536a724a34957561cec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:5bd94e6b4c3e442c6dc4eb732661c359de3e8d678ec3978fa09ad95ec138ffed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1036559835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef74e821976a91f4c2b9c5e01357957731c99e6b9d14ed9398876d74c3b3685`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74ee56bd6cbaf56b94ca33f0f6147e9a1978e52d9452b03dae07b30225e6756`  
		Last Modified: Thu, 26 Sep 2024 22:59:24 GMT  
		Size: 175.4 MB (175439166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04f4bf6fe244657c84a3d1e15755430a5aeeb36260b361d5a5f5025455b8341`  
		Last Modified: Thu, 26 Sep 2024 22:59:37 GMT  
		Size: 831.6 MB (831584807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3377c26664ffff6f3449332f58e06a9810261b1ca5c791b5c96468450c73a4b`  
		Last Modified: Thu, 26 Sep 2024 22:59:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:869c3d761b413ffe43e7a9518eef98cfab93a6615f8a4a3acf94ddbb74a8080b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8214580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7945f4c06bfdcd0249fab6754d3a0c2227f9a3951a99e4f41aa5c9440e2651e`

```dockerfile
```

-	Layers:
	-	`sha256:8f2988f6e3eca4c9a22dcd1d100c5258b7f0f2da87b9c66e985a279fa0179d60`  
		Last Modified: Thu, 26 Sep 2024 22:59:20 GMT  
		Size: 8.2 MB (8198873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3230965ef6cf44afefaabac1ca9b7f855396948b8f497a74e36665e6319c313`  
		Last Modified: Thu, 26 Sep 2024 22:59:20 GMT  
		Size: 15.7 KB (15707 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d2375a1be11594d40d57bc308113af1cb39caca955acd3a9435a0937ab444db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1025463037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6132c3c6c60bcdc5a8a8654a6a4c18f520644071bda0eab4ead41f6947e17ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4cf0ffc78fea97df6b548d2b1104922a293f96c7f5f7d489275ff7c46a8ff9`  
		Last Modified: Tue, 17 Sep 2024 03:45:52 GMT  
		Size: 171.7 MB (171663262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46a155c7309229adbce3b57d57a457ce3972d70accc9e52ff477345577e4fda`  
		Last Modified: Tue, 17 Sep 2024 17:05:34 GMT  
		Size: 826.4 MB (826441271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e63592a2374161547a32ad0fa9520169f8426246744ca6f2ce8014c5aef71c1`  
		Last Modified: Tue, 17 Sep 2024 17:05:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:bbaa2bdbf4c72e1425b6635583961ec07ee2644ceeda9f9aeb95398c24fd96ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8204625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b899b18208b136aff69023c25a3bb42faa47d27e5793a70adc45c88d89a63ba`

```dockerfile
```

-	Layers:
	-	`sha256:abcdadb458ecfc556947d0b2183ce101d04854366632f75525a7438b84f5f563`  
		Last Modified: Tue, 17 Sep 2024 17:05:10 GMT  
		Size: 8.2 MB (8188642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90f771aa7e0c550c9dca2344dc21813be9d458f9f745f9e93af097b86f9190c`  
		Last Modified: Tue, 17 Sep 2024 17:05:09 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json
