## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:824660bd66cb2182e854624af758d54fd9eb2ab53f98fae8060e5c66f9262fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:fb3991d676854d52902019b7073ec748847fd415a976a698d6207da4027df5c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **823.7 MB (823669290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d3826a61033b01c969b18d7a00ccf4e4b748dddf31f554c9410b7245f0e628`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:24 GMT
ADD file:49f57596962113c3c41279525f4e356babf54415c63af2dbf9d3b71642cf423d in / 
# Thu, 29 Feb 2024 14:19:24 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:24 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:25 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.3"
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 29 Feb 2024 14:19:25 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:25 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:25 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:26 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 29 Feb 2024 14:19:26 GMT
LABEL release=1610
# Thu, 29 Feb 2024 14:19:26 GMT
ADD file:5c044b2f97600771ae4c6dedc6ffb1230609e7a1c16fc81371a5b25b24a5d48e in /root/buildinfo/content_manifests/ubi9-container-9.3-1610.json 
# Thu, 29 Feb 2024 14:19:26 GMT
ADD file:c4dee968aa55387598edc7a709f7a93db58ea7cc3df10935dea7105b5f88056f in /root/buildinfo/Dockerfile-ubi9-9.3-1610 
# Thu, 29 Feb 2024 14:19:26 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T13:57:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="eb726081eeafc660c182aae53074ec6631cb473e" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.3-1610"
# Thu, 29 Feb 2024 14:19:27 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:28 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:30 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 15 Apr 2024 19:03:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Apr 2024 19:03:06 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Apr 2024 19:03:22 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Mon, 15 Apr 2024 19:03:23 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Mon, 15 Apr 2024 19:03:23 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 15 Apr 2024 19:03:23 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Mon, 15 Apr 2024 19:03:23 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Mon, 15 Apr 2024 19:03:23 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Apr 2024 19:03:23 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Apr 2024 19:04:09 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Mon, 15 Apr 2024 19:04:16 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:1153e061da4ea9623b0dcdb9e8638b9432d5aa919217cc7c115b5a858f40f306`  
		Last Modified: Tue, 05 Mar 2024 22:02:06 GMT  
		Size: 78.8 MB (78778130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad32131a3c2edc58a2e47fc603a21196f4f438f4b4ba50a8be20b8ef6d6da4f`  
		Last Modified: Mon, 15 Apr 2024 19:12:21 GMT  
		Size: 121.7 MB (121706198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fbcb46ba5fb6d0046fe9f0c1b7d4ec5831bffc5b83da10b73dfc9f2ad108e2`  
		Last Modified: Mon, 15 Apr 2024 19:13:30 GMT  
		Size: 623.2 MB (623184765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905c634abb6e6d5ef0380e3acf3de72bea1cc242a57d7f603bf039240627cc4b`  
		Last Modified: Mon, 15 Apr 2024 19:12:06 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:490fdc847f804e2f84cf78473192393bebd78b4a796948c6cbcc13cbc13b7bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **809.6 MB (809592855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdc089a4dd4ccd699a0c364a340be5eea7aebc9eb52cc9ec637867024fc2d77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:23 GMT
ADD file:bfc5a43326e1a6069156047b679434b9dbed0d7cc5fedada96ba2c47597f1c81 in / 
# Thu, 29 Feb 2024 14:19:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:25 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.3"
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:25 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 29 Feb 2024 14:19:25 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:25 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:26 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:27 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 29 Feb 2024 14:19:27 GMT
LABEL release=1610
# Thu, 29 Feb 2024 14:19:27 GMT
ADD file:e48c9a6e8594d3bc355bd0cdb7b5bc70df6213dd23480f37e74d05963e00401a in /root/buildinfo/content_manifests/ubi9-container-9.3-1610.json 
# Thu, 29 Feb 2024 14:19:27 GMT
ADD file:75a182bdd1323b9b6afcb408f15edd368de54262df8a93900b56d8f2a960eeef in /root/buildinfo/Dockerfile-ubi9-9.3-1610 
# Thu, 29 Feb 2024 14:19:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T13:57:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="eb726081eeafc660c182aae53074ec6631cb473e" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.3-1610"
# Thu, 29 Feb 2024 14:19:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 15 Apr 2024 18:54:46 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Apr 2024 18:54:46 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Apr 2024 18:55:01 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Mon, 15 Apr 2024 18:55:03 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Mon, 15 Apr 2024 18:55:03 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 15 Apr 2024 18:55:03 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Mon, 15 Apr 2024 18:55:03 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Mon, 15 Apr 2024 18:55:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Apr 2024 18:55:03 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Apr 2024 18:55:51 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Mon, 15 Apr 2024 18:56:03 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:0af708ca56aa0f8f6981a42770d4f78c2499c7bc5928caa1a0475658fc31ace2`  
		Last Modified: Tue, 05 Mar 2024 22:02:07 GMT  
		Size: 76.5 MB (76482720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d3bb158ed1035d089f873078e8ff5122c27b6b3d7a68c04a77647106f2b14`  
		Last Modified: Mon, 15 Apr 2024 19:01:48 GMT  
		Size: 115.7 MB (115720677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86e121da4b13c0f62163e53ed67cf7382dd11d80ddf018c00cdce87b64ec9f9`  
		Last Modified: Mon, 15 Apr 2024 19:02:42 GMT  
		Size: 617.4 MB (617389261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be298391b63bfc94919d79f8a648ff134eda2d6d0d243210af8e07d28f6be61`  
		Last Modified: Mon, 15 Apr 2024 19:01:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
