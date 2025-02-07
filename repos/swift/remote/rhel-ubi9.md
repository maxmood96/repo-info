## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:42733eae39d944e7138846f1750d4abfa6bc6c88dbfbf4c8b54349d29606b163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:e85060324958cd5bb320bbbf8b3abac28b0eacf47eb7016db2a184cfefff51ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1011877716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb28f84eb820092dca55f1b414548848ba54d5fe1794dc8ebdfa0f72ff1fe2e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 12 Dec 2024 07:44:15 GMT
ENV container oci
# Thu, 12 Dec 2024 07:44:15 GMT
COPY dir:63a4287a6e02ef536ab7236227cde983fc555d2501cb8a0770e9b52a5941cb59 in / 
# Thu, 12 Dec 2024 07:44:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL "build-date"="2025-02-06T04:08:23" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f224cb95f5b43bbe01ac7468ebdc5b78f26ab4c1" "build-date"="2025-02-06T04:01:28Z" "release"="1738814488"
# Thu, 12 Dec 2024 07:44:15 GMT
RUN /bin/sh
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:338ab464ba548e31abeca2fc0fd45ca689f1899e98fb2355a4f8d916771b8755`  
		Last Modified: Thu, 06 Feb 2025 05:02:53 GMT  
		Size: 88.5 MB (88499158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c230f8027b989d4cf14f952a4557eb7691f0adaf5ed86fb972b2a41e72c25d`  
		Last Modified: Thu, 06 Feb 2025 05:02:49 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541299e7a2335401b95081a575fbfdfe99fbbd8b783a6674c32722e0aaa16fc2`  
		Last Modified: Fri, 07 Feb 2025 00:33:26 GMT  
		Size: 123.1 MB (123100592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becb7870dcf6d647e51c7c441149215366fec01a7644653ad7f9dc8baebabdb5`  
		Last Modified: Thu, 12 Dec 2024 22:37:40 GMT  
		Size: 800.3 MB (800277307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534cbedb7930261ffa00989de8fcb38fd5c0c1dee12f45bb0359ac7442c5d72a`  
		Last Modified: Fri, 07 Feb 2025 00:33:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:13577ddb9c3a8d078201c48548457ec62e2976ca4ca55587ed1ae3835903cac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13990505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2b6ddfe238e88f298f7e0dff29ef247ea4d1349b11fe3f9a391fec89f2cdba`

```dockerfile
```

-	Layers:
	-	`sha256:3ef418be59384f6c9d01fe6e178fb6ef89f4615d850b774d1aa9f6869401f5f1`  
		Last Modified: Fri, 07 Feb 2025 00:33:24 GMT  
		Size: 14.0 MB (13975430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d41c78b2a70f7fad2825d5305f4401f6ad9d7755fd1b76d30ef60001c6dae298`  
		Last Modified: Fri, 07 Feb 2025 00:33:23 GMT  
		Size: 15.1 KB (15075 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:8e6f4bd1fcf67f50437302bdfc601e026eb19d521756a3f10c00ded9441e7c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **999.7 MB (999656242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d881988c78b59e06e6d8376126617246af94b4e4b6173c04708846ae3bf6c592`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 12 Dec 2024 07:44:15 GMT
ENV container oci
# Thu, 12 Dec 2024 07:44:15 GMT
COPY dir:1819224142417371d751621bc38e99ca15f9eaddcace1547ee3c7c135d82af46 in / 
# Thu, 12 Dec 2024 07:44:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL "build-date"="2025-02-04T04:46:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4371344f505f230dd8b447590dba1946ab022b7" "build-date"="2025-02-04T04:32:30Z" "release"="1738643550"
# Thu, 12 Dec 2024 07:44:15 GMT
RUN /bin/sh
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:45b3ea5d26da2699422d716f7553e9605ef1984c5c5bd7ad70e2884e6c4ddcdb`  
		Last Modified: Tue, 04 Feb 2025 06:08:49 GMT  
		Size: 86.3 MB (86297007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231fb10c8f7b63cd82e798581a75cac3b4f2a859c1026aa254968a1370aaab7c`  
		Last Modified: Tue, 04 Feb 2025 06:08:46 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a850a7b31e6705a109659520992785c530be69beaa3b079bd7f72d455b3ce6b`  
		Last Modified: Wed, 05 Feb 2025 04:31:49 GMT  
		Size: 116.9 MB (116885063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f936313db041fe3dee46ad15cc3dda672e3ec8f43c577c59bd936fefae706a1a`  
		Last Modified: Fri, 13 Dec 2024 00:30:33 GMT  
		Size: 796.5 MB (796473513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7be6390858fb9182d3db3543cd4dabf03a6f0ca7d6e7a2f6613be7fd0fe6d`  
		Last Modified: Wed, 05 Feb 2025 04:31:45 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:b59e7d44598c90ae1db07be21d9a54d6047466b55a573c50405dedd637c25e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13863681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08549b82ad0b8bc4a8f952a3d168f82055428a4f6460a920a54392efc7d04a44`

```dockerfile
```

-	Layers:
	-	`sha256:0d4e8da082f3af1df21a6883fd8202cdd7dfa4d281ecc33f07f67e82071e78c0`  
		Last Modified: Wed, 05 Feb 2025 04:31:46 GMT  
		Size: 13.8 MB (13848490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b9b179a3cacf592b4a924941cb069260df2b75ad54cdea327556e306e26edfd`  
		Last Modified: Wed, 05 Feb 2025 04:31:45 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json
