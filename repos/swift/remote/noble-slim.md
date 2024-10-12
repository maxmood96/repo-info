## `swift:noble-slim`

```console
$ docker pull swift@sha256:4713ac605d4a84422dbfb25d5e6a16ab9bebdd74be9a0666e6f793b6ee574919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble-slim` - linux; amd64

```console
$ docker pull swift@sha256:cdb4c59104d1abe57572ec410811584b6fa11e8ce95de6299943a661f48050ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113383304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33b862a90002eaaa8c8c3c076ef1aca76896d1940b270428469f52df2bf24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Sep 2024 05:07:02 GMT
ARG RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Wed, 25 Sep 2024 05:07:02 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a73c316db7eb8b94984a24d918b2bcb407945c5eaff22df041ab101b769ae`  
		Last Modified: Sat, 12 Oct 2024 00:01:44 GMT  
		Size: 20.0 MB (20013813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd3d298dba517ca1e693cdc1626e7d50c752bd196cdbc4e180de98a5a857448`  
		Last Modified: Sat, 12 Oct 2024 00:01:45 GMT  
		Size: 63.6 MB (63619034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:23e4f6a911c7f89b2f1a40726a0133d7d6da3ffd98ca4bef29ea2c80c40c8ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efec79dcbd41a406ce54c465895f1e5c6caf00c9a285f5456d994e9d51b1eb0f`

```dockerfile
```

-	Layers:
	-	`sha256:a4851691416e4106f364ff6393e55256ad2e7229ef8ed98da1b22bbda420e66d`  
		Last Modified: Sat, 12 Oct 2024 00:01:44 GMT  
		Size: 2.4 MB (2360067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58e19fdd25f712364be8685d5073dc2941883e554766b75d1883a72ca74af3eb`  
		Last Modified: Sat, 12 Oct 2024 00:01:44 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:95583d03c0d028a916935bf6e23e6c7d1799eb9c411f0272060601e2f5398cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112192325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea7c5442bf0664a512a54fd70b33ea383e083e212d0eb013e2a2c2a633c743a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Sep 2024 05:07:02 GMT
ARG RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Wed, 25 Sep 2024 05:07:02 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f03ebac938c57dcd44e83214bcae466cff2eea64736556d122187ecae52e8a`  
		Last Modified: Sat, 12 Oct 2024 05:44:30 GMT  
		Size: 20.0 MB (20028343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae9114a25398bd25fa9631a8e2b25d3a32465bc2933a1f3cb5e514a0bf081e5`  
		Last Modified: Sat, 12 Oct 2024 05:44:31 GMT  
		Size: 63.3 MB (63278366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:fc1f1d1cf1db91dd141303f47cc19fd675ac5dfc86f2ed9fe6b9ba7d44c3c063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808c036bdd6192b865e47a738f533d8b608b5e6988ff26c8e41948a5ade98082`

```dockerfile
```

-	Layers:
	-	`sha256:4e0ea2de77bd1fdf4e36159b76d3b5ac00761195088411113a7fa1a8f9671d5f`  
		Last Modified: Sat, 12 Oct 2024 05:44:29 GMT  
		Size: 2.4 MB (2361183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08fd740ccbe47cb469639644dd4e61c6cc0d59a99f014d1c3f57a79279b072ee`  
		Last Modified: Sat, 12 Oct 2024 05:44:29 GMT  
		Size: 14.8 KB (14802 bytes)  
		MIME: application/vnd.in-toto+json
