## `swift:noble`

```console
$ docker pull swift@sha256:39b4cc29ce8b012d9b0f09beaf40174151a80e21ee91dfe6296ba7d17dbe349e
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
$ docker pull swift@sha256:72009dbe66d4fa393728b3c9b8db6071bb8f29140dad7868a7ee9590f4f116c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 MB (987861687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cde95d8353b87166f6cf9cc5008a7c2f87b9e27987857ec072c5b147237daa`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be226981a9d34f1b404ba6f1d0a0055a4090cd3ff3bc7587d0ab0de711bdf642`  
		Last Modified: Tue, 03 Dec 2024 11:01:26 GMT  
		Size: 129.2 MB (129153350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f82f614e907d3985c71d4c6a4fe9bf9c2415bc923678cb72ba2dc7c3100ea35`  
		Last Modified: Tue, 03 Dec 2024 11:01:40 GMT  
		Size: 829.8 MB (829815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c483f63d51d4dc162b481b92642d7cf66014d3e1eeae407e1408bfe3ece3d9`  
		Last Modified: Tue, 03 Dec 2024 11:01:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:5903bf2c431b997bdcb7727c3cdcf00dbcea77c240f82d5453ddf436a1cdf7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7713516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a8b054d78490f964a4b14e415c76938d9c9bae3a3ccd0ebcb40a5120f54b4d`

```dockerfile
```

-	Layers:
	-	`sha256:186968efdd7ac0232a3dfb58d56e94a4dd0b5aff03bb809feaaa6514f9e78e38`  
		Last Modified: Tue, 03 Dec 2024 11:01:23 GMT  
		Size: 7.7 MB (7696518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773734305ce9bf8b61f77cbca351f7c3498259ded8d2b073357ce6f2f2f8e3de`  
		Last Modified: Tue, 03 Dec 2024 11:01:23 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json
