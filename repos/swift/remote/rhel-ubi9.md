## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:ff29e8fb8bc5ff0f252a89864d6745d959e2ec354832bcbb4b42bd91f61bce83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:51f31836b379e3937dce0c02fe39bfabdecd2ce7ff729e1fe330a4ea4bb2de82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.8 MB (756825905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ee93977acb1f3ddeacfb91b0bc33dc0d670ad6374f28c52dc88e6aacb28f31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 01:53:13 GMT
ADD file:556fface2f78883b2174cda857a8421f0e7381c89023b271df819ad1b2edffb5 in / 
# Thu, 15 Jun 2023 01:53:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:53:14 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:53:14 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:53:14 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:53:14 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.2"
# Thu, 15 Jun 2023 01:53:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:53:14 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:53:14 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:53:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 15 Jun 2023 01:53:14 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:53:14 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 15 Jun 2023 01:53:14 GMT
ENV container oci
# Thu, 15 Jun 2023 01:53:14 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:53:14 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:53:15 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:53:16 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 15 Jun 2023 01:53:16 GMT
LABEL release=696
# Thu, 15 Jun 2023 01:53:16 GMT
ADD file:c04cc3fff2140dbf81f67c42b15d8a3e3385e9f5be6b1e85eebfc1cded10dc4e in /root/buildinfo/content_manifests/ubi9-container-9.2-696.json 
# Thu, 15 Jun 2023 01:53:16 GMT
ADD file:e980a1bfdb85f97d684317bf176a565f04d88f35b1e4e1e9188a7e8e31fb12e2 in /root/buildinfo/Dockerfile-ubi9-9.2-696 
# Thu, 15 Jun 2023 01:53:16 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:06" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="6b5892a11894993e819f9a93ee1d7aaa80dc3a17" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.2-696"
# Thu, 15 Jun 2023 01:53:17 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:53:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:53:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 01:15:26 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 22 Jun 2023 01:15:26 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 22 Jun 2023 01:15:41 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Thu, 22 Jun 2023 01:15:41 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 22 Jun 2023 01:15:41 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 22 Jun 2023 01:15:41 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Thu, 22 Jun 2023 01:15:42 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Thu, 22 Jun 2023 01:15:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 22 Jun 2023 01:15:42 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 22 Jun 2023 01:16:21 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 22 Jun 2023 01:16:27 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:7b3dd25bf011f6e84d1eaf4cce367d6d7c3d1d82385a65ebb394b5bf096f8d7a`  
		Last Modified: Wed, 21 Jun 2023 16:29:13 GMT  
		Size: 78.1 MB (78057447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec144cf16c99ea9b6adcc4a86582c1c9b4fa988bbd1d815970cb43380eae512`  
		Last Modified: Thu, 22 Jun 2023 01:24:09 GMT  
		Size: 121.5 MB (121513699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc589d6c58b97b6c53f2fd225ff978ec761e138239b3eb074774537351d10bb`  
		Last Modified: Thu, 22 Jun 2023 01:25:08 GMT  
		Size: 557.3 MB (557254535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc387d9f2b13b72d406ad86b23da9c9219f406aeae7585232e0b7283a4012db`  
		Last Modified: Thu, 22 Jun 2023 01:23:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c2134376d0b052c0adecbda6d131b16367e7f34d3f9949bb31eff233c3a6de7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.8 MB (738799089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a009ea7cb84881c0642b1aebba3438e876b56e0d08286b86f0d5fc8410c3042d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 01:53:11 GMT
ADD file:2c138c3ba62f39a5186843f14784f547d92d9a30b4c8b05ee8ac08e53943513c in / 
# Thu, 15 Jun 2023 01:53:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:53:13 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:53:13 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:53:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:53:13 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.2"
# Thu, 15 Jun 2023 01:53:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:53:13 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:53:13 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:53:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 15 Jun 2023 01:53:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:53:13 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 15 Jun 2023 01:53:13 GMT
ENV container oci
# Thu, 15 Jun 2023 01:53:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:53:13 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:53:14 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:53:15 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 15 Jun 2023 01:53:15 GMT
LABEL release=696
# Thu, 15 Jun 2023 01:53:15 GMT
ADD file:ddaa45289615330516ed36908d2845d90a2c1805788124bae86a5a22a83265a6 in /root/buildinfo/content_manifests/ubi9-container-9.2-696.json 
# Thu, 15 Jun 2023 01:53:15 GMT
ADD file:918b57c8e0af79d91c9c73bc62a232f075b0cb15723d33913db34b49c269647c in /root/buildinfo/Dockerfile-ubi9-9.2-696 
# Thu, 15 Jun 2023 01:53:15 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:06" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="6b5892a11894993e819f9a93ee1d7aaa80dc3a17" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.2-696"
# Thu, 15 Jun 2023 01:53:17 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:53:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:53:19 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 01:28:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 22 Jun 2023 01:28:09 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 22 Jun 2023 01:28:31 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip
# Thu, 22 Jun 2023 01:28:33 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 22 Jun 2023 01:28:33 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 22 Jun 2023 01:28:33 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Thu, 22 Jun 2023 01:28:33 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Thu, 22 Jun 2023 01:28:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 22 Jun 2023 01:28:33 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 22 Jun 2023 01:29:13 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 22 Jun 2023 01:29:25 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:8218e3eb82c38bb61ec8dfa5a01aa99485cab058180fb9e1d0a6bbbd2b6c5b86`  
		Last Modified: Wed, 21 Jun 2023 18:06:30 GMT  
		Size: 75.8 MB (75777365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8587f6d2714eddfc624431a820e8a9222180026b4ea486ab42ebf5740c5118`  
		Last Modified: Thu, 22 Jun 2023 01:30:58 GMT  
		Size: 115.3 MB (115305889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1373af8a94db243944623818b40b58390d86176eca7d9c67342bc0c10b99867e`  
		Last Modified: Thu, 22 Jun 2023 01:31:41 GMT  
		Size: 547.7 MB (547715606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ea4c49c67f31685194c137384a48b363eda25ae0655ecd4e847854f10a9827`  
		Last Modified: Thu, 22 Jun 2023 01:30:48 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
