## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:0940f756ceda1a56be06f00aaf1b837f6f048658b57f661677cc8468c1f7fb27
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
$ docker pull swift@sha256:8255ff213ce779a322d058057586186546221b1960897a58427f4bde6f9c1af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1214469280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5786de28945b26745a0135ddb62ac3db8ae169d37ecdc153867d6258a196b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 12 Nov 2025 12:11:26 GMT
ENV container oci
# Wed, 12 Nov 2025 12:11:29 GMT
COPY dir:99aa92d5e798a2ae59a1f88d8eb6d7d3092b2a77aafd72504d5e5bb659ae6464 in /      
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 12:11:29 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:dcdaded54259c0f330e3f96e5d91fac95a48ff9151e9495c79f0fc6924c1d6df in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:dcdaded54259c0f330e3f96e5d91fac95a48ff9151e9495c79f0fc6924c1d6df in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 12:11:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a195462c6565447d74f1338d8bdae5fccb5a4f36" "org.opencontainers.image.revision"="a195462c6565447d74f1338d8bdae5fccb5a4f36" "build-date"="2025-11-12T12:11:01Z" "release"="1762948793"org.opencontainers.image.revision=a195462c6565447d74f1338d8bdae5fccb5a4f36
# Fri, 14 Nov 2025 01:37:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 14 Nov 2025 01:37:43 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 14 Nov 2025 01:37:43 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Fri, 14 Nov 2025 01:37:43 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 14 Nov 2025 01:37:43 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 14 Nov 2025 01:37:43 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Fri, 14 Nov 2025 01:37:43 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Fri, 14 Nov 2025 01:37:43 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 14 Nov 2025 01:37:43 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 14 Nov 2025 01:38:21 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 14 Nov 2025 01:38:22 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2ea79eba6aac7ec77ffba3f470f3e821fac31f6f0eb75d6017ecf29c44bc7d9b`  
		Last Modified: Wed, 12 Nov 2025 14:41:51 GMT  
		Size: 77.7 MB (77708170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71df7ca9d77b0ede6db9ce51ce706ffd56bc20c90aa81f4ab1ff0cb1b8753f3`  
		Last Modified: Fri, 14 Nov 2025 01:40:42 GMT  
		Size: 118.2 MB (118151292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddef3547821a1751f340d01b0a4642a5c7128317d72c4ab95f398bdbdabe7e02`  
		Last Modified: Tue, 04 Nov 2025 22:02:23 GMT  
		Size: 1.0 GB (1018609645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db511eaf62b4673d62d8eb1e582ce90e9aacba91122ee35f33f422babf3afeb`  
		Last Modified: Fri, 14 Nov 2025 01:40:33 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:1439c1b8cb075e03408777bc9d877c8215244b8f5113c5b1b46d398d3debdc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12875955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a88cbd39ef4734d15dbe6a35c94321da4100530cc48d0a80f58e9e2d3c7727`

```dockerfile
```

-	Layers:
	-	`sha256:21f0bb8817cf1f7675d8680edf79982405a41151c62e05a40f1b947c59261535`  
		Last Modified: Fri, 14 Nov 2025 02:51:59 GMT  
		Size: 12.9 MB (12861397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dabea705981ab8111eecf20c9f85e271376cf174f4df75f03861203aababf4`  
		Last Modified: Fri, 14 Nov 2025 02:52:00 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
