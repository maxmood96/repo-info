## `swift:latest`

```console
$ docker pull swift@sha256:1f323e0a029a401cfd6e4f11dc9b64ecc1ccf198fb8a79cac01cf2ca96b7fd04
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
$ docker pull swift@sha256:f5e223ed75fc01e11b6ec5a2f8c337b51121f9eef06c4a50eace4ea873f9e47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **957.4 MB (957410994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fba260c0ad349a57791f941bf88edee6c75fe0b8501a3de756656dae4e3703`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60989e263316a595f08b5404c7df3a9718a036deda5183cf354c480a9837b68e`  
		Last Modified: Thu, 12 Dec 2024 23:59:22 GMT  
		Size: 129.4 MB (129427718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0a385c983f157c81c09462561c71fa74d0d4b9d193dec53abbced651432179`  
		Last Modified: Thu, 12 Dec 2024 23:59:38 GMT  
		Size: 799.1 MB (799090405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef7323a99545bbf5259b674c43ab55d9fde5912c1b84500bc12db5e91965305`  
		Last Modified: Thu, 12 Dec 2024 23:59:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:c45d415e239775afa296eae9d68e2c133e30ff9fe7c0eaacadcb6475d6520b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7712743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f8a178c0f6f399c89315035700f43d4a044dc18e3a293a2fc62cf645d4a3ce`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9b002863108e85421d20027cbe233d4d670d41115586495163488e7cf64c4`  
		Last Modified: Thu, 12 Dec 2024 23:59:19 GMT  
		Size: 7.7 MB (7695746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f0e267f5468c6d49cbac1c1cd9b89c493a815eeab80803a852c7f6f6708968b`  
		Last Modified: Thu, 12 Dec 2024 23:59:19 GMT  
		Size: 17.0 KB (16997 bytes)  
		MIME: application/vnd.in-toto+json
