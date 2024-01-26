## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:8296d0de123836a6a4128399f680a7d31b51b3c234f0889b634b21ff7ab1bf7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:4988e7ca2c2416a87b72840cc060bd02ffcb2775ff5002d51cfb87f7a38bddf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124268714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40450859856ccb4e07dbea6d78ca84ae2bce5352be3f113bac9bc73f8f928366`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jan 2024 19:19:56 GMT
ADD file:203d8a440d4a212a3de9f4b263e3745c6128caae02b75208c4ab08afa02c8042 in / 
# Wed, 17 Jan 2024 19:19:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:19:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:19:58 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.3"
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 17 Jan 2024 19:19:58 GMT
ENV container oci
# Wed, 17 Jan 2024 19:19:58 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:19:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:19:59 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:19:59 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 17 Jan 2024 19:19:59 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:20:00 GMT
ADD file:a2f04c734a30ef620587d3de15d7c0c1984aa702a61dbdd568e3301056771155 in /root/buildinfo/content_manifests/ubi9-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:20:00 GMT
ADD file:e8a28bfd49796b6e1cb4385742ffd9e5e7709c8dd2ba9a76b1a8c5fb4cfe4405 in /root/buildinfo/Dockerfile-ubi9-9.3-1552 
# Wed, 17 Jan 2024 19:20:00 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:40" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="eb726081eeafc660c182aae53074ec6631cb473e" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.3-1552"
# Wed, 17 Jan 2024 19:20:01 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:20:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:20:05 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 26 Jan 2024 02:05:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 26 Jan 2024 02:05:59 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 26 Jan 2024 02:07:09 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 26 Jan 2024 02:07:09 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 26 Jan 2024 02:07:09 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Fri, 26 Jan 2024 02:07:09 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Fri, 26 Jan 2024 02:07:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 26 Jan 2024 02:07:09 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 26 Jan 2024 02:07:36 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:1bd75c368cb585e77e0b3234a750db4235fa64ff8b5b9ca8da8bf7a34ec9ecaa`  
		Last Modified: Thu, 25 Jan 2024 18:06:59 GMT  
		Size: 78.9 MB (78853820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756c5e6ae023c10ee761b9164da49ffeaa18e00381b732c625d49393c25decf3`  
		Last Modified: Fri, 26 Jan 2024 02:14:17 GMT  
		Size: 45.4 MB (45414894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:fe7ab24cfd2d019236bfbee924dcef18ac7cd3f79e67590038b4d327897f193c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120576670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b3a0bd8d5907f4eb0d94f9d65776c2817983b1b05b3ba494ac99b35495d77f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jan 2024 19:19:52 GMT
ADD file:aff8bc779c8789d35ac2a80d9a02f20b74e69b456173a040eaf73fe97d9a3f11 in / 
# Wed, 17 Jan 2024 19:19:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:19:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:19:54 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.3"
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 17 Jan 2024 19:19:54 GMT
ENV container oci
# Wed, 17 Jan 2024 19:19:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:19:54 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:19:55 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:19:57 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 17 Jan 2024 19:19:57 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:19:57 GMT
ADD file:1b29ebbd958d302277790a4e064782c082d19926c466a9dd447aa453b2bc65d2 in /root/buildinfo/content_manifests/ubi9-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:19:57 GMT
ADD file:db3ad7c9c52d4b1c490f1ebf564a128ce62fad1d213e5e94e2f1393551715c6b in /root/buildinfo/Dockerfile-ubi9-9.3-1552 
# Wed, 17 Jan 2024 19:19:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:40" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="eb726081eeafc660c182aae53074ec6631cb473e" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.3-1552"
# Wed, 17 Jan 2024 19:19:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:20:00 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:20:02 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 26 Jan 2024 02:32:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 26 Jan 2024 02:32:09 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 26 Jan 2024 02:33:31 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 26 Jan 2024 02:33:31 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 26 Jan 2024 02:33:31 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Fri, 26 Jan 2024 02:33:31 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Fri, 26 Jan 2024 02:33:31 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 26 Jan 2024 02:33:31 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 26 Jan 2024 02:34:03 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:2f4c7b011e02135ccee6607271ddd903269b4fd07b493ae6abc9b26f162f9499`  
		Last Modified: Thu, 25 Jan 2024 18:07:07 GMT  
		Size: 76.5 MB (76515496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7140eb398967032de442060584ff4c5077926d6237097094ed1e4da5e1aa31a`  
		Last Modified: Fri, 26 Jan 2024 02:38:12 GMT  
		Size: 44.1 MB (44061174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
