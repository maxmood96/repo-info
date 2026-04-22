## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:ac5068d19e31497b02bf132420fecff1460a8bc1d9982ea7e99778e00074cddd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:573efe81fecb41aecd5866a031cf1252ea9332fa65da3a4e6574aa38909c71dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1288713574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814078640926b6fff75004204931562f5dc348e8cc573e1280a5dcc64e05d8e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 22 Apr 2026 05:03:07 GMT
ENV container oci
# Wed, 22 Apr 2026 05:03:09 GMT
COPY dir:3ff2d39ae06fb20eccb68f3beaa79fe1e9823a8c7eb1e60e613146e57008c0d4 in /      
# Wed, 22 Apr 2026 05:03:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:03:09 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:03:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:03:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:03:09 GMT
COPY file:3a9736838f6dce34051adcc517f0e1bb8bb71915214cae605d0267eddbd9e63b in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:03:10 GMT
COPY file:3a9736838f6dce34051adcc517f0e1bb8bb71915214cae605d0267eddbd9e63b in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:03:10 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0809ab29dc0248030bc33288f153b9d237dc704c" "org.opencontainers.image.revision"="0809ab29dc0248030bc33288f153b9d237dc704c" "build-date"="2026-04-22T05:02:44Z" "org.opencontainers.image.created"="2026-04-22T05:02:44Z" "release"="1776834047"org.opencontainers.image.revision=0809ab29dc0248030bc33288f153b9d237dc704c,org.opencontainers.image.created=2026-04-22T05:02:44Z
# Wed, 22 Apr 2026 18:20:16 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 22 Apr 2026 18:20:16 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 22 Apr 2026 18:20:16 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 22 Apr 2026 18:20:16 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 22 Apr 2026 18:20:16 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 22 Apr 2026 18:20:16 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Wed, 22 Apr 2026 18:20:16 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Wed, 22 Apr 2026 18:20:16 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 18:20:16 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 18:21:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 22 Apr 2026 18:21:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:15ff23c3b2e178cb3ea1caa12f6fbe9ba23536bf0d0c938ef17359ac61bb5174`  
		Last Modified: Wed, 22 Apr 2026 05:54:32 GMT  
		Size: 80.0 MB (79952719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5b13e131be0c042c1489ad5828a3bc8a070ff7a56bf0c39612450db79763e0`  
		Last Modified: Wed, 22 Apr 2026 18:23:28 GMT  
		Size: 124.7 MB (124711337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f7355d20d694d145fbf4688c63a728cb08f4edbff524635d4047a4f954daba`  
		Last Modified: Mon, 20 Apr 2026 21:56:34 GMT  
		Size: 1.1 GB (1084049344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5992a4e1877daf19ace576cb4bdd4c2d65be4f0584d062941b4120dcb88c457f`  
		Last Modified: Wed, 22 Apr 2026 18:23:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:33f198bac1af263ef715e1be5305f126c84e3e03be4e8bf12a975e4d22538db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12999488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f956c8ce771562c1be4c30ec980f68deca0477304478c8b050c133d95e8c8cf7`

```dockerfile
```

-	Layers:
	-	`sha256:627975059f5ef828f8e3307d0bc37cace09ab937534f331f70176f1a62da92d6`  
		Last Modified: Wed, 22 Apr 2026 18:23:25 GMT  
		Size: 13.0 MB (12985046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c252dc3ad9047999235fe9486987c4a6d05d2842412037557083647ac676b5`  
		Last Modified: Wed, 22 Apr 2026 18:23:24 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:cc75bd6fa4b766881d40d341b727adfded2290b23184bc53cfb6b0369a1f9026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276179931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71348f754305b08d7b1f1c30471f9e8140d76858af37228acc1950a7454ea0d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 22 Apr 2026 05:05:04 GMT
ENV container oci
# Wed, 22 Apr 2026 05:05:07 GMT
COPY dir:fe2980062460e3bd4a122856fdac1c3ffa44768921f36afe9a319714831cf225 in /      
# Wed, 22 Apr 2026 05:05:07 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:05:07 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:05:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:05:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:05:08 GMT
COPY file:5a90691d0ef9b2fd3584bc1f13654e876db73891f849088e105da14b4e634263 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:08 GMT
COPY file:5a90691d0ef9b2fd3584bc1f13654e876db73891f849088e105da14b4e634263 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:09 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0809ab29dc0248030bc33288f153b9d237dc704c" "org.opencontainers.image.revision"="0809ab29dc0248030bc33288f153b9d237dc704c" "build-date"="2026-04-22T05:04:47Z" "org.opencontainers.image.created"="2026-04-22T05:04:47Z" "release"="1776834047"org.opencontainers.image.revision=0809ab29dc0248030bc33288f153b9d237dc704c,org.opencontainers.image.created=2026-04-22T05:04:47Z
# Wed, 22 Apr 2026 18:19:31 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 22 Apr 2026 18:19:31 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 22 Apr 2026 18:19:31 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 22 Apr 2026 18:19:31 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 22 Apr 2026 18:19:31 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 22 Apr 2026 18:19:31 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Wed, 22 Apr 2026 18:19:31 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Wed, 22 Apr 2026 18:19:31 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 18:19:31 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 18:20:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 22 Apr 2026 18:20:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:3bec630204a194f3a0b7caaca2685445f836c478dcaeab77c747628d52fb567c`  
		Last Modified: Wed, 22 Apr 2026 05:57:16 GMT  
		Size: 77.7 MB (77690700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499dde9556929a558a0df066d6368fd4b0c196f231f1a5a079bf40f6c4331fb3`  
		Last Modified: Wed, 22 Apr 2026 18:22:21 GMT  
		Size: 118.2 MB (118210374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6fdf9a00e14597ecc9dfe9618d4ce7bd4e61ee02520f5014ac6ae58fe238e0`  
		Last Modified: Mon, 20 Apr 2026 22:03:23 GMT  
		Size: 1.1 GB (1080278683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2cfb1e25f323e89b27440fcb48313088136c25f8a85d416192e4dc7f08b2e5`  
		Last Modified: Wed, 22 Apr 2026 18:22:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:00d9020ccd8b532357c07480e663145013e6cc39ecb7f755965d0da4326b4196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12872841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0902c1d6a73c8e745aeb1e59709aee41cbaa216df13979e305e83fd376241d9f`

```dockerfile
```

-	Layers:
	-	`sha256:c2bbf4623ea2badb3639ffe85fb7ef39b532cdc5ab97df5e0c907ef791e13159`  
		Last Modified: Wed, 22 Apr 2026 18:22:19 GMT  
		Size: 12.9 MB (12858283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5006d2ed4ab4e5d19e30fd2b150c97c3342a35773ffbc02572a5544a75ab8309`  
		Last Modified: Wed, 22 Apr 2026 18:22:19 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
