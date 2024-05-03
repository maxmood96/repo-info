## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:71c4825214a06c9b1053925123e2848ba114f70fa7b3057d35be054309164e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:a4375577bc4ec5bea313a16124a99e626b87286aa2e7e471820f03b90fc9c553
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125029560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7bfa84051d513217c82f9eb8ea080e524fe61d494b9ad2de42d4394212df41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 18:01:08 GMT
ADD file:fb22765d5c67514e681b696e92016cf73eb71f9e7ff6dd84d219c046c44b3b4a in / 
# Tue, 23 Apr 2024 18:01:09 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 23 Apr 2024 18:01:09 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 23 Apr 2024 18:01:09 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 23 Apr 2024 18:01:09 GMT
ENV container oci
# Tue, 23 Apr 2024 18:01:09 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 18:01:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 18:01:10 GMT
RUN rm -rf /var/log/*
# Tue, 23 Apr 2024 18:01:10 GMT
RUN mkdir -p /var/log/rhsm
# Tue, 23 Apr 2024 18:01:10 GMT
LABEL release=947
# Tue, 23 Apr 2024 18:01:10 GMT
ADD file:b9adbf9c748da42c5f6ba1342523fc78eeb061e7f048dda184a7ca4455ca27df in /root/buildinfo/content_manifests/ubi9-container-9.4-947.json 
# Tue, 23 Apr 2024 18:01:11 GMT
ADD file:2aa7cceeb371ddee2202f208c62907965fed93d26ecb2484d897185750962c92 in /root/buildinfo/Dockerfile-ubi9-9.4-947 
# Tue, 23 Apr 2024 18:01:11 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:39:44" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-947"
# Tue, 23 Apr 2024 18:01:11 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Tue, 23 Apr 2024 18:01:12 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 23 Apr 2024 18:01:14 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 02 May 2024 23:59:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 02 May 2024 23:59:10 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 03 May 2024 00:00:21 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 03 May 2024 00:00:21 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 03 May 2024 00:00:21 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Fri, 03 May 2024 00:00:21 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Fri, 03 May 2024 00:00:21 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 May 2024 00:00:21 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 May 2024 00:00:52 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:b2247c764f046145dfc92ceaeddfdfe33d90047471cdda0197abc15e62f64498`  
		Last Modified: Tue, 30 Apr 2024 15:30:24 GMT  
		Size: 79.3 MB (79289157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5250317dd2d0f7bd2d10ed03ae20116f9f52e9b18c8bc0249115d91a5c138834`  
		Last Modified: Fri, 03 May 2024 00:09:17 GMT  
		Size: 45.7 MB (45740403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a2a1b1f296ba953dbb5c2421d5a8fe62db9284c06dcce79906aa87d3b81835d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121277054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b0b83485530ec554c28ad944c125d06adba4cdc2d159e90f0fb68017fdadea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Apr 2024 18:01:08 GMT
ADD file:5a96c8589ef94a2970e71220aebbfd2d5dc76b05fd86db04915b48d4422a37f9 in / 
# Tue, 23 Apr 2024 18:01:09 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 23 Apr 2024 18:01:09 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 23 Apr 2024 18:01:09 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Apr 2024 18:01:09 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 23 Apr 2024 18:01:09 GMT
ENV container oci
# Tue, 23 Apr 2024 18:01:09 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 18:01:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 18:01:10 GMT
RUN rm -rf /var/log/*
# Tue, 23 Apr 2024 18:01:12 GMT
RUN mkdir -p /var/log/rhsm
# Tue, 23 Apr 2024 18:01:12 GMT
LABEL release=947
# Tue, 23 Apr 2024 18:01:12 GMT
ADD file:339cff5faeba7117326fe27895908f14be38e86ee19bdd9d9793325a925ad985 in /root/buildinfo/content_manifests/ubi9-container-9.4-947.json 
# Tue, 23 Apr 2024 18:01:12 GMT
ADD file:89f95eb4ca82b66482a2cec8a1c119f3ef924382f879e55ee3ca36897448dfef in /root/buildinfo/Dockerfile-ubi9-9.4-947 
# Tue, 23 Apr 2024 18:01:12 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:39:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-947"
# Tue, 23 Apr 2024 18:01:13 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Tue, 23 Apr 2024 18:01:14 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 23 Apr 2024 18:01:16 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 03 May 2024 00:07:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 03 May 2024 00:07:32 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 03 May 2024 00:09:09 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 03 May 2024 00:09:09 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 03 May 2024 00:09:09 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Fri, 03 May 2024 00:09:09 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Fri, 03 May 2024 00:09:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 May 2024 00:09:09 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 May 2024 00:09:45 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:182d15970afb085be58213270b5714e52c184686e0f270aa333d9500ff61eaf2`  
		Last Modified: Tue, 30 Apr 2024 15:30:23 GMT  
		Size: 77.0 MB (76986730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63b7e54a093341c050c451fc67c2b470eac7a2ffa66adf66e79398c3b96513f`  
		Last Modified: Fri, 03 May 2024 00:15:24 GMT  
		Size: 44.3 MB (44290324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
