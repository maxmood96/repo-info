## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:e73f1d8f195c9e431873b54e2cfcc75c90be8d96e9a6650be92d80ed7683ffc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:6b190ac69a56cfa9b79b1432215630b36339846b81ae01ead35a7eca1e126cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134511472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef90ae209edae44d9e33c74001b85ce9475c1a6753ab22db9e4d2491db25d9a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 28 May 2025 17:53:13 GMT
LABEL url="https://www.redhat.com"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 28 May 2025 17:53:13 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 28 May 2025 17:53:13 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 28 May 2025 17:53:13 GMT
ENV container oci
# Wed, 28 May 2025 17:53:13 GMT
COPY dir:7492816a02b6a9fdb8e1478b30db4fcac269261988d565b14116767fecae0aba in /    
# Wed, 28 May 2025 17:53:13 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Wed, 28 May 2025 17:53:13 GMT
LABEL "build-date"="2025-07-02T08:45:33" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e54274dfd7f5b9d250f44c3cc6fbc4a269fe90d9" "release"="1751445649"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:991b1257896fd60a9811bb63340736f452483a56f8142d025ae07697ecd87e57`  
		Last Modified: Wed, 02 Jul 2025 12:09:14 GMT  
		Size: 79.6 MB (79581151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940a01b7856b7db49bb72e71ca040e1c1e3ae76bc06644bd8091ee25f5064436`  
		Last Modified: Wed, 02 Jul 2025 18:45:22 GMT  
		Size: 54.9 MB (54930321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:929231aaa33351f1e08ecc6670b8b28e25b63c3d8064e9a4d01f6c74f2391f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6412635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44ff9c622af3a987b9b336558c990f816df00d9b1980945726a8cc07280a54c`

```dockerfile
```

-	Layers:
	-	`sha256:50fee12ce60d269d33ee4b01db53ececfae5f935a5e354f556efa8881c43c092`  
		Last Modified: Wed, 02 Jul 2025 19:48:28 GMT  
		Size: 6.4 MB (6401137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96af3fd2e8927edd5a9b44054f87d8e26b3189c9a9ac352854e4cbee0d87c26`  
		Last Modified: Wed, 02 Jul 2025 19:48:29 GMT  
		Size: 11.5 KB (11498 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:1465437742b52bc05197bd346210f03f2a3ad6ce8bc264251d785048a9ee5256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130969560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e4d1535cf3c9334849cf2e1eb679460c3d0baafbcc770c7016b36bba151d00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 28 May 2025 17:53:13 GMT
LABEL url="https://www.redhat.com"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 28 May 2025 17:53:13 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 28 May 2025 17:53:13 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 28 May 2025 17:53:13 GMT
ENV container oci
# Wed, 28 May 2025 17:53:13 GMT
COPY dir:42d787c85c3225f4ba157c2deeba72e69e93f12a80db442d151ec5f4c2c764fc in /    
# Wed, 28 May 2025 17:53:13 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Wed, 28 May 2025 17:53:13 GMT
LABEL "build-date"="2025-07-02T08:45:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e54274dfd7f5b9d250f44c3cc6fbc4a269fe90d9" "release"="1751445649"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:7810b4123c84611d25aab307c7583ee5e99c194789b59694115fdf4fc85f685c`  
		Last Modified: Wed, 02 Jul 2025 12:09:11 GMT  
		Size: 77.3 MB (77316574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080d5d9a35b5e841139792d7ce410f9c97076cc32b01e8c20a48fe9b856f9d0a`  
		Last Modified: Wed, 02 Jul 2025 19:16:15 GMT  
		Size: 53.7 MB (53652986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:7763f4b7126318df625ad0df5613ea72770ee8c609a96a1a324c83336a3f4036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6408524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4323a0a52cdc6a4d828b3b6fcb046ac7ecfb3d57ae891665a9486b4f631de276`

```dockerfile
```

-	Layers:
	-	`sha256:d90d45aa366beb7ac9e455d3c8a09849e7e1987f9866b77b6323995e9071e024`  
		Last Modified: Wed, 02 Jul 2025 22:48:35 GMT  
		Size: 6.4 MB (6396940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7e3b254a4605b21f4a94eb2d2d1a8ad5bb7aec97051e4d921a9991d5c23fca`  
		Last Modified: Wed, 02 Jul 2025 22:48:35 GMT  
		Size: 11.6 KB (11584 bytes)  
		MIME: application/vnd.in-toto+json
