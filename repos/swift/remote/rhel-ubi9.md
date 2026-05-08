## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:6453dd7eeaf0891d0c898918bd7cd5becfcd1d0c629da18680574c38538ffe6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:6d2bf3d3719b7bc33287d2e4e056cb485441c9658362daf05f8da167f2de7909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1288721202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3003a9f67e949c8169ea896f62efd805f0259ab6e4e31c93b5218bdb8ff5cbdf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2026 05:08:45 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 06 May 2026 05:08:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 05:08:45 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 05:08:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 05:08:45 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 06 May 2026 05:08:45 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 05:08:45 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 05:08:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 06 May 2026 05:08:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 05:08:45 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 06 May 2026 05:08:45 GMT
ENV container oci
# Wed, 06 May 2026 05:08:47 GMT
COPY dir:f0b01036154156a4da023621c7c5ef563524b9c8eb3fedaba574d6edea6266e5 in /      
# Wed, 06 May 2026 05:08:47 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 05:08:47 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 05:08:47 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 05:08:47 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 05:08:47 GMT
COPY file:52a6153dd691ee514c9ab05db0778d567afa136afb7d963d4230cb782ce67e83 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 05:08:47 GMT
COPY file:52a6153dd691ee514c9ab05db0778d567afa136afb7d963d4230cb782ce67e83 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 05:08:48 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="42f90b40710e06a0ad1c492bb8665f3fe3afffc7" "org.opencontainers.image.revision"="42f90b40710e06a0ad1c492bb8665f3fe3afffc7" "build-date"="2026-05-06T05:08:32Z" "org.opencontainers.image.created"="2026-05-06T05:08:32Z" "release"="1778044007"org.opencontainers.image.revision=42f90b40710e06a0ad1c492bb8665f3fe3afffc7,org.opencontainers.image.created=2026-05-06T05:08:32Z
# Fri, 08 May 2026 16:23:58 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 08 May 2026 16:23:58 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 08 May 2026 16:23:58 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 08 May 2026 16:23:58 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 08 May 2026 16:24:35 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 08 May 2026 16:24:35 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:5b6b4a422899b7c3f69297c3a1c12a35910c86075c2b21d4bb6536e9c25e5f82`  
		Last Modified: Wed, 06 May 2026 06:06:36 GMT  
		Size: 80.0 MB (79961611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5207db642c2bcae0e098f5ede1dd21b807219c748f0631abf42e66cc3a7fb6e7`  
		Last Modified: Fri, 08 May 2026 16:26:42 GMT  
		Size: 124.7 MB (124710073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f7355d20d694d145fbf4688c63a728cb08f4edbff524635d4047a4f954daba`  
		Last Modified: Mon, 20 Apr 2026 21:56:34 GMT  
		Size: 1.1 GB (1084049344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e72f610889e6fcf18d1538480e02ab9a0f05dd4ee03afeaec14357684fe2675`  
		Last Modified: Fri, 08 May 2026 16:26:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:ff55974276951d1b0f5fcd71b7e56e2eafc7c145ea67ab72aa92aa955cb13b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f6d3011dc741ff8a21469910ddc3336eb5718597b01d50d73283d9590a03cb`

```dockerfile
```

-	Layers:
	-	`sha256:684702b82d9c0f7f98d6301e1973f5b350353e02bcfc6ad1f0def7f63d4bdac9`  
		Last Modified: Fri, 08 May 2026 16:26:40 GMT  
		Size: 13.0 MB (12985054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb485eb456bc51305fdec58b81596459a257c79cab3568f53cc9270f0c323bbc`  
		Last Modified: Fri, 08 May 2026 16:26:39 GMT  
		Size: 14.4 KB (14441 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d5acf35c46e0c6e9b18f81cbb87d78fbb86f13c11de12dfbce357f7a28e01dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276230860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b184926d23fa199feeb2bdab5798e7b4b918ff43fafeb213c12dc7c9098a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2026 05:11:03 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 06 May 2026 05:11:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 05:11:03 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 05:11:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 05:11:03 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 06 May 2026 05:11:03 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 05:11:03 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 05:11:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 06 May 2026 05:11:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 05:11:03 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 06 May 2026 05:11:03 GMT
ENV container oci
# Wed, 06 May 2026 05:11:06 GMT
COPY dir:4571cd64ebc9ca4c415c774f859d96ef73c2f060db0d48db524b934ad6ad3747 in /      
# Wed, 06 May 2026 05:11:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 05:11:07 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 05:11:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 05:11:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 05:11:07 GMT
COPY file:ec7bfb9945298146fce03f7477d437586c60b9185c84d05da54671f4d9acaa90 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 05:11:07 GMT
COPY file:ec7bfb9945298146fce03f7477d437586c60b9185c84d05da54671f4d9acaa90 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 05:11:08 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="42f90b40710e06a0ad1c492bb8665f3fe3afffc7" "org.opencontainers.image.revision"="42f90b40710e06a0ad1c492bb8665f3fe3afffc7" "build-date"="2026-05-06T05:10:47Z" "org.opencontainers.image.created"="2026-05-06T05:10:47Z" "release"="1778044007"org.opencontainers.image.revision=42f90b40710e06a0ad1c492bb8665f3fe3afffc7,org.opencontainers.image.created=2026-05-06T05:10:47Z
# Fri, 08 May 2026 16:23:58 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 08 May 2026 16:23:58 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 08 May 2026 16:23:58 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Fri, 08 May 2026 16:23:58 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 08 May 2026 16:23:58 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 08 May 2026 16:24:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 08 May 2026 16:24:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:d3fcda722faf8a11853f20478465c0ed63994bad8b7eae297881a7aeed3c4d2e`  
		Last Modified: Wed, 06 May 2026 06:09:24 GMT  
		Size: 77.7 MB (77743799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b38538353e437788199f3ef0b002a93a1ed92f926aa895406aaa4933882a4a`  
		Last Modified: Fri, 08 May 2026 16:26:50 GMT  
		Size: 118.2 MB (118208204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6fdf9a00e14597ecc9dfe9618d4ce7bd4e61ee02520f5014ac6ae58fe238e0`  
		Last Modified: Mon, 20 Apr 2026 22:03:23 GMT  
		Size: 1.1 GB (1080278683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510a1a3a39ed81ed7f6c75f0fc92e27a3a0af02a3065ffef1ca6b76979daa03`  
		Last Modified: Fri, 08 May 2026 16:26:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:74030d7e7344215546064f572bca2625b4f91c8ea19fc79975ecfd045e9287c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f189c3f066538ff305b0f16c292b25e0b09c4f642ca2638908dcd7e3120a5a`

```dockerfile
```

-	Layers:
	-	`sha256:cc5a5b1fd3e7531824ebe48f7057388b6560af93fe1f4ddf76b23c2218db9b5a`  
		Last Modified: Fri, 08 May 2026 16:26:47 GMT  
		Size: 12.9 MB (12858291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6e3fc3f10730e37b5eb2e1a525be1d43d9e609f6cb67d0b386ca9cfa4650ee`  
		Last Modified: Fri, 08 May 2026 16:26:46 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
