## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:1875bd02eac0a50757a1cf9be8e163174135177ecff01b6c525c03054afc79ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:1b21da91eb1770a6ebd65ac7c03a981bd63bf7e069b729625ef4d78535ef9a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136358429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6869c31e923417436ddc7cc3cd1a02269a4fad267242dc7a41212e785fb9af7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 12:01:20 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 12 Nov 2025 12:01:21 GMT
ENV container oci
# Wed, 12 Nov 2025 12:01:22 GMT
COPY dir:c4af8cfc19e3b7fef88c17e44e81034a660e9f4c6801670d3e7b7b41cda389f5 in /      
# Wed, 12 Nov 2025 12:01:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 12:01:22 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 12:01:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 12:01:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 12:01:22 GMT
COPY file:8da21356049927cca36ebed49e3acc1a0bb13226da7434cd96c01e82384e79b8 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 12:01:23 GMT
COPY file:8da21356049927cca36ebed49e3acc1a0bb13226da7434cd96c01e82384e79b8 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 12:01:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a195462c6565447d74f1338d8bdae5fccb5a4f36" "org.opencontainers.image.revision"="a195462c6565447d74f1338d8bdae5fccb5a4f36" "build-date"="2025-11-12T12:01:01Z" "release"="1762948793"org.opencontainers.image.revision=a195462c6565447d74f1338d8bdae5fccb5a4f36
# Fri, 14 Nov 2025 01:22:03 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 14 Nov 2025 01:22:03 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 14 Nov 2025 01:22:03 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 14 Nov 2025 01:22:03 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 14 Nov 2025 01:22:03 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Fri, 14 Nov 2025 01:22:03 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Fri, 14 Nov 2025 01:22:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 14 Nov 2025 01:22:03 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 14 Nov 2025 01:22:03 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:3022abd78a961678ba580f66f4abc6871189b6620202a20e5a15ea1adef11a8c`  
		Last Modified: Wed, 12 Nov 2025 14:41:50 GMT  
		Size: 80.0 MB (80041611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cb23d6f8ca6affcb0f634188911492b5fff9069240302f2bf79cd2cde4dbe3`  
		Last Modified: Fri, 14 Nov 2025 01:22:37 GMT  
		Size: 56.3 MB (56316818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:787c068366d3b6ff26726549ff042e2f73307966f9897781ce37d9d72ff3dc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b7df08c419254ab9d643bd0d9451ec9e9d0acb7eb44c42d4cf46bb5447ac54`

```dockerfile
```

-	Layers:
	-	`sha256:d9d2d95cfb03a7230b2cca7b18c6e9bb4801ad6e9b4708873acb54f0a1ff2c32`  
		Last Modified: Fri, 14 Nov 2025 02:51:51 GMT  
		Size: 6.4 MB (6409552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc679f98b7bad1c3ddfe5b5ef34c94e7b2dc66d7d0b47d8f2fc2ec1413cb085d`  
		Last Modified: Fri, 14 Nov 2025 02:51:51 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:995d4de8153d22fa5c200e5b21ea866fbb033f5bb09382880deb31d656b05f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132581164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73ea1d3a1453d1396301189a0f89a79a767499e94c89c623c45f0f4f9ce49e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 12:11:26 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 12 Nov 2025 12:11:26 GMT
ENV container oci
# Wed, 12 Nov 2025 12:11:29 GMT
COPY dir:99aa92d5e798a2ae59a1f88d8eb6d7d3092b2a77aafd72504d5e5bb659ae6464 in /      
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 12:11:29 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:dcdaded54259c0f330e3f96e5d91fac95a48ff9151e9495c79f0fc6924c1d6df in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 12:11:29 GMT
COPY file:dcdaded54259c0f330e3f96e5d91fac95a48ff9151e9495c79f0fc6924c1d6df in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 12:11:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a195462c6565447d74f1338d8bdae5fccb5a4f36" "org.opencontainers.image.revision"="a195462c6565447d74f1338d8bdae5fccb5a4f36" "build-date"="2025-11-12T12:11:01Z" "release"="1762948793"org.opencontainers.image.revision=a195462c6565447d74f1338d8bdae5fccb5a4f36
# Fri, 14 Nov 2025 01:38:27 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 14 Nov 2025 01:38:27 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 14 Nov 2025 01:38:27 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 14 Nov 2025 01:38:27 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 14 Nov 2025 01:38:27 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Fri, 14 Nov 2025 01:38:27 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Fri, 14 Nov 2025 01:38:27 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 14 Nov 2025 01:38:27 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 14 Nov 2025 01:38:27 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:2ea79eba6aac7ec77ffba3f470f3e821fac31f6f0eb75d6017ecf29c44bc7d9b`  
		Last Modified: Wed, 12 Nov 2025 14:41:51 GMT  
		Size: 77.7 MB (77708170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef05410801558bb95b3dff680082b8ff2088e8fcd64d504f14cc08974a6e2288`  
		Last Modified: Fri, 14 Nov 2025 01:38:55 GMT  
		Size: 54.9 MB (54872994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:ed805c97466175a3d45b0340ee830e3bf022d3b0ad851c17543f7d9a9df07963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7dc6e49bbae501fa29b57d7140c7b5c719b1c0b8aded51c25a5c42cc9cb7f7`

```dockerfile
```

-	Layers:
	-	`sha256:f875223d827b22f2556564dddcb02375ec860af393bc0efdc94e30a7a8f14448`  
		Last Modified: Fri, 14 Nov 2025 02:51:57 GMT  
		Size: 6.4 MB (6405355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6f339db1f4c92afe9142cef974338d1797b253835316e264ea3c216e329f40`  
		Last Modified: Fri, 14 Nov 2025 02:51:59 GMT  
		Size: 11.6 KB (11552 bytes)  
		MIME: application/vnd.in-toto+json
