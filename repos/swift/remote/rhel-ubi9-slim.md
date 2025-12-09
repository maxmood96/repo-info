## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:7e1b53d356eac0307bf24ca791cd5526cdd7e66523e72ed80ecd10d94454e8dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:fa74df4e80e9e307f1bca378fe3b62580fd76039968ae9137fb5ca49e1ce8268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136427033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419280cebd41f8f4ca365180942df9f451c205ce7f118d844c174d435acbdd6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 03 Dec 2025 20:39:51 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:53 GMT
COPY dir:e028f696326f03cd7252c4c349f445b8770570e8560a604b425cd138de4f6500 in /      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:53 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:3510fe100acabb01d1f82e20899ef080183d1fa839353ecc75b35a4f9f617700 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:54 GMT
COPY file:3510fe100acabb01d1f82e20899ef080183d1fa839353ecc75b35a4f9f617700 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:54 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "org.opencontainers.image.revision"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "build-date"="2025-12-03T20:39:28Z" "org.opencontainers.image.created"="2025-12-03T20:39:28Z" "release"="1764794285"org.opencontainers.image.revision=6ab6aed6d7cb84504700f3d038e41e8b4b3c3116,org.opencontainers.image.created=2025-12-03T20:39:28Z
# Tue, 09 Dec 2025 17:39:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:39:32 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:39:32 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:39:32 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 09 Dec 2025 17:39:32 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:39:32 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:39:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:32 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:32 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:d9ce76bfbf66102c69a90574796db9749bc7ac51bea111e75112291f6c0326c5`  
		Last Modified: Wed, 03 Dec 2025 21:13:53 GMT  
		Size: 80.0 MB (80040124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41404210a096b43167594222e6025ed358e03732af10739f52f605c69e9bc40a`  
		Last Modified: Tue, 09 Dec 2025 17:39:58 GMT  
		Size: 56.4 MB (56386909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:1560497c8888b7400714d1016e18261c014e6832c57ec2e687df23e900399cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8fc96eb92f5cc8827cc197c54349e02fd7c8a62156ac5a75d2ff3d5148bc1e`

```dockerfile
```

-	Layers:
	-	`sha256:2374ff6ace4f8a63d3f51d33c2ff4e1797467d6fff82b3516fac01f2bb26eb07`  
		Last Modified: Tue, 09 Dec 2025 20:48:57 GMT  
		Size: 6.4 MB (6409564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05ed29740fb911feecce965ae41370202b8fbd741991b676a92d70b0b4c0529`  
		Last Modified: Tue, 09 Dec 2025 20:48:58 GMT  
		Size: 11.5 KB (11467 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:7b34674371f5da5050749820f1b92284efa4eb222be0bb565cb16d983725ee49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132648593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1aea709e83fa4d387172eab38138f227450c5e46cfb905d90f1d3b3a42d4009`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 03 Dec 2025 20:44:54 GMT
ENV container oci
# Wed, 03 Dec 2025 20:44:57 GMT
COPY dir:eb9bf5494000bc25c9b7b9c079b1fafa2372042b89728acc56982ccb84aecd0f in /      
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:44:57 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:44:58 GMT
COPY file:f4709671a5a80ff0d54c4f0107ef89c6244ef4daa403ef182c946f77eda0aa0f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:44:58 GMT
COPY file:f4709671a5a80ff0d54c4f0107ef89c6244ef4daa403ef182c946f77eda0aa0f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:44:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "org.opencontainers.image.revision"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "build-date"="2025-12-03T20:44:35Z" "org.opencontainers.image.created"="2025-12-03T20:44:35Z" "release"="1764794285"org.opencontainers.image.revision=6ab6aed6d7cb84504700f3d038e41e8b4b3c3116,org.opencontainers.image.created=2025-12-03T20:44:35Z
# Tue, 09 Dec 2025 17:39:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:39:43 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:39:43 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:39:43 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 09 Dec 2025 17:39:43 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:39:43 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:39:43 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:43 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:43 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:04818a5cef267e6e003591a4574d021a2141ec6ef8efc36216cf70aac950e30b`  
		Last Modified: Wed, 03 Dec 2025 21:16:16 GMT  
		Size: 77.7 MB (77711266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7638feeb8cf9d2912ef313f5720775e525f6a502053748841ff0980c18f1f47`  
		Last Modified: Tue, 09 Dec 2025 17:40:12 GMT  
		Size: 54.9 MB (54937327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:f3262a04cd758741c9121a4ef2d56a5d18a8fd6f68994fff899357d8c2fe136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81e3999c808730ae038304a3562c572a89796a43428fa504869444fe68059d2`

```dockerfile
```

-	Layers:
	-	`sha256:1f0d4d8f1173ebed4f608c545dec99d91fa1e9916049516817f8cb02d7e42148`  
		Last Modified: Tue, 09 Dec 2025 20:49:14 GMT  
		Size: 6.4 MB (6405367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9bfcb9cf0722c4c0302da34d1498eace56f5e01a4f78f2736036ffb5b186c7b`  
		Last Modified: Tue, 09 Dec 2025 20:49:14 GMT  
		Size: 11.6 KB (11554 bytes)  
		MIME: application/vnd.in-toto+json
