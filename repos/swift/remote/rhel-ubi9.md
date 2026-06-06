## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:595f895be9cacbcffbab8f38d82f3394fe2fdb55001151317b7b00950832464c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:bb12e07988ba99828902bb79870218f72d296929cb21407706e666003eaa237c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1290892114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac808cddf9da4d55fd007816b3f285ba1cb9aa6c92e820a49f30d7c58130e17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Jun 2026 06:24:30 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 06:24:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 06:24:30 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 04 Jun 2026 06:24:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 06:24:31 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 04 Jun 2026 06:24:31 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 06:24:31 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 06:24:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 04 Jun 2026 06:24:31 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 06:24:31 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 04 Jun 2026 06:24:31 GMT
ENV container oci
# Thu, 04 Jun 2026 06:24:32 GMT
COPY dir:07aeab3c4260c4bbc2a45a839e8a21dc718cb9873501f166c234cef3b22ffd6c in /      
# Thu, 04 Jun 2026 06:24:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 06:24:32 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 06:24:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 06:24:33 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 06:24:33 GMT
COPY file:eaa80c113d813991e10fd37cca06b510a857dd1a5d13219a777d082739c9f33c in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 06:24:33 GMT
COPY file:eaa80c113d813991e10fd37cca06b510a857dd1a5d13219a777d082739c9f33c in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 06:24:34 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a1ff645e4d0b83aad1b77555a562c5807a8af5bf" "org.opencontainers.image.revision"="a1ff645e4d0b83aad1b77555a562c5807a8af5bf" "build-date"="2026-06-04T06:24:17Z" "org.opencontainers.image.created"="2026-06-04T06:24:17Z" "release"="1780554162"org.opencontainers.image.revision=a1ff645e4d0b83aad1b77555a562c5807a8af5bf,org.opencontainers.image.created=2026-06-04T06:24:17Z
# Fri, 05 Jun 2026 22:44:41 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 05 Jun 2026 22:44:41 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 05 Jun 2026 22:44:41 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Fri, 05 Jun 2026 22:44:41 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 05 Jun 2026 22:44:41 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 05 Jun 2026 22:44:41 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Fri, 05 Jun 2026 22:44:41 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Fri, 05 Jun 2026 22:44:41 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 05 Jun 2026 22:44:41 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 05 Jun 2026 22:45:24 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 05 Jun 2026 22:45:24 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:1d5cc9690f8e983825683dec7f7527629407c325fe8a87ca8ebe81776bfbd222`  
		Last Modified: Thu, 04 Jun 2026 13:23:38 GMT  
		Size: 80.5 MB (80504421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c804985d673d9ff75068120b6a11d8a9d33df0750be4d4b5de68d5af8e29473`  
		Last Modified: Fri, 05 Jun 2026 22:47:48 GMT  
		Size: 126.5 MB (126464300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec82f397aadc643580e3fb9f811fcb374c771614968d9324a8ee2bd6bd174904`  
		Last Modified: Wed, 13 May 2026 18:20:44 GMT  
		Size: 1.1 GB (1083923220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf5453c2e78396f22062e8be8d04486f939518479217c56a520be7393711f87`  
		Last Modified: Fri, 05 Jun 2026 22:47:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:913782b0f767e98380bc960cf32abc3194eeb7b96a232b2db2b2f0341f0456b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13014233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efb402e5a669b032aa17642f9bdab91bd3dfd01be0ef79e3a25bad9adb0cc98`

```dockerfile
```

-	Layers:
	-	`sha256:33f435266f5710a446faedd140566c6401210d985cde7546d69831dc979e9bb6`  
		Last Modified: Fri, 05 Jun 2026 22:47:46 GMT  
		Size: 13.0 MB (12999791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c24cb1c135f9e19511ad9ab7acf24e549f2137492cf2cd1c19caeb863dc91e82`  
		Last Modified: Fri, 05 Jun 2026 22:47:45 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:1919ab650996dbe1c212f26908ca64bdc19a81a6640fd67bd65ebae911a612a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1278099112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce34a8f8b645b64c9f02947a5c4db5bbdc101f56056e65f71d0b94b4f5301591`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 06:26:42 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 04 Jun 2026 06:26:42 GMT
ENV container oci
# Thu, 04 Jun 2026 06:26:45 GMT
COPY dir:68503833e5ae35afd2261329a266e6347dcf55b5e500af4aa4e2b84eadb81caa in /      
# Thu, 04 Jun 2026 06:26:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 06:26:45 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 06:26:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 06:26:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 06:26:45 GMT
COPY file:d4e1bea2e2b886620a94f6cfd2794e03c22d51e44b685f0f56cdacf65b44892a in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 06:26:46 GMT
COPY file:d4e1bea2e2b886620a94f6cfd2794e03c22d51e44b685f0f56cdacf65b44892a in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 06:26:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a1ff645e4d0b83aad1b77555a562c5807a8af5bf" "org.opencontainers.image.revision"="a1ff645e4d0b83aad1b77555a562c5807a8af5bf" "build-date"="2026-06-04T06:26:26Z" "org.opencontainers.image.created"="2026-06-04T06:26:26Z" "release"="1780554162"org.opencontainers.image.revision=a1ff645e4d0b83aad1b77555a562c5807a8af5bf,org.opencontainers.image.created=2026-06-04T06:26:26Z
# Fri, 05 Jun 2026 22:45:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 05 Jun 2026 22:45:10 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 05 Jun 2026 22:45:10 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Fri, 05 Jun 2026 22:45:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 05 Jun 2026 22:45:10 GMT
ARG SWIFT_PLATFORM=ubi9
# Fri, 05 Jun 2026 22:45:10 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Fri, 05 Jun 2026 22:45:10 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Fri, 05 Jun 2026 22:45:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 05 Jun 2026 22:45:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 05 Jun 2026 22:45:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 05 Jun 2026 22:45:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:418f24f4c43df094b9abd2068c778f9c6aec39d82de6a12ced71c215c568ccc7`  
		Last Modified: Thu, 04 Jun 2026 13:24:53 GMT  
		Size: 78.2 MB (78160512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafbe1863c1cd2817e53fab002204b986d0bc909e872418ecdf75e123310628b`  
		Last Modified: Fri, 05 Jun 2026 22:48:05 GMT  
		Size: 119.8 MB (119832710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44ed9a9b258612e96029485a3a9d687b406d4f639aead7bfe9f142a2b16fe6f`  
		Last Modified: Wed, 13 May 2026 18:08:43 GMT  
		Size: 1.1 GB (1080105717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09be7ad8b31f84cdd51137e93591c29520d15b81a47cf983a732f0d507eedb73`  
		Last Modified: Fri, 05 Jun 2026 22:48:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:03a0ba96b5d76e10f61c5d84e3999522b977eda697dcda16ddc68d0e43a9166b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12887048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b43d2ba98b60bdedc0df8da0b57e2b056ab841f2b103b9b54c9028024e75f5`

```dockerfile
```

-	Layers:
	-	`sha256:d6a03a891494b8629e410a2ce93759622b46e8579aa0ebbeb9bc95c90af4965f`  
		Last Modified: Fri, 05 Jun 2026 22:48:03 GMT  
		Size: 12.9 MB (12872490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd0dc5864c754cc8d03ca1e1da29212e79b04c66b4c8d146fe483ad3d85ff33`  
		Last Modified: Fri, 05 Jun 2026 22:48:02 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
