## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:06ecb36aa3c011758a5b6849436d41bdcf4b390e4ea81e73e1fe62e942d11d2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:bb7e248fb8026a732baf1980869c54d8e638b2f02b2029722eaadcfd2864cbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1227280411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e22a577d15b194447c5541275be129ad5a0c9904c4c7b663ab9bf8c77d23d0`
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
# Wed, 18 Feb 2026 19:23:49 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 18 Feb 2026 19:23:49 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 18 Feb 2026 19:23:49 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 18 Feb 2026 19:23:49 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 18 Feb 2026 19:23:49 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 18 Feb 2026 19:23:49 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Wed, 18 Feb 2026 19:23:49 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Wed, 18 Feb 2026 19:23:49 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 18 Feb 2026 19:23:49 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 18 Feb 2026 19:24:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 18 Feb 2026 19:24:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:56b2ec53eb90753f4259bc1fd55c9b03d2aeb15f32351977d3513cdfc735b78c`  
		Last Modified: Tue, 17 Feb 2026 18:40:27 GMT  
		Size: 80.0 MB (79983951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af91f38c840d7fd5074085d0929809c152a346bd5f14d228e00554e18086056`  
		Last Modified: Wed, 18 Feb 2026 19:26:24 GMT  
		Size: 124.7 MB (124738121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc0e106ef704982969b3e90271f78f768ed1d02b9fc9dcf75437b65cb0a25fc`  
		Last Modified: Fri, 12 Dec 2025 22:46:46 GMT  
		Size: 1.0 GB (1022558165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3280180e29f3d86c703432555084178a6d56a0ffe2428bc3ee0b16787fec1ef0`  
		Last Modified: Wed, 18 Feb 2026 19:26:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:6fb6d3848056680775619e4683f495e910c4c1865d1b0af78e216730c091fdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0e103d6ce73bc97b91c281c192405ecc27520e945e4bba9c2c730c490f0b87`

```dockerfile
```

-	Layers:
	-	`sha256:864d9cfc55e6ae9f4bab33fb0d6f2f841d89f1ac287f5e97df5c80f35cfd3f8b`  
		Last Modified: Wed, 18 Feb 2026 19:26:22 GMT  
		Size: 13.0 MB (12984992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0063c0f1b03de32c89ff66e6a6c17ef8b7c57cfb380309925a41412248bf5f56`  
		Last Modified: Wed, 18 Feb 2026 19:26:21 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:1fe4518d459d5f68ce41910fe339e1e65ad5319c25c0403bdbd54b1f12b5dcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1214758407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91335d2fd599a1d326a7c7dfcb3fdac8f5eb92683b3ae8660d3c218e1c47304`
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
# Wed, 18 Feb 2026 19:22:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 18 Feb 2026 19:22:09 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 18 Feb 2026 19:22:09 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 18 Feb 2026 19:22:09 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 18 Feb 2026 19:22:09 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 18 Feb 2026 19:22:09 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Wed, 18 Feb 2026 19:22:09 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Wed, 18 Feb 2026 19:22:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 18 Feb 2026 19:22:09 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 18 Feb 2026 19:22:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 18 Feb 2026 19:22:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b421874d977add29d57baaaa2863eab6b8bab43f7b364a22264ad51b223156a4`  
		Last Modified: Tue, 17 Feb 2026 18:40:36 GMT  
		Size: 77.7 MB (77698505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8b2f57b2534d811fbb31404e52978e47371f80b69ac32edeceaa4065c12463`  
		Last Modified: Wed, 18 Feb 2026 19:24:59 GMT  
		Size: 118.2 MB (118228223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b167ffd31ed78c1696bf65d2b800745a3fdb21176ef4c8f31317e8023e9c14`  
		Last Modified: Fri, 12 Dec 2025 22:46:35 GMT  
		Size: 1.0 GB (1018831504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf9812e12db1e5bc6475f95afcba0d42f81ecad596a0b00f9b0fd8bb5268b`  
		Last Modified: Wed, 18 Feb 2026 19:24:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:4817f7d8892cd03d9cf0ad37586acfa5804d82c55d07a0e7b864f52358b7bbf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c3f3dbe479c2300cc1dcf78a2e60b57a844c2ab4e496810190b878ddb2533c`

```dockerfile
```

-	Layers:
	-	`sha256:1a958fe6a5c0035e3e3a8ff196f776464bec9658867df92cb83defbc9013f4ec`  
		Last Modified: Wed, 18 Feb 2026 19:24:57 GMT  
		Size: 12.9 MB (12858229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d8e340fff7eb05f51639988c379c6c3668043bd92eb421013270827e722cd6f`  
		Last Modified: Wed, 18 Feb 2026 19:24:57 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
