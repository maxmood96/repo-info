## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:b908053524d9401ec3405e2ded4b1ac6a1e9dde415d5ef125d34874033ba446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:5ac855c6a182c320d7a64b4ab274ed22f6fce5093c08595fca2b2c4d6622f89e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125315372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8a39ca78f11888d21385cbe65a8926897772bcc9eba98d15949a1b1a98fbf1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 May 2024 16:48:58 GMT
ADD file:12f80c7d45b3eb0d8b3a39452a80daf9d72b5bcb3e26111bf1196b65f77dd422 in / 
# Thu, 02 May 2024 16:48:58 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 16:48:59 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 16:48:59 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 16:48:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 16:48:59 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 02 May 2024 16:48:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 16:48:59 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 02 May 2024 16:48:59 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 16:48:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 02 May 2024 16:48:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 16:48:59 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 02 May 2024 16:48:59 GMT
ENV container oci
# Thu, 02 May 2024 16:48:59 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 16:48:59 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 16:48:59 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 16:49:00 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 02 May 2024 16:49:00 GMT
ADD file:28e44343bae7309a38fcd4fee147791844f2b5a40d92f20475d4a22a3390baac in /root/buildinfo/content_manifests/ubi9-container-9.4-947.1714667021.json 
# Thu, 02 May 2024 16:49:01 GMT
ADD file:e9d6c5d1c0023a6f2768fe173d5406a1a666af1148809618b37a36eadee060be in /root/buildinfo/Dockerfile-ubi9-9.4-947.1714667021 
# Thu, 02 May 2024 16:49:01 GMT
LABEL "release"="947.1714667021" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T16:25:06" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-947.1714667021"
# Thu, 02 May 2024 16:49:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 16:49:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 16:49:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 07 May 2024 22:37:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 May 2024 22:37:43 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 07 May 2024 22:38:53 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 07 May 2024 22:38:53 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 07 May 2024 22:38:53 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Tue, 07 May 2024 22:38:53 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Tue, 07 May 2024 22:38:53 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 May 2024 22:38:53 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 May 2024 22:39:25 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:6b20e0c6c1e16f403ab42ddafa7c2b351b4e0da50ae0d410cd77097acfd48a79`  
		Last Modified: Mon, 06 May 2024 15:31:21 GMT  
		Size: 79.3 MB (79282021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4c243bd8ad1a051a58e8f0b42906d9d7dfce9406bb7ae7e1f92c9f4bebddaf`  
		Last Modified: Tue, 07 May 2024 22:48:15 GMT  
		Size: 46.0 MB (46033351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:1d4d7d24e52ede4a205c0872fe7e10e56c3ef595552207ab6e4419700942ba73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121546107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e116a35d3160607ff6546d319ac8d28fc44b85edea40d1bb7117266fdb5c459`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 May 2024 16:48:56 GMT
ADD file:e30ac40cde9444effc8f95b5548fc11921461d70534362b16b27b56bf83336e3 in / 
# Thu, 02 May 2024 16:48:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 16:48:57 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 16:48:57 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 16:48:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 16:48:57 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Thu, 02 May 2024 16:48:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 16:48:57 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 02 May 2024 16:48:57 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 16:48:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 02 May 2024 16:48:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 16:48:57 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 02 May 2024 16:48:57 GMT
ENV container oci
# Thu, 02 May 2024 16:48:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 16:48:57 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 16:48:59 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 16:49:00 GMT
RUN mkdir -p /var/log/rhsm
# Thu, 02 May 2024 16:49:00 GMT
ADD file:5f29616ce831c5b40d04f6cc84af85992f0ace2a00666b780aa364bbc71ac55e in /root/buildinfo/content_manifests/ubi9-container-9.4-947.1714667021.json 
# Thu, 02 May 2024 16:49:00 GMT
ADD file:3f25e72c079da40c937b5dda22614a4e4e82169ac6b1b63f3b271a0c93871df3 in /root/buildinfo/Dockerfile-ubi9-9.4-947.1714667021 
# Thu, 02 May 2024 16:49:00 GMT
LABEL "release"="947.1714667021" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T16:25:06" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92a4a475241865d0d11bd861fb2b29fbd9b17df0" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-947.1714667021"
# Thu, 02 May 2024 16:49:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 16:49:03 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 16:49:05 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 07 May 2024 23:41:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 May 2024 23:41:43 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 07 May 2024 23:43:05 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 07 May 2024 23:43:06 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 07 May 2024 23:43:06 GMT
ARG SWIFT_BRANCH=swift-5.10-release
# Tue, 07 May 2024 23:43:06 GMT
ARG SWIFT_VERSION=swift-5.10-RELEASE
# Tue, 07 May 2024 23:43:06 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 May 2024 23:43:06 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-5.10-release SWIFT_VERSION=swift-5.10-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 May 2024 23:43:34 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
```

-	Layers:
	-	`sha256:4736dc14b679eb3fb1cfb3cd07f8551f2959854a19fcfa3afd7c0cbef20e093e`  
		Last Modified: Mon, 06 May 2024 16:21:16 GMT  
		Size: 77.0 MB (77022694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12fe3670a8b7e1d9fd05aa0faaf999696fcfd989fc3ee4d2ecd67fb638fa303`  
		Last Modified: Tue, 07 May 2024 23:49:42 GMT  
		Size: 44.5 MB (44523413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
