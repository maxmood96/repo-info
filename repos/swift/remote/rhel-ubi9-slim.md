## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:09121a54303a85e2d90324aac3940821d35536b18ec6657dbfa4f3079f79b7e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:00b2b0944174156b1f2326ec6c02b0adb7aa1a4e6a18051601e8479bc0db9fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148557392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb99fb17885aa490c3753d819bef6277bd76d7a967df4e8d5dbd0e4d565ee23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:0067eb9f2ee25ab2d666a7639a85fe707b582902a09242761abf30c53664069b in / 
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 17 Sep 2024 00:51:42 GMT
ADD multi:7a67822d03b1a3ddb205cc3fcf7acd9d3180aef5988a5d25887bc0753a7a493b in /etc/yum.repos.d/ 
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 17 Sep 2024 00:51:42 GMT
ENV container oci
# Tue, 17 Sep 2024 00:51:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 00:51:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -rf /var/log/*
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mkdir -p /var/log/rhsm
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:ed34e436a5c2cc729eecd8b15b94c75028aea1cb18b739cafbb293b5e4ad5dae in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1726694543.json 
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:d56bb1961538221b52d7e292418978f186bf67b9906771f38530fc3996a9d0d4 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1726694543 
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL "release"="1214.1726694543" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:30" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1726694543"
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496925-3b364.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:40049f9dc50417693bf704b63a02d64347b23867b33ac7776be3fae4a2d178b0`  
		Last Modified: Mon, 23 Sep 2024 14:28:12 GMT  
		Size: 79.6 MB (79592786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eaf2e03215a4d178ec345a90813fbf096c170211254d7bb62ea5edb1295d2f`  
		Last Modified: Tue, 24 Sep 2024 01:01:04 GMT  
		Size: 69.0 MB (68964606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:a49cca5a7756c320101ff1a0d5a942f21b7d8b2eb78f831f81984a505168d5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 KB (11250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e66e9047cf0e95289506a87dbc0a7604f32d2dfb93b123d48aee9b20bca6ae`

```dockerfile
```

-	Layers:
	-	`sha256:6755a5bae949979dd532c524cf0ef66d6c939ef820e96eb3462b6deaf1495da7`  
		Last Modified: Tue, 24 Sep 2024 01:01:02 GMT  
		Size: 11.2 KB (11250 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:e432593aa45c76d551ad5e8dafb6116609e3c711e07cc8c5f610b2ee20924265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145216799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c20315e558904e90445129108dff6c81e40f87760fda995f320971c76b0411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:d6101aaaa0ea140d84b6346291651ad4d2bce8c444478e1fc83508b02136ec0f in / 
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 17 Sep 2024 00:51:42 GMT
ADD multi:7a67822d03b1a3ddb205cc3fcf7acd9d3180aef5988a5d25887bc0753a7a493b in /etc/yum.repos.d/ 
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 17 Sep 2024 00:51:42 GMT
ENV container oci
# Tue, 17 Sep 2024 00:51:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Sep 2024 00:51:42 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -rf /var/log/*
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mkdir -p /var/log/rhsm
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:6744b3d23896832934836f8b77190150a7f9f836065a064436c5b9dc47a95425 in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1726694543.json 
# Tue, 17 Sep 2024 00:51:42 GMT
ADD file:19c58e8e8129cd749e0ec129d64db36f9eb2b3729bc034e6755ab07ad478a419 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1726694543 
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL "release"="1214.1726694543" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:30" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1726694543"
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496925-3b364.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Tue, 17 Sep 2024 00:51:42 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 17 Sep 2024 00:51:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:642dd3de0a7ba3fef28a56da54f6c6b620e3bdff1c55b20751a3029bea383326`  
		Last Modified: Mon, 23 Sep 2024 14:28:14 GMT  
		Size: 77.4 MB (77352301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda45f8bac855282e5fd4771b408cade6f87c0d86ef29b5e112adbc7af9417c3`  
		Last Modified: Tue, 24 Sep 2024 01:30:43 GMT  
		Size: 67.9 MB (67864498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d919dc4108f85a80548376399aa43d2490f2f786c7b2adcecba96fb2a26a7f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4cc4483e12e74b543d9cbc6686a31faceaf7aff96919d4012435dfbe07295a`

```dockerfile
```

-	Layers:
	-	`sha256:a826f9b44a980a4a813940b5a1cfb8abe4a683c420c4e055c28245ee1af8205e`  
		Last Modified: Tue, 24 Sep 2024 01:30:41 GMT  
		Size: 6.4 MB (6377806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b86d92624f16d80fc9d830b52319397864c2f05d9ed7a628eaafb2b846ae87`  
		Last Modified: Tue, 24 Sep 2024 01:30:40 GMT  
		Size: 11.8 KB (11757 bytes)  
		MIME: application/vnd.in-toto+json
