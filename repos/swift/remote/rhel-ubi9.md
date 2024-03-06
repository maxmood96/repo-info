## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:842382f84e158298d7e443667fcfa8ec0eb53bced2625f0fe94959c259318a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:f440e8bc3717f13abfbc0289e1b0f5b899d593ded7f993c7a5213eb120de42f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **823.8 MB (823757560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c0d677e3f7a0f6f6cb880b78c4e25b99b0952da6dc990746cddda6a9e6bc2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jan 2024 19:19:56 GMT
ADD file:203d8a440d4a212a3de9f4b263e3745c6128caae02b75208c4ab08afa02c8042 in / 
# Wed, 17 Jan 2024 19:19:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:19:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:19:58 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.3"
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:19:58 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 17 Jan 2024 19:19:58 GMT
ENV container oci
# Wed, 17 Jan 2024 19:19:58 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:19:58 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:19:59 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:19:59 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 17 Jan 2024 19:19:59 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:20:00 GMT
ADD file:a2f04c734a30ef620587d3de15d7c0c1984aa702a61dbdd568e3301056771155 in /root/buildinfo/content_manifests/ubi9-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:20:00 GMT
ADD file:e8a28bfd49796b6e1cb4385742ffd9e5e7709c8dd2ba9a76b1a8c5fb4cfe4405 in /root/buildinfo/Dockerfile-ubi9-9.3-1552 
# Wed, 17 Jan 2024 19:20:00 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:40" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="eb726081eeafc660c182aae53074ec6631cb473e" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.3-1552"
# Wed, 17 Jan 2024 19:20:01 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:20:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:20:05 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 26 Jan 2024 02:05:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 26 Jan 2024 02:05:59 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 26 Jan 2024 02:06:17 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Fri, 26 Jan 2024 02:06:18 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 26 Jan 2024 02:06:18 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 06 Mar 2024 21:05:19 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Wed, 06 Mar 2024 21:05:19 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Wed, 06 Mar 2024 21:05:19 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:05:19 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:06:02 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 06 Mar 2024 21:06:10 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:1bd75c368cb585e77e0b3234a750db4235fa64ff8b5b9ca8da8bf7a34ec9ecaa`  
		Last Modified: Thu, 25 Jan 2024 18:06:59 GMT  
		Size: 78.9 MB (78853820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986582b0c0b05fba5b1514d65c3bbc63a0fda9ee4813c2c2312a89fc1f85a2a`  
		Last Modified: Fri, 26 Jan 2024 02:12:52 GMT  
		Size: 121.7 MB (121718711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694e79115f5eacddabb1c86a31d45744b95744d82c88505fdd91dd3d2427ce3e`  
		Last Modified: Wed, 06 Mar 2024 21:20:12 GMT  
		Size: 623.2 MB (623184830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ce9b3c87fe458241bb1f9b8bc752e00299b6f86682deb880f1d344e529ce4f`  
		Last Modified: Wed, 06 Mar 2024 21:18:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2742a0b0b1ebcff6bb8f17d33f01a9c25f2f1b58af21e01238c082dff8041a8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **809.7 MB (809664114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720659effc4258651240e595f0c0724cb8f8d29e50c2cc3fe9a564da40d3a560`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Jan 2024 19:19:52 GMT
ADD file:aff8bc779c8789d35ac2a80d9a02f20b74e69b456173a040eaf73fe97d9a3f11 in / 
# Wed, 17 Jan 2024 19:19:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:19:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:19:54 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.3"
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:19:54 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 17 Jan 2024 19:19:54 GMT
ENV container oci
# Wed, 17 Jan 2024 19:19:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:19:54 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:19:55 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:19:57 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 17 Jan 2024 19:19:57 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:19:57 GMT
ADD file:1b29ebbd958d302277790a4e064782c082d19926c466a9dd447aa453b2bc65d2 in /root/buildinfo/content_manifests/ubi9-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:19:57 GMT
ADD file:db3ad7c9c52d4b1c490f1ebf564a128ce62fad1d213e5e94e2f1393551715c6b in /root/buildinfo/Dockerfile-ubi9-9.3-1552 
# Wed, 17 Jan 2024 19:19:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:40" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="eb726081eeafc660c182aae53074ec6631cb473e" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.3-1552"
# Wed, 17 Jan 2024 19:19:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:20:00 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:20:02 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 26 Jan 2024 02:32:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 26 Jan 2024 02:32:09 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 26 Jan 2024 02:32:27 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Fri, 26 Jan 2024 02:32:30 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 26 Jan 2024 02:32:30 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 06 Mar 2024 21:26:05 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Wed, 06 Mar 2024 21:26:05 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Wed, 06 Mar 2024 21:26:05 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:26:05 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 06 Mar 2024 21:26:44 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 06 Mar 2024 21:26:57 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:2f4c7b011e02135ccee6607271ddd903269b4fd07b493ae6abc9b26f162f9499`  
		Last Modified: Thu, 25 Jan 2024 18:07:07 GMT  
		Size: 76.5 MB (76515496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21511505b4e4de3fb17d7957f3330c9d4459edd5786dfe95fb30478b14c7df46`  
		Last Modified: Fri, 26 Jan 2024 02:37:07 GMT  
		Size: 115.8 MB (115759131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20870a4d2e5164d570b86d567335b5c16bcc2bba869e9741be22301474825eb`  
		Last Modified: Wed, 06 Mar 2024 21:34:56 GMT  
		Size: 617.4 MB (617389289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8582d9a19c8744f37bfabb2d78fcb5bcf8f783bd1326acf94acdba0070f03d97`  
		Last Modified: Wed, 06 Mar 2024 21:33:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
