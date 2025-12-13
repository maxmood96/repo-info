## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:4d8969a5ebcfc2b5da63dceeb09a6784267506585e389067b0d5559696d48850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:d65548d335d765cc1d84b62c69cdbf14b2ffcea0ae5befebb19b510e105a6fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136440191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb24b02a76fe063899b12da528fa9fbaa506442fc452309be6eebda178b3257`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 03 Dec 2025 20:39:51 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:53 GMT
COPY dir:e028f696326f03cd7252c4c349f445b8770570e8560a604b425cd138de4f6500 in /      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:53 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:3510fe100acabb01d1f82e20899ef080183d1fa839353ecc75b35a4f9f617700 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:54 GMT
COPY file:3510fe100acabb01d1f82e20899ef080183d1fa839353ecc75b35a4f9f617700 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:54 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "org.opencontainers.image.revision"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "build-date"="2025-12-03T20:39:28Z" "org.opencontainers.image.created"="2025-12-03T20:39:28Z" "release"="1764794285"org.opencontainers.image.revision=6ab6aed6d7cb84504700f3d038e41e8b4b3c3116,org.opencontainers.image.created=2025-12-03T20:39:28Z
# Fri, 12 Dec 2025 22:44:11 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Dec 2025 22:44:11 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Dec 2025 22:44:11 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 12 Dec 2025 22:44:11 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 12 Dec 2025 22:44:11 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Fri, 12 Dec 2025 22:44:11 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Fri, 12 Dec 2025 22:44:11 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:44:11 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:44:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:d9ce76bfbf66102c69a90574796db9749bc7ac51bea111e75112291f6c0326c5`  
		Last Modified: Wed, 03 Dec 2025 21:13:53 GMT  
		Size: 80.0 MB (80040124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2246fda6da48c3ab00728138429dd36dd9d74aa045a11bc341005af913dabaf3`  
		Last Modified: Fri, 12 Dec 2025 22:44:40 GMT  
		Size: 56.4 MB (56400067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:9c55e6e49329eadfaf189d99f21052b72d81f162b0a7ccf8abfd3aba00700cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2770030f24e11f1b3b7d354f4be4e2e5fb02854ecda8563425d72017c7a5b475`

```dockerfile
```

-	Layers:
	-	`sha256:2def13683d643038544532525bcbf9b0c9ce8103ad1803c10eef738e6e986413`  
		Last Modified: Fri, 12 Dec 2025 23:48:52 GMT  
		Size: 6.4 MB (6409564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86270b02342d0007ccfb06924c58a0ba56d16e3793c0ca7d1dfe1a06c7d9d5da`  
		Last Modified: Fri, 12 Dec 2025 23:48:53 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:25ec26132f6fb9144d1d9fabb0069afb85863cdeda69c64b42f1defa22a17635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132647746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797379b99acf20aa6acf8b375a35ce997fa32a92486de23d6d830b05cf9fecf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 03 Dec 2025 20:44:54 GMT
ENV container oci
# Wed, 03 Dec 2025 20:44:57 GMT
COPY dir:eb9bf5494000bc25c9b7b9c079b1fafa2372042b89728acc56982ccb84aecd0f in /      
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:44:57 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:44:58 GMT
COPY file:f4709671a5a80ff0d54c4f0107ef89c6244ef4daa403ef182c946f77eda0aa0f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:44:58 GMT
COPY file:f4709671a5a80ff0d54c4f0107ef89c6244ef4daa403ef182c946f77eda0aa0f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:44:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "org.opencontainers.image.revision"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "build-date"="2025-12-03T20:44:35Z" "org.opencontainers.image.created"="2025-12-03T20:44:35Z" "release"="1764794285"org.opencontainers.image.revision=6ab6aed6d7cb84504700f3d038e41e8b4b3c3116,org.opencontainers.image.created=2025-12-03T20:44:35Z
# Fri, 12 Dec 2025 22:43:49 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Dec 2025 22:43:49 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Dec 2025 22:43:49 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 12 Dec 2025 22:43:49 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 12 Dec 2025 22:43:49 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Fri, 12 Dec 2025 22:43:49 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Fri, 12 Dec 2025 22:43:49 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:43:49 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:43:49 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:04818a5cef267e6e003591a4574d021a2141ec6ef8efc36216cf70aac950e30b`  
		Last Modified: Wed, 03 Dec 2025 21:16:16 GMT  
		Size: 77.7 MB (77711266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1174ff067865d7627423b112e9a83fccef50faaa66553f455306db3c76a07ed9`  
		Last Modified: Fri, 12 Dec 2025 22:44:14 GMT  
		Size: 54.9 MB (54936480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:5b732e924526727849641749e29d510dd8bf53e74c3f6e091352255345287e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfd97c81beff781cf950328fd0f68ff2bba8b44b4021e48bdedf86dfbdd7a13`

```dockerfile
```

-	Layers:
	-	`sha256:23852ed20187143e25f176b482512c19579eec54c8db6015a1e99a23ab70082b`  
		Last Modified: Fri, 12 Dec 2025 23:48:58 GMT  
		Size: 6.4 MB (6405367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d1004800bff9c2ff73799d5d440cf3067f719563296dee91e79a3fcc4eefb1f`  
		Last Modified: Fri, 12 Dec 2025 23:48:59 GMT  
		Size: 11.6 KB (11554 bytes)  
		MIME: application/vnd.in-toto+json
