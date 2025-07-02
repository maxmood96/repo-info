## `swift:slim`

```console
$ docker pull swift@sha256:aec3f3f43ff9d0d064a9ecfb936757f8c60b18d342f379a311e1357e565974cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:ae2eddd6a10cb602844eb30ad26f82f8e604f87d3a3335fa0e81005d6a05b608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98755156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9065dd3c0f7554c909be7fecb92a99ab0c045022524760b7c3a8b7e031874d58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
ARG RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 17:53:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 17:53:13 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 17:53:13 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e22eb76b235b38afe6f356d06542e7868408906f7e96bdd32cb187f6715c23b`  
		Last Modified: Wed, 02 Jul 2025 08:05:41 GMT  
		Size: 20.0 MB (20017331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1e7712b9fc9eae73b9cba24c5221cdb006b364898fbf944a315779b356cf5`  
		Last Modified: Wed, 02 Jul 2025 08:05:42 GMT  
		Size: 49.0 MB (49019459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:30145ba2a22ab6d34ce5e2ad801f5c2b458c75c6103d53ce5d9d0a366571ad4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a6009cd2fb3bb781a0b7fd7d7db0c856201dede611ca75a286b0576251c3be`

```dockerfile
```

-	Layers:
	-	`sha256:c87b837fa5ae462713ef320a1fed064133de80c6b3bfec41daa10a6438e8a3bb`  
		Last Modified: Wed, 02 Jul 2025 07:49:02 GMT  
		Size: 2.5 MB (2497192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3c5d91ee90df9e138933938eb5814085ff5d7c36185a50bd5c757f39c7586ab`  
		Last Modified: Wed, 02 Jul 2025 07:49:02 GMT  
		Size: 14.9 KB (14880 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:cab2d581a5ebbe035bafc6ba7682f6a212cb14502e875e95876420dd8cfc16e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97337966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e28d7575213c9a7ca1d7b97e42325e3f4b7b07486371fa4fd85e34ea7baf26`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
ARG RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 17:53:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 17:53:13 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 28 May 2025 17:53:13 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c06b770f93a822e85ceb309c96c11d9e5ab5379ef87011d7d81724d128e5796`  
		Last Modified: Wed, 02 Jul 2025 06:55:23 GMT  
		Size: 20.0 MB (20027515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fdbfc2eddbdefa798e2f40a1ede3c101aa7ec3c459cafffafb1b906c6bf86d`  
		Last Modified: Wed, 02 Jul 2025 06:55:20 GMT  
		Size: 48.5 MB (48454433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:304774d6f9b36afa4bd5e8d48bc85abc2733ee877358be18ae610f33a24e5067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ea331dfe8c579e0d96bf72524022887a4fec1e8af324024debde83c7b20456`

```dockerfile
```

-	Layers:
	-	`sha256:cb74626675dfc18662026a07b1a07559a5ff63e27d8a156058e8e21e599009d6`  
		Last Modified: Wed, 02 Jul 2025 07:49:07 GMT  
		Size: 2.5 MB (2498308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9704ee2eb2d7237ef2a7ed7d1d4cd0208adb46b8cc71252ee1a9cb0b1495044`  
		Last Modified: Wed, 02 Jul 2025 07:49:07 GMT  
		Size: 15.0 KB (15024 bytes)  
		MIME: application/vnd.in-toto+json
