## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:f72e88b18cdf4f7d3208c68caece5950dc68ef30a8ad00ec5d6604900bcda567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:7741d91221b67507ca2fb531616b7e09ded86756ab8b6281f4c9174ee326e0af
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.6 MB (825633368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47af3176b69d09f614aba7a10cb24a62944fad1ddd1c9b2957c8e478b0baf43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 07:43:16 GMT
ADD file:a39e39cd7aad7a577d39d64808b4c090e96fb35852b56da2c3b283372460bc69 in / 
# Fri, 28 Jun 2024 07:43:17 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 28 Jun 2024 07:43:17 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 28 Jun 2024 07:43:17 GMT
ADD multi:061215fe5c3ae072bec6a393d07eed4e23cd262b9ac55be47f1423e9b7a0fa9b in /etc/yum.repos.d/ 
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL io.openshift.expose-services=""
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL io.openshift.tags="base rhel9"
# Fri, 28 Jun 2024 07:43:17 GMT
ENV container oci
# Fri, 28 Jun 2024 07:43:17 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jun 2024 07:43:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 07:43:18 GMT
RUN rm -rf /var/log/*
# Fri, 28 Jun 2024 07:43:19 GMT
RUN mkdir -p /var/log/rhsm
# Fri, 28 Jun 2024 07:43:19 GMT
ADD file:e2860f591e48df213f28e961858e597f1a926cedceb7d085891c6b0a46348fdc in /root/buildinfo/content_manifests/ubi9-container-9.4-1123.1719560047.json 
# Fri, 28 Jun 2024 07:43:19 GMT
ADD file:eb17d50d46bdbb2eafa65ae804418b719596414b3b75d810ace78940f7dd698e in /root/buildinfo/Dockerfile-ubi9-9.4-1123.1719560047 
# Fri, 28 Jun 2024 07:43:19 GMT
LABEL "release"="1123.1719560047" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-28T07:36:05" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1123.1719560047"
# Fri, 28 Jun 2024 07:43:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3231928-93eb2.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Fri, 28 Jun 2024 07:43:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 28 Jun 2024 07:43:23 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 02 Jul 2024 00:51:51 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 02 Jul 2024 00:51:51 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 02 Jul 2024 00:52:07 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Tue, 02 Jul 2024 00:52:08 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 02 Jul 2024 00:52:08 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 02 Jul 2024 00:52:08 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Tue, 02 Jul 2024 00:52:08 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Tue, 02 Jul 2024 00:52:08 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jul 2024 00:52:08 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jul 2024 00:52:53 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Tue, 02 Jul 2024 00:53:00 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:f50ab65647ec96ba313779f24c41e04bc6fde3e3ee79ee377ea8fd1901b896d5`  
		Last Modified: Mon, 01 Jul 2024 10:03:48 GMT  
		Size: 79.3 MB (79313334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae3ad70190742b9ebaeb8b048984412cbff4a7b2b785fa0e20239164738faa2`  
		Last Modified: Tue, 02 Jul 2024 00:59:32 GMT  
		Size: 122.8 MB (122827001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d94e6cf8a615d1fc6f6968d14c6cc7abcc5b6360c9d7d30306f730ca4ed097f`  
		Last Modified: Tue, 02 Jul 2024 01:00:38 GMT  
		Size: 623.5 MB (623492859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac92837241816087f2dd5c941d1eb91cafbb0fb518f806d9409bd7a8dc457c5`  
		Last Modified: Tue, 02 Jul 2024 00:59:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c4235e05c52fa47753fbc8776c3993192324b9ba80df13235ed61454e848b845
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **811.7 MB (811658104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3730ee363da2f7f92fd145395e3384e21a7c354d3f78e006f7ed73d8b9a5e14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 07:43:15 GMT
ADD file:335ed73bbd571a2d8d265acfbef89aef7685ebe43551753a631835d4fa4a5d82 in / 
# Fri, 28 Jun 2024 07:43:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Fri, 28 Jun 2024 07:43:17 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Fri, 28 Jun 2024 07:43:17 GMT
ADD multi:061215fe5c3ae072bec6a393d07eed4e23cd262b9ac55be47f1423e9b7a0fa9b in /etc/yum.repos.d/ 
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL io.openshift.expose-services=""
# Fri, 28 Jun 2024 07:43:17 GMT
LABEL io.openshift.tags="base rhel9"
# Fri, 28 Jun 2024 07:43:17 GMT
ENV container oci
# Fri, 28 Jun 2024 07:43:17 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jun 2024 07:43:17 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 07:43:18 GMT
RUN rm -rf /var/log/*
# Fri, 28 Jun 2024 07:43:19 GMT
RUN mkdir -p /var/log/rhsm
# Fri, 28 Jun 2024 07:43:19 GMT
ADD file:e9817068e897613d5d39fa1542ce3521ea8895568929673880634bcde722f159 in /root/buildinfo/content_manifests/ubi9-container-9.4-1123.1719560047.json 
# Fri, 28 Jun 2024 07:43:19 GMT
ADD file:8af4e5c3d9f50568285a6bcdbaf84d8a90f0dbbf7c170224d357209637fb938f in /root/buildinfo/Dockerfile-ubi9-9.4-1123.1719560047 
# Fri, 28 Jun 2024 07:43:19 GMT
LABEL "release"="1123.1719560047" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-28T07:36:05" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1123.1719560047"
# Fri, 28 Jun 2024 07:43:21 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3231928-93eb2.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Fri, 28 Jun 2024 07:43:22 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Fri, 28 Jun 2024 07:43:24 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 02 Jul 2024 00:54:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 02 Jul 2024 00:54:28 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 02 Jul 2024 00:54:44 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Tue, 02 Jul 2024 00:54:46 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 02 Jul 2024 00:54:46 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 02 Jul 2024 00:54:46 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Tue, 02 Jul 2024 00:54:46 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Tue, 02 Jul 2024 00:54:46 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jul 2024 00:54:46 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Jul 2024 00:55:24 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Tue, 02 Jul 2024 00:55:36 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:42928cefe51f8d29dc26f18234bb712e5c35d72ca2a8c175b7e4147fcabe9805`  
		Last Modified: Mon, 01 Jul 2024 12:07:19 GMT  
		Size: 77.0 MB (77009884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccdd9520640c7e672d8fce83827ad30e1328ba738500188dd8ef830c7b3a0e1`  
		Last Modified: Tue, 02 Jul 2024 01:09:09 GMT  
		Size: 117.0 MB (116963611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b6fd68532c586cd4f833fe25d423f5fbc90209d25f73f1e598d7be8baf4071`  
		Last Modified: Tue, 02 Jul 2024 01:09:59 GMT  
		Size: 617.7 MB (617684433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e229c23c05a3e588a3bf77e44f78819d8e99573495d9b247802002e437babc`  
		Last Modified: Tue, 02 Jul 2024 01:08:57 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
