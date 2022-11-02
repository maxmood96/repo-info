## `swift:slim`

```console
$ docker pull swift@sha256:56e2d2335ea349f4893d29657be0c883fc7d88430620e2d03d3487537c5a950d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:86185b0ef965d02b252e636872854612e1655b8211bc58a19bc776ea81a70e21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139011571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b7dddc219dbcec5fcc764cf7cf74ef070fe5601470db142862f194d3217f10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:31:01 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 02 Nov 2022 19:31:01 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 02 Nov 2022 19:33:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:33:02 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 02 Nov 2022 19:33:02 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 02 Nov 2022 22:50:16 GMT
ARG SWIFT_BRANCH=swift-5.7.1-release
# Wed, 02 Nov 2022 22:50:16 GMT
ARG SWIFT_VERSION=swift-5.7.1-RELEASE
# Wed, 02 Nov 2022 22:50:17 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Nov 2022 22:50:17 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.1-release SWIFT_VERSION=swift-5.7.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Nov 2022 22:50:53 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3bc50ca2338ed4cd6bd5ab685e84d8bd833a6bc4263ea1407aa0cf3d35e680`  
		Last Modified: Wed, 02 Nov 2022 19:43:01 GMT  
		Size: 19.1 MB (19139236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2564df091d9ae2426415b768ea60213789d6855b3646c87fa6758c8cf39cf114`  
		Last Modified: Wed, 02 Nov 2022 23:06:51 GMT  
		Size: 89.4 MB (89446728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:4a1e7d1ff69e18b631b4eb01ac0aabfc074077403ec2c8f4c9e895b696acf0ac
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2950110c42940ccbbe249ee0c598e693d1d109810bcfa89e58a5612e780eaf12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:52:49 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 02 Nov 2022 19:52:49 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 02 Nov 2022 19:55:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:55:02 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 02 Nov 2022 19:55:02 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 02 Nov 2022 19:55:02 GMT
ARG SWIFT_BRANCH=swift-5.7.1-release
# Wed, 02 Nov 2022 19:55:03 GMT
ARG SWIFT_VERSION=swift-5.7.1-RELEASE
# Wed, 02 Nov 2022 19:55:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Nov 2022 19:55:03 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.7.1-release SWIFT_VERSION=swift-5.7.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Nov 2022 19:55:50 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b1a0fbad0b22a881b87c63d63112a8f9160ebce84d729613779c614a7a2f40`  
		Last Modified: Wed, 02 Nov 2022 20:01:43 GMT  
		Size: 19.0 MB (19005694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe36fa44543ac7731b2a05786ae3f3d476fb98c65684fdc8374f1ea274fb44f3`  
		Last Modified: Wed, 02 Nov 2022 20:01:50 GMT  
		Size: 88.3 MB (88275465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
