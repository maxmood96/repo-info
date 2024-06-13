## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:12c0084a37d8c046a4ab5c38f9fd60da333b01e78a9e8de9557f8b9fe2721430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:11aa08e600adaa21a578c178ca22f82e7f4f6242a1cb54c8439fb95b2d93eac2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.5 MB (825536405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6427dc01115650efeb9236aba43a101414992d52c6bd67f4e78927aea6f58de4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 00:58:16 GMT
ADD file:dc4be39847cc4bfa7b7926e6ad0273d3e62da6a38ea000e1a56b21b84d236c73 in / 
# Thu, 06 Jun 2024 00:58:17 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 00:58:17 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 00:58:18 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 00:58:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 00:58:18 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 06 Jun 2024 00:58:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 00:58:18 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 00:58:18 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 00:58:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 06 Jun 2024 00:58:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 00:58:18 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 06 Jun 2024 00:58:18 GMT
ENV container oci
# Thu, 06 Jun 2024 00:58:18 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 00:58:18 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 00:58:18 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 00:58:19 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 06 Jun 2024 00:58:19 GMT
LABEL release=1123
# Thu, 06 Jun 2024 00:58:19 GMT
ADD file:534ad296f6f7045b0ff8d163e9f8af021b11ef21959d0d254708ce64c10a1975 in /root/buildinfo/content_manifests/ubi9-container-9.4-1123.json 
# Thu, 06 Jun 2024 00:58:19 GMT
ADD file:3fd2917f1f80ce168bd1530e703a64254eba861e91870a7e793d9a2735b77e6f in /root/buildinfo/Dockerfile-ubi9-9.4-1123 
# Thu, 06 Jun 2024 00:58:19 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:48:40" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1123"
# Thu, 06 Jun 2024 00:58:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 00:58:21 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 00:58:23 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 13 Jun 2024 18:58:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 13 Jun 2024 18:58:59 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 13 Jun 2024 18:59:16 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Thu, 13 Jun 2024 18:59:16 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 13 Jun 2024 18:59:17 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 13 Jun 2024 18:59:17 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 13 Jun 2024 18:59:17 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 13 Jun 2024 18:59:17 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Jun 2024 18:59:17 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Jun 2024 18:59:55 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 13 Jun 2024 19:00:02 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:edab65b863aead24e3ed77cea194b6562143049a9307cd48f86b542db9eecb6e`  
		Last Modified: Thu, 13 Jun 2024 09:28:28 GMT  
		Size: 79.3 MB (79287874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0494df9cb57bd7046a9652dfffe0d48341f06a8511e5da6e0b6a789a4dadd54f`  
		Last Modified: Thu, 13 Jun 2024 19:06:56 GMT  
		Size: 122.8 MB (122755500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f150ba9a9cce0b5566903ce30b81d54ba11cba30e8bc3eb78b3f955793c4868`  
		Last Modified: Thu, 13 Jun 2024 19:08:05 GMT  
		Size: 623.5 MB (623492858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c63038b88e40a6bcc848890e75b488a59887867d86426e272de39a18449a9f3`  
		Last Modified: Thu, 13 Jun 2024 19:06:41 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:870ae5515fce5401065db8ececaebfcc41df75c1130b6ab5114bced633690425
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **811.6 MB (811557956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2352aa0108cc6816b1796829438436280e34802d7ba04f178ce739bf1fde2128`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 00:58:13 GMT
ADD file:be4e99ab737bcd60d63aab82589b0dcc7640435761ae0b2cb1b52cf399f72ba9 in / 
# Thu, 06 Jun 2024 00:58:15 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 00:58:15 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 00:58:15 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 00:58:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 00:58:15 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 06 Jun 2024 00:58:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 00:58:15 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 00:58:15 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 00:58:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 06 Jun 2024 00:58:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 00:58:15 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 06 Jun 2024 00:58:15 GMT
ENV container oci
# Thu, 06 Jun 2024 00:58:15 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 00:58:15 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 00:58:16 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 00:58:17 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 06 Jun 2024 00:58:17 GMT
LABEL release=1123
# Thu, 06 Jun 2024 00:58:17 GMT
ADD file:d3727a02a184b622f798fbc18d3203991a1d8385f2063e3ef8f98b53baf93c73 in /root/buildinfo/content_manifests/ubi9-container-9.4-1123.json 
# Thu, 06 Jun 2024 00:58:17 GMT
ADD file:40f204d0f952f40c45f8f07df81499d4021b3465ca4be003cbd97003ec3ce8ba in /root/buildinfo/Dockerfile-ubi9-9.4-1123 
# Thu, 06 Jun 2024 00:58:17 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:48:40" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1123"
# Thu, 06 Jun 2024 00:58:19 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 00:58:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 00:58:22 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 13 Jun 2024 18:38:20 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 13 Jun 2024 18:38:20 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 13 Jun 2024 18:38:32 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Thu, 13 Jun 2024 18:38:33 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 13 Jun 2024 18:38:34 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 13 Jun 2024 18:38:34 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 13 Jun 2024 18:38:34 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 13 Jun 2024 18:38:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Jun 2024 18:38:34 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Jun 2024 18:39:25 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 13 Jun 2024 18:39:38 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:7d712778376a75b29c264e8d58699a6d1644d455a63d3014bb050a9fafdc3544`  
		Last Modified: Thu, 13 Jun 2024 12:09:06 GMT  
		Size: 77.0 MB (76986664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e968a88a5a57300adc54f617f1f4e7592eb5b52ff9d77bf571ffafe6f462fb25`  
		Last Modified: Thu, 13 Jun 2024 18:45:11 GMT  
		Size: 116.9 MB (116886608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3e22d6914ff0bea632d5f358e1dddcf0c43b80c57321661844f23339d2cad5`  
		Last Modified: Thu, 13 Jun 2024 18:46:00 GMT  
		Size: 617.7 MB (617684509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f9f0a78d6e79d2c6d2642368348920ecdc9f43180072b9cb5b986a36c05393`  
		Last Modified: Thu, 13 Jun 2024 18:44:58 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
