## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:b538eb735814166aa86ea191f8a3e4be237cf43040a879b37ef01dfd6d13e041
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:da5a4d91dd97b4090a3ba2e0361eb48bc7ba7a81e6487a46c6604b97b759c85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137604922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58752b9a50a23c9983816fe7514313cb782cba600770e6f77ffe6e7297411239`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Mar 2026 05:17:59 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Mar 2026 05:18:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 25 Mar 2026 05:18:00 GMT
LABEL io.openshift.expose-services=""
# Wed, 25 Mar 2026 05:18:00 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 25 Mar 2026 05:18:00 GMT
ENV container oci
# Wed, 25 Mar 2026 05:18:01 GMT
COPY dir:5f42172b9bd80150725c18296732df201c1f7ba4225c031a0e4175eb57c8aaf7 in /      
# Wed, 25 Mar 2026 05:18:01 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 25 Mar 2026 05:18:01 GMT
CMD ["/bin/bash"]
# Wed, 25 Mar 2026 05:18:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 25 Mar 2026 05:18:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 25 Mar 2026 05:18:02 GMT
COPY file:d3c056c2cffb5ef231b335663d74f1a5511def9489d289f0fbddc2b79453f000 in /usr/share/buildinfo/labels.json      
# Wed, 25 Mar 2026 05:18:02 GMT
COPY file:d3c056c2cffb5ef231b335663d74f1a5511def9489d289f0fbddc2b79453f000 in /root/buildinfo/labels.json      
# Wed, 25 Mar 2026 05:18:03 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="07b654b5754308740ae2e8c2adde29678c5e9667" "org.opencontainers.image.revision"="07b654b5754308740ae2e8c2adde29678c5e9667" "build-date"="2026-03-25T05:17:41Z" "org.opencontainers.image.created"="2026-03-25T05:17:41Z" "release"="1774415752"org.opencontainers.image.revision=07b654b5754308740ae2e8c2adde29678c5e9667,org.opencontainers.image.created=2026-03-25T05:17:41Z
# Wed, 25 Mar 2026 17:48:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Mar 2026 17:48:33 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Mar 2026 17:48:33 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Mar 2026 17:48:33 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Mar 2026 17:48:33 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 25 Mar 2026 17:48:33 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 25 Mar 2026 17:48:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Mar 2026 17:48:33 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Mar 2026 17:48:33 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:96cadc7a5c0105296da36547c7820a31a86ff861ec8f67526bcb80a161a0523f`  
		Last Modified: Wed, 25 Mar 2026 06:43:26 GMT  
		Size: 80.0 MB (79965699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e537002c000d154e9396d7636f16199253e6fc6d50f3948d931b385707ab3b`  
		Last Modified: Wed, 25 Mar 2026 17:49:16 GMT  
		Size: 57.6 MB (57639223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:7005fd0c2c26e4a409211dbe029f7a94d2bc75dc9274c7e758fd0974dea1f13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6417812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeed01ef7f92b48fa35ccfccc4ed5586ef278e1f5b2e4baaf214a5c24eb7e845`

```dockerfile
```

-	Layers:
	-	`sha256:b3e5f6a05c10b40602dc1a2262a6ebfbcad5663f46306f956185e59281cb8ace`  
		Last Modified: Wed, 25 Mar 2026 17:49:14 GMT  
		Size: 6.4 MB (6406352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4171377ba0c2957b133154a664e534a44ea47150fc59bf8dd863b5964d519f6f`  
		Last Modified: Wed, 25 Mar 2026 17:49:13 GMT  
		Size: 11.5 KB (11460 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:00af288d56990b498155e9bb22cc88e63b7f323bb489914b2c46273f956223c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133772046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3faebab47ab74284ddd32747c4333295549cf305e137bc962356fb66625dd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 25 Mar 2026 05:21:01 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 25 Mar 2026 05:21:01 GMT
ENV container oci
# Wed, 25 Mar 2026 05:21:05 GMT
COPY dir:e508066e907da1d4d6c6186e42de70836eb08907574181ae07dba9e0203c8a59 in /      
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 25 Mar 2026 05:21:05 GMT
CMD ["/bin/bash"]
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:899533d1478875a4f4ed147cd383f908cdf9d76e471c24d3caeca5b7c9c91d8c in /usr/share/buildinfo/labels.json      
# Wed, 25 Mar 2026 05:21:05 GMT
COPY file:899533d1478875a4f4ed147cd383f908cdf9d76e471c24d3caeca5b7c9c91d8c in /root/buildinfo/labels.json      
# Wed, 25 Mar 2026 05:21:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="07b654b5754308740ae2e8c2adde29678c5e9667" "org.opencontainers.image.revision"="07b654b5754308740ae2e8c2adde29678c5e9667" "build-date"="2026-03-25T05:20:44Z" "org.opencontainers.image.created"="2026-03-25T05:20:44Z" "release"="1774415752"org.opencontainers.image.revision=07b654b5754308740ae2e8c2adde29678c5e9667,org.opencontainers.image.created=2026-03-25T05:20:44Z
# Wed, 25 Mar 2026 17:49:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Mar 2026 17:49:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Mar 2026 17:49:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Mar 2026 17:49:13 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Mar 2026 17:49:13 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 25 Mar 2026 17:49:13 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 25 Mar 2026 17:49:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Mar 2026 17:49:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Mar 2026 17:49:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:2dba26dca7a080db23ce08a57a530936de117c1ae8824a001d239e6b578a5db0`  
		Last Modified: Wed, 25 Mar 2026 06:37:37 GMT  
		Size: 77.7 MB (77729981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9a588f7881f240fd605e9f05a15879e88e21ba531954e1342bc9a802104709`  
		Last Modified: Wed, 25 Mar 2026 17:49:39 GMT  
		Size: 56.0 MB (56042065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:1daf7ecee59d06d2eaf243771ef00e7aaa209f13765038e093e69a3e3577386a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3623afc0811c5435c0d0a640c06b66af5a53137f957bac0171fb1506d45b98bf`

```dockerfile
```

-	Layers:
	-	`sha256:b624b6bce4d219b7cdab1c6377e65c683622f00a2ffa398488da68745f2bc173`  
		Last Modified: Wed, 25 Mar 2026 17:49:37 GMT  
		Size: 6.4 MB (6402151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f248df5fa8e57bd37a26b91e6d36441f5622517ffb14a8eede72bbdc5a3cdab`  
		Last Modified: Wed, 25 Mar 2026 17:49:36 GMT  
		Size: 11.5 KB (11546 bytes)  
		MIME: application/vnd.in-toto+json
