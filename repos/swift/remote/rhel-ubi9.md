## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:f18f63ef35acbfff0ef5548497c9538ae9942556ebab6d474e43ef320ca9103b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:4def6acf4589d6c66ae8f56f11d3a05552fc71ce137eec8f9a99c290e6700012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1288526947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e72280c2b27281a82f8ee090033bf0ff33f2eb4051e9068303f6078eb87d43e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Mar 2026 05:18:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 25 Mar 2026 05:18:00 GMT
LABEL io.openshift.expose-services=""
# Wed, 25 Mar 2026 05:18:00 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 25 Mar 2026 05:18:00 GMT
ENV container oci
# Wed, 25 Mar 2026 05:18:01 GMT
COPY dir:5f42172b9bd80150725c18296732df201c1f7ba4225c031a0e4175eb57c8aaf7 in /      
# Wed, 25 Mar 2026 05:18:01 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 25 Mar 2026 05:18:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Mar 2026 05:18:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 25 Mar 2026 05:18:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 25 Mar 2026 05:18:02 GMT
COPY file:d3c056c2cffb5ef231b335663d74f1a5511def9489d289f0fbddc2b79453f000 in /usr/share/buildinfo/labels.json      
# Wed, 25 Mar 2026 05:18:02 GMT
COPY file:d3c056c2cffb5ef231b335663d74f1a5511def9489d289f0fbddc2b79453f000 in /root/buildinfo/labels.json      
# Wed, 25 Mar 2026 05:18:03 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="07b654b5754308740ae2e8c2adde29678c5e9667" "org.opencontainers.image.revision"="07b654b5754308740ae2e8c2adde29678c5e9667" "build-date"="2026-03-25T05:17:41Z" "org.opencontainers.image.created"="2026-03-25T05:17:41Z" "release"="1774415752"org.opencontainers.image.revision=07b654b5754308740ae2e8c2adde29678c5e9667,org.opencontainers.image.created=2026-03-25T05:17:41Z
# Wed, 25 Mar 2026 17:47:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Mar 2026 17:47:06 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Mar 2026 17:47:06 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 25 Mar 2026 17:47:06 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Mar 2026 17:47:06 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Mar 2026 17:47:06 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 25 Mar 2026 17:47:06 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 25 Mar 2026 17:47:06 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Mar 2026 17:47:06 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Mar 2026 17:47:44 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 25 Mar 2026 17:47:45 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:96cadc7a5c0105296da36547c7820a31a86ff861ec8f67526bcb80a161a0523f`  
		Last Modified: Wed, 25 Mar 2026 06:43:26 GMT  
		Size: 80.0 MB (79965699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d59ed24c620d3761de4c233b6f33d558170ba32370494904ca96a7a3d4e7bf8`  
		Last Modified: Wed, 25 Mar 2026 17:50:05 GMT  
		Size: 124.7 MB (124736710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a59214f566cae843f63b761f195f32d3a880cb172420d206e63435164aa070`  
		Last Modified: Tue, 24 Mar 2026 22:16:10 GMT  
		Size: 1.1 GB (1083824366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7074fcdef42c7dcfd66069f9c1cd48197eaa071312f7fc1054f9820b4873fe`  
		Last Modified: Wed, 25 Mar 2026 17:50:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:2616dc694a5a0fa3990990275d0761ba86fcce8727a5cb1a53ab81a24e6396db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9756f12fb60732cd5b9917cb1d9e448e7c090cbf6a856a50b83702aa45aba2f0`

```dockerfile
```

-	Layers:
	-	`sha256:4ffa2929f5aaddf26c3cdecdf8eb9aa3cd2bd077a6081d10a29a8d0a8a4a5ed3`  
		Last Modified: Wed, 25 Mar 2026 17:50:03 GMT  
		Size: 13.0 MB (12985018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348cb031c36bd5cf89a43185aa3fa2e4fddc0e89c837796d79d8d2a8151894e2`  
		Last Modified: Wed, 25 Mar 2026 17:50:02 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:5791d277725304426fa5af6289a9d4309764585f7d5b0c55306d2d7d4c4eabfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276028268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829412048c07cae151675975be38732f377228e4216215a04967dba34ec48dc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 25 Mar 2026 05:21:01 GMT
ENV container oci
# Wed, 25 Mar 2026 05:21:05 GMT
COPY dir:e508066e907da1d4d6c6186e42de70836eb08907574181ae07dba9e0203c8a59 in /      
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 25 Mar 2026 05:21:05 GMT
CMD ["/bin/bash"]
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:899533d1478875a4f4ed147cd383f908cdf9d76e471c24d3caeca5b7c9c91d8c in /usr/share/buildinfo/labels.json      
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:899533d1478875a4f4ed147cd383f908cdf9d76e471c24d3caeca5b7c9c91d8c in /root/buildinfo/labels.json      
# Wed, 25 Mar 2026 05:21:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="07b654b5754308740ae2e8c2adde29678c5e9667" "org.opencontainers.image.revision"="07b654b5754308740ae2e8c2adde29678c5e9667" "build-date"="2026-03-25T05:20:44Z" "org.opencontainers.image.created"="2026-03-25T05:20:44Z" "release"="1774415752"org.opencontainers.image.revision=07b654b5754308740ae2e8c2adde29678c5e9667,org.opencontainers.image.created=2026-03-25T05:20:44Z
# Wed, 25 Mar 2026 17:48:25 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Mar 2026 17:48:25 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Mar 2026 17:48:25 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 25 Mar 2026 17:48:25 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Mar 2026 17:48:25 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Mar 2026 17:48:25 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 25 Mar 2026 17:48:25 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 25 Mar 2026 17:48:25 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Mar 2026 17:48:25 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Mar 2026 17:49:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 25 Mar 2026 17:49:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2dba26dca7a080db23ce08a57a530936de117c1ae8824a001d239e6b578a5db0`  
		Last Modified: Wed, 25 Mar 2026 06:37:37 GMT  
		Size: 77.7 MB (77729981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc73f03275dfa0d8e612b7b71ce5121f101c81092ab1d7d88c6568e64772ba`  
		Last Modified: Wed, 25 Mar 2026 17:51:18 GMT  
		Size: 118.2 MB (118235768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afa09088faa46bde909962bad099be0f37b95eda016a32e6c5b35632ae2ffda`  
		Last Modified: Tue, 24 Mar 2026 22:16:33 GMT  
		Size: 1.1 GB (1080062345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e0ad7ccac9249701576956a7468e46176c7afeb6e2065b50bea499ffb06279`  
		Last Modified: Wed, 25 Mar 2026 17:51:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:dca30915224f904f03b2d1d226fbe6cb0edf4b2a3ed0f2fc97a93a00df97dd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4209f9551f9d21d9bbccab76fd841f708f9f0ef8eb2932a9e2978ca43c2512f2`

```dockerfile
```

-	Layers:
	-	`sha256:a8ac3acd752ae92d0fd68009d86c285f713f3483afc5985ae50d912bf0e0f614`  
		Last Modified: Wed, 25 Mar 2026 17:51:15 GMT  
		Size: 12.9 MB (12858255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e82b9a03d76027b60c12bc8625a0a99f5d38ef90e802deb15af3bd7206997f4f`  
		Last Modified: Wed, 25 Mar 2026 17:51:14 GMT  
		Size: 14.5 KB (14546 bytes)  
		MIME: application/vnd.in-toto+json
