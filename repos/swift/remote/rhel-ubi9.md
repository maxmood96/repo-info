## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:20940f6ec0debfd9ad40be6f7e75f97fb65c8d5f09a445bc93afaa6314ee5a47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:841b577222a3f0258b74a30e0dd2544efbe1e981267b2fe4c2fb5323146bbb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1227131194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b366766a7d39d3ef64076fa3798d129742551a99407e9c1e5ef1e8ed6a9b6943`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:53 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:53 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:53 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:53 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:53 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 01 Dec 2025 08:45:54 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:54 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 01 Dec 2025 08:45:54 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:56 GMT
COPY dir:46fbd2019e68549ca8d24430cbb86753551f96d5b71a900ff539c6295590f15b in /      
# Mon, 01 Dec 2025 08:45:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:56 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:57 GMT
COPY file:3d3efe180857a638784e19b113cd57aa9c64b9c4c28ac91d03a49e8b860d7085 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:57 GMT
COPY file:3d3efe180857a638784e19b113cd57aa9c64b9c4c28ac91d03a49e8b860d7085 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:58 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="bd89b0898f46c7b1903073e8d2392eeef49c1341" "org.opencontainers.image.revision"="bd89b0898f46c7b1903073e8d2392eeef49c1341" "build-date"="2025-12-01T08:45:30Z" "org.opencontainers.image.created"="2025-12-01T08:45:30Z" "release"="1764578509"org.opencontainers.image.revision=bd89b0898f46c7b1903073e8d2392eeef49c1341,org.opencontainers.image.created=2025-12-01T08:45:30Z
# Tue, 02 Dec 2025 00:44:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 02 Dec 2025 00:44:06 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 02 Dec 2025 00:44:06 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 02 Dec 2025 00:44:06 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 02 Dec 2025 00:44:06 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 02 Dec 2025 00:44:06 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 02 Dec 2025 00:44:06 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 02 Dec 2025 00:44:06 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Dec 2025 00:44:06 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Dec 2025 00:44:49 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 02 Dec 2025 00:44:50 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:a6ae885dc0a379e92e7b234f66b3d2c23cbe3ecf46ad423d02ea53fdb9de1488`  
		Last Modified: Mon, 01 Dec 2025 09:43:39 GMT  
		Size: 80.0 MB (80022085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80746b87c011347377a77b6a54165e7b51a6ff5cc46f5055b79f09ed1caa1b01`  
		Last Modified: Tue, 02 Dec 2025 00:47:32 GMT  
		Size: 124.7 MB (124706288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26680006a5e69f18fea192c7ddb54de3eda701a42806d7537679024eadc73a28`  
		Last Modified: Tue, 04 Nov 2025 23:53:02 GMT  
		Size: 1.0 GB (1022402647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9b6e6f483c806b1024641515b7d614f9b34a5064fd17cd823f2c44f5fb4c67`  
		Last Modified: Tue, 02 Dec 2025 00:47:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:67a6eecb4b90da40706090c4223ea721a83fa8e8700da7015bc158b98f4bc7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13002612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83309815ad8c30b16cf9598940effa5e893549197bec75b58eb9aefc3e685547`

```dockerfile
```

-	Layers:
	-	`sha256:1dac949cbb5bd9da627479a7c945f9ead1eca6eeb0bcedcac91049f8d01d9328`  
		Last Modified: Tue, 02 Dec 2025 02:49:07 GMT  
		Size: 13.0 MB (12988170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ebfbd24c9c1b462b73a6744e2ef0128e2fa107ed91c3f8dbe30ac38c776a096`  
		Last Modified: Tue, 02 Dec 2025 02:49:08 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c10222a9b37aac7ed5f6ed0696bccb5f9c27fa37ad4dc6e9636f93545de48ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1214538181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9439c6c6a37aa2c9a2f0354471521bb7f894afe260b5dfe364c88984ca37f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:48:17 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 01 Dec 2025 08:48:17 GMT
ENV container oci
# Mon, 01 Dec 2025 08:48:20 GMT
COPY dir:4f0c605f401424ec858624c9aee5cddefb6d5ad91a5fe06b7a458f928d986849 in /      
# Mon, 01 Dec 2025 08:48:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:48:20 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:48:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:48:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:48:21 GMT
COPY file:3e84aed8cd0465d8234883b4bf47b0c690a914794d73cc295f9b8c63e8cbd911 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:48:21 GMT
COPY file:3e84aed8cd0465d8234883b4bf47b0c690a914794d73cc295f9b8c63e8cbd911 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:48:22 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="bd89b0898f46c7b1903073e8d2392eeef49c1341" "org.opencontainers.image.revision"="bd89b0898f46c7b1903073e8d2392eeef49c1341" "build-date"="2025-12-01T08:47:53Z" "org.opencontainers.image.created"="2025-12-01T08:47:53Z" "release"="1764578509"org.opencontainers.image.revision=bd89b0898f46c7b1903073e8d2392eeef49c1341,org.opencontainers.image.created=2025-12-01T08:47:53Z
# Tue, 02 Dec 2025 00:49:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 02 Dec 2025 00:49:09 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 02 Dec 2025 00:49:09 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 02 Dec 2025 00:49:09 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 02 Dec 2025 00:49:09 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 02 Dec 2025 00:49:09 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 02 Dec 2025 00:49:09 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 02 Dec 2025 00:49:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Dec 2025 00:49:09 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 02 Dec 2025 00:49:47 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 02 Dec 2025 00:49:47 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:d719ea5b6e943938dc345595bd6d2413bb99ac6151d302d5c2c79932b539c58f`  
		Last Modified: Mon, 01 Dec 2025 09:42:38 GMT  
		Size: 77.7 MB (77723813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba01f71daf9b2c65145c17f442c2df28e39564f2d8671d599f9263d34540ff2c`  
		Last Modified: Tue, 02 Dec 2025 00:52:14 GMT  
		Size: 118.2 MB (118204551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddef3547821a1751f340d01b0a4642a5c7128317d72c4ab95f398bdbdabe7e02`  
		Last Modified: Tue, 04 Nov 2025 22:02:23 GMT  
		Size: 1.0 GB (1018609645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9e5435d410906426b151aad9c95295e4c521831a69d68d81f4a952b692e24a`  
		Last Modified: Tue, 02 Dec 2025 00:51:59 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:1e8ef17dfd78140ed1c51fab6fe39323fedf17bf4e363a289538a99c061d2346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12875971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8797a3962fadb5599790c11f48bad14511d261142c6766426469b0004e2b4f52`

```dockerfile
```

-	Layers:
	-	`sha256:1f9c89fe744b11b3be0b7b4146842bcccb8fcc8cf6a194645e4d611bbf9884f0`  
		Last Modified: Tue, 02 Dec 2025 02:49:20 GMT  
		Size: 12.9 MB (12861413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7feb1e28cdf22fc35a5c67f53a799157ad3d654e52e6aaad82521bcaf3c108aa`  
		Last Modified: Tue, 02 Dec 2025 02:49:20 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
