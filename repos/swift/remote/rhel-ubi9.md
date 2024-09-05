## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:953e5e3575fec10d481f3c30f0be2facb0957aa83118c2907a91a61501ec4375
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:103bf63c29ee07b78256363a663267e42ca8c628de27ad8e75997eaca6812c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.8 MB (825841455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fddd2c89253cdc31b6e4accacc9332119aa6315dde44a9bc64e9ccec115d28ed`
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
	-	`sha256:f5e6502d2728ac70bea5ebf27077abc1ccfcc4b6601b93055132a1559bac5151`  
		Last Modified: Wed, 04 Sep 2024 07:10:17 GMT  
		Size: 79.6 MB (79604225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f70fc22733abf269cc872c37342ff14ee9eb2ea1a8f3876f715cca937f7311`  
		Last Modified: Wed, 04 Sep 2024 21:59:08 GMT  
		Size: 122.7 MB (122743262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc89b4bdacdb7b3c36c7880be0354e09c972bef53218d216901ba139173099cd`  
		Last Modified: Mon, 22 Jul 2024 22:10:13 GMT  
		Size: 623.5 MB (623493795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41f71e18ea54594d0aa2c0fe6c3cf6123371204c27eea67952a100d03ed6c51`  
		Last Modified: Wed, 04 Sep 2024 21:59:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:0f3758242e9d08697a58d147d9f933be6b780bb2190fda804e2a7ab4779663b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12879235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f4177e91e8aad68d41a7c71a0b3009348c883df0de37669c799a86232e9ae3`

```dockerfile
```

-	Layers:
	-	`sha256:d3b9a07c9221ac6761cb085fa87ab63bdd4945a65b6c4aad274c12d130c1ac99`  
		Last Modified: Wed, 04 Sep 2024 21:59:06 GMT  
		Size: 12.9 MB (12864740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060eac5f25a6b5689d0a208049d31bcb73d2c955985090f58120fd2b8de0843a`  
		Last Modified: Wed, 04 Sep 2024 21:59:05 GMT  
		Size: 14.5 KB (14495 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:494ee1d3d24ad06eaf3c79054e13fea251e0790f18720722aae35beec91d7ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **811.9 MB (811949442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba75fdef2773863c0f9bc5dd2178297fadffffa1921b6340048b809cd03007a1`
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
	-	`sha256:5fa3c2b243a50b3675f35932b5f4935ef65e57cddc5d4cc7ba71679269790399`  
		Last Modified: Wed, 04 Sep 2024 07:10:02 GMT  
		Size: 77.4 MB (77359035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf536604e0b164c8109df29c069b47db5d3b19da4d5fba7b157b82099e7fe37`  
		Last Modified: Thu, 05 Sep 2024 03:51:31 GMT  
		Size: 116.9 MB (116905523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a45a45f8c3402fa68c9eb441600db731621950faa44316a68132651b518bff`  
		Last Modified: Wed, 24 Jul 2024 09:18:06 GMT  
		Size: 617.7 MB (617684710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af968ddbe5d5e2d495faaa6dd71f46ce1a2d91725b0d926f9e9248371611f10`  
		Last Modified: Thu, 05 Sep 2024 03:51:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:fd8f309c187e5ed417dfca9cb8f2b5efe4cca2afcbb0a8be2340b76996934de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12754410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771c1ce03736df22da1cb6ca89bc0667137640c318d322b4becab41a1a24b06f`

```dockerfile
```

-	Layers:
	-	`sha256:31da2a043ed73114e86818d28d0510b083ade86282721d2539849d83b9a772f6`  
		Last Modified: Thu, 05 Sep 2024 03:51:29 GMT  
		Size: 12.7 MB (12739627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef161fad35bb983323195d77443047b0e8591e765a43b515f7a841b444f60fb5`  
		Last Modified: Thu, 05 Sep 2024 03:51:28 GMT  
		Size: 14.8 KB (14783 bytes)  
		MIME: application/vnd.in-toto+json
