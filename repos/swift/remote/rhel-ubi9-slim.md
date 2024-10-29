## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:2d45c79f616574257170ab9eb49ecd5fd6a60c125ea97a598ce0a9685e481115
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:094380638800a6b278b739e5add016679fc5bf8df7ac8434b5377b3ecdccb0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148649410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa0ffd87aa587c622612dad46ba3aa2cd49ff0c85fe5d1d2e5ef32d9af155f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:e440e2e895b3a66881097278a06892dd875b1bc7072257b72ae2504ac0c49f1c in / 
# Wed, 25 Sep 2024 05:07:02 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 25 Sep 2024 05:07:02 GMT
ADD multi:7667a8c78bcd0d2f5fc0f3a30636b6cc467f1598bc123dd6bb6df338d6af61b2 in /etc/yum.repos.d/ 
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 25 Sep 2024 05:07:02 GMT
ENV container oci
# Wed, 25 Sep 2024 05:07:02 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Sep 2024 05:07:02 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
RUN rm -rf /var/log/*
# Wed, 25 Sep 2024 05:07:02 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:a3a9d84d530a03761c99ebb86fad28353a6fefb3788ecb2efcd893258425b1f7 in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1729773476.json 
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:2569396c709099fb9a7bcc960974a77b96c3f8b8081c5bd2c6eca79a275afbd4 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1729773476 
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL "release"="1214.1729773476" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-10-24T12:46:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1729773476"
# Wed, 25 Sep 2024 05:07:02 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3606863-5170f.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 25 Sep 2024 05:07:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 25 Sep 2024 05:07:02 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:a20d5f0bec2bce34d8adb0eb98f3536f214c292b20c6cf1a3a46c802662d912b`  
		Last Modified: Mon, 28 Oct 2024 02:25:04 GMT  
		Size: 79.7 MB (79685624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2caa77d9bb70f9ce992902332899a48ea79405b27f841acf1d01d1fb39fc64`  
		Last Modified: Mon, 28 Oct 2024 18:57:49 GMT  
		Size: 69.0 MB (68963786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:5fb0f035628f40c82573cd73ddcc5106ba71f9f93be01f76f2ccbe6c9ae2a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6391617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cba7b46b5c2d0a59678587961e16752a26e086fce687af6b5c29adc34c66b5`

```dockerfile
```

-	Layers:
	-	`sha256:c5d37d577bc8fd6c080dea92873280f21d22317c9c328e2668227706bda41c2e`  
		Last Modified: Mon, 28 Oct 2024 18:57:48 GMT  
		Size: 6.4 MB (6380107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6221f9cbb627440fce79001a4a3c7b8506205cb6e772ee04b2ffbfcfd5bc6c80`  
		Last Modified: Mon, 28 Oct 2024 18:57:47 GMT  
		Size: 11.5 KB (11510 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:0bb4e2138e609687089821f730179d4da829886f7e1caccc574a44e3f40660c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145201546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1531e920eeb5f3a73dd04ee015a4f09d3e5e37b3a4ad78c65adc17fc5e0baa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:3def11aa7049be971d277735f8f093f625faba74b902c57aa70c6c97b33f7114 in / 
# Wed, 25 Sep 2024 05:07:02 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 25 Sep 2024 05:07:02 GMT
ADD multi:7667a8c78bcd0d2f5fc0f3a30636b6cc467f1598bc123dd6bb6df338d6af61b2 in /etc/yum.repos.d/ 
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 25 Sep 2024 05:07:02 GMT
ENV container oci
# Wed, 25 Sep 2024 05:07:02 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Sep 2024 05:07:02 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
RUN rm -rf /var/log/*
# Wed, 25 Sep 2024 05:07:02 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:6c28f3d79976a4be283478442eee5845e61cd469e19b0e37cf3520cac74a0e56 in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1729773476.json 
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:e2ff9f74efa0c1bbf337298182594ba1f2ad863058666d8cd6203320cd0af6d9 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1729773476 
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL "release"="1214.1729773476" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-10-24T12:46:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1729773476"
# Wed, 25 Sep 2024 05:07:02 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3606863-5170f.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 25 Sep 2024 05:07:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 25 Sep 2024 05:07:02 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:2f96caed8c701f83533a430c874ce02b0e27edfea8aa57e7e82a60a6b2fba09d`  
		Last Modified: Mon, 28 Oct 2024 02:25:03 GMT  
		Size: 77.3 MB (77335334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92658b242d8093c0d49ec6619c62bbac6f814a0f6a6d51fbfde69a08cfb6f6c`  
		Last Modified: Mon, 28 Oct 2024 19:01:02 GMT  
		Size: 67.9 MB (67866212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:f65b90b6ba9eee6e6e0a99a8943a268de90d9af265dc212769af04bf9a46a4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c22f3cb4b811f44bdb5927a7e21d80e6753c5433982fb950752b9e9294042ef`

```dockerfile
```

-	Layers:
	-	`sha256:dd01c8205702502ee53d982a9854ef034385dc46497b461cef536086b1e62469`  
		Last Modified: Mon, 28 Oct 2024 19:01:00 GMT  
		Size: 6.4 MB (6377806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60be8ba764b8e0569dd46113f71cfe91a2e97b95cb98d2a7fd5ba1e5e6d0428a`  
		Last Modified: Mon, 28 Oct 2024 19:01:00 GMT  
		Size: 11.6 KB (11597 bytes)  
		MIME: application/vnd.in-toto+json
