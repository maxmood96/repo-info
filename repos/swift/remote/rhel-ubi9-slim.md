## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:530f87c6046a7c554200d06ac5152c5adf217602cf6e941ce003d59358fa0a92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:a5d51ecb010ac2b80b164b75916b62105350d5a215dab225769508603195ff9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143236041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487241abe44a09c504ccee4d29b0f2b7ccf3f10eafa8e8ddb7427888ace2acf0`
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
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
	-	`sha256:13e6e86eaf07a2a983abc4519d535a4f29be1f7aaaff9c7d42115a47ce61cfa2`  
		Last Modified: Sat, 08 Feb 2025 00:55:43 GMT  
		Size: 54.7 MB (54736423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:042e253d38448808f91b369e8f35455e362b7f79b70ebc3f1dd54ada4287c4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a030cdb432fa02223ad53bb7e3a25644b2f1cfc71f5c6da545ec010310d7f65`

```dockerfile
```

-	Layers:
	-	`sha256:911035d26359c543d0fc892218c914cf74a4f7eb76b1f0077c0b2d4601b03177`  
		Last Modified: Fri, 07 Feb 2025 00:31:43 GMT  
		Size: 7.5 MB (7473242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82883d02618450ef84a73befd9beb9509038e6f594e4fbbf38fa789d1c707d68`  
		Last Modified: Fri, 07 Feb 2025 00:31:42 GMT  
		Size: 11.8 KB (11807 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:007f463aa80dcfa553f3a57e2677e6f58193aa99235cd44bd702d1949db26ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139949133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c628c98f56a45cec34e6f2739871a88f8fafd6381745894b3e41b3afa5615e`
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
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
	-	`sha256:f931160cecaa01447c751ab9fa53750de3987e2470b19ea129713a85307640c4`  
		Last Modified: Sat, 08 Feb 2025 00:51:21 GMT  
		Size: 53.7 MB (53651362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:3635349ff76e2d47e6e668b2c7b2c5e9073b8cd6dbf9b4891344428b205c67f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbcebbc1f7725d478288d9de18a05b04c2bcf201df6470a9e0c48a1321df075`

```dockerfile
```

-	Layers:
	-	`sha256:66a6fe7a0d7772bb79017d00704548f09a3fd2e36036cd5fdb63b5346d5701eb`  
		Last Modified: Fri, 07 Feb 2025 03:20:36 GMT  
		Size: 7.5 MB (7469045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeadee9f1a339f6c65c43ea7df4ffcbef547e00a2a19b56315c7b244413a26f6`  
		Last Modified: Fri, 07 Feb 2025 03:20:36 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.in-toto+json
