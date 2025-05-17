## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:2af43adee1d3fd8f1c4c9d3c3d0c4293706c3bf2871023fdfb610b2a28ac0552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:30e969c0fbd42eeb1d3f82851b9e79ddc5e37010b8d86fec069427d7c1316c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1096831764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b36e928fdd764c7eaaea9df57e333146df6f196e39f6a9ddaff466db75e56c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL url="https://www.redhat.com"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
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
COPY dir:d030c7d773f0a9a0288768cf73fd68603fb78790fc50998f9cb91d0c08117212 in / 
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL "build-date"="2025-05-14T10:40:37" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2f42d95842ada13f4b1358571e36e1ab62406115" "release"="1747219013"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:92efcdccd1058003df257e9cbdf756ff6b10bd276551590536a5a1678e099aaf`  
		Last Modified: Thu, 15 May 2025 19:25:11 GMT  
		Size: 79.6 MB (79592859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109256f8c1f9d23148400dec331b7433bfdc6eb53036696a13f12a315a91bb23`  
		Last Modified: Sat, 17 May 2025 01:33:06 GMT  
		Size: 124.4 MB (124410320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c7a91a4cd942cf259b9a0a4b340e167411225580f6094cfa5cd8aa79969e2`  
		Last Modified: Thu, 08 May 2025 22:14:33 GMT  
		Size: 892.8 MB (892828412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5738f6cbce85ff91cdc881c09ff9319091cecef6d27fe382e09ce0a9cdfd8bd`  
		Last Modified: Fri, 16 May 2025 19:29:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:752a03d15baab3c26c25734502a0ab3f4b8afc1f8837bff0e98884f274136b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12976967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56e093e617157866847842b8102ddd84beb917cfe8636c154e099d2c05239c6`

```dockerfile
```

-	Layers:
	-	`sha256:fae761cdbad49adcf6f043a65f6a4b3103073b8239cffa7d12f9c12cacef8fa1`  
		Last Modified: Wed, 14 May 2025 23:51:05 GMT  
		Size: 13.0 MB (12962520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11a633fa6a280cb02dfa57a14f21cae9e7d27e4aeaf990fc30791da0d80470e`  
		Last Modified: Wed, 14 May 2025 23:51:04 GMT  
		Size: 14.4 KB (14447 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:12c3f468c9959e9a682f040583eef36154b383ec5b247b13fa46f7ccccb5b033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1084947562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ef43e3904b06324b467c93f64b6144e23928c639ccce67cfcdd1d58bbed957`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL url="https://www.redhat.com"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
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
COPY dir:c394b2914ae3358d61caf86b7a5bbfd4d11ff5b87984e3a14471c2a88888fa14 in / 
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL "build-date"="2025-05-14T10:43:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2f42d95842ada13f4b1358571e36e1ab62406115" "release"="1747219013"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:391637b3b0856f2a27f616fdf8fe3f1dbd07848a70722ba154c00b969ead8c76`  
		Last Modified: Thu, 15 May 2025 20:31:11 GMT  
		Size: 77.4 MB (77372407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac989b9b7a061304a4313f57a5c75166b0ca722d44372939bcf4488b8d2d80`  
		Last Modified: Sat, 17 May 2025 03:01:11 GMT  
		Size: 118.1 MB (118113327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863be352cf308f98508d8edca1c315d6970d6eff40f84c274bc9add322b91f5b`  
		Last Modified: Fri, 09 May 2025 03:00:46 GMT  
		Size: 889.5 MB (889461654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628eba78a075a4ce249b607f45fe4a9b2bcf232aafdd774c281952bd9072e2b3`  
		Last Modified: Fri, 16 May 2025 19:27:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:8f612db0c16389bf1fb79b7942efd58337833a5157b8438d85dbc1ba3d7a1847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12850330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a44af9177045b584a17a5aa8581de1039162e237a028746e50f68bf31d376a`

```dockerfile
```

-	Layers:
	-	`sha256:f5aa520eaf89a124c0773bc4004e4af0935f7ea49d5f715c7bd40606d8ee806f`  
		Last Modified: Thu, 15 May 2025 00:16:01 GMT  
		Size: 12.8 MB (12835767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3acdfc107437bef655ef859508323080db24672cb5444ce46a0e0b5347702ba3`  
		Last Modified: Thu, 15 May 2025 00:15:59 GMT  
		Size: 14.6 KB (14563 bytes)  
		MIME: application/vnd.in-toto+json
