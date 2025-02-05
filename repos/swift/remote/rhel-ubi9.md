## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:039ec8f8de735c83d68bc9c6c2774c40ff7c62937b4ab0a0ee4d749a90fe42af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:6a4fba2a4e97293a7af5eb9ca2d93136b7d48aaba43033bc3640beb135c81a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1011875549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea94b43d679472df5e8b6ec8b88676e071a98f5ae5a412ad0d11124d49330fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 12 Dec 2024 07:44:15 GMT
ENV container oci
# Thu, 12 Dec 2024 07:44:15 GMT
COPY dir:5bb879c94b3c2ff1570d6397a19e735efa694941fe59a0d69caa3c2a8d60e461 in / 
# Thu, 12 Dec 2024 07:44:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL "build-date"="2025-02-04T04:39:49" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4371344f505f230dd8b447590dba1946ab022b7" "build-date"="2025-02-04T04:32:30Z" "release"="1738643550"
# Thu, 12 Dec 2024 07:44:15 GMT
RUN /bin/sh
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:d4cb20dd5cad1ea19f0e857b56614f8b02eb977288e4f1a49f5bbbef8ff64b43`  
		Last Modified: Tue, 04 Feb 2025 05:22:17 GMT  
		Size: 88.5 MB (88497912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d117d635acf411b6b4106c39d1cdcadbe7b7b49d48995c3585269733701f6a`  
		Last Modified: Tue, 04 Feb 2025 05:22:06 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1491e180af597c3fba013fb5c9a0759508ed683e39b43692c6405caec238464d`  
		Last Modified: Tue, 04 Feb 2025 20:36:37 GMT  
		Size: 123.1 MB (123099669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becb7870dcf6d647e51c7c441149215366fec01a7644653ad7f9dc8baebabdb5`  
		Last Modified: Thu, 12 Dec 2024 22:37:40 GMT  
		Size: 800.3 MB (800277307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947896c499e61d610f4a05b40da723502cd4d4a2c3e7629cb1bd0fa2b2e56f37`  
		Last Modified: Tue, 04 Feb 2025 20:36:35 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:42d5f5bf618a6958865ed584f521e10e62c0298e94b1353061237310437cb178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13990505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8c5738d3f86be0b98073dda832a3f37b4bc974928974d3e89a59f5cd4e34bc`

```dockerfile
```

-	Layers:
	-	`sha256:a38c0e86320a61b72c6b062e8d7de103a9961dcc4ad78983601c0ce7b902aab0`  
		Last Modified: Tue, 04 Feb 2025 20:36:36 GMT  
		Size: 14.0 MB (13975430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70977e3fe423d6ef79c17dc70293b3d62f528e0f8e95e639cc687d138f9f71e6`  
		Last Modified: Tue, 04 Feb 2025 20:36:35 GMT  
		Size: 15.1 KB (15075 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:71d70d5dba6683ac28ef5e438ea5667820ec4aec5299f25d501375a5abf15e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **999.6 MB (999576488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331df8c1a152a58fbc58e53042bbc6602053a5864c4c031197621ae7f49dcedc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 12 Dec 2024 07:44:15 GMT
ENV container oci
# Thu, 12 Dec 2024 07:44:15 GMT
COPY dir:3ca43e73148a468ad8a46c2eba62ef2a6a5d7be81a9c91017df4efecdbca008f in / 
# Thu, 12 Dec 2024 07:44:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL "build-date"="2025-01-09T06:38:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d029ef1bed7f4b1258ff0991bfd682219c5c5b1a" "build-date"="2025-01-09T06:27:16Z" "release"="1736404036"
# Thu, 12 Dec 2024 07:44:15 GMT
RUN /bin/sh
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:17f7af7a37d4b6da17d2725f33537953d09fe9cf30df676b1d1dd561e35971ab`  
		Last Modified: Thu, 09 Jan 2025 09:08:04 GMT  
		Size: 86.2 MB (86220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999dbdae714d45c5dfdb9663ce8a4dacdeb39839c23fbdee19edd1ce2645e53`  
		Last Modified: Thu, 09 Jan 2025 09:08:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50635eae3d7e7664d11aeaa036d0929629c6d7e2a66cb443acf802e2910019e6`  
		Last Modified: Sat, 11 Jan 2025 01:50:50 GMT  
		Size: 116.9 MB (116881641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f936313db041fe3dee46ad15cc3dda672e3ec8f43c577c59bd936fefae706a1a`  
		Last Modified: Fri, 13 Dec 2024 00:30:33 GMT  
		Size: 796.5 MB (796473513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5df158bd9f86a909080579ba411c73b2c81d13ca1070139533732cf9435974a`  
		Last Modified: Sat, 11 Jan 2025 01:50:47 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:71da96186d61c82abef90d3626482f3a144d6403add2729f140eb92001a687aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13863661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda9a73531fc010fd290528d31d4be9aefb9fbc172f8dd6d0d159b3e6e066ba9`

```dockerfile
```

-	Layers:
	-	`sha256:4cdb13370235614aa562d2a3f7ffa086b0e0dc2ddeef239784a621fac06d31d3`  
		Last Modified: Sat, 11 Jan 2025 01:50:48 GMT  
		Size: 13.8 MB (13848470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972f76971e092616eec4bff7e429928a07c5ea20922744e60f62d034a5167284`  
		Last Modified: Sat, 11 Jan 2025 01:50:47 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json
