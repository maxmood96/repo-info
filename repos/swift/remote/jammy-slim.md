## `swift:jammy-slim`

```console
$ docker pull swift@sha256:aa6e2ec858ef0d21cd873e306726d4c1521e92abc50ff006634c835ff1bfc26d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:a1c528dae284fe0614f3dab891699825370da433811b3ffdfd689b1f4badf561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100090900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ca5c151c0abeba6fc167d2423c68f56b315ca7b48666a94a35ae92ecb037af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 22:12:36 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Mar 2026 22:12:36 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Mar 2026 22:12:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 22:12:36 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Mar 2026 22:12:36 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 24 Mar 2026 22:12:36 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 24 Mar 2026 22:12:36 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 24 Mar 2026 22:12:36 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:12:36 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:18 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f9080ef5479747a60c7d435116d104c4b6ac7cb34a93cc6fdd8c2e657cfacf`  
		Last Modified: Tue, 24 Mar 2026 22:13:30 GMT  
		Size: 19.2 MB (19225231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fac238cde7a9f894e011adbb675b4e957ccc11182149daf58d36647544979b4`  
		Last Modified: Tue, 24 Mar 2026 22:13:31 GMT  
		Size: 51.3 MB (51327149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:8f991ca9fed9a240c83bd66c0f7c4a56350c7837c92d66139b73bd9268e78e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f934200d525310dc79ab97c6775cbc106a1d0836ff791288894ea62816de55`

```dockerfile
```

-	Layers:
	-	`sha256:648de03f79850f47d9b300f1bcfc0cdaf3f4b9f9ecaf8d0f1dba639612eb6236`  
		Last Modified: Tue, 24 Mar 2026 22:13:30 GMT  
		Size: 3.1 MB (3055481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17ed88edb11c8ab205dfbff527cb959b15cc9362d3fe9e58437b7a8a8f325dc`  
		Last Modified: Tue, 24 Mar 2026 22:13:29 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:50f7b1598adee059850192ca35e09342dcad769613294865c26a2bbbbb918090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97116756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4aab9334b62b917cd0c9b6008fd71634a84de9bc2c85235dd8acf9d280fd9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 22:13:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 24 Mar 2026 22:13:02 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 24 Mar 2026 22:13:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 24 Mar 2026 22:13:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 24 Mar 2026 22:13:43 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412f6095f7595d57aa36fc4dfe6c442662698e62c6120cd84beaefa8d4d030e2`  
		Last Modified: Tue, 24 Mar 2026 22:13:56 GMT  
		Size: 19.1 MB (19104407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135084ab12bde808cb68da766de8d25c5aa33df3bd32a17d232685ac691dc7d6`  
		Last Modified: Tue, 24 Mar 2026 22:13:57 GMT  
		Size: 50.6 MB (50623324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:cb0bf8522336ff7a6c48f4e8d86dd3bf59055cf6b8f4fd8bc39cf2890eb4a63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c14f3f0b328c7034032796658b74597ccdc1e3843180139ef24421fac73cc2`

```dockerfile
```

-	Layers:
	-	`sha256:dd649944ce15bf5c10f4898a0d8dd61fe17d9dd374a2e9e4fee943731cca3130`  
		Last Modified: Tue, 24 Mar 2026 22:13:55 GMT  
		Size: 3.1 MB (3055768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b811a85b9c851bf97566e444c5875f38d028124b2ec642de6294f52c07b7f62a`  
		Last Modified: Tue, 24 Mar 2026 22:13:55 GMT  
		Size: 14.0 KB (14035 bytes)  
		MIME: application/vnd.in-toto+json
