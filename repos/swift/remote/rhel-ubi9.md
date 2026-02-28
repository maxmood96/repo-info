## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:452e25a177a24bcc1c1bf0fab1de34cb77acbd014ee40dc8e900fbb3759a5bd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:fd6915d5ac0aba63eef34cb8fb588ae43aabe44c974c7389662a9b5eb69b5727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1227609719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4917ca6a830e59fb37138621c9d6a9091417315004b4cb9b5a1b1ad23da8cd97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:48:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 17 Feb 2026 16:48:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:48:06 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 17 Feb 2026 16:48:06 GMT
ENV container oci
# Tue, 17 Feb 2026 16:48:08 GMT
COPY dir:044009bcad68a63810df7b2a79a5fbd57bbd048f70aed9c80fca25b3757f2cb8 in /      
# Tue, 17 Feb 2026 16:48:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:48:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:48:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:48:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:48:10 GMT
COPY file:ab0176372e5af8a8d1c3b049741d0c5e75d527a597b7c8a836b568335bef6b28 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:48:10 GMT
COPY file:ab0176372e5af8a8d1c3b049741d0c5e75d527a597b7c8a836b568335bef6b28 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:48:11 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8726709260f051bcc33519b9b82af822eb97f840" "org.opencontainers.image.revision"="8726709260f051bcc33519b9b82af822eb97f840" "build-date"="2026-02-17T16:47:43Z" "org.opencontainers.image.created"="2026-02-17T16:47:43Z" "release"="1771346757"org.opencontainers.image.revision=8726709260f051bcc33519b9b82af822eb97f840,org.opencontainers.image.created=2026-02-17T16:47:43Z
# Fri, 27 Feb 2026 22:44:29 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 27 Feb 2026 22:44:29 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 27 Feb 2026 22:44:29 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Fri, 27 Feb 2026 22:44:29 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 27 Feb 2026 22:44:29 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 27 Feb 2026 22:44:29 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Fri, 27 Feb 2026 22:44:29 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Fri, 27 Feb 2026 22:44:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:44:29 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:45:07 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 27 Feb 2026 22:45:07 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:56b2ec53eb90753f4259bc1fd55c9b03d2aeb15f32351977d3513cdfc735b78c`  
		Last Modified: Tue, 17 Feb 2026 18:40:27 GMT  
		Size: 80.0 MB (79983951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6434db7aa953510675f5381f4fbd56cff6424dfc97e7c32437719f3bda65d6dd`  
		Last Modified: Fri, 27 Feb 2026 22:47:25 GMT  
		Size: 124.7 MB (124745573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f7ff0fa3ff82b16b7f6c9677d168169143594a044f306817bf0bbe57a57393`  
		Last Modified: Fri, 27 Feb 2026 22:47:41 GMT  
		Size: 1.0 GB (1022880021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072ed1254738ec5b81a756eda7efb9d11a3fb4409d99d2064e8ed55b9638e0ba`  
		Last Modified: Fri, 27 Feb 2026 22:47:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:c0e93aedb0b54ce2897ddf4d7af5fd3365073dcdd10c60ef0b45cbaf44a9b570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911a749bd6cb5f4f4d15de7ad8bbf03a6add34b7b9b03339285b11c8d5630e8a`

```dockerfile
```

-	Layers:
	-	`sha256:6e599534264958862d1d21eb612f97b9c8ecbc0f300d412ed583d1d57806f322`  
		Last Modified: Fri, 27 Feb 2026 22:47:22 GMT  
		Size: 13.0 MB (12984992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a2ce3f72b9ab81aecf58a80e84d41c75c3b71f929c50e0a4683d71fd339ea2`  
		Last Modified: Fri, 27 Feb 2026 22:47:21 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b253e4ca9f81689021271a4b95c5e5e4bd8a3af525f6c1c224b73a00c447cdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1215083936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ee0b98af40808c5afb000d95e3d1063f57a108ea554ce0176fdf36d0588521`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:49:45 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 17 Feb 2026 16:49:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:49:48 GMT
COPY dir:fe5bb3dc6233e05c0db4d9e9ac24173fdde10a4e3a3f958ab4e4c567c15fe9fb in /      
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:49:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:08d009316d9d419ba8cfeaa9c1c45c2b75422378e0b92b9f0861e4ba6eb7d7f5 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:08d009316d9d419ba8cfeaa9c1c45c2b75422378e0b92b9f0861e4ba6eb7d7f5 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:49:49 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8726709260f051bcc33519b9b82af822eb97f840" "org.opencontainers.image.revision"="8726709260f051bcc33519b9b82af822eb97f840" "build-date"="2026-02-17T16:49:28Z" "org.opencontainers.image.created"="2026-02-17T16:49:28Z" "release"="1771346757"org.opencontainers.image.revision=8726709260f051bcc33519b9b82af822eb97f840,org.opencontainers.image.created=2026-02-17T16:49:28Z
# Fri, 27 Feb 2026 22:43:12 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 27 Feb 2026 22:43:12 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 27 Feb 2026 22:43:12 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Fri, 27 Feb 2026 22:43:12 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 27 Feb 2026 22:43:12 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 27 Feb 2026 22:43:12 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Fri, 27 Feb 2026 22:43:12 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Fri, 27 Feb 2026 22:43:12 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:43:12 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:43:51 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 27 Feb 2026 22:43:51 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b421874d977add29d57baaaa2863eab6b8bab43f7b364a22264ad51b223156a4`  
		Last Modified: Tue, 17 Feb 2026 18:40:36 GMT  
		Size: 77.7 MB (77698505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a98dd5c4c26afa0202756743b3254e1ec8274cb2d33518da2ea36b6af9aa61`  
		Last Modified: Fri, 27 Feb 2026 22:45:57 GMT  
		Size: 118.2 MB (118237290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b55884c84db3855eb68e82bd6bf4569706432c6de459ebdef04be94444dd63`  
		Last Modified: Fri, 27 Feb 2026 22:46:12 GMT  
		Size: 1.0 GB (1019147967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baea6781ba50c302590c3c42c544cf8a06a964befe52640e06a6b3995703d6cf`  
		Last Modified: Fri, 27 Feb 2026 22:45:53 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:65dc5b25a3742095f9040de902bad05493a999ec6e6837ba7063d9267cfadaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f28a3026553f69e1bb16f965e3ec617f11bdf9370f0bf14463fbd33f53f3eb4`

```dockerfile
```

-	Layers:
	-	`sha256:46cf23d21a618743be9374e4ee4ebbca1aa0ccc4b2d7ede96226de83ec822ef9`  
		Last Modified: Fri, 27 Feb 2026 22:45:54 GMT  
		Size: 12.9 MB (12858229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc87d92c89ae6165b040a4877440f10e964d3bffe1d4bb27f338c4c4bdb2dca6`  
		Last Modified: Fri, 27 Feb 2026 22:45:53 GMT  
		Size: 14.6 KB (14557 bytes)  
		MIME: application/vnd.in-toto+json
