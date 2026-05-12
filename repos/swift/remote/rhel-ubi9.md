## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:1ac85712559a024052643ecdeb6849794309c5a41b4d7e00be4d5e713cd1a061
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:0146e7bf88c3a72d715c4a52b181b4e5db2c8bf421e4b266ad2062f00093cdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1288714943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90ebdb5ec096d728a55c2021a6574f3f3d040cc32d1f802d336ed79a3d6d1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 01:10:44 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:44 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:44 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:44 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:44 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 11 May 2026 01:10:44 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:44 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 11 May 2026 01:10:44 GMT
ENV container oci
# Mon, 11 May 2026 01:10:46 GMT
COPY dir:3e9b69065f1b03614a43fdc2cafc8b2f104c4c87073a2b71cb0164f16480691a in /      
# Mon, 11 May 2026 01:10:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:46 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:46 GMT
COPY file:7ff2c6266c483d4bc5f41607ac60902030e6dfea5adeec7d894fdb8e18e061d3 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:46 GMT
COPY file:7ff2c6266c483d4bc5f41607ac60902030e6dfea5adeec7d894fdb8e18e061d3 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:47 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b94dc3e0b7deccdcc3e7872a74a11c0c527edf71" "org.opencontainers.image.revision"="b94dc3e0b7deccdcc3e7872a74a11c0c527edf71" "build-date"="2026-05-11T01:10:29Z" "org.opencontainers.image.created"="2026-05-11T01:10:29Z" "release"="1778461714"org.opencontainers.image.revision=b94dc3e0b7deccdcc3e7872a74a11c0c527edf71,org.opencontainers.image.created=2026-05-11T01:10:29Z
# Tue, 12 May 2026 00:09:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 12 May 2026 00:09:06 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 12 May 2026 00:09:06 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 12 May 2026 00:09:06 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 12 May 2026 00:09:06 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 12 May 2026 00:09:06 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Tue, 12 May 2026 00:09:06 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Tue, 12 May 2026 00:09:06 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 May 2026 00:09:06 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 May 2026 00:09:49 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 12 May 2026 00:09:50 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:c3a6b73ebcf8fae497bbbaf7aaf1d1bdcf798345f97e5fc3247486d03efe9955`  
		Last Modified: Mon, 11 May 2026 02:48:53 GMT  
		Size: 80.0 MB (79961413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695e1ce12cbfa5b676977c88f916b7a2c72fac7616f00fda596d632c62b4690d`  
		Last Modified: Tue, 12 May 2026 00:11:57 GMT  
		Size: 124.7 MB (124704015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f7355d20d694d145fbf4688c63a728cb08f4edbff524635d4047a4f954daba`  
		Last Modified: Mon, 20 Apr 2026 21:56:34 GMT  
		Size: 1.1 GB (1084049344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc5c9e61c7f8b1278dace09815491b7575aef4c3a4bab115f5657dee7f9b2d`  
		Last Modified: Tue, 12 May 2026 00:11:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:2530481b2c49d33470aa7d7e8632b8547d0eaa5df637fbfcc01aa52a92b0d18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391628546207536cace3e6f88db06372c5e1be0c96238f124ed174ade686481d`

```dockerfile
```

-	Layers:
	-	`sha256:d294d78918cdef6a1ef913acb5f5a70a2051d96a99474e15bccb15920c5d0b6b`  
		Last Modified: Tue, 12 May 2026 00:11:55 GMT  
		Size: 13.0 MB (12985056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506fad27ea8ebad4030581991a2af465c13fd332754009ea4f88a41e17197c81`  
		Last Modified: Tue, 12 May 2026 00:11:54 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d6be14507130c5ca30617074d70ad827a4d34437bbe3b1dec4fe183cfd0a43ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276231701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe5fadd3d1fb66b2eae84d859ee184963bda37f64d6fa18dd6cd1992f7797c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 01:13:30 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:13:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:13:30 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:13:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:13:30 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:13:30 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:13:30 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:13:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 11 May 2026 01:13:30 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:13:30 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 11 May 2026 01:13:30 GMT
ENV container oci
# Mon, 11 May 2026 01:13:33 GMT
COPY dir:bc072d8abb88c1da7ec2ffd18b89f05c03ddd43385faa870145aad7bdbff64d6 in /      
# Mon, 11 May 2026 01:13:33 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:13:33 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:13:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:13:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:13:34 GMT
COPY file:485f321861052d76ef8e3d132f5bd210103b3b01dc0034be966c560cd5c6456a in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:13:34 GMT
COPY file:485f321861052d76ef8e3d132f5bd210103b3b01dc0034be966c560cd5c6456a in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:13:35 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="b94dc3e0b7deccdcc3e7872a74a11c0c527edf71" "org.opencontainers.image.revision"="b94dc3e0b7deccdcc3e7872a74a11c0c527edf71" "build-date"="2026-05-11T01:13:13Z" "org.opencontainers.image.created"="2026-05-11T01:13:13Z" "release"="1778461714"org.opencontainers.image.revision=b94dc3e0b7deccdcc3e7872a74a11c0c527edf71,org.opencontainers.image.created=2026-05-11T01:13:13Z
# Tue, 12 May 2026 00:08:57 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 12 May 2026 00:08:57 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 12 May 2026 00:08:57 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 12 May 2026 00:08:57 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 12 May 2026 00:08:57 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 12 May 2026 00:08:57 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Tue, 12 May 2026 00:08:57 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Tue, 12 May 2026 00:08:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 May 2026 00:08:57 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 May 2026 00:09:38 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 12 May 2026 00:09:38 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:45ec008552f45d7abdfca35526774cc442d795d361684b2793bdb7ed6e7f07f0`  
		Last Modified: Mon, 11 May 2026 02:50:34 GMT  
		Size: 77.7 MB (77743776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921b16ec39f9da6d2af954d3dd47c9708eaf42a056c8a98a614edad7d8c95b2e`  
		Last Modified: Tue, 12 May 2026 00:11:50 GMT  
		Size: 118.2 MB (118209070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6fdf9a00e14597ecc9dfe9618d4ce7bd4e61ee02520f5014ac6ae58fe238e0`  
		Last Modified: Mon, 20 Apr 2026 22:03:23 GMT  
		Size: 1.1 GB (1080278683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d80dc445967c1fe87f8a49d96c470226e8c0e798735789eee106b4208cf4b`  
		Last Modified: Tue, 12 May 2026 00:11:47 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:1815fb2b39771e3d0ca24005ccaf3cb200128a2c7a5883115407b8b5f463873c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d22605d79da164f64777fb874215cc2378b524faf456ad6712c7d9c679c4cd4`

```dockerfile
```

-	Layers:
	-	`sha256:e7f42b599c09d1cbcd5b8c3a4aaf01a729a8ae4bfacc96006085755490a41753`  
		Last Modified: Tue, 12 May 2026 00:11:47 GMT  
		Size: 12.9 MB (12858293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e5d3dfd6bd438277a82ac64af3a260b4f5ab019060003a70f1e970e61e84dd`  
		Last Modified: Tue, 12 May 2026 00:11:47 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
