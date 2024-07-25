## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:9f327fec672ab8ca57505a24fcbe7067e7e26fe56a43cff84465328b4a62f954
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:6eb9bca8d2c28e63c48450b137480d392c01b973e2fc25b8b0e7cbc457057056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125533255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bda0bddf982835e5be64ffcf476bd9d03816b5b304a37f974b7bbb5513e7f5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:4273cb3c493137612818aa350c7f43f1dc53be552cdf9f2baeb5969fc5eee49a in / 
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
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
LABEL release=1181
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:af4877a497e904efadfffc12189a7282b22f0759faff72a5076dd6343618969c in /root/buildinfo/content_manifests/ubi9-container-9.4-1181.json 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:932d340d4cb6ac98a446453c39c99fc9ea0e0c62c5755320a5ef85986cf1b2b5 in /root/buildinfo/Dockerfile-ubi9-9.4-1181 
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:47:19" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1181"
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
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
	-	`sha256:cc296d75b61273dcb0db7527435a4c3bd03f7723d89a94d446d3d52849970460`  
		Last Modified: Tue, 23 Jul 2024 23:40:21 GMT  
		Size: 79.4 MB (79428966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d310fce65719ae904e99f0711c108fd6bc8bf593276d7297a2569461b775d0`  
		Last Modified: Wed, 24 Jul 2024 22:59:09 GMT  
		Size: 46.1 MB (46104289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:f587fb89c9f5e7ef80514e5976ec29a4ca0e66e1b9208eb5e9f126950661b34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6293249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f630848a2061ce07e42b5fe6f9f60f6525829eea9ce60c4d91acfe7ea613650`

```dockerfile
```

-	Layers:
	-	`sha256:762efaf58d419b579c0e8ebd308bcd8b837e5e81e98aa06b495591d9ee4c22b7`  
		Last Modified: Wed, 24 Jul 2024 22:59:08 GMT  
		Size: 6.3 MB (6281729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5a1171752569e7a43830582baf566c92296b547e7d6ff9fd3538df6decde88`  
		Last Modified: Wed, 24 Jul 2024 22:59:08 GMT  
		Size: 11.5 KB (11520 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b03b26cf89e44940527f606ba7a634b16f0fba51c5ea38ead2c0e58cafa91908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121765584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1669ec44f2659ca5db2992d1e7580c2c693ebbe30fbb187b42fc9fb8091466`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:6421efd001a2914c5535f9b35c895e111ae089cecaaca9d0e812c570c03a0888 in / 
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
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
LABEL release=1181
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:32d24d55162f3b2e5cec5b52fb9756c98be529a5b377f0cf1e2927121efe2e8f in /root/buildinfo/content_manifests/ubi9-container-9.4-1181.json 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:4ff516e78e08e8a5d01a05e0581ed2a6a43d9668783ca33e115cd2e24bbb5618 in /root/buildinfo/Dockerfile-ubi9-9.4-1181 
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:47:19" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1181"
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
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
	-	`sha256:c6f5847a7d5ebb6d4fe76423af992ea0acefca3cbf204f5e1004116397e1f65e`  
		Last Modified: Wed, 24 Jul 2024 00:08:36 GMT  
		Size: 77.2 MB (77167574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e95316710f85bf3ba4d9aa0a265475bff22c87b5f5fd604681c8a694121a7`  
		Last Modified: Wed, 24 Jul 2024 23:12:08 GMT  
		Size: 44.6 MB (44598010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:acbc477f0751327826e5efb41b9ccd860c929233bd28b5425b2551511340f982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6291237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc98900e5d105675e5123ee0affbe1adb254f7f0348bb6b0f8699e1e6373eff`

```dockerfile
```

-	Layers:
	-	`sha256:a8307819f43315996421090420a68557583c7d90b242078cb682012039572edc`  
		Last Modified: Wed, 24 Jul 2024 23:12:07 GMT  
		Size: 6.3 MB (6279428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfa0a10acfb51306605a2d72c7868d0b89e5df9603a501b4c4bc55d27bdb614`  
		Last Modified: Wed, 24 Jul 2024 23:12:06 GMT  
		Size: 11.8 KB (11809 bytes)  
		MIME: application/vnd.in-toto+json
