## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:76abd8c5f934e073503e70be5c2c2ffc656552987de071b98d2002f3d3ac3a94
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
$ docker pull swift@sha256:976c0e9c03eb56f42b3686837c19de5c24b611cc5216971ceeb4bf2575222667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121607899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0906747f8805140d75a3906eb4da527d6635cf6b3e9a2066f51086a4e2ef646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:335ed73bbd571a2d8d265acfbef89aef7685ebe43551753a631835d4fa4a5d82 in / 
# Thu, 06 Jun 2024 15:11:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD multi:061215fe5c3ae072bec6a393d07eed4e23cd262b9ac55be47f1423e9b7a0fa9b in /etc/yum.repos.d/ 
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
ADD file:e9817068e897613d5d39fa1542ce3521ea8895568929673880634bcde722f159 in /root/buildinfo/content_manifests/ubi9-container-9.4-1123.1719560047.json 
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:8af4e5c3d9f50568285a6bcdbaf84d8a90f0dbbf7c170224d357209637fb938f in /root/buildinfo/Dockerfile-ubi9-9.4-1123.1719560047 
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL "release"="1123.1719560047" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-28T07:36:05" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1123.1719560047"
# Thu, 06 Jun 2024 15:11:32 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3231928-93eb2.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:42928cefe51f8d29dc26f18234bb712e5c35d72ca2a8c175b7e4147fcabe9805`  
		Last Modified: Mon, 01 Jul 2024 12:07:19 GMT  
		Size: 77.0 MB (77009884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d33d33762e6b102cbfd4dc36b317363a517b9e950fc4a27574a87a4e2df540`  
		Last Modified: Wed, 24 Jul 2024 09:19:06 GMT  
		Size: 44.6 MB (44598015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:9be404e58e1d2544c09d3de9269b0c9bdf4cdc0a00f0409963d75ae1e2c7ebcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6290564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfc64c84ccf0faaaf7ab2bbab1339cd2240ddffe9fc03f7635bf18ddc1ad743`

```dockerfile
```

-	Layers:
	-	`sha256:d935db89e0983dcddf9b2735837559e9adef3b9026407951b30ce4e72191d4d6`  
		Last Modified: Wed, 24 Jul 2024 09:19:05 GMT  
		Size: 6.3 MB (6278756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace0ac1d603e8f7c4b2bb2f640a0a6c0684a86385c17199a549baa22c6f44f69`  
		Last Modified: Wed, 24 Jul 2024 09:19:05 GMT  
		Size: 11.8 KB (11808 bytes)  
		MIME: application/vnd.in-toto+json
