## `swift:noble`

```console
$ docker pull swift@sha256:57c8dd2f54f92bea5cc58a6ed3fff4578220aa4240de4ce00ddfda2db23cecc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble` - linux; amd64

```console
$ docker pull swift@sha256:99a58f1acd5d06f93be2731896a811df0547c94c51a9a621fae4a083b2f2d48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1256613032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cc67f5fa8089321ebf2e11bd3031d50cbb3de3208a1a1d9b691ecaaf8938c7`
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
# Tue, 30 Jun 2026 18:54:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:54:55 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:54:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 18:54:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:54:55 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 30 Jun 2026 18:54:55 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:54:55 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:54:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:54:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:55:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 30 Jun 2026 18:55:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d12a285071bb37a4196f1054f1c5396f76b620f9de6ec0b01315127342c4917`  
		Last Modified: Tue, 30 Jun 2026 18:58:01 GMT  
		Size: 134.5 MB (134489140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f5ba92c0b711457d0ab8fe9fe1cc1dbf91f16c41f080b5dbfd42f94f9ae5b7`  
		Last Modified: Tue, 30 Jun 2026 18:58:22 GMT  
		Size: 1.1 GB (1092390914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad7555370ef43585c566a0f203293b479abbbc60af2831579df660805700813`  
		Last Modified: Tue, 30 Jun 2026 18:57:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:ae015c86cb398df7d7949b10c314cc55618d993ca50ff395c0e996c1c638f029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4b84fd611da75ba94f93e5cb1de3d5e18c9c65909680149e5a0aa4ed2d4836`

```dockerfile
```

-	Layers:
	-	`sha256:b8b1425997fc39164c07f8c67da4ca1506b43d0a28702231a683969f5337ef12`  
		Last Modified: Tue, 30 Jun 2026 18:57:56 GMT  
		Size: 7.9 MB (7850197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417bedc9c6bfcd50f00ad42df43e8d386f037f4cbbd9fe1b18102bc1a3b5f391`  
		Last Modified: Tue, 30 Jun 2026 18:57:55 GMT  
		Size: 16.8 KB (16799 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:0f3095c5b3be8d24d17f5e9f9afe23d00546ba76a2b885ed34d8c2315ba5e49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1248678442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fda2e87becb31cdf2dcbcbe1ad6967a819daaf7586c56d8ae6cc9888606e1b0`
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
# Tue, 30 Jun 2026 18:54:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:54:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:54:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 18:54:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:54:42 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 30 Jun 2026 18:54:42 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:54:42 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:54:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:54:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:55:31 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 30 Jun 2026 18:55:31 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e044cca5e8f7662c4c5faf9b457d281c63a2a909c6016ac1bffcb6e346ab77`  
		Last Modified: Tue, 30 Jun 2026 18:57:43 GMT  
		Size: 133.4 MB (133386864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4464aff3dbd517c108a323f987784fa9f6a0922482d28d238d1210b4f9067192`  
		Last Modified: Tue, 30 Jun 2026 18:57:58 GMT  
		Size: 1.1 GB (1086414998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767f54ce3edf762ae7337c7c02b795618becd598c5e79174f71cc1d5e4becf24`  
		Last Modified: Tue, 30 Jun 2026 18:57:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:eaa9aa3044be7d3bce565d4bd39fc091ace5c983643fb16a1c8e4442a4999162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7889635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd28b3df29a03d7fa6dc3a74d271aa8fa7056020a399fbd9fb29df11253adf2`

```dockerfile
```

-	Layers:
	-	`sha256:c0215ce48b0bc555d07571e7361327b849a881e2d0f1752b7772aab2c02d5a94`  
		Last Modified: Tue, 30 Jun 2026 18:57:38 GMT  
		Size: 7.9 MB (7872678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213cf77c535d4a789191f352370368b43ab0edaa655d88da6ba93e80271ccce6`  
		Last Modified: Tue, 30 Jun 2026 18:57:37 GMT  
		Size: 17.0 KB (16957 bytes)  
		MIME: application/vnd.in-toto+json
