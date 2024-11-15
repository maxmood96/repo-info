## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:5012919ea1f28adc0aa018f98a12d2df72afc28b96e0d0f27e6ecc19c2dcfa0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:f6cd6a91b4405c1841831f84617847c1b8441031f5d924f5e733ef1435b69fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157961353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d75e653d7499a76c2d76719db35cbf86641c15918db0feaba0849a06578918`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL url="https://www.redhat.com"
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 28 Oct 2024 18:01:55 GMT
ENV container oci
# Mon, 28 Oct 2024 18:01:55 GMT
COPY dir:ba4831586e47630cfc4837a80b3c2dcae6159429dfc338826e2ce717f0c470ab in / 
# Mon, 28 Oct 2024 18:01:55 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 28 Oct 2024 18:01:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL "build-date"="2024-11-13T17:19:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4791df7b99a7414ef74cb63e54e6405dc4ca3a15" "build-date"="2024-11-13T17:11:29Z" "release"="1731517889"
# Mon, 28 Oct 2024 18:01:55 GMT
RUN /bin/sh
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:e70dd633c3a82ff3d3a647f7cfc71882040576a13d2648982bb4c3d075c66ed6`  
		Last Modified: Wed, 13 Nov 2024 18:12:44 GMT  
		Size: 88.5 MB (88492170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef27b1eec136c7519f606a0edeefc96920f7e98b757c83922fe83c6ce8f37c8`  
		Last Modified: Wed, 13 Nov 2024 18:12:41 GMT  
		Size: 113.7 KB (113696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daa5f59232dd201f164f7608c9f638c6be75c21fc3f89f2b5c5dab0431fc87a`  
		Last Modified: Thu, 14 Nov 2024 21:14:34 GMT  
		Size: 69.4 MB (69355487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:90078a1cc1c53b3d8e7e79fd61a952dd5f8229361e400b62f5065bb0c4b369b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bb377ba06b3fd4e7997f12cfd74eebc3d7c604b6c25e513dcb0062425e0904`

```dockerfile
```

-	Layers:
	-	`sha256:173997dd704b860256c9a09ae9df61dd155ee1a839d8801601b27f270b80258f`  
		Last Modified: Thu, 14 Nov 2024 21:14:33 GMT  
		Size: 7.5 MB (7487103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef7350ad3147c75ce637fb8d6eac37552192385206711184917e8390f7f4c13`  
		Last Modified: Thu, 14 Nov 2024 21:14:33 GMT  
		Size: 11.8 KB (11813 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:bfb2789f78c9b8f7d0394fb6e809e887444c74153bc2b17881d05d2b91df8af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154535846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571a8a2297675f7d0141e29c9d1bdf7dc359cc310690a58da4622c61a231239d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL url="https://www.redhat.com"
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 28 Oct 2024 18:01:55 GMT
ENV container oci
# Mon, 28 Oct 2024 18:01:55 GMT
COPY dir:6eea6b5715b604139fd0e0c009e6e68aa17fa1ca988a0856bc784e4945d40e4e in / 
# Mon, 28 Oct 2024 18:01:55 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 28 Oct 2024 18:01:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL "build-date"="2024-11-13T17:22:19" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4791df7b99a7414ef74cb63e54e6405dc4ca3a15" "build-date"="2024-11-13T17:11:29Z" "release"="1731517889"
# Mon, 28 Oct 2024 18:01:55 GMT
RUN /bin/sh
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:506ece80033fcdbbeb33349586abadd186fb79d4520fe3bec3dfdb6a303636f6`  
		Last Modified: Wed, 13 Nov 2024 18:12:52 GMT  
		Size: 86.2 MB (86212534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5211b697630598ef645928cf8cd884ea904e3e9f20ef5058c7d3dc9ed408abfc`  
		Last Modified: Wed, 13 Nov 2024 18:12:56 GMT  
		Size: 113.7 KB (113724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d1f9cc6ed1d68b59b4bc76c8036ba85eebac7210cef021de4e1ca4c403ed92`  
		Last Modified: Thu, 14 Nov 2024 22:21:25 GMT  
		Size: 68.2 MB (68209588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:128e99ecebb6d2e21fe95ebd49b3b174a6ab4cbf9f4f6976b21a8c0d64528613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f61975bf7a8a4b730906819e0d1be26e83bbed08d5cf34437739de221fdbc7f`

```dockerfile
```

-	Layers:
	-	`sha256:9403ee04c98b3341fbb1e5e6fc8c3c240f32fdc66d11bda8cb58debda2a76114`  
		Last Modified: Thu, 14 Nov 2024 22:21:23 GMT  
		Size: 7.5 MB (7482899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56e08a86442f7f9833e2b234810e743a3bdeee85ecbcc4b2dd573e58dbf73eb`  
		Last Modified: Thu, 14 Nov 2024 22:21:22 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.in-toto+json
