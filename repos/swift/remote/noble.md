## `swift:noble`

```console
$ docker pull swift@sha256:4b19809b8da2751b2b9de99f02a20ba8ed68317691739029bccdbab25a75c0a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble` - linux; amd64

```console
$ docker pull swift@sha256:83ee6b5e069499ac31202142c0faccda2c5e37772bcfb602c3d1d3745299156d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.2 MB (992174692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a70766b7e3fff73ce7da10ecb3d2824ea080fef7893ecf9e6fe00519dc3993`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
ARG RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Oct 2024 18:01:55 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Mon, 28 Oct 2024 18:01:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f572705168c49b588c11ad61dc24d99bc200f64158211e08068d6f29618868`  
		Last Modified: Tue, 03 Dec 2024 02:40:06 GMT  
		Size: 130.1 MB (130120694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fc680b0432cdce4baab4665d987db1273bdba1e4f022d6f33387cde5c74db0`  
		Last Modified: Tue, 03 Dec 2024 02:40:19 GMT  
		Size: 832.3 MB (832301858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36d429d23547866b1ce6c2852f776d818f55801a76616738910079cb67795f`  
		Last Modified: Tue, 03 Dec 2024 02:40:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:c608cefd4e0adfa0bbb701ebb2b9d911e76178804b02a23e18eef7165002be84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7690559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1eb17784cb80fbb52e5d7d3f5ffeb64b4b09f0dd2281f85214b25a65bd9487`

```dockerfile
```

-	Layers:
	-	`sha256:1287da4f422e6148cfcc503897e92c51c5d3f6d5e3945e47324cf454e935c37f`  
		Last Modified: Tue, 03 Dec 2024 02:40:03 GMT  
		Size: 7.7 MB (7673719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ed61b9ee2d0caceafba6c51fe1e20691324ba717d5a8ae46a979b2e64304a8`  
		Last Modified: Tue, 03 Dec 2024 02:40:02 GMT  
		Size: 16.8 KB (16840 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:0114f0adc88773d470481bcdba2f7e11251c0742b7c5c80baae3ef0af9b8b5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 MB (987859677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ba5ed86b6addcad2d641ca2e8a707509c26e6dc7c4e27f92f64b0d14e93fac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8232defe3fdb044242b25268bf7cbe3a5a0ce102daa00f0314188334940c9c`  
		Last Modified: Sat, 16 Nov 2024 04:00:52 GMT  
		Size: 129.2 MB (129151782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc22fdb7585d5e5bfef1856e4a9d211a4839903f60ab40a5ef412120cf909a`  
		Last Modified: Sat, 16 Nov 2024 04:01:05 GMT  
		Size: 829.8 MB (829815297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09814480003c931c6762252246d0959e0fb0f0e678b03c9bd719f797bb43aa20`  
		Last Modified: Sat, 16 Nov 2024 04:00:48 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:32cca57513579d00d29b17e8c280deffaa216850796d1288bfbf7bc771f42bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7713496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c160bb9c219241123f3e2fb39590bdd7da14e53eea4052ef50fc1dc44b3d87`

```dockerfile
```

-	Layers:
	-	`sha256:25c8a6bd321b34a21a57175fd42e90ad823e1efbec5459fda524625bf1481e11`  
		Last Modified: Sat, 16 Nov 2024 04:00:49 GMT  
		Size: 7.7 MB (7696498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8eacc939b8c737ebb28df0c4be656f19aa2f99e9161a64d21a948cac89c0ebb`  
		Last Modified: Sat, 16 Nov 2024 04:00:48 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json
