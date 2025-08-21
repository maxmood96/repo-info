## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:17eb38c80b136d5f385878072ae34cd8d4b8269b0a87827441793ff9e843abbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:903f2ece190ad58a88a2a009fc162e487497ff0d90688d2348dd8e0a31d6489b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094624159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb3a59cac8c5dc5c49aadf8e4707d01fc87b3db3c9099b2720c555b42c4e822`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 28 May 2025 17:53:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 28 May 2025 17:53:13 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 28 May 2025 17:53:13 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 28 May 2025 17:53:13 GMT
ENV container oci
# Wed, 28 May 2025 17:53:13 GMT
COPY dir:0222bc7b4b212f92e0fd9b1e2fb869faddda099368d73a11ebdca50e91a01fb3 in / 
# Wed, 28 May 2025 17:53:13 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 28 May 2025 17:53:13 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 28 May 2025 17:53:13 GMT
LABEL "build-date"="2025-08-20T08:31:23" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="171f11b52e43aee013fe4ef4c4caed923f25c5c1" "release"="1755678605"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:d77aa8574845b508d5fa16c7d0d6fbfc3bd0bb3c4d68b0cf4ea6bf3f20a1b3c5`  
		Last Modified: Wed, 20 Aug 2025 13:41:16 GMT  
		Size: 79.6 MB (79597952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798b3612bc30dd409442a2cba95400c4fb603689e567be467578006e1905172a`  
		Last Modified: Thu, 21 Aug 2025 19:11:04 GMT  
		Size: 124.4 MB (124416078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcd9042a6b13defe243d1dd84d563f45f7ead75c07d1598785319b0b77ba9a9`  
		Last Modified: Tue, 03 Jun 2025 20:30:52 GMT  
		Size: 890.6 MB (890609955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9174a84e7546d7d9f2d00eea4654d3f6a2560a4aaa434e0a6efea632cf9a9c6`  
		Last Modified: Thu, 21 Aug 2025 19:02:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:2693fdc111f1de2c3906ab950e080fdf5468a7bcb72eb18502dbe78a15c2e52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12987199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c2ee0f1247f2f6aa79674f1d6997b4ceaab21c7ba6a0da5cfba5bcea5913c0`

```dockerfile
```

-	Layers:
	-	`sha256:f2e2d33cd796fa0094555df99cb1368d8a780155670781bf70e8c0d673b3c8b5`  
		Last Modified: Thu, 21 Aug 2025 19:48:16 GMT  
		Size: 13.0 MB (12972740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d7acf43a4c8089d6627c1eb8ea832903e0b1111b1b068cfedc1cecc2f79f51`  
		Last Modified: Thu, 21 Aug 2025 19:48:17 GMT  
		Size: 14.5 KB (14459 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:823a644684c2443bb06f6ff1ebd2ced0ee20d5699344575137835cae2f98cc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082747025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01be5a04fbb7b11d859568bbf6c794ddfd28290ebc9540d6215950df9322ddaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 28 May 2025 17:53:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 28 May 2025 17:53:13 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 28 May 2025 17:53:13 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 28 May 2025 17:53:13 GMT
ENV container oci
# Wed, 28 May 2025 17:53:13 GMT
COPY dir:201c1b26478eb260de8e06d484f452528500ce88a37d35f2fe8e5d60789fc1d1 in / 
# Wed, 28 May 2025 17:53:13 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 28 May 2025 17:53:13 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 28 May 2025 17:53:13 GMT
LABEL "build-date"="2025-08-20T08:36:14" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="171f11b52e43aee013fe4ef4c4caed923f25c5c1" "release"="1755678605"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:f369a35b8dcd50ca9a1e43a99c63b3a9a6ead5cbe92cb0614d468e4417f834aa`  
		Last Modified: Wed, 20 Aug 2025 13:50:58 GMT  
		Size: 77.3 MB (77295931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64d97d826fdb53316cc7abcb4cd9d587c9e0ade9af900a50fb86c0b7e133b8d`  
		Last Modified: Thu, 21 Aug 2025 19:47:58 GMT  
		Size: 118.1 MB (118091021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c0d074e38755136a9465305aafe08516ebba1fecf7d780eff797053a3359fa`  
		Last Modified: Wed, 04 Jun 2025 15:11:16 GMT  
		Size: 887.4 MB (887359898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ad9cee9a887579b503c55bafe333b0fbb460b96ddeaaa5cbffa34569af0282`  
		Last Modified: Thu, 21 Aug 2025 19:47:39 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:385f1036217bb8bf6fee4d2719d9ac91f73e8e9815da0bd94934d490b7c6c7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12860562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e284e73321c8efb9bc04191f316de14b44f733c56e8a510753cf2529e741204c`

```dockerfile
```

-	Layers:
	-	`sha256:5ea868e9ffcb56ddcb834a62518e5c83b08b9dfdd72fe931916dc64a5e3f72a4`  
		Last Modified: Thu, 21 Aug 2025 22:48:26 GMT  
		Size: 12.8 MB (12845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8567bda9fe39d4c33f7494a0fefa3352aa0a3804b2034c60b1129b3d5ca742d7`  
		Last Modified: Thu, 21 Aug 2025 22:48:27 GMT  
		Size: 14.6 KB (14575 bytes)  
		MIME: application/vnd.in-toto+json
