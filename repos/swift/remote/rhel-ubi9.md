## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:8b9d3870f4f0dd88430b398fc7d82286c0944b36c6925ae683ad3e24d1d947dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:b594a30f04c999073be2c6ed2ff1ed97087fe10a3ad8e09ffd99cdee5e7e4545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1042875327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5a11ed6a3961b22e6f1973e71a118eda55f5561d91ddb0f1578f8404e5f820`
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
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
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
	-	`sha256:a9ef8e948fb686cebeb282bf36f36d2772033996c94ff0cfc22005d6ddbd9459`  
		Last Modified: Thu, 14 Nov 2024 21:14:56 GMT  
		Size: 123.1 MB (123066378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a600617c8630172f35fb08c8c402eafa9019f718ebae9b539beb1c780e6fa293`  
		Last Modified: Mon, 28 Oct 2024 21:00:38 GMT  
		Size: 831.2 MB (831202908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa24ea9a77b3befc73b2f9eee6a01b80331ab9956161def0159557613174b9a`  
		Last Modified: Thu, 14 Nov 2024 21:14:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:b4151b8c208d7af625834e3df571e2ba370a006dc8bd341fd956fd736f117ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14019466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547820384e64473bed39121795cb242294082ba80c06005cc67201419f3771f3`

```dockerfile
```

-	Layers:
	-	`sha256:5bcdf412ec205cecceddd5e0e6a77c7a643187529b7ac55ff24698e217e85e04`  
		Last Modified: Thu, 14 Nov 2024 21:14:55 GMT  
		Size: 14.0 MB (14004379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e30fd1fe9d29c2f02fc2c2d8f2f0b84f0112fef7d7944b7434b684823a828a68`  
		Last Modified: Thu, 14 Nov 2024 21:14:55 GMT  
		Size: 15.1 KB (15087 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ea8434ab7401089d6aab96fb4b255e6b36ff2ca85c573e6aa07db829928c2a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1030591906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8013be5ef004af845d69cc02bb631fb819bc427a6bb275ea2db9197adaca93d0`
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
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
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
	-	`sha256:44c6debe4d7689eba7d055de93fd67b32163843fd64691b804e1707a5ea1c5c8`  
		Last Modified: Thu, 14 Nov 2024 22:20:03 GMT  
		Size: 116.8 MB (116807730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1accd7a96b5a62a6a22740ccfb38fd3d7f802819b1376d3f51febf07abd9d48d`  
		Last Modified: Mon, 28 Oct 2024 21:35:05 GMT  
		Size: 827.5 MB (827457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37ffdfc56ad0ed20379501a74a9f4673176fd9a63f2ff90e268982e843de63`  
		Last Modified: Thu, 14 Nov 2024 22:20:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:af8f283fe2d3c0b465e7d807a3b25e65588aba95ad73266a24cfc39881c0e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13892566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300a5504342d36bf56c2c50c14d3d558f4b5a66ddc7c5abc22919a3dfdeae91a`

```dockerfile
```

-	Layers:
	-	`sha256:6eb6e13fe9ab0540b39ad8f9a225b90f311109dd9c6a1b6a4ef1fcf4466cde46`  
		Last Modified: Thu, 14 Nov 2024 22:20:03 GMT  
		Size: 13.9 MB (13877363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cb7ab32272ee9f0761bd2db5e91bbad376f4c53734ff85e27f463e6dc47d1a1`  
		Last Modified: Thu, 14 Nov 2024 22:19:59 GMT  
		Size: 15.2 KB (15203 bytes)  
		MIME: application/vnd.in-toto+json
