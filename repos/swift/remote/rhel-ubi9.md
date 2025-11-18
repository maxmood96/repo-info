## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:b7a957c7f6b83082cf48d2001bcad306a4128ef9eea465e85246d313e0620e90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:8b4f91572858341b67ed37e1578ddeb2592e10fad30920262d5a8d3ee217bc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1227082079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf588f6c2c7af698b2ed92b214253afeb0d75fec27929f88e5151994a8c59b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 12 Nov 2025 12:01:21 GMT
ENV container oci
# Wed, 12 Nov 2025 12:01:22 GMT
COPY dir:c4af8cfc19e3b7fef88c17e44e81034a660e9f4c6801670d3e7b7b41cda389f5 in /      
# Wed, 12 Nov 2025 12:01:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 12:01:22 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 12:01:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 12:01:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 12:01:22 GMT
COPY file:8da21356049927cca36ebed49e3acc1a0bb13226da7434cd96c01e82384e79b8 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 12:01:23 GMT
COPY file:8da21356049927cca36ebed49e3acc1a0bb13226da7434cd96c01e82384e79b8 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 12:01:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a195462c6565447d74f1338d8bdae5fccb5a4f36" "org.opencontainers.image.revision"="a195462c6565447d74f1338d8bdae5fccb5a4f36" "build-date"="2025-11-12T12:01:01Z" "release"="1762948793"org.opencontainers.image.revision=a195462c6565447d74f1338d8bdae5fccb5a4f36
# Fri, 14 Nov 2025 01:21:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 14 Nov 2025 01:21:33 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 14 Nov 2025 01:21:33 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Fri, 14 Nov 2025 01:21:33 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 14 Nov 2025 01:21:33 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 14 Nov 2025 01:21:33 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Fri, 14 Nov 2025 01:21:33 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Fri, 14 Nov 2025 01:21:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 14 Nov 2025 01:21:33 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 14 Nov 2025 01:22:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 14 Nov 2025 01:22:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:3022abd78a961678ba580f66f4abc6871189b6620202a20e5a15ea1adef11a8c`  
		Last Modified: Wed, 12 Nov 2025 14:41:50 GMT  
		Size: 80.0 MB (80041611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851a491dd0cae7b7870f07fb67b30f72db2bad9a643d581a456ed24e14d3416c`  
		Last Modified: Fri, 14 Nov 2025 01:24:40 GMT  
		Size: 124.6 MB (124637647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26680006a5e69f18fea192c7ddb54de3eda701a42806d7537679024eadc73a28`  
		Last Modified: Tue, 04 Nov 2025 23:53:02 GMT  
		Size: 1.0 GB (1022402647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb0a67e0cbbc6da19a1e7c425312984d48adbea24d7e33fc62eabeda18d1fd9`  
		Last Modified: Fri, 14 Nov 2025 01:24:30 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:f6c47599924fee2513dbd3dffe4e3c31e16197ef547eeab7061e153723bd4b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13002596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d021d2f012a043f08de924fa7eb1306db1575fccc92a76444708fe83584c1c4`

```dockerfile
```

-	Layers:
	-	`sha256:1fce726a5bb9634e0aa65dcebf67b8d97db4e8b31baf88b4f1337e0d86102750`  
		Last Modified: Fri, 14 Nov 2025 02:51:48 GMT  
		Size: 13.0 MB (12988154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cdfdaf9bae12fc01598af5be76620ec63568820db4c56c638e2160a56eef2f3`  
		Last Modified: Fri, 14 Nov 2025 02:51:49 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a40faf2251490c26ab316121f0cd5c3ebd0d8049b77cc20ec37fc316d79dfdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1214545769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de401f534118b981f71652829ddcbdb453bf65be7a0d565055ee8298d58b458c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 00:53:04 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 17 Nov 2025 00:53:04 GMT
ENV container oci
# Mon, 17 Nov 2025 00:53:07 GMT
COPY dir:ed3483b671fddac319dde73cd52fc0648bfa84606321e009bbbb409e83827c18 in /      
# Mon, 17 Nov 2025 00:53:07 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 00:53:07 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 00:53:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 00:53:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 00:53:07 GMT
COPY file:df0b4e38e352e0d795a88c61996a2a8ce3e9fa90b02c0f50ccc5bc8c77ed053d in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 00:53:07 GMT
COPY file:df0b4e38e352e0d795a88c61996a2a8ce3e9fa90b02c0f50ccc5bc8c77ed053d in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 00:53:08 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="84ea7c19db44cfaaf0c8ed0d67f74214aeb5ecf4" "org.opencontainers.image.revision"="84ea7c19db44cfaaf0c8ed0d67f74214aeb5ecf4" "build-date"="2025-11-17T00:52:43Z" "release"="1763340522"org.opencontainers.image.revision=84ea7c19db44cfaaf0c8ed0d67f74214aeb5ecf4
# Mon, 17 Nov 2025 23:19:56 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 17 Nov 2025 23:19:56 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 17 Nov 2025 23:19:56 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Mon, 17 Nov 2025 23:19:56 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 17 Nov 2025 23:19:56 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 17 Nov 2025 23:19:56 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Mon, 17 Nov 2025 23:19:56 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Mon, 17 Nov 2025 23:19:56 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 17 Nov 2025 23:19:56 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 17 Nov 2025 23:20:34 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 17 Nov 2025 23:20:35 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:7b9fa4fe5cdca98ea394c6767d2cc6e7ab184f5746ff004063182f41b88e6706`  
		Last Modified: Mon, 17 Nov 2025 03:49:19 GMT  
		Size: 77.7 MB (77723909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c357d20f74062dc29deed68ad6b43e855885e417ef63767257ca14573cd8f7`  
		Last Modified: Mon, 17 Nov 2025 23:23:06 GMT  
		Size: 118.2 MB (118212044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddef3547821a1751f340d01b0a4642a5c7128317d72c4ab95f398bdbdabe7e02`  
		Last Modified: Tue, 04 Nov 2025 22:02:23 GMT  
		Size: 1.0 GB (1018609645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf6e2444e35a7dcd6b2ac991690360e88c9addddc3b854a33f1d822741af351`  
		Last Modified: Mon, 17 Nov 2025 23:22:51 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:0d49702b7f4eb44fe999cbe36062f898c079a5b65ce325d61456d73f2685303e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12875962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59951b165a4befe7ff4676fd92337f3ca9251708e54f6c789b5287fad68fc5a`

```dockerfile
```

-	Layers:
	-	`sha256:c36924777193f2717fe10d4104b92354855ee183cda1704a62597dd2c14e9116`  
		Last Modified: Mon, 17 Nov 2025 23:48:38 GMT  
		Size: 12.9 MB (12861405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:140f5ec82dee84f2b0d4f3872d07bff8d3752b2a6876df69b6073373735ff674`  
		Last Modified: Mon, 17 Nov 2025 23:48:39 GMT  
		Size: 14.6 KB (14557 bytes)  
		MIME: application/vnd.in-toto+json
