## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:d2f41ef407433ab6a21034d8befabde5576e87b6c084a8a1d8623c04651fc11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:95d67a37402f3615af8677ac3a78bde5152c36e1dbb8b24534b94a8f95a173a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.4 MB (825355688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c1721073eb467f841fa9cd6aca35afdba513c7e457a2285932f469b724358b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 May 2024 16:48:58 GMT
ADD file:12f80c7d45b3eb0d8b3a39452a80daf9d72b5bcb3e26111bf1196b65f77dd422 in / 
# Thu, 02 May 2024 16:48:58 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 16:48:59 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 16:48:59 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 16:48:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 16:48:59 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 02 May 2024 16:48:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 16:48:59 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 02 May 2024 16:48:59 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 16:48:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 02 May 2024 16:48:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 16:48:59 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 02 May 2024 16:48:59 GMT
ENV container oci
# Thu, 02 May 2024 16:48:59 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 16:48:59 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 16:48:59 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 16:49:00 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 02 May 2024 16:49:00 GMT
ADD file:28e44343bae7309a38fcd4fee147791844f2b5a40d92f20475d4a22a3390baac in /root/buildinfo/content_manifests/ubi9-container-9.4-947.1714667021.json 
# Thu, 02 May 2024 16:49:01 GMT
ADD file:e9d6c5d1c0023a6f2768fe173d5406a1a666af1148809618b37a36eadee060be in /root/buildinfo/Dockerfile-ubi9-9.4-947.1714667021 
# Thu, 02 May 2024 16:49:01 GMT
LABEL "release"="947.1714667021" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T16:25:06" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-947.1714667021"
# Thu, 02 May 2024 16:49:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 16:49:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 16:49:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 07 May 2024 22:37:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 May 2024 22:37:43 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 07 May 2024 22:37:58 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Tue, 07 May 2024 22:37:59 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 07 May 2024 22:37:59 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 07 May 2024 22:37:59 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Tue, 07 May 2024 22:37:59 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Tue, 07 May 2024 22:37:59 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 May 2024 22:37:59 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 May 2024 22:38:42 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Tue, 07 May 2024 22:38:49 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:6b20e0c6c1e16f403ab42ddafa7c2b351b4e0da50ae0d410cd77097acfd48a79`  
		Last Modified: Mon, 06 May 2024 15:31:21 GMT  
		Size: 79.3 MB (79282021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a71377fc34e6bd94a26bb62239db1a1cf0438e22b2d1c96a417e82b09d14fc0`  
		Last Modified: Tue, 07 May 2024 22:46:48 GMT  
		Size: 122.9 MB (122888765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d01dfef7a24611b1934292a812e839eb462ee2c555a3fa1da423dd85cec8792`  
		Last Modified: Tue, 07 May 2024 22:47:59 GMT  
		Size: 623.2 MB (623184703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5623b618d538663cc78d91a4af72777881a616ff21b307cad9d72096b800d39f`  
		Last Modified: Tue, 07 May 2024 22:46:34 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:94ca2f4c9f44d6df940da9637979ea444fe0548f3ccf75c46df32c3c77ea0961
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **812.0 MB (812044977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6803ca0939d5f05ccf274e3aadf0897dc993e7d779f9841d156f553ead84c2f`
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
# Fri, 03 May 2024 00:07:48 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Fri, 03 May 2024 00:07:50 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 03 May 2024 00:07:50 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 03 May 2024 00:07:50 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Fri, 03 May 2024 00:07:50 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Fri, 03 May 2024 00:07:50 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 May 2024 00:07:50 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 May 2024 00:08:41 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 03 May 2024 00:08:55 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:182d15970afb085be58213270b5714e52c184686e0f270aa333d9500ff61eaf2`  
		Last Modified: Tue, 30 Apr 2024 15:30:23 GMT  
		Size: 77.0 MB (76986730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d902eac4d541cc15b4ae8ea03d278082b028e9e40f7decd37a7eddf3fc43780`  
		Last Modified: Fri, 03 May 2024 00:14:21 GMT  
		Size: 117.7 MB (117668846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57ea31113cc778d41d2348b9e4842492a022add441318e9ec97bae19a859f23`  
		Last Modified: Fri, 03 May 2024 00:15:09 GMT  
		Size: 617.4 MB (617389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edeca3347f181e6520ab496da6f42690cb58be04316fec2f86a98448e621fc4e`  
		Last Modified: Fri, 03 May 2024 00:14:08 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
