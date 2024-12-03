## `swift:bookworm`

```console
$ docker pull swift@sha256:6459f9fdc836252b3a6c53c1c32f5990378ffe3c09fb67c802f024469ca4718d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:e21dde60a31669aa58a2979efba6cc1619d986b0144a6b25ceb9ce79f94821be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1072936955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198676751473abd6be500ba73e545645e5fdd9e2e4bedcd2e9f13115403aa0f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1212991382127db001c7aab5f3e4a69a53749426911b2f3c793118cb0c5ba2b6`  
		Last Modified: Tue, 03 Dec 2024 02:39:39 GMT  
		Size: 194.9 MB (194906479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88c92986e7e3921aa3c8494eec3ceb9655abb828f3e899fbccdf7796e03bf64`  
		Last Modified: Tue, 03 Dec 2024 02:39:50 GMT  
		Size: 829.5 MB (829533092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743f6b0994fb9b2227535942f917f8a7d8e60844518beba933022953390ccb92`  
		Last Modified: Tue, 03 Dec 2024 02:39:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:87f752f713888ab0df38cfa76180ff955eeedc5f9009cb63917d939842959293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10483082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6371f27cb732064f48707b414b12488c3518fc0927798980477067d6f185f616`

```dockerfile
```

-	Layers:
	-	`sha256:c4f0d5482844d6d292cd25b4029fcb252640347c212997e54430a44a3d049ee3`  
		Last Modified: Tue, 03 Dec 2024 02:39:37 GMT  
		Size: 10.5 MB (10467398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c6790ef463e970ffe966e8f6d8a5eae3ac0706a83fde349460805f265d0199`  
		Last Modified: Tue, 03 Dec 2024 02:39:37 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ed0e442e16df543a19756f535a1ca242a46bd094eafb15de3605105e325e0c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1063369282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f590e306e903cfd8a80f643b1b0621472094d767d369097ada1dc87324bd1b0d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54af59ed29fe2473743614e5284176ca92be55244d4084ee5279338156199f52`  
		Last Modified: Wed, 13 Nov 2024 00:40:28 GMT  
		Size: 186.7 MB (186713553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5cb8bf761a7b5c0f612e5f8bb406797cd6d53e0608233acd4f5eacf4e02260`  
		Last Modified: Wed, 13 Nov 2024 00:40:39 GMT  
		Size: 827.1 MB (827068354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a435d261a46d992e9bd27f7abe69ea31bb30a5ec494b61494a59526a493af2a9`  
		Last Modified: Wed, 13 Nov 2024 00:40:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:f682cbe4cba4f5d20557167dd51da6df1899a77bc1ccf53689621b0a6a602269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10512461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2ed4a76bcf878bbf3c0e2447595a1119115359859afaa0909e19a2857045b7`

```dockerfile
```

-	Layers:
	-	`sha256:e51bdd781c3e102b72df4645b83670350e001ade590b9e07854807fded11a65c`  
		Last Modified: Wed, 13 Nov 2024 00:40:24 GMT  
		Size: 10.5 MB (10496655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a330391ae0ac3128796e885adfcee0732e1bafbb433f2593b704cd1b931e8b9`  
		Last Modified: Wed, 13 Nov 2024 00:40:23 GMT  
		Size: 15.8 KB (15806 bytes)  
		MIME: application/vnd.in-toto+json
