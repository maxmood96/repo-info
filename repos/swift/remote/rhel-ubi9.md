## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:5c387b4e813ee977653c19dc9b769f2176a8455ba2d7f4cf1d4bf8a34ff5478d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:c6e5084c59fae41ef1919bd308519c079b2b86b3eeb6be7a591a89190b88ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1029313592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6a72ba7f8053b564243ab74f715627def7f0c416ce3e09afab694c83c9f946`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 21:36:31 GMT
ADD file:0067eb9f2ee25ab2d666a7639a85fe707b582902a09242761abf30c53664069b in / 
# Wed, 18 Sep 2024 21:36:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:36:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:36:32 GMT
ADD multi:7a67822d03b1a3ddb205cc3fcf7acd9d3180aef5988a5d25887bc0753a7a493b in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 18 Sep 2024 21:36:32 GMT
ENV container oci
# Wed, 18 Sep 2024 21:36:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:36:32 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:36:33 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:36:34 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 18 Sep 2024 21:36:35 GMT
ADD file:ed34e436a5c2cc729eecd8b15b94c75028aea1cb18b739cafbb293b5e4ad5dae in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1726694543.json 
# Wed, 18 Sep 2024 21:36:35 GMT
ADD file:d56bb1961538221b52d7e292418978f186bf67b9906771f38530fc3996a9d0d4 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1726694543 
# Wed, 18 Sep 2024 21:36:35 GMT
LABEL "release"="1214.1726694543" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:30" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1726694543"
# Wed, 18 Sep 2024 21:36:36 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496925-3b364.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:36:37 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:36:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:40049f9dc50417693bf704b63a02d64347b23867b33ac7776be3fae4a2d178b0`  
		Last Modified: Mon, 23 Sep 2024 14:28:12 GMT  
		Size: 79.6 MB (79592786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938ded3fb58091355acf792fbf0ce14e32b6d1732e6e27f191996ea1d9b58adc`  
		Last Modified: Thu, 26 Sep 2024 22:59:18 GMT  
		Size: 122.7 MB (122699846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d27dad1c0ccf0982dfae8fd7f9c90d669afb08f9e2c6ea6b52a5913ae372c8`  
		Last Modified: Thu, 26 Sep 2024 22:59:28 GMT  
		Size: 827.0 MB (827020785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89011947fe50c670f939182b6a1eaa713f68d8454cc59314a6e0f974de7638b`  
		Last Modified: Thu, 26 Sep 2024 22:59:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:e05e064ab89c864f2784731070ae73630c8790cef1d68191ca98e221781fdb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12879230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e882494e0016664f53f7aae5b229f10c7a05dadff559b345b9c2ce1982e999`

```dockerfile
```

-	Layers:
	-	`sha256:b6de1737e81f7bca1d7ab4f2cb37ca7bbc1af2616938e0c9b696bf9ce7d37bc4`  
		Last Modified: Thu, 26 Sep 2024 22:59:17 GMT  
		Size: 12.9 MB (12864781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36948bd3bae3db0f83300b185e596e447b329ea3e22e5826d46888e8df9fea3`  
		Last Modified: Thu, 26 Sep 2024 22:59:17 GMT  
		Size: 14.4 KB (14449 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:0ae4c52700cf2c2f58e22053b92c3c8023cb82ccc2d130122b364f87ce711990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1017362548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8a453783e4bc1e92634311f4ad4e170ee93a76155ddac0b639a27600b976d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:d6101aaaa0ea140d84b6346291651ad4d2bce8c444478e1fc83508b02136ec0f in / 
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 17 Sep 2024 00:51:42 GMT
ADD multi:7a67822d03b1a3ddb205cc3fcf7acd9d3180aef5988a5d25887bc0753a7a493b in /etc/yum.repos.d/ 
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 17 Sep 2024 00:51:42 GMT
ENV container oci
# Tue, 17 Sep 2024 00:51:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 00:51:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -rf /var/log/*
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mkdir -p /var/log/rhsm
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:6744b3d23896832934836f8b77190150a7f9f836065a064436c5b9dc47a95425 in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1726694543.json 
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:19c58e8e8129cd749e0ec129d64db36f9eb2b3729bc034e6755ab07ad478a419 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1726694543 
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL "release"="1214.1726694543" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:30" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1726694543"
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496925-3b364.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:642dd3de0a7ba3fef28a56da54f6c6b620e3bdff1c55b20751a3029bea383326`  
		Last Modified: Mon, 23 Sep 2024 14:28:14 GMT  
		Size: 77.4 MB (77352301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c76da7f7952f608a13aafb0e3eb1613de41b053dd21b310a2d9588c9ca9511`  
		Last Modified: Tue, 24 Sep 2024 01:29:37 GMT  
		Size: 116.9 MB (116851306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b1129369064aa6a6d2392a20506ffa9f9b787933cfcf90a305d053ea33aae`  
		Last Modified: Tue, 17 Sep 2024 17:29:28 GMT  
		Size: 823.2 MB (823158767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5209fea90de839ee33d06fb5a315850f5de96eb64070882aad71b38ea1a877`  
		Last Modified: Tue, 24 Sep 2024 01:29:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:9ae27290b963970758a1027b062fa3358972c9e43d4f4b66f33cad56f35abb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12754375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b17dc8a02da0f4aa516998b26eedd51f8f99abbf434fee03cc51d360d86c80`

```dockerfile
```

-	Layers:
	-	`sha256:60cca33d2cf093ebb2a8e060d0427f4832b444e1504e6001e0aa782feb6a515e`  
		Last Modified: Tue, 24 Sep 2024 01:29:35 GMT  
		Size: 12.7 MB (12739651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c336d4d599b810a0a7c9aeb8ac6c810c4aa710993c839c85ba0dacc462f5676e`  
		Last Modified: Tue, 24 Sep 2024 01:29:35 GMT  
		Size: 14.7 KB (14724 bytes)  
		MIME: application/vnd.in-toto+json
