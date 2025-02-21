## `swift:latest`

```console
$ docker pull swift@sha256:21ec2ef4572c5989ca7c0113ee9286931715f0a2f8e216df63b8af059c9b25c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:a17b2631beeba788f8febbefe94026bb623e73b93091cce8d556882d503168aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **965.1 MB (965072430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba38592dc0e4bc4a94dbe90b7b84c75698363eed34d272fc60a9ca516008ad21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
ARG RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 12 Dec 2024 07:44:15 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e605d5c6db3139c45994cdf354770415e2bc6588e3d3b738884381cedbfd1bfc`  
		Last Modified: Tue, 04 Feb 2025 04:52:53 GMT  
		Size: 133.7 MB (133671099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0078b636cc22b63fa07f9ca278db7c53a1ac33c236868282ef86d07e8648be`  
		Last Modified: Tue, 04 Feb 2025 04:53:07 GMT  
		Size: 801.6 MB (801646840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ad2fa492d542f625282603e322b101fd7053acef0f498bdb5c26b80220a814`  
		Last Modified: Tue, 04 Feb 2025 04:52:49 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:88f309740887a4febced79a77f7ec6f09f0753174f5ba96a8762162fa99b505b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7684447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67a846a3410031bdc3e80fbdd40c3ed81ba4d3125fe41bb133d3f5871c3460`

```dockerfile
```

-	Layers:
	-	`sha256:c0f085f120b8c7084dd618e2a42c455fe0901c4a358cf714620b3ccbbf3bab41`  
		Last Modified: Tue, 04 Feb 2025 04:52:50 GMT  
		Size: 7.7 MB (7667607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf67ebb7f849490a2be316eea4514d5d9129b173d5e8ed17de40c4414c8364d0`  
		Last Modified: Tue, 04 Feb 2025 04:52:49 GMT  
		Size: 16.8 KB (16840 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f6d27bd6d5cef44b2149a92964ad7d4b7e2157eefe7b50b4e64926ba12338e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.8 MB (959797833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4fc1950473608fe9e0ec798dd4f32ff087cdcb591092a164b13bf544acb4e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
ARG RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 12 Dec 2024 07:44:15 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c86af1439505257ae860fd3fad726768cf57eb619727090b3f6eda1a9858046`  
		Last Modified: Tue, 04 Feb 2025 15:47:53 GMT  
		Size: 131.8 MB (131813055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d71b9490344c7018e54a41c6faee981a60005e4732c1d19cf4eb562f1fd4cd5`  
		Last Modified: Tue, 04 Feb 2025 15:48:05 GMT  
		Size: 799.1 MB (799090979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df45399d30e0c1979b71ba96e337f96fe52cfb5c8d649bb59869b5600acb425`  
		Last Modified: Tue, 04 Feb 2025 15:47:49 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:d9623494f901dbe873c0777d5198534336990297333cdcf81cb26c5df5c833b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7707381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7371d7e028b7cd0aded5a30ee21cafb85e1df88e789ad0e2ca779f9614ee4641`

```dockerfile
```

-	Layers:
	-	`sha256:5865b4023da5f6b86b36a3db4f6ba714fa7ab8e893d8f37769a78f03995a7acb`  
		Last Modified: Tue, 04 Feb 2025 15:47:50 GMT  
		Size: 7.7 MB (7690383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fa5de5c92e23f93bcd83738a8e5b6333b6c4d3ad08878eedbf7a3025f981e0`  
		Last Modified: Tue, 04 Feb 2025 15:47:49 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json
