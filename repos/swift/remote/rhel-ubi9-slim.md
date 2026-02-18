## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:affa08eacda740918fcf716d9475502687ab1b08b6a285de28c4422189187164
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:eb574fef220a4aaa9affe234a35a2741f179e5130ca823244d4e3652b8ce0280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136423659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117fec39cc46af4c9072c36b48bdd818b17d2107ea75390bd1f8e54a8a978c4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:48:05 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:48:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 17 Feb 2026 16:48:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:48:06 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 17 Feb 2026 16:48:06 GMT
ENV container oci
# Tue, 17 Feb 2026 16:48:08 GMT
COPY dir:044009bcad68a63810df7b2a79a5fbd57bbd048f70aed9c80fca25b3757f2cb8 in /      
# Tue, 17 Feb 2026 16:48:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:48:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:48:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:48:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:48:10 GMT
COPY file:ab0176372e5af8a8d1c3b049741d0c5e75d527a597b7c8a836b568335bef6b28 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:48:10 GMT
COPY file:ab0176372e5af8a8d1c3b049741d0c5e75d527a597b7c8a836b568335bef6b28 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:48:11 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8726709260f051bcc33519b9b82af822eb97f840" "org.opencontainers.image.revision"="8726709260f051bcc33519b9b82af822eb97f840" "build-date"="2026-02-17T16:47:43Z" "org.opencontainers.image.created"="2026-02-17T16:47:43Z" "release"="1771346757"org.opencontainers.image.revision=8726709260f051bcc33519b9b82af822eb97f840,org.opencontainers.image.created=2026-02-17T16:47:43Z
# Wed, 18 Feb 2026 19:24:19 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 18 Feb 2026 19:24:19 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 18 Feb 2026 19:24:19 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 18 Feb 2026 19:24:19 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 18 Feb 2026 19:24:19 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Wed, 18 Feb 2026 19:24:19 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Wed, 18 Feb 2026 19:24:19 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 18 Feb 2026 19:24:19 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 18 Feb 2026 19:24:19 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:56b2ec53eb90753f4259bc1fd55c9b03d2aeb15f32351977d3513cdfc735b78c`  
		Last Modified: Tue, 17 Feb 2026 18:40:27 GMT  
		Size: 80.0 MB (79983951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0e2566e698a600e3006bc1049f4c53931f85639044771ff1e146f6704a9f78`  
		Last Modified: Wed, 18 Feb 2026 19:24:35 GMT  
		Size: 56.4 MB (56439708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:5f7a09e1f4a5a5585d3ff52d36a2e82f9e12e81360509305e2fea1358b5ca78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6417794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e251f9632dfeb9dd7d00da7d7a3b3bb3cb12fce65b4b5c20258c0606e9096d9`

```dockerfile
```

-	Layers:
	-	`sha256:f30a32c80815a594977ed46d34faf154ebfccb5a7e6832ca4ac3fcece13532f9`  
		Last Modified: Wed, 18 Feb 2026 19:24:33 GMT  
		Size: 6.4 MB (6406326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7189ec314058b51d3b5130c52897dbcfeaa664f90cd2584c9c5f824d5a8a78a2`  
		Last Modified: Wed, 18 Feb 2026 19:24:32 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:202d5c7dfccae1765a78ba4bf8f3c49c2f4a3f1c0f21095be98550123cf8b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132662951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac62a521985e9798d7eea3fc58df6c4f897827e7a87a4cffe1ad41dc0b8ef42f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 17 Feb 2026 16:49:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:49:45 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 17 Feb 2026 16:49:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:49:48 GMT
COPY dir:fe5bb3dc6233e05c0db4d9e9ac24173fdde10a4e3a3f958ab4e4c567c15fe9fb in /      
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:49:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:08d009316d9d419ba8cfeaa9c1c45c2b75422378e0b92b9f0861e4ba6eb7d7f5 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:49:48 GMT
COPY file:08d009316d9d419ba8cfeaa9c1c45c2b75422378e0b92b9f0861e4ba6eb7d7f5 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:49:49 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8726709260f051bcc33519b9b82af822eb97f840" "org.opencontainers.image.revision"="8726709260f051bcc33519b9b82af822eb97f840" "build-date"="2026-02-17T16:49:28Z" "org.opencontainers.image.created"="2026-02-17T16:49:28Z" "release"="1771346757"org.opencontainers.image.revision=8726709260f051bcc33519b9b82af822eb97f840,org.opencontainers.image.created=2026-02-17T16:49:28Z
# Wed, 18 Feb 2026 19:22:34 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 18 Feb 2026 19:22:34 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 18 Feb 2026 19:22:34 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 18 Feb 2026 19:22:34 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 18 Feb 2026 19:22:34 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Wed, 18 Feb 2026 19:22:34 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Wed, 18 Feb 2026 19:22:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 18 Feb 2026 19:22:34 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 18 Feb 2026 19:22:34 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:b421874d977add29d57baaaa2863eab6b8bab43f7b364a22264ad51b223156a4`  
		Last Modified: Tue, 17 Feb 2026 18:40:36 GMT  
		Size: 77.7 MB (77698505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fb2533ac4cd97c4cf741dd2939d6d8f08126acd7ce47f6f744d7f7ada3ea8b`  
		Last Modified: Wed, 18 Feb 2026 19:22:50 GMT  
		Size: 55.0 MB (54964446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:bd7230003453db8772512bb7873b7d259f66a62af07b400cdf4eacaad1a61251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11805ab59344fd59ae4f05119606ef13e41bd780d3789937d7f8c3253e5ec429`

```dockerfile
```

-	Layers:
	-	`sha256:a05de1eb56ca36fbca34e73cae6e789524e7f75fc0ec1d843aba18ecf19f9768`  
		Last Modified: Wed, 18 Feb 2026 19:22:48 GMT  
		Size: 6.4 MB (6402125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3621368d174b9a1ffbff75489f3d36c227bebb50cbc47f165817ee816ad35f3`  
		Last Modified: Wed, 18 Feb 2026 19:22:48 GMT  
		Size: 11.6 KB (11553 bytes)  
		MIME: application/vnd.in-toto+json
