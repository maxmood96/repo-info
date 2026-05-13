## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:3b44bd9aacd02c1b56144da243284219bb2d01e97c8e21b79c85caee164679e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:3f711f013bfb131c786e986af1cf5387aae00afdf3a62947aa461614e90d5fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1288590739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030de07ad44c0680d1a0d2aa6493fb231c3db4ec60ef4b815da2f2ca2fe9116d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 May 2026 09:01:01 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:01:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:01:01 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 09:01:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:01:01 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 12 May 2026 09:01:01 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:01:01 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:01:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 12 May 2026 09:01:01 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:01:01 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 12 May 2026 09:01:01 GMT
ENV container oci
# Tue, 12 May 2026 09:01:03 GMT
COPY dir:dc2903ccadfb17708e4f3606c837c7a2dcaefcf45e7650b8e21eaa8685308f51 in /      
# Tue, 12 May 2026 09:01:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:01:03 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:01:03 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:01:03 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:01:03 GMT
COPY file:b5436b9382ece22e983fc2ba25df27bf2a379c73c669aa0a75af228b6c9148f3 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:01:03 GMT
COPY file:b5436b9382ece22e983fc2ba25df27bf2a379c73c669aa0a75af228b6c9148f3 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:01:04 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa4fa8db6226e15f9e1c73bc3815043f0c0a439d" "org.opencontainers.image.revision"="aa4fa8db6226e15f9e1c73bc3815043f0c0a439d" "build-date"="2026-05-12T09:00:42Z" "org.opencontainers.image.created"="2026-05-12T09:00:42Z" "release"="1778576335"org.opencontainers.image.revision=aa4fa8db6226e15f9e1c73bc3815043f0c0a439d,org.opencontainers.image.created=2026-05-12T09:00:42Z
# Wed, 13 May 2026 18:17:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:17:09 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:17:09 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 13 May 2026 18:17:09 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:17:09 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 13 May 2026 18:17:09 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:17:09 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:17:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:17:09 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:17:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 13 May 2026 18:17:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b66ab30abd6c3aa6e70bb84e4b3f0025035459b0fa3fc0d28bb37e057cde7b50`  
		Last Modified: Tue, 12 May 2026 10:09:26 GMT  
		Size: 80.0 MB (79954768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a2a9689132dbf30935b1bbbae3ada57b23a3cee648e9970d847f1faa9e912f`  
		Last Modified: Wed, 13 May 2026 18:20:05 GMT  
		Size: 124.7 MB (124712577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec82f397aadc643580e3fb9f811fcb374c771614968d9324a8ee2bd6bd174904`  
		Last Modified: Wed, 13 May 2026 18:20:44 GMT  
		Size: 1.1 GB (1083923220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0739b5e8bb168ead1df1535026a83aa1215b55c99e2f26b9f8d424c5392c037e`  
		Last Modified: Wed, 13 May 2026 18:19:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:4207e125ce0226ee1259678cf9b191a152135ff5342b17b92c15f5567e0e509c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eed018c46ee740b95e6e8686da6f5b80c2bbd082fa1573a43da41a1908cb7fe`

```dockerfile
```

-	Layers:
	-	`sha256:fa176e624a92f6931c1cffacf1119300506335db7fddac912938fb55047a8379`  
		Last Modified: Wed, 13 May 2026 18:19:59 GMT  
		Size: 13.0 MB (12985056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c99ed3b349402c5adf210ea31b98a55c1ae68549ebd7661948b10024d22fc2`  
		Last Modified: Wed, 13 May 2026 18:19:58 GMT  
		Size: 14.4 KB (14441 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:978518529628b914fab44cce33f55bb8706e446b88805983cbc1aa2293488e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276059428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e52e8a152128dececfce89753bad640be80835a81795c54c3740911d8fac4b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 May 2026 09:02:53 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:02:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:02:54 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 09:02:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:02:54 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 12 May 2026 09:02:54 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:02:54 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:02:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 12 May 2026 09:02:54 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:02:54 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 12 May 2026 09:02:54 GMT
ENV container oci
# Tue, 12 May 2026 09:02:57 GMT
COPY dir:79843c7a11b82518bdac5c3918cb04f59fa9fd5e588d4ad937331cdae04daaf1 in /      
# Tue, 12 May 2026 09:02:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:02:57 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:02:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:02:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:02:57 GMT
COPY file:09ce45df509134aee3aee77e0b739651c99a05567d56c48d6dfcbc2b68737b85 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:02:57 GMT
COPY file:09ce45df509134aee3aee77e0b739651c99a05567d56c48d6dfcbc2b68737b85 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:02:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa4fa8db6226e15f9e1c73bc3815043f0c0a439d" "org.opencontainers.image.revision"="aa4fa8db6226e15f9e1c73bc3815043f0c0a439d" "build-date"="2026-05-12T09:02:37Z" "org.opencontainers.image.created"="2026-05-12T09:02:37Z" "release"="1778576335"org.opencontainers.image.revision=aa4fa8db6226e15f9e1c73bc3815043f0c0a439d,org.opencontainers.image.created=2026-05-12T09:02:37Z
# Wed, 13 May 2026 18:04:56 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:04:56 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:04:56 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 13 May 2026 18:04:56 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:04:56 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 13 May 2026 18:04:56 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:04:56 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:04:56 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:04:56 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:05:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 13 May 2026 18:05:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:66c47a7ff47768837c084e8a7889a768b3f736f72ddb31d8896c4c5112926914`  
		Last Modified: Tue, 12 May 2026 10:02:33 GMT  
		Size: 77.7 MB (77744299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc64b743174c4cd6b870a94308c69182879e87eee34232344916ddba6332fc3`  
		Last Modified: Wed, 13 May 2026 18:08:16 GMT  
		Size: 118.2 MB (118209238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44ed9a9b258612e96029485a3a9d687b406d4f639aead7bfe9f142a2b16fe6f`  
		Last Modified: Wed, 13 May 2026 18:08:43 GMT  
		Size: 1.1 GB (1080105717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a0b79ad596b2b47b7b69802b2b288f87d1e43e3b2069e6f49fdbbb6ef10618`  
		Last Modified: Wed, 13 May 2026 18:07:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:905f020c88008656ced985e4ef650af4a07fb3da937ce51d92159e95d38b079f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6f94be652d786757e36f75fd05af4960080f06d587d8bb3529634d06ac559a`

```dockerfile
```

-	Layers:
	-	`sha256:84d0bdf31bf074b9cc3225ffbf433bab05a8f24dc78a3e7e5781040caa1e77c7`  
		Last Modified: Wed, 13 May 2026 18:07:59 GMT  
		Size: 12.9 MB (12858293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550c66f9ab1356d946c0f1ec9e598c8e2061eb3886315c0686aa3fa46f5bac49`  
		Last Modified: Wed, 13 May 2026 18:07:51 GMT  
		Size: 14.6 KB (14556 bytes)  
		MIME: application/vnd.in-toto+json
