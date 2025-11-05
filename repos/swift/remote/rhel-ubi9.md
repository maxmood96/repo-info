## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:683f5c5f4ab4e8c59921789dd73488f68a23c9c5960175886e6fd3bd8d7c71cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:26c7f7c607b240095377166c2999d86b541027342dc5248063c0b70e59ae4138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1231318347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4220d9bdeb9e92c0fe99b96de0177eb184be9bfc84a992f1f3ed5bde1bc3670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Oct 2025 07:37:06 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 13 Oct 2025 07:37:06 GMT
ENV container oci
# Mon, 13 Oct 2025 07:37:07 GMT
COPY dir:91d00d24ce3ba29551746ee5faca2e3a563eef65ecd488882ee5f2d4f984589d in /      
# Mon, 13 Oct 2025 07:37:07 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Oct 2025 07:37:07 GMT
CMD ["/bin/bash"]
# Mon, 13 Oct 2025 07:37:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Oct 2025 07:37:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Oct 2025 07:37:08 GMT
COPY file:a782d4cd79a0c61643bc1cbf3cd5798a42f1495fe330dde8598373d62cac62dd in /root/buildinfo/labels.json      
# Mon, 13 Oct 2025 07:37:08 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="60d587d1286655c5e777e63959aaae224123ea95" "org.opencontainers.image.revision"="60d587d1286655c5e777e63959aaae224123ea95" "build-date"="2025-10-13T07:36:46Z" "release"="1760340943"org.opencontainers.image.revision=60d587d1286655c5e777e63959aaae224123ea95
# Tue, 04 Nov 2025 22:27:05 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 22:27:05 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 22:27:05 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 04 Nov 2025 22:27:05 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 22:27:05 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 04 Nov 2025 22:27:05 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 22:27:05 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 22:27:05 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:27:05 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:27:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 04 Nov 2025 22:27:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:35d6a5cce6a146ea7213377edde7d1d27f34dda18ce9fac98ea2ab40a6b110f6`  
		Last Modified: Mon, 13 Oct 2025 08:55:32 GMT  
		Size: 79.6 MB (79593305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afc556a3a8e4db34369d61e696f8ee54d9488a7ba1ab63d7d3e7e198eac6c68`  
		Last Modified: Tue, 04 Nov 2025 23:52:15 GMT  
		Size: 129.3 MB (129322221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26680006a5e69f18fea192c7ddb54de3eda701a42806d7537679024eadc73a28`  
		Last Modified: Tue, 04 Nov 2025 23:53:02 GMT  
		Size: 1.0 GB (1022402647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4654b9c80ba5db4ada1210f0cb5456e989612b90c81acd6cfd3c911ca5aee9f1`  
		Last Modified: Tue, 04 Nov 2025 22:30:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:652be8b3a97c204fcb0045272c500b88fc71bb6b7cf440110f2744ead1631493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13305042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeee4c6052771bbad166940bd4eab3e0aa5ab537f166657e36588209e8e17d5c`

```dockerfile
```

-	Layers:
	-	`sha256:aa60bd29720db34b022fb2d90ba3c9725299e9af5cbfed831f57a6f768b9166b`  
		Last Modified: Tue, 04 Nov 2025 23:48:27 GMT  
		Size: 13.3 MB (13290600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d1bc4c6091eff1a3e69f0289a4110a81ca110c0aa84fd9d12ec61c2f397d6e`  
		Last Modified: Tue, 04 Nov 2025 23:48:29 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:9adb29867ec6ea120475399086cbdd48596f6a83635a0bd542c03692a9da0eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1218422649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5651e9a7cd68eb3a8a208190db8b2c0d1ddbef79e14b880e887d84aaf657d8da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Oct 2025 07:42:13 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 13 Oct 2025 07:42:13 GMT
ENV container oci
# Mon, 13 Oct 2025 07:42:16 GMT
COPY dir:b9ca9ee30ad427ffb29be1a6c8e68d7dfc3fa9352a21a6a76346c5782783c7a9 in /      
# Mon, 13 Oct 2025 07:42:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Oct 2025 07:42:16 GMT
CMD ["/bin/bash"]
# Mon, 13 Oct 2025 07:42:16 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Oct 2025 07:42:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Oct 2025 07:42:17 GMT
COPY file:d2bf1cf35fa0b6f9865b8418d392585e592bd0e3566050282498c9984d00cc1b in /root/buildinfo/labels.json      
# Mon, 13 Oct 2025 07:42:18 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="60d587d1286655c5e777e63959aaae224123ea95" "org.opencontainers.image.revision"="60d587d1286655c5e777e63959aaae224123ea95" "build-date"="2025-10-13T07:41:49Z" "release"="1760340943"org.opencontainers.image.revision=60d587d1286655c5e777e63959aaae224123ea95
# Tue, 04 Nov 2025 19:24:17 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 19:24:17 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 19:24:17 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 04 Nov 2025 19:24:17 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 19:24:17 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 04 Nov 2025 19:24:17 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 19:24:17 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 19:24:17 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:17 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 04 Nov 2025 19:24:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:47c325a0b847affaa9b64f57de793eff43b8d44ae93c70c8f50b53cc15ac6046`  
		Last Modified: Mon, 13 Oct 2025 12:10:12 GMT  
		Size: 77.3 MB (77323400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b35475c3d500a8da2907032bba74f2c6fd832c12024c55e91cd16fb64daeb4`  
		Last Modified: Tue, 04 Nov 2025 19:27:42 GMT  
		Size: 122.5 MB (122489430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddef3547821a1751f340d01b0a4642a5c7128317d72c4ab95f398bdbdabe7e02`  
		Last Modified: Tue, 04 Nov 2025 22:02:23 GMT  
		Size: 1.0 GB (1018609645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf93c7b77efa85cd93e7ef082cf4d4cf4d76eefe37c966edf2a844c422451039`  
		Last Modified: Tue, 04 Nov 2025 19:27:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:254536ce9f0868570c3b96c74b76e98d2f206e786a7d8974fe5883395f72e693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13178405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83946fd02827c1bcdd87e49f0e9e6860c04bc92a33812b54499c3b8be43e8996`

```dockerfile
```

-	Layers:
	-	`sha256:5a2a37a135062cf6f5c51cd91ef99e494988768604dab0c54394b35ce924d105`  
		Last Modified: Tue, 04 Nov 2025 20:48:36 GMT  
		Size: 13.2 MB (13163847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926bc9a94255e49f7a712192d0c4af24a8a0647ffb9defe64c1b8f3ccdce6ef6`  
		Last Modified: Tue, 04 Nov 2025 20:48:37 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
