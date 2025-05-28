## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:d0f7500e125a44a9e58d8e750a07e01ea8815415eec4d284c73340de3f806881
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:4baecc024420718d8dcb7ebdbfd3ac728b8485dd1bf8b299fbb83ac6bba48a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094611721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769c900eae57244cddc6e8fd4e250d67db3717b9f091b9782ffe26522b413c23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 10:40:59 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:40:59 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:40:59 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:40:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:40:59 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:40:59 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:40:59 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:40:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 14 May 2025 10:40:59 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:40:59 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 14 May 2025 10:40:59 GMT
ENV container oci
# Wed, 14 May 2025 10:41:01 GMT
COPY dir:d030c7d773f0a9a0288768cf73fd68603fb78790fc50998f9cb91d0c08117212 in / 
# Wed, 14 May 2025 10:41:01 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:41:01 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:41:01 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:41:02 GMT
LABEL "build-date"="2025-05-14T10:40:37" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2f42d95842ada13f4b1358571e36e1ab62406115" "release"="1747219013"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:92efcdccd1058003df257e9cbdf756ff6b10bd276551590536a5a1678e099aaf`  
		Last Modified: Wed, 14 May 2025 14:00:32 GMT  
		Size: 79.6 MB (79592859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3847060e7655a64a89b237ffe2a507f99ab6e20e3b9293ee67bfff503e92838f`  
		Last Modified: Wed, 28 May 2025 18:30:17 GMT  
		Size: 124.4 MB (124408732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcd9042a6b13defe243d1dd84d563f45f7ead75c07d1598785319b0b77ba9a9`  
		Last Modified: Wed, 28 May 2025 18:30:29 GMT  
		Size: 890.6 MB (890609955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2114fd7a899211b468c22b763565b35c3defe676ace6a1b1aec4691807735`  
		Last Modified: Wed, 28 May 2025 18:30:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:e01fd4919af592a93d5e5a6b194698b506ce5a0d9662e16629a080cfdebbc8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12976983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaa957ef391233c6615aa61ea7b1241bc17a9b67dae8e71079ec50486932c65`

```dockerfile
```

-	Layers:
	-	`sha256:2c884ccd4b0068e2ea7fc2c1c7ce4520708c87d73a8323916ff1ab11ea3a973c`  
		Last Modified: Wed, 28 May 2025 18:30:15 GMT  
		Size: 13.0 MB (12962524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e276f4105d738b04dd3d52cbf47a8ced1813778b29e6a7fce4f974d5ffb6f0`  
		Last Modified: Wed, 28 May 2025 18:30:14 GMT  
		Size: 14.5 KB (14459 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ff00ac03bd210cfa593ebcc968de81ab17359cabc1131aefd8717808f4ff8d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082843610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1c57c30a967a1e918551799c3dc01129eef9a43129c20d7b4511e8f666ad26`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 10:43:47 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 14 May 2025 10:43:47 GMT
LABEL url="https://www.redhat.com"
# Wed, 14 May 2025 10:43:47 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
# Wed, 14 May 2025 10:43:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 14 May 2025 10:43:48 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 14 May 2025 10:43:48 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:43:48 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 14 May 2025 10:43:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 14 May 2025 10:43:48 GMT
LABEL io.openshift.expose-services=""
# Wed, 14 May 2025 10:43:48 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 14 May 2025 10:43:48 GMT
ENV container oci
# Wed, 14 May 2025 10:43:51 GMT
COPY dir:c394b2914ae3358d61caf86b7a5bbfd4d11ff5b87984e3a14471c2a88888fa14 in / 
# Wed, 14 May 2025 10:43:51 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 14 May 2025 10:43:51 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 10:43:51 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 14 May 2025 10:43:52 GMT
LABEL "build-date"="2025-05-14T10:43:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2f42d95842ada13f4b1358571e36e1ab62406115" "release"="1747219013"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:391637b3b0856f2a27f616fdf8fe3f1dbd07848a70722ba154c00b969ead8c76`  
		Last Modified: Wed, 14 May 2025 14:25:42 GMT  
		Size: 77.4 MB (77372407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f202315f3a182fe7aeebd6705e0c9e5945fcf41f63ec79b47f007e2943fc362d`  
		Last Modified: Tue, 27 May 2025 21:37:39 GMT  
		Size: 118.1 MB (118111131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c0d074e38755136a9465305aafe08516ebba1fecf7d780eff797053a3359fa`  
		Last Modified: Wed, 28 May 2025 18:53:39 GMT  
		Size: 887.4 MB (887359898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a33e7ab122212f97f3d10570de9def247fc80520806a1c83625f1878f9df0f9`  
		Last Modified: Wed, 28 May 2025 18:53:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:a8b9531e5a4f4b98827bd32c3652e4546bda7a3c5caebac9e15a147216c0cdd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12850346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbffa9751a7d2ba7e33420f605c45a00f013d841e3da32b6d887a72b7d91aa09`

```dockerfile
```

-	Layers:
	-	`sha256:175de17e82a3d51c3d78b258f44967cf0293cc194599a860fc593142e442a00e`  
		Last Modified: Wed, 28 May 2025 18:53:17 GMT  
		Size: 12.8 MB (12835771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39c776a96718587ef4343864ffa4427f97a84dbfa61c8e11d53b3ebbcdd5ab8b`  
		Last Modified: Wed, 28 May 2025 18:53:16 GMT  
		Size: 14.6 KB (14575 bytes)  
		MIME: application/vnd.in-toto+json
