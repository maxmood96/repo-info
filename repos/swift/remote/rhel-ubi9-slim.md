## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:9daca453d21c45c0e1d50bfb89e4136eebf475a4e08fd0ecb60a4511728c74f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:a1d2e4bb13a89e7c050a21ae5a4fd0ed020f2d1bb6c3a403fafe37173113d403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133804907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e19f260a8bf0332f86a094071f06a47f68c4c4fb80890293a5302cecbfb80a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL url="https://www.redhat.com"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.openshift.expose-services=""
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 01 Apr 2025 00:12:10 GMT
ENV container oci
# Tue, 01 Apr 2025 00:12:10 GMT
COPY dir:84f5c0847c9695a665a4703c9cc51c3bb1a14f8a0922801e49eb1d541581dd69 in / 
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL "build-date"="2025-04-08T08:45:23" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7c3ec864c7dfbb620cbb0fe45bfc382aedcc452f" "build-date"="2025-04-08T08:37:46Z" "release"="1744101466"
# Tue, 01 Apr 2025 00:12:10 GMT
RUN /bin/sh
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:e98f4315d8c98025e71393880225f972b254436fc5f6f69f1363f3d2fb1de16f`  
		Last Modified: Tue, 08 Apr 2025 11:31:48 GMT  
		Size: 79.1 MB (79119020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b7d555f3bb98897444b1bab43c508e55f8b8f3a00f6ca70affe9084c2c9594`  
		Last Modified: Tue, 08 Apr 2025 11:31:47 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bdd0cc52f19c277ad3ded16721a0fd5e9edb5a071c4f1785440490bd2d2591`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 54.7 MB (54685428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:f1cc621868803555f54052383dea9aec18c650b5b639a61e1f0ee17b8fad000d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6390186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f64594fe3616f1699bfe1eea97779721346712debc600060979e01d51fb1f9`

```dockerfile
```

-	Layers:
	-	`sha256:0cc4cf154264b9229446652f86ac8cdd31c001a1fee8556331c5da304c5f3e0f`  
		Last Modified: Tue, 08 Apr 2025 17:29:38 GMT  
		Size: 6.4 MB (6378387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928bb0e2d6b01773be234c6adad8ce0881434f1bad250cc64eb560223d74ef6b`  
		Last Modified: Tue, 08 Apr 2025 17:29:37 GMT  
		Size: 11.8 KB (11799 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a5e8fa670e6214b23dc6ef7c34465967a12b2993fc3b986e8a102eaaa66a71b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130260196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e998d8c0b76d5f13f58261652912de01639b5e63e57568a2b2ec86090e70b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 25 Mar 2025 16:17:22 GMT
ENV container oci
# Tue, 25 Mar 2025 16:17:25 GMT
COPY dir:790f9791dd310f5c4f341398ef28213daea60b81f9d5ca5d793e3b44f1a87b8a in / 
# Tue, 25 Mar 2025 16:17:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 16:17:26 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 16:17:26 GMT
LABEL "build-date"="2025-03-25T16:16:51" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e98aeded1f394c8879effc230f1b407e9e55e58f" "build-date"="2025-03-25T15:58:30Z" "release"="1742918310"
# Tue, 25 Mar 2025 16:17:55 GMT
RUN /bin/sh
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:b452a63227db6d456465c0555e20993f41c55628f058989c5f14eea506e4d722`  
		Last Modified: Tue, 25 Mar 2025 17:28:31 GMT  
		Size: 76.8 MB (76808094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2a478782fd67aaa55b76530967d570765009de89d1fe3c6e7a5c1f81781b8`  
		Last Modified: Tue, 25 Mar 2025 17:28:30 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9b965b7ce037a3a3c9c66cad1f5bff3046a0a9f9453aa04717784c0cadeb75`  
		Last Modified: Tue, 01 Apr 2025 19:32:23 GMT  
		Size: 53.5 MB (53451645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:cd3082eeb1a75ffc6e82b6ce15196aa3d58dbb6e9fe254a740aac91bf798c06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584454c2a2016478219baefa5aa6f771cf749c5f24bda443761e47a1d374415d`

```dockerfile
```

-	Layers:
	-	`sha256:40a4b8e7a21b332f6ae3ebd5d7daed5ed2f5b24db34efc388acd2ebc0c94c2b3`  
		Last Modified: Tue, 01 Apr 2025 19:32:22 GMT  
		Size: 6.4 MB (6372312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:925608803d28d53af0b855bae786ebcf321b1faf5035436e42e4f25eeed66813`  
		Last Modified: Tue, 01 Apr 2025 19:32:21 GMT  
		Size: 11.9 KB (11885 bytes)  
		MIME: application/vnd.in-toto+json
