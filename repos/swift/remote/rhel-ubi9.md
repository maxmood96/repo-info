## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:ef3c5af097541a3e442f443918684a9dbd32e2b575623b05787a2ec2fcb86162
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:c2d395bacb6f30ac05d1566f998126244ea79b5a6e387e4fe9f7b20c9efdac1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1096616943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a234394d6668fb3dcce806a0996469b0e22574ebd25e2460f78a53a8dc988b3`
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
# Mon, 26 May 2025 22:39:21 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 26 May 2025 22:39:21 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 26 May 2025 22:39:21 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_BRANCH=swift-6.1.1-release
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_VERSION=swift-6.1.1-RELEASE
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 May 2025 22:39:21 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 May 2025 22:39:21 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 26 May 2025 22:39:21 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:92efcdccd1058003df257e9cbdf756ff6b10bd276551590536a5a1678e099aaf`  
		Last Modified: Wed, 14 May 2025 14:00:32 GMT  
		Size: 79.6 MB (79592859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824fcf78fa4314ad51db022ff3a8b0f63054c9db49efc9bb151e42b2c4f73156`  
		Last Modified: Tue, 27 May 2025 18:58:40 GMT  
		Size: 124.4 MB (124408689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589bb62ab92af65ca55db9589f18de749312aa2d82ed7986d93de8948bb4cf5b`  
		Last Modified: Tue, 27 May 2025 18:58:54 GMT  
		Size: 892.6 MB (892615221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c4d082a69618bf5acf880d1d2e58519deee23ca16f1554339f50bbdbf71dc`  
		Last Modified: Tue, 27 May 2025 18:58:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:f23e1f033ab012042d13536802560bf4d6eaff4a86ac5ea6c7177dcef71c8faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12976982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a9edf2271e2bb30625a606ae37d08cb47cb0fcfe0c7c6e082dd485d46d982c`

```dockerfile
```

-	Layers:
	-	`sha256:0c8db81e8e36645693ba739ed7c821f1fccfdf35fc1c00daf04787c4b6b0d978`  
		Last Modified: Tue, 27 May 2025 18:58:38 GMT  
		Size: 13.0 MB (12962524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67393d9497735a432f1ca638554f7fd453e62ddc7c88717e5bc72502725c33f1`  
		Last Modified: Tue, 27 May 2025 18:58:37 GMT  
		Size: 14.5 KB (14458 bytes)  
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
		Last Modified: Wed, 14 May 2025 14:25:42 GMT  
		Size: 77.4 MB (77372407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac989b9b7a061304a4313f57a5c75166b0ca722d44372939bcf4488b8d2d80`  
		Last Modified: Thu, 15 May 2025 00:16:02 GMT  
		Size: 118.1 MB (118113327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863be352cf308f98508d8edca1c315d6970d6eff40f84c274bc9add322b91f5b`  
		Last Modified: Tue, 01 Apr 2025 18:53:37 GMT  
		Size: 889.5 MB (889461654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628eba78a075a4ce249b607f45fe4a9b2bcf232aafdd774c281952bd9072e2b3`  
		Last Modified: Thu, 15 May 2025 00:15:59 GMT  
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
