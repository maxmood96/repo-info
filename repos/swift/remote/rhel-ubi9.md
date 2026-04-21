## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:1c39793227318e6a9183383448ceb28963a5d501ebf11655bf1aad0c6c29f730
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:3f645847d523efcb1a187ac5b85f659ad9bf358fe73225e241aa55c53d568c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1288705779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d25fcf81b29e5f074bc30c1be4ff9bdab220fec0714a9d9270236fc467d918f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 20 Apr 2026 00:48:25 GMT
ENV container oci
# Mon, 20 Apr 2026 00:48:27 GMT
COPY dir:9a0cfc741c4cab249eaab8224f70bdd207359932aecdce6446b4832d7b8792d0 in /      
# Mon, 20 Apr 2026 00:48:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:48:27 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:48:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:48:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:48:27 GMT
COPY file:d5b433accc161e9a86825930ccaf382f8a415a8a3931575cace27dfa463177f8 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:28 GMT
COPY file:d5b433accc161e9a86825930ccaf382f8a415a8a3931575cace27dfa463177f8 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ddae96bb8cf093c58e0392070f5d0f6636e3415" "org.opencontainers.image.revision"="3ddae96bb8cf093c58e0392070f5d0f6636e3415" "build-date"="2026-04-20T00:48:09Z" "org.opencontainers.image.created"="2026-04-20T00:48:09Z" "release"="1776645994"org.opencontainers.image.revision=3ddae96bb8cf093c58e0392070f5d0f6636e3415,org.opencontainers.image.created=2026-04-20T00:48:09Z
# Mon, 20 Apr 2026 23:09:38 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 20 Apr 2026 23:09:38 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 20 Apr 2026 23:09:38 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Mon, 20 Apr 2026 23:09:38 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 20 Apr 2026 23:09:38 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 20 Apr 2026 23:09:38 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 20 Apr 2026 23:09:38 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 20 Apr 2026 23:09:38 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 23:09:38 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 23:10:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 20 Apr 2026 23:10:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b6465ca781aee78355d6e3fb79fcf2437d6666324b86768319788e1dd559c04e`  
		Last Modified: Mon, 20 Apr 2026 08:04:32 GMT  
		Size: 80.0 MB (79950683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae7f1165462ea01331304a5b1dbd1e9d2046c68e2969885da2939d5183d9db9`  
		Last Modified: Mon, 20 Apr 2026 23:12:23 GMT  
		Size: 124.7 MB (124705578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f7355d20d694d145fbf4688c63a728cb08f4edbff524635d4047a4f954daba`  
		Last Modified: Mon, 20 Apr 2026 21:56:34 GMT  
		Size: 1.1 GB (1084049344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376bcf44ec66da475eda433f51225ee9698939d6ad0f61b21e7ce5a9f7e799a3`  
		Last Modified: Mon, 20 Apr 2026 23:12:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:45b075dcb00f9e78d1861b9f7afcf0e435af8358df088cbeb4ddf15f5620e175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b300c94d990acad146718e0ce42d3beb998fe66a9e6df04d2ec6feb553404164`

```dockerfile
```

-	Layers:
	-	`sha256:fb68ca9b2562fa09321d16d5b6dcba8915c37712e08e8c343530b4e15c328083`  
		Last Modified: Mon, 20 Apr 2026 23:12:20 GMT  
		Size: 13.0 MB (12985046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c6412e899c661958ffad53eb0ba170260cfa23a0bf1918be585141412ef2328`  
		Last Modified: Mon, 20 Apr 2026 23:12:19 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:9657a50506d2f192d2271a2b4043a3d4f39e1a5ad9268d0f7b1f18aff40ac620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276177497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cddfd92664632204d45141cc83e35fef19dd473534b5792747e5f84afedec96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 00:51:19 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:51:20 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 20 Apr 2026 00:51:20 GMT
ENV container oci
# Mon, 20 Apr 2026 00:51:23 GMT
COPY dir:cde882f56692443b8b10e5db02754fa9362dc55fd06b3bf318b168934d22c801 in /      
# Mon, 20 Apr 2026 00:51:23 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:51:23 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:51:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:51:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:51:23 GMT
COPY file:321db79fe465208667177f293fdd0585a314bddde8a52d9c1dd063598a1c04c3 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:51:23 GMT
COPY file:321db79fe465208667177f293fdd0585a314bddde8a52d9c1dd063598a1c04c3 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:51:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ddae96bb8cf093c58e0392070f5d0f6636e3415" "org.opencontainers.image.revision"="3ddae96bb8cf093c58e0392070f5d0f6636e3415" "build-date"="2026-04-20T00:51:03Z" "org.opencontainers.image.created"="2026-04-20T00:51:03Z" "release"="1776645994"org.opencontainers.image.revision=3ddae96bb8cf093c58e0392070f5d0f6636e3415,org.opencontainers.image.created=2026-04-20T00:51:03Z
# Mon, 20 Apr 2026 23:07:14 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 20 Apr 2026 23:07:14 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 20 Apr 2026 23:07:14 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Mon, 20 Apr 2026 23:07:14 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 20 Apr 2026 23:07:14 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 20 Apr 2026 23:07:14 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 20 Apr 2026 23:07:14 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 20 Apr 2026 23:07:14 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 23:07:14 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 23:07:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 20 Apr 2026 23:07:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:8f4b560eefb627e9afb5c032d69667ab64e59a4479469073f60eb5ae3940e874`  
		Last Modified: Mon, 20 Apr 2026 08:05:05 GMT  
		Size: 77.7 MB (77689400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7918a4dbaa10f74856b2a8789835c9f9df46e8a59c23bea61ac4a1d9423f12cc`  
		Last Modified: Mon, 20 Apr 2026 23:10:04 GMT  
		Size: 118.2 MB (118209240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6fdf9a00e14597ecc9dfe9618d4ce7bd4e61ee02520f5014ac6ae58fe238e0`  
		Last Modified: Mon, 20 Apr 2026 22:03:23 GMT  
		Size: 1.1 GB (1080278683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338ef466da99f9600c04884e246456cdb9a605e739315d048c418119ea4403e7`  
		Last Modified: Mon, 20 Apr 2026 23:10:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:4e6231b9efd1b1989c41ed391570eca0351d1d6f0359433aca14b6fcf27a93a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7428d1990477085809946a0474e0f86b4e3a9f5b8a829c08b6f57328bb20a4`

```dockerfile
```

-	Layers:
	-	`sha256:eb0a6d7950873c1320568905636584bc58f0fc49fb6624e8da4e086abb693854`  
		Last Modified: Mon, 20 Apr 2026 23:10:02 GMT  
		Size: 12.9 MB (12858283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff32aec8a94c61e0fdc0e0628b411b1165856c13b51998e3f7dc03ee174620e`  
		Last Modified: Mon, 20 Apr 2026 23:10:02 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
