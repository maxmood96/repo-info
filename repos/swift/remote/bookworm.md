## `swift:bookworm`

```console
$ docker pull swift@sha256:943bb41624442cef8ccca256f1ff7830ce25209cbad88ebfede0aaef268a8a80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:d8f2b2fc2333c715e17f1ae4de55401a10d32da9209325713d275a4e3221b9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1338651574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394a0617a9cce93582ce51c3a06956e0055145c377abb5c096929fe0cd8b90d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 24 Mar 2026 22:12:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Mar 2026 22:12:59 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Mar 2026 22:12:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 22:12:59 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Mar 2026 22:12:59 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 24 Mar 2026 22:12:59 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 24 Mar 2026 22:12:59 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 24 Mar 2026 22:12:59 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:12:59 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:49 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 24 Mar 2026 22:13:49 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59453cb17662f227aac3f95dac52d3faa44d0c60265a3b91a4058349677060fd`  
		Last Modified: Tue, 24 Mar 2026 22:16:11 GMT  
		Size: 198.5 MB (198451333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7b27ab8928e971f8f73d12ad78478bec1ad36a1c4603b9e60ad44cfcb3bcd2`  
		Last Modified: Tue, 24 Mar 2026 22:16:38 GMT  
		Size: 1.1 GB (1091711483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1375243670288b6cb68f0f02ee88718c7df802d5dfac35876292653a71e736d9`  
		Last Modified: Tue, 24 Mar 2026 22:16:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:ca6be42018808bbe642888e212eb0b84d2c61b8e40ae92cd173db6e56732c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11330707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc63f8aa1fe0aa3b3ea26bd9112c49d2f1672b919026cb903633f16f3b0bfbe`

```dockerfile
```

-	Layers:
	-	`sha256:4624e1c6f6258188944f49d18654eec1bf129e6727b44b97ac4df189f85387db`  
		Last Modified: Tue, 24 Mar 2026 22:16:06 GMT  
		Size: 11.3 MB (11314997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab619b47131e84001cfd0cc75507df8b102c21f76f53a56288da2b93b2e1432e`  
		Last Modified: Tue, 24 Mar 2026 22:16:05 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:54a6a871690a1ec77517980cb6c999c0155c4056a74b901fe308b863ee447078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1324812639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1530919061f0593470ccb7ea00b308936bb0255b9b778a6798581d243d4389e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 24 Mar 2026 22:13:20 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Mar 2026 22:13:20 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Mar 2026 22:13:20 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 22:13:20 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Mar 2026 22:13:20 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 24 Mar 2026 22:13:20 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 24 Mar 2026 22:13:20 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 24 Mar 2026 22:13:20 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:20 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:14:05 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 24 Mar 2026 22:14:05 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee72bbfe45fc8a84f849748398b76afe5a95877399129678489517a4cfb0b223`  
		Last Modified: Tue, 24 Mar 2026 22:16:21 GMT  
		Size: 190.5 MB (190473048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c1c28a390a8b28ec090d91d79cfcf8efe4eae395f85e4a479159e4453be2ab`  
		Last Modified: Tue, 24 Mar 2026 22:16:39 GMT  
		Size: 1.1 GB (1085966385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a92e2d134cc03c546c053287be1e0dc83340622130b179c78dbe0ad3f521c9`  
		Last Modified: Tue, 24 Mar 2026 22:16:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:f0666ddd3777b37d579f055a375240dd34d9f0e051a99b97c2494e3efe3cfbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e329853aba4ef4fa76fe4a698b4226630f1eead64b28bd1baffb7aba2c588f2c`

```dockerfile
```

-	Layers:
	-	`sha256:c58d2d50523f8c13653af23c0a2e67a06a7c7454f2f43836cff8233f124a9204`  
		Last Modified: Tue, 24 Mar 2026 22:16:16 GMT  
		Size: 11.3 MB (11343002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a965d645d59612671aa8dc6f5ece7f12722a32d6f31cbe6f9fff6f0f5776d4e1`  
		Last Modified: Tue, 24 Mar 2026 22:16:15 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json
