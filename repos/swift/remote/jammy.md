## `swift:jammy`

```console
$ docker pull swift@sha256:5f846f008aa76859377d4e9dafe2826c74dde99421bbc60ae2b98d0f1daf72cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:45cc5c9afd80b30f505c7af9a6eecee22ed5e8d753e4f52d58ed5880b2fef3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1296331020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9788eb6d17c537118364d288dc3bc59dd4672a978e0ee2d02ca3575ee662ca46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:22:35 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 15 May 2026 21:22:35 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 15 May 2026 21:22:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:22:35 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 15 May 2026 21:22:35 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 15 May 2026 21:22:35 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Fri, 15 May 2026 21:22:35 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Fri, 15 May 2026 21:22:35 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 15 May 2026 21:22:35 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 15 May 2026 21:23:19 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Fri, 15 May 2026 21:23:20 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dbfb16583c5a0e7587822e185417142f90939b35f87888632606b33d8c25fe`  
		Last Modified: Fri, 15 May 2026 21:25:47 GMT  
		Size: 175.6 MB (175645632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f493432139efbb70a63b3e0da4d6b95120597094a22ade305028941c3e6824a`  
		Last Modified: Fri, 15 May 2026 21:26:04 GMT  
		Size: 1.1 GB (1090948530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ab673dbfe475eebf4a4a3709b8b54a0962237553b40a5ac568e56ce8c68aa7`  
		Last Modified: Fri, 15 May 2026 21:25:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:57917e8f3cc58aaf00e3fad8b989af6d728817c5f8662f4b8c93e9613da9ab5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f0d6e5306cb9d86fffc2347925be641f36bd2e540f075031903cf615cc3ae4`

```dockerfile
```

-	Layers:
	-	`sha256:49a44a6c6caf7ef462cbbcfc38d93aef3d259cc33428d671850a007caf88f330`  
		Last Modified: Fri, 15 May 2026 21:25:41 GMT  
		Size: 8.5 MB (8477487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffddbe5f2ed111b2b8e57159298c455f62032c38a3cee5044df1068ef61ccb0`  
		Last Modified: Fri, 15 May 2026 21:25:41 GMT  
		Size: 15.9 KB (15919 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:24e400e6f546fe88875773bbd93fcf3079ffa6c6eebe5c974d3d2654e4d898ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1285008326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07967b602ec21156a4c9c1bd968675fe5cc7a38c41ebaf50e80cb398f04d963d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:22:50 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 15 May 2026 21:22:50 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 15 May 2026 21:22:50 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:22:50 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 15 May 2026 21:22:50 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 15 May 2026 21:22:50 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Fri, 15 May 2026 21:22:50 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Fri, 15 May 2026 21:22:50 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 15 May 2026 21:22:50 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 15 May 2026 21:23:39 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Fri, 15 May 2026 21:23:39 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8964a2b230e7f6e46b1e25977eaa92b30cc22380f6c94404eb6e6a2f303bce`  
		Last Modified: Fri, 15 May 2026 21:25:53 GMT  
		Size: 172.0 MB (172008754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee69949e662507473111e6402bd96be1c9d3fa25aba0c9f8028194fb740f9d82`  
		Last Modified: Fri, 15 May 2026 21:26:14 GMT  
		Size: 1.1 GB (1085392776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996769534d13448f9f027f110e3536983519fead743d3789d3aa2dd42e380136`  
		Last Modified: Fri, 15 May 2026 21:25:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:f40da4accd2e733cff5f058717f4e8d44cdcdcbf29f7795b46acf3c144cf26c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ddde680267105af4f2fceaa0901405036715ea1cca0abb07d34c601cd6ad05`

```dockerfile
```

-	Layers:
	-	`sha256:78343504e778d39fc59392aecbaefe01f51013cec5bb38efa615a42f1928f9f8`  
		Last Modified: Fri, 15 May 2026 21:25:47 GMT  
		Size: 8.5 MB (8473173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3eef88df72830615991b318948d02620efce5aff631aebb609531952ffaec02`  
		Last Modified: Fri, 15 May 2026 21:25:47 GMT  
		Size: 16.0 KB (16042 bytes)  
		MIME: application/vnd.in-toto+json
