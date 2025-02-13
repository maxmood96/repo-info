## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:633ffc27a5d82a8df22217155c7c2bd5ac63cc11cea0e3dc86a2947896237d82
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
		Last Modified: Thu, 06 Feb 2025 05:03:21 GMT  
		Size: 88.5 MB (88499158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c230f8027b989d4cf14f952a4557eb7691f0adaf5ed86fb972b2a41e72c25d`  
		Last Modified: Thu, 06 Feb 2025 05:03:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541299e7a2335401b95081a575fbfdfe99fbbd8b783a6674c32722e0aaa16fc2`  
		Last Modified: Fri, 07 Feb 2025 02:55:44 GMT  
		Size: 123.1 MB (123100592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becb7870dcf6d647e51c7c441149215366fec01a7644653ad7f9dc8baebabdb5`  
		Last Modified: Fri, 13 Dec 2024 20:05:18 GMT  
		Size: 800.3 MB (800277307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534cbedb7930261ffa00989de8fcb38fd5c0c1dee12f45bb0359ac7442c5d72a`  
		Last Modified: Fri, 07 Feb 2025 02:55:39 GMT  
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
		Last Modified: Fri, 07 Feb 2025 08:53:43 GMT  
		Size: 14.0 MB (13975430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d41c78b2a70f7fad2825d5305f4401f6ad9d7755fd1b76d30ef60001c6dae298`  
		Last Modified: Fri, 07 Feb 2025 00:33:23 GMT  
		Size: 15.1 KB (15075 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:7c064d5f37b91037e6d9b0dbdf121e5df11beffad264a21ff73a626347cca762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **999.6 MB (999645050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ec02aade36fa9899852237e4b5cdc3fcb4255eddddc7f9e2167f15f30fcfd2`
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
COPY dir:27e025b591c1d25127127b9f62a2532c98d6288b3d70640cbb2ed9a925313720 in / 
# Thu, 12 Dec 2024 07:44:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL "build-date"="2025-02-06T04:11:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f224cb95f5b43bbe01ac7468ebdc5b78f26ab4c1" "build-date"="2025-02-06T04:01:28Z" "release"="1738814488"
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
	-	`sha256:ec3e3bc2c155b2c89fc61dfba75496f580318614c5638592247ad33b146f35da`  
		Last Modified: Thu, 06 Feb 2025 06:26:18 GMT  
		Size: 86.3 MB (86297311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437b861084ee700c712b1a52a2f96ac3a531faf33e756f1d181499444305a2f2`  
		Last Modified: Thu, 06 Feb 2025 06:26:15 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dcb9f624abdb7f5b6c596a0fb28a5cdef253c289904328078c4962a33601fd`  
		Last Modified: Fri, 07 Feb 2025 08:54:21 GMT  
		Size: 116.9 MB (116873565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f936313db041fe3dee46ad15cc3dda672e3ec8f43c577c59bd936fefae706a1a`  
		Last Modified: Fri, 13 Dec 2024 16:18:45 GMT  
		Size: 796.5 MB (796473513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5285ef02ade785eba274d8b283fce2f57f723335060aebf5e3a8e6ebc1e3b5`  
		Last Modified: Fri, 07 Feb 2025 05:55:15 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:14dcb36ead84d570d5a14b494f6c2614935f3bb9d889af4c34e09319fce1947e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13863681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7a9d35fdf74989a88372e0917d03cb957ae5aa15d977e39db3365cce5a5758`

```dockerfile
```

-	Layers:
	-	`sha256:793af43c6ce80ff9fd007697e997578534d8600a47ea7544e63bd6d045bd6106`  
		Last Modified: Fri, 07 Feb 2025 03:19:36 GMT  
		Size: 13.8 MB (13848490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f244fcdc54a0782b34b491ff926fb657f73caa5a1c938afc356e9f430dbaf3`  
		Last Modified: Fri, 07 Feb 2025 03:19:35 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json
