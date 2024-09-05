## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:56ff0d44d10876843b5bb7f3c7bfb134e71a9d33915ea9dbe54b6be5a816e3c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:a433cb888f1712ed84b65550efd4c3dac371368bbb91ff5e101965187329f218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125729067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09185d19f15a188aff9a1a657e1cb97c541db5a51e992e636b550c2ead4aa9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:01be11a4edc5f73313eef328b5de2912f91dd1c2d7904c06220518690d124b6e in / 
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 06 Jun 2024 15:11:32 GMT
ENV container oci
# Thu, 06 Jun 2024 15:11:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL release=1214
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:49f87467f43dd232d5c4fbe9e85640506af2175999c8f25ba8775bef0f233ac2 in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.json 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:e89c55d504fdde412a9c38a6571496598f8aeb75bd131f90d24edcd177a642a8 in /root/buildinfo/Dockerfile-ubi9-9.4-1214 
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:58:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214"
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:f5e6502d2728ac70bea5ebf27077abc1ccfcc4b6601b93055132a1559bac5151`  
		Last Modified: Wed, 04 Sep 2024 07:10:17 GMT  
		Size: 79.6 MB (79604225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38db811af19844454095782d95740c4e380f994451b7749d1f58b38c74351ce6`  
		Last Modified: Wed, 04 Sep 2024 21:57:43 GMT  
		Size: 46.1 MB (46124842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:1b60bf472ed99b3c5f2db4a918c2c6bbe7763beaca7d6b4bf338fb49bccbf34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6391608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2ed4e3fc0427b7c03912371210af162d77a7eac55f7c94eb81f1e858cab827`

```dockerfile
```

-	Layers:
	-	`sha256:8013d474c9949a398a930efcac95ea0baffd451bb688793e2b2c7e28c0382ab6`  
		Last Modified: Wed, 04 Sep 2024 21:57:42 GMT  
		Size: 6.4 MB (6380087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a0dbe7ca73428b1ac598b56f6c0099dfce65b4869669d11ac729a0fa3f52b3a`  
		Last Modified: Wed, 04 Sep 2024 21:57:41 GMT  
		Size: 11.5 KB (11521 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:89fe8f9abc2235a67442134aa7c52b066cde182b99b961db057bbef1b7fd3a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121967956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f53627c6bc5172d85406fac704d283f26b6eab228d588f7ad89e4f839cf5f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:892c969952ad1930bf02287084976a3c2108e1394deefcd9aa504d553834ca68 in / 
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 06 Jun 2024 15:11:32 GMT
ENV container oci
# Thu, 06 Jun 2024 15:11:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL release=1214
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:33f097a789b5da23a0bb62fef8d2f4a758f4c496eb3348b424ca5f7481ba6beb in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.json 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:c854513bc77aa9582b9f770afd875abf58f5fcc832f116093b9be575a8cc6e8e in /root/buildinfo/Dockerfile-ubi9-9.4-1214 
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:58:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214"
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:5fa3c2b243a50b3675f35932b5f4935ef65e57cddc5d4cc7ba71679269790399`  
		Last Modified: Wed, 04 Sep 2024 07:10:02 GMT  
		Size: 77.4 MB (77359035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7b18443cbed9ddbbc706d96a1da1832e81e18aa94b2c04193448ca476ed2ca`  
		Last Modified: Thu, 05 Sep 2024 03:52:25 GMT  
		Size: 44.6 MB (44608921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:8844d3354009bd48c21032af9ea0780a26a92b5fc928d93902004220455aa3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb301c003ce711baa6a10d373b1d400f7da1a80ef7605dc4e30319811ea2dcf`

```dockerfile
```

-	Layers:
	-	`sha256:f7e4d937f28bbe11c108a3e27a3d0221bb4010f4353852232cb877e558ed3fcb`  
		Last Modified: Thu, 05 Sep 2024 03:52:24 GMT  
		Size: 6.4 MB (6377786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632bb01b387ebec0b61edbb3a686dd40d061cdd4588267084692f227b692c0b4`  
		Last Modified: Thu, 05 Sep 2024 03:52:23 GMT  
		Size: 11.8 KB (11808 bytes)  
		MIME: application/vnd.in-toto+json
