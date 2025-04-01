## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:6f7297e612d947b13ff357b2bd4af63b0ac82b2397302c65be8f9779952ca702
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:865a960058d4e70cd36682959a933d39abc9aeb2064fef96c14f7668912f78eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094776359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38b72e90d124056da2281f9703b4c9cbb004d5f46cf4e4e922de1a3f96dcc1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 16:13:06 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 25 Mar 2025 16:13:06 GMT
ENV container oci
# Tue, 25 Mar 2025 16:13:07 GMT
COPY dir:0edc96071d03673970c637eceeec74369b8fdf1ae3d39376b389539c592ba907 in / 
# Tue, 25 Mar 2025 16:13:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 16:13:08 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 16:13:08 GMT
LABEL "build-date"="2025-03-25T16:12:35" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e98aeded1f394c8879effc230f1b407e9e55e58f" "build-date"="2025-03-25T15:58:30Z" "release"="1742918310"
# Tue, 25 Mar 2025 16:13:22 GMT
RUN /bin/sh
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:e996822e3bf30e4160bdb68906e63c226910f63f161100bf04642f443cb2eeab`  
		Last Modified: Tue, 25 Mar 2025 17:28:28 GMT  
		Size: 79.1 MB (79121942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b61797c1e3c6d3f23c1aa848e42c0b5e6cc35c534d8d503ffb9bad27ecb239`  
		Last Modified: Tue, 25 Mar 2025 17:28:26 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719fa17e92334fecb1d37bfee05021e494627fa6dad50d540b97457937fff6a`  
		Last Modified: Tue, 01 Apr 2025 17:13:29 GMT  
		Size: 122.8 MB (122825376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c7a91a4cd942cf259b9a0a4b340e167411225580f6094cfa5cd8aa79969e2`  
		Last Modified: Tue, 01 Apr 2025 17:14:11 GMT  
		Size: 892.8 MB (892828412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3571d4b09bf06b814851a70eb627166e514a8a274cbc2aba4d9ddae4d10dbee9`  
		Last Modified: Tue, 01 Apr 2025 17:13:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:80fb3149d2239d205a69bc6f98ddcf357b95bf0bf20dbf8347657e86bef93bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12893922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0f7c845ef64afeab8a6d470deb97e7300da16751b8539bf0a39507f6afa64a`

```dockerfile
```

-	Layers:
	-	`sha256:555072ae8c618362e0419004d4c7e7b6192c9b6a89893a7ca8938ff8f99a4cac`  
		Last Modified: Tue, 01 Apr 2025 17:13:26 GMT  
		Size: 12.9 MB (12878859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc5c2712881247d7a77e659570e92a5e906146a7ccfb72800adbf914da82bd7`  
		Last Modified: Tue, 01 Apr 2025 17:13:25 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:761c1466f344aa1d6e1886f041162dc89fb0b2b52f57bcefbbe89451bfbc6d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082858908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4874c65aefec409b49edbdaa58f7b286e4612f08c50ce98b56ba674bbaf6e837`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 16:17:22 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 25 Mar 2025 16:17:22 GMT
ENV container oci
# Tue, 25 Mar 2025 16:17:25 GMT
COPY dir:790f9791dd310f5c4f341398ef28213daea60b81f9d5ca5d793e3b44f1a87b8a in / 
# Tue, 25 Mar 2025 16:17:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 16:17:26 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 16:17:26 GMT
LABEL "build-date"="2025-03-25T16:16:51" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e98aeded1f394c8879effc230f1b407e9e55e58f" "build-date"="2025-03-25T15:58:30Z" "release"="1742918310"
# Tue, 25 Mar 2025 16:17:55 GMT
RUN /bin/sh
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b452a63227db6d456465c0555e20993f41c55628f058989c5f14eea506e4d722`  
		Last Modified: Tue, 25 Mar 2025 17:28:31 GMT  
		Size: 76.8 MB (76808094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2a478782fd67aaa55b76530967d570765009de89d1fe3c6e7a5c1f81781b8`  
		Last Modified: Tue, 25 Mar 2025 17:28:30 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e741203ce5c87ab52306882c5f09254a66d60107345f9ab6421f0ed87973847`  
		Last Modified: Thu, 27 Mar 2025 18:26:43 GMT  
		Size: 116.6 MB (116588530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863be352cf308f98508d8edca1c315d6970d6eff40f84c274bc9add322b91f5b`  
		Last Modified: Tue, 01 Apr 2025 18:53:37 GMT  
		Size: 889.5 MB (889461654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4df2c987f8440561a98155c0070f4aca2b9024dd63b686b458b48c2632910b`  
		Last Modified: Tue, 01 Apr 2025 18:53:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:5c564a7281651039180a97b58b048ab040ae6316f21233c67f65c60525d89c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12767110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61474b300a83c78b55f0c59b5a52186b06c630a2a82df77158f0a3285d302d7`

```dockerfile
```

-	Layers:
	-	`sha256:23faff8d8aafe23fac859e94995504c35ba19bc0f2f8b05ed079fbe60a4c4470`  
		Last Modified: Tue, 01 Apr 2025 18:53:09 GMT  
		Size: 12.8 MB (12751931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b4dae1a74be818b39af0bc7577f2b13d606b5adb442a16c060ac6f4146a0638`  
		Last Modified: Tue, 01 Apr 2025 18:53:08 GMT  
		Size: 15.2 KB (15179 bytes)  
		MIME: application/vnd.in-toto+json
