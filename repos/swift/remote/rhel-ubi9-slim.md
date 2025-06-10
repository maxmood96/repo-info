## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:0e07f4a4b11a1d8955f3070093cb11a96673454d1eb8c84f10ae8eb94d2e3e5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:e9bf68338c5d93dce35f146e3303ea5f6c531f7085411ecc8b4029cbc657a3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134538167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4d220d6e40806360a7f4cf323b8539bf9ce9500077b7ebc76f6ac36273695b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 28 May 2025 17:53:13 GMT
LABEL url="https://www.redhat.com"
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
COPY dir:7570021887a0f5927849fc20a3596c266eb91c70d742a5af360cefd1fe0436f1 in / 
# Wed, 28 May 2025 17:53:13 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 28 May 2025 17:53:13 GMT
LABEL "build-date"="2025-06-10T08:01:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4534bba8604259ffbc5f2dbf3fd6616b7896d111" "release"="1749542372"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:97971704aef24e8b1129c4f1b2e2241c7800b8bb89a14e77a7efebccd4193661`  
		Last Modified: Tue, 10 Jun 2025 09:17:19 GMT  
		Size: 79.6 MB (79594817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0584b01edcf2528384556a8f961b78f8782294bd877271aeeae9aa16b6628a4`  
		Last Modified: Tue, 10 Jun 2025 17:35:54 GMT  
		Size: 54.9 MB (54943350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:912d154f451e37dfb2bdddea27943b39210790f87d960898668fe01411f1c1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6412480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416bef6450820608ad9249ea39d6553fbe0905b9429e15cb57a4e0119bb16480`

```dockerfile
```

-	Layers:
	-	`sha256:1fabb99e936eda7b06f4e401844b71bf5fce6b901c97d6c00d2bbbaf8ca7239d`  
		Last Modified: Tue, 10 Jun 2025 19:48:43 GMT  
		Size: 6.4 MB (6400981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb7b4bbfe8ce28da4390dacc0cb100bf3278f4b08a65f95bd957189aac409fb`  
		Last Modified: Tue, 10 Jun 2025 19:48:44 GMT  
		Size: 11.5 KB (11499 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3ca127c5c378685dbb74f218c8849f2e0b014aa6ef3d7736cc93854fc53420e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131028664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a037308006bfba48ea82dc818a752e613efd20c3a3214d570913ef2673391`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 28 May 2025 17:53:13 GMT
LABEL url="https://www.redhat.com"
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
COPY dir:95f9966dc31c74b3d4d750c7bff7adb99647bf8873291f41039559c21f99ce61 in / 
# Wed, 28 May 2025 17:53:13 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 28 May 2025 17:53:13 GMT
LABEL "build-date"="2025-06-10T08:05:37" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4534bba8604259ffbc5f2dbf3fd6616b7896d111" "release"="1749542372"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:c0c6f119f250bcd571815218a238bf91fcd968aa4bfe95c224309ec367df747e`  
		Last Modified: Tue, 10 Jun 2025 10:02:06 GMT  
		Size: 77.4 MB (77359481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b35bcd4835b80f966932f3c260159131ef74f29efbb250500fd47ca0db0eb7`  
		Last Modified: Tue, 10 Jun 2025 18:03:08 GMT  
		Size: 53.7 MB (53669183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:5d8337d3ffe98f69209f4c1a98dde67576ef448aafe98671ca930aef9118585e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6408369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3005222a3c7111ff540efd65ba745fea150aac5b5d285e418630011f6d309`

```dockerfile
```

-	Layers:
	-	`sha256:c36b78f1a9d84c2b5bef229f3c54af6ce98dda1f8123b14a7706f114efb2b1a5`  
		Last Modified: Tue, 10 Jun 2025 19:48:51 GMT  
		Size: 6.4 MB (6396784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:408f427532046db72bdc84715fdcca6e9743e0218306936d7634a632af53d845`  
		Last Modified: Tue, 10 Jun 2025 19:48:52 GMT  
		Size: 11.6 KB (11585 bytes)  
		MIME: application/vnd.in-toto+json
