## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:3ac10309d508322e5018f3771c80c62977f7e586a7b40facfaa115cd3192c64f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:cc98fa73380d52a5a5d3eeaf568bad41c97c2e76d981e28c946d295469f83d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.7 MB (825682721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c71ba2871215000915dadb9f457c712a669c0b6a67a3255943b9324fa3c6c8f`
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
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:cc296d75b61273dcb0db7527435a4c3bd03f7723d89a94d446d3d52849970460`  
		Last Modified: Tue, 23 Jul 2024 23:40:21 GMT  
		Size: 79.4 MB (79428966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daeeb25e357d18e26fdf093516303336f596fb499f70bafd4ed846a8cc04480`  
		Last Modified: Wed, 24 Jul 2024 23:00:46 GMT  
		Size: 122.8 MB (122759787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc89b4bdacdb7b3c36c7880be0354e09c972bef53218d216901ba139173099cd`  
		Last Modified: Mon, 22 Jul 2024 22:10:13 GMT  
		Size: 623.5 MB (623493795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0884ce35f9960bc1b60fb2c0eda95a83d9429105f99bd22c4fa4ef20a8c79cb7`  
		Last Modified: Wed, 24 Jul 2024 23:00:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:fe51b7924eca259fc69a92cc83d508c8b4cacafaea8c33c1b37175c83367167d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12780873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb6dfb5efa5a86be6f16b27f2f89e32ca773ddc6058c0df8fd45cea3d8ee73c`

```dockerfile
```

-	Layers:
	-	`sha256:8ca8398348193410820230464ea8a74bf43ced83eaaa384c5d3b1d5fcecd4e07`  
		Last Modified: Wed, 24 Jul 2024 23:00:43 GMT  
		Size: 12.8 MB (12766378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a614803e85bcb985ead3c0fc334690cacf227ee0a527be005432b09478385ee`  
		Last Modified: Wed, 24 Jul 2024 23:00:43 GMT  
		Size: 14.5 KB (14495 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:08873eab38abe5c52a02afb2d0f97bc2d62c5b64220bc837efb0048b08bcbbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.4 MB (820425416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e078c2450340689da8f3d461d3cdce1829b7ddc94598fd41ff7f60593b1c6ed`
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
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:42928cefe51f8d29dc26f18234bb712e5c35d72ca2a8c175b7e4147fcabe9805`  
		Last Modified: Mon, 01 Jul 2024 12:07:19 GMT  
		Size: 77.0 MB (77009884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f4b5b564089d70bb45956e77ff1bf19d02172720ea2a910c3c8cea79a19eec`  
		Last Modified: Wed, 24 Jul 2024 09:17:56 GMT  
		Size: 125.7 MB (125730647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a45a45f8c3402fa68c9eb441600db731621950faa44316a68132651b518bff`  
		Last Modified: Wed, 24 Jul 2024 09:18:06 GMT  
		Size: 617.7 MB (617684710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfcf47f203f8fb0b46f32e43461e4b22a3be97470ab141f788c65208e965f59`  
		Last Modified: Wed, 24 Jul 2024 09:17:53 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:1289bd27b61ca3f1f69ae3799f11e5d4fb33222e5375d733d1b125b6a29a8db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12658540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d665df33ffcaaf8c3b0be5c8801477ae7efad69b2dcf41cb634b2a69a3360457`

```dockerfile
```

-	Layers:
	-	`sha256:11bd7f166fbd02fc46f016da51afaf04fb5650c4f9555378c0f661ad6bee51e7`  
		Last Modified: Wed, 24 Jul 2024 09:17:54 GMT  
		Size: 12.6 MB (12643757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cfcd49a87338ace33b1cca6d934807da40e60933bb2de3ffcfd83b43236e9fe`  
		Last Modified: Wed, 24 Jul 2024 09:17:58 GMT  
		Size: 14.8 KB (14783 bytes)  
		MIME: application/vnd.in-toto+json
