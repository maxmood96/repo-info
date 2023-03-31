## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:68f327ed2ae4c7f4ca898d9b433940facb6a70614cc98bbd2c7eb4761d331817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:e835d64fe483185dc0879272cad2ade1f7ec00f84b5417f5dd5b276617c45ef2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166313947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc226ffcdf3122d84859b62744d6d7e410dda186d1a4d9dc60323c32480d6d02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 Feb 2023 09:38:02 GMT
ADD file:c622fa0d56b7c3183f431d2f06555da263ed653fdfb0acb60e3b350252324b1e in / 
# Wed, 22 Feb 2023 09:38:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 22 Feb 2023 09:38:03 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 22 Feb 2023 09:38:04 GMT
ADD multi:0882c44110b6a64b078cdd328390626e44b18b514d5b9b155c169898325afa84 in /etc/yum.repos.d/ 
# Wed, 22 Feb 2023 09:38:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Feb 2023 09:38:04 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.1.0"
# Wed, 22 Feb 2023 09:38:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Feb 2023 09:38:04 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 22 Feb 2023 09:38:04 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Feb 2023 09:38:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 22 Feb 2023 09:38:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Feb 2023 09:38:04 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 22 Feb 2023 09:38:04 GMT
ENV container oci
# Wed, 22 Feb 2023 09:38:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Feb 2023 09:38:04 GMT
CMD ["/bin/bash"]
# Wed, 22 Feb 2023 09:38:04 GMT
RUN rm -rf /var/log/*
# Wed, 22 Feb 2023 09:38:06 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 22 Feb 2023 09:38:06 GMT
LABEL release=1782
# Wed, 22 Feb 2023 09:38:06 GMT
ADD file:05d7057e015acf79744164439aaa05665ed396230a5dae915b56ae48c6a9078a in /root/buildinfo/content_manifests/ubi9-container-9.1.0-1782.json 
# Wed, 22 Feb 2023 09:38:06 GMT
ADD file:532fb2856565f80bbf8b97f3dce9ed5f7ac2a8f5977e57b11832ba00b592dd2e in /root/buildinfo/Dockerfile-ubi9-9.1.0-1782 
# Wed, 22 Feb 2023 09:38:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-02-22T09:23:14" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="cf87ad00feaef3d9d7a442dad55ab6a14f6a3f81" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.1.0-1782"
# Wed, 22 Feb 2023 09:38:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-5af5d.repo' '/etc/yum.repos.d/repo-93eaf.repo'
# Wed, 22 Feb 2023 09:38:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 22 Feb 2023 09:38:10 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 31 Mar 2023 21:29:23 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 31 Mar 2023 21:29:23 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 31 Mar 2023 21:30:21 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 31 Mar 2023 21:30:21 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 31 Mar 2023 21:30:21 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Fri, 31 Mar 2023 21:30:21 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Fri, 31 Mar 2023 21:30:21 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Mar 2023 21:30:21 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Mar 2023 21:30:47 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:2a625e4afab51b49edb0e5f4ff37d8afbb20ec644ed1e68641358a6305557de3`  
		Last Modified: Tue, 28 Feb 2023 12:07:08 GMT  
		Size: 79.2 MB (79170714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844c1350b95de515f975a97e91cfbb57fadea0064993f000d224c1beaff24cdb`  
		Last Modified: Fri, 31 Mar 2023 21:48:36 GMT  
		Size: 87.1 MB (87143233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:4c90cd46ac71d1109ca8f7a3d0c0234092c215f208a72a4d15cccdee6b8ba229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161802721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edc6492caa3830594445001a0292056ca8c707def5ac4b1008776803018b4bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 Feb 2023 09:37:34 GMT
ADD file:ad18dcce8187a0692024c681a3ed2e0d77df2afd895f6378d1c9243d5b0269c0 in / 
# Wed, 22 Feb 2023 09:37:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 22 Feb 2023 09:37:35 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 22 Feb 2023 09:37:36 GMT
ADD multi:0882c44110b6a64b078cdd328390626e44b18b514d5b9b155c169898325afa84 in /etc/yum.repos.d/ 
# Wed, 22 Feb 2023 09:37:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Feb 2023 09:37:36 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.1.0"
# Wed, 22 Feb 2023 09:37:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Feb 2023 09:37:36 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 22 Feb 2023 09:37:36 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Feb 2023 09:37:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 22 Feb 2023 09:37:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Feb 2023 09:37:36 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 22 Feb 2023 09:37:36 GMT
ENV container oci
# Wed, 22 Feb 2023 09:37:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Feb 2023 09:37:36 GMT
CMD ["/bin/bash"]
# Wed, 22 Feb 2023 09:37:37 GMT
RUN rm -rf /var/log/*
# Wed, 22 Feb 2023 09:37:38 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 22 Feb 2023 09:37:38 GMT
LABEL release=1782
# Wed, 22 Feb 2023 09:37:39 GMT
ADD file:3f68054ed1e0e4e6501151443ecce82db7fbb0bffd14751decd7c93ab7ec8159 in /root/buildinfo/content_manifests/ubi9-container-9.1.0-1782.json 
# Wed, 22 Feb 2023 09:37:39 GMT
ADD file:1ff876120bf008ec2b9d36122a5ec967e2c77d35f9fa0511444b26e8bd3841b0 in /root/buildinfo/Dockerfile-ubi9-9.1.0-1782 
# Wed, 22 Feb 2023 09:37:39 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-02-22T09:23:14" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="cf87ad00feaef3d9d7a442dad55ab6a14f6a3f81" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.1.0-1782"
# Wed, 22 Feb 2023 09:37:40 GMT
RUN rm -f '/etc/yum.repos.d/repo-5af5d.repo' '/etc/yum.repos.d/repo-93eaf.repo'
# Wed, 22 Feb 2023 09:37:42 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 22 Feb 2023 09:37:44 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 31 Mar 2023 21:56:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 31 Mar 2023 21:56:09 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 31 Mar 2023 21:57:17 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 31 Mar 2023 21:57:17 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 31 Mar 2023 21:57:18 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Fri, 31 Mar 2023 21:57:18 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Fri, 31 Mar 2023 21:57:18 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Mar 2023 21:57:18 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Mar 2023 21:57:38 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:16a04852951035f5435456f98eabbcc1af8b8cafa63d8485c67ecd79fae7edd8`  
		Last Modified: Tue, 28 Feb 2023 12:07:22 GMT  
		Size: 76.8 MB (76822883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2871696d7b89926bbb3d12cb9a2ba8cf629e723d7b26ec83bde143a4bea91f`  
		Last Modified: Fri, 31 Mar 2023 22:04:02 GMT  
		Size: 85.0 MB (84979838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
