## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:3da2c7c7ad943a30c5efeeb17a75b252f164bf3818100053490b404b5dc65184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:8e67cb856080c4d80055208d6ebb54bcfcef0e0f1b7088e082dfca27b64eced2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1033565038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68728fa306bfabfd2269d7ca1ddb4319f873256f2fb6427dcac2bc481c90ffe5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 24 Oct 2024 12:58:55 GMT
ADD file:e440e2e895b3a66881097278a06892dd875b1bc7072257b72ae2504ac0c49f1c in / 
# Thu, 24 Oct 2024 12:59:10 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 24 Oct 2024 12:59:10 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 24 Oct 2024 12:59:11 GMT
ADD multi:7667a8c78bcd0d2f5fc0f3a30636b6cc467f1598bc123dd6bb6df338d6af61b2 in /etc/yum.repos.d/ 
# Thu, 24 Oct 2024 12:59:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 24 Oct 2024 12:59:11 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 24 Oct 2024 12:59:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 24 Oct 2024 12:59:11 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 24 Oct 2024 12:59:11 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 24 Oct 2024 12:59:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 24 Oct 2024 12:59:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 24 Oct 2024 12:59:11 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 24 Oct 2024 12:59:11 GMT
ENV container oci
# Thu, 24 Oct 2024 12:59:11 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 12:59:11 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 12:59:12 GMT
RUN rm -rf /var/log/*
# Thu, 24 Oct 2024 12:59:13 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 24 Oct 2024 12:59:13 GMT
ADD file:a3a9d84d530a03761c99ebb86fad28353a6fefb3788ecb2efcd893258425b1f7 in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1729773476.json 
# Thu, 24 Oct 2024 12:59:14 GMT
ADD file:2569396c709099fb9a7bcc960974a77b96c3f8b8081c5bd2c6eca79a275afbd4 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1729773476 
# Thu, 24 Oct 2024 12:59:14 GMT
LABEL "release"="1214.1729773476" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-10-24T12:46:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1729773476"
# Thu, 24 Oct 2024 12:59:15 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3606863-5170f.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 24 Oct 2024 12:59:15 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 24 Oct 2024 12:59:19 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:a20d5f0bec2bce34d8adb0eb98f3536f214c292b20c6cf1a3a46c802662d912b`  
		Last Modified: Mon, 28 Oct 2024 02:25:04 GMT  
		Size: 79.7 MB (79685624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705e681e6c070ad11253b12ccc33801d0f9a2ca9d951d742898ff8db66d463cc`  
		Last Modified: Mon, 28 Oct 2024 21:00:26 GMT  
		Size: 122.7 MB (122676332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a600617c8630172f35fb08c8c402eafa9019f718ebae9b539beb1c780e6fa293`  
		Last Modified: Mon, 28 Oct 2024 21:00:38 GMT  
		Size: 831.2 MB (831202908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5438c6bea3ee70f8528e1df4048ee9f9089afec7ebfdfa1e3ac05a8fdbf641`  
		Last Modified: Mon, 28 Oct 2024 21:00:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:1f4c54d0b4949e0443e93f7f5735591ab71a3e94f5dd6a871106deb05f5ad9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12879356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34da6b4e04031008fcec7712e006871208c8413f1d67cd2e4bf151ddf6ccf90a`

```dockerfile
```

-	Layers:
	-	`sha256:73ce1da61ccea04c2f0267778a5bd1c37c1fe9e7990e15baba7df51861e65753`  
		Last Modified: Mon, 28 Oct 2024 21:00:24 GMT  
		Size: 12.9 MB (12864874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f689b762e838bd8e43cdfe3e825d7eb5db0f641ce7d7c3a835860ca03ffac336`  
		Last Modified: Mon, 28 Oct 2024 21:00:23 GMT  
		Size: 14.5 KB (14482 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d30fbba0bad57db9e0e235ef807d560e6b5b3286f6cf470bde9b36519d8fcb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1021607979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dffeca7ae99dcf4118f4c243dd2b3864fa17cbaf0573c7d276b1675fa6d27a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 24 Oct 2024 12:58:51 GMT
ADD file:3def11aa7049be971d277735f8f093f625faba74b902c57aa70c6c97b33f7114 in / 
# Thu, 24 Oct 2024 12:58:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 24 Oct 2024 12:58:53 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 24 Oct 2024 12:58:53 GMT
ADD multi:7667a8c78bcd0d2f5fc0f3a30636b6cc467f1598bc123dd6bb6df338d6af61b2 in /etc/yum.repos.d/ 
# Thu, 24 Oct 2024 12:58:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 24 Oct 2024 12:58:53 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 24 Oct 2024 12:58:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 24 Oct 2024 12:58:53 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 24 Oct 2024 12:58:53 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 24 Oct 2024 12:58:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 24 Oct 2024 12:58:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 24 Oct 2024 12:58:53 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 24 Oct 2024 12:58:53 GMT
ENV container oci
# Thu, 24 Oct 2024 12:58:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Oct 2024 12:58:53 GMT
CMD ["/bin/bash"]
# Thu, 24 Oct 2024 12:58:55 GMT
RUN rm -rf /var/log/*
# Thu, 24 Oct 2024 12:58:57 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 24 Oct 2024 12:58:57 GMT
ADD file:6c28f3d79976a4be283478442eee5845e61cd469e19b0e37cf3520cac74a0e56 in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1729773476.json 
# Thu, 24 Oct 2024 12:58:57 GMT
ADD file:e2ff9f74efa0c1bbf337298182594ba1f2ad863058666d8cd6203320cd0af6d9 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1729773476 
# Thu, 24 Oct 2024 12:58:57 GMT
LABEL "release"="1214.1729773476" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-10-24T12:46:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1729773476"
# Thu, 24 Oct 2024 12:58:59 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3606863-5170f.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 24 Oct 2024 12:59:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 24 Oct 2024 12:59:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2f96caed8c701f83533a430c874ce02b0e27edfea8aa57e7e82a60a6b2fba09d`  
		Last Modified: Mon, 28 Oct 2024 02:25:03 GMT  
		Size: 77.3 MB (77335334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0af817f0505acb11e540b5fa4e9ed69cc9894c5cd63809fe889a8c00083aea`  
		Last Modified: Mon, 28 Oct 2024 18:59:47 GMT  
		Size: 116.8 MB (116814730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1accd7a96b5a62a6a22740ccfb38fd3d7f802819b1376d3f51febf07abd9d48d`  
		Last Modified: Mon, 28 Oct 2024 21:35:05 GMT  
		Size: 827.5 MB (827457743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf72432cd9d630a288b37b298eaf3570e802fe375342cdd8d6df9d752b6c82`  
		Last Modified: Mon, 28 Oct 2024 21:34:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:b9dfd03708297a24ae89790450e65edba47fe921a7fd39611069573da97e6d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12754360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8711efafae925ce49ff14753bf2c0283e359c4000f00b3ebdd0a618fd5bceafc`

```dockerfile
```

-	Layers:
	-	`sha256:30aa86613fce1b89b62ba0f197b39f6f922020e36eb6c878d7354228dac925d5`  
		Last Modified: Mon, 28 Oct 2024 21:34:49 GMT  
		Size: 12.7 MB (12739761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59373822dffdacdd8a580fb2b907dbfb11f2265face06673d65cf809b118035f`  
		Last Modified: Mon, 28 Oct 2024 21:34:48 GMT  
		Size: 14.6 KB (14599 bytes)  
		MIME: application/vnd.in-toto+json
