## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:c2a6c9333da1f004432d84fc480e9dda6cced6c73ff4f12f75277d6feb65ae94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:c0f92499406d00c4ec25c3409b9aad69833fb91f6ef449e690ab2ca79419971a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1288473855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b91985f137faf819fe744c0ee08abae1ec9b67ba7898fec7d8143847578b66e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:07 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:07 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:08 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:08 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:08 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 08 Apr 2026 04:55:08 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:08 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 08 Apr 2026 04:55:08 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:09 GMT
COPY dir:077cf32f0e57d0f1e801be3757eb22de02dc49119f111ffd433b20759f21e5c3 in /      
# Wed, 08 Apr 2026 04:55:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:09 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:10 GMT
COPY file:d5a5d627786faf7ea9c3cf65e4846600ce23c6922b7c5e5c3d139ba118931537 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:10 GMT
COPY file:d5a5d627786faf7ea9c3cf65e4846600ce23c6922b7c5e5c3d139ba118931537 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:11 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="66e8aa3cc8d2a684f6d699381efbcf6383bc2387" "org.opencontainers.image.revision"="66e8aa3cc8d2a684f6d699381efbcf6383bc2387" "build-date"="2026-04-08T04:54:54Z" "org.opencontainers.image.created"="2026-04-08T04:54:54Z" "release"="1775624009"org.opencontainers.image.revision=66e8aa3cc8d2a684f6d699381efbcf6383bc2387,org.opencontainers.image.created=2026-04-08T04:54:54Z
# Wed, 08 Apr 2026 17:43:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 08 Apr 2026 17:43:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 08 Apr 2026 17:43:02 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 08 Apr 2026 17:43:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 08 Apr 2026 17:43:02 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 08 Apr 2026 17:43:02 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 08 Apr 2026 17:43:02 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 08 Apr 2026 17:43:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 08 Apr 2026 17:43:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 08 Apr 2026 17:43:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 08 Apr 2026 17:43:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2a35ea4a0f227689f2da83ed16c71957d06241ec5063b61a9753a0165a8df3ff`  
		Last Modified: Wed, 08 Apr 2026 06:08:46 GMT  
		Size: 79.9 MB (79939847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269bcdc1d1bd3a77322169fe174c6189ba31fffba6db79ffe5234632fff4c960`  
		Last Modified: Wed, 08 Apr 2026 17:46:14 GMT  
		Size: 124.7 MB (124709467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a59214f566cae843f63b761f195f32d3a880cb172420d206e63435164aa070`  
		Last Modified: Tue, 24 Mar 2026 22:16:10 GMT  
		Size: 1.1 GB (1083824366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9854df2f9a436ece8fdfb2487ed7c5b95f9548724df073b1b526a520c1ce9cf9`  
		Last Modified: Wed, 08 Apr 2026 17:46:10 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:dd2eedb414b8467b02e0cad1df0f34a77898d022ad024e58f933f26d2892946a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da8597c8bb1ca9b200a31ed14bcc6e399d809f20bfc11987811be9ecc03a0f`

```dockerfile
```

-	Layers:
	-	`sha256:7f06bf7183b69ace829fd60973e28f71b82148dddb37ac1163446e279617dfe5`  
		Last Modified: Wed, 08 Apr 2026 17:46:11 GMT  
		Size: 13.0 MB (12985026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8a6206e186762b3b672bacd954b6bedd709a450fbbd6b972d30a7555724c65`  
		Last Modified: Wed, 08 Apr 2026 17:46:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:6e4d29e99cf9dddceccda141e4cd424859aed65f1f21887065a70e5028de1eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1275957263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec235a764b63617d264c1bc8cd2a17b4b60e356c5ad6e02c6400f56191b0f42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:58:21 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 08 Apr 2026 04:58:21 GMT
ENV container oci
# Wed, 08 Apr 2026 04:58:25 GMT
COPY dir:b3f7ba874fb9a0facccbe37fad7969ea636b5781c932a8205b3ba6da40a242aa in /      
# Wed, 08 Apr 2026 04:58:25 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:58:25 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:58:25 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:58:25 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:58:25 GMT
COPY file:63e588d9789be5ee3b1978b61b6e19c7cc5e5274c197b137fbb74171d0442cc0 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:58:25 GMT
COPY file:63e588d9789be5ee3b1978b61b6e19c7cc5e5274c197b137fbb74171d0442cc0 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:58:26 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="66e8aa3cc8d2a684f6d699381efbcf6383bc2387" "org.opencontainers.image.revision"="66e8aa3cc8d2a684f6d699381efbcf6383bc2387" "build-date"="2026-04-08T04:58:03Z" "org.opencontainers.image.created"="2026-04-08T04:58:03Z" "release"="1775624009"org.opencontainers.image.revision=66e8aa3cc8d2a684f6d699381efbcf6383bc2387,org.opencontainers.image.created=2026-04-08T04:58:03Z
# Wed, 08 Apr 2026 17:46:34 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 08 Apr 2026 17:46:34 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 08 Apr 2026 17:46:34 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 08 Apr 2026 17:46:34 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 08 Apr 2026 17:46:34 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 08 Apr 2026 17:46:34 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 08 Apr 2026 17:46:34 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 08 Apr 2026 17:46:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 08 Apr 2026 17:46:34 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 08 Apr 2026 17:47:19 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 08 Apr 2026 17:47:19 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b179f1ebac4c74b59ec89f73cd415c0e37f86c2d9bb2f7ecbca4d556ae93597d`  
		Last Modified: Wed, 08 Apr 2026 06:09:02 GMT  
		Size: 77.7 MB (77690771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c9149a181c7d6b6d88ba3dfc901d5e6ab71c49bfac63a2817b86563660b654`  
		Last Modified: Wed, 08 Apr 2026 17:49:32 GMT  
		Size: 118.2 MB (118203972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afa09088faa46bde909962bad099be0f37b95eda016a32e6c5b35632ae2ffda`  
		Last Modified: Tue, 24 Mar 2026 22:16:33 GMT  
		Size: 1.1 GB (1080062345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f7db18bcff0fa07b0b9a4960d1e19459e1883635165a559636ab02be61384b`  
		Last Modified: Wed, 08 Apr 2026 17:49:28 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:866744d409aa10334642b0f0a8bc6f9bc5e572d127f231e28104b73b97164f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8a111d54bba47096705f7d1bfc6fe559420faee476d076ac56ef0cfe00ca8b`

```dockerfile
```

-	Layers:
	-	`sha256:d3ea59d141b28ba9de08cc94b091158862b7f4cfc41310db911c65a753f5358c`  
		Last Modified: Wed, 08 Apr 2026 17:49:29 GMT  
		Size: 12.9 MB (12858263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf6ee87464c7d4b2354f26130208f7e05712032c9e388650927bd4921196b72`  
		Last Modified: Wed, 08 Apr 2026 17:49:28 GMT  
		Size: 14.5 KB (14546 bytes)  
		MIME: application/vnd.in-toto+json
