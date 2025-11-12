## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:d0a19246aacfa03646ccd571a6648e756e5d9a1f89b55ceff33add7fbc3d7d8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:4ec52e476d42920a7c1d21770b7ab15129a1593538a35793f2907c2fe60431c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136817480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f360b43aabd5aad41f2076ea960576107337fbd965d7f58d4563cd1b0e7454a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 03 Nov 2025 14:31:11 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:31:11 GMT
ENV container oci
# Mon, 03 Nov 2025 14:31:13 GMT
COPY dir:79bac1e0bd4a3461e32789ccd5d7d2c6c244ebd79c4f0da6de8bffd3b359be95 in /      
# Mon, 03 Nov 2025 14:31:13 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:31:13 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:31:13 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:31:13 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:31:13 GMT
COPY file:e43846473107cab1071a89f5f522f42f8a8d587809bf13d710ba08955398ce95 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:31:13 GMT
COPY file:e43846473107cab1071a89f5f522f42f8a8d587809bf13d710ba08955398ce95 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:31:14 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="00c43f8dc3947b5f7b934623bc5ac982b185c750" "org.opencontainers.image.revision"="00c43f8dc3947b5f7b934623bc5ac982b185c750" "build-date"="2025-11-03T14:30:55Z" "release"="1762180182"org.opencontainers.image.revision=00c43f8dc3947b5f7b934623bc5ac982b185c750
# Wed, 12 Nov 2025 00:30:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 12 Nov 2025 00:30:32 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 12 Nov 2025 00:30:32 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 12 Nov 2025 00:30:32 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 12 Nov 2025 00:30:32 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Wed, 12 Nov 2025 00:30:32 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Wed, 12 Nov 2025 00:30:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 12 Nov 2025 00:30:32 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 12 Nov 2025 00:30:32 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:eaacaedf7cb8afeed496639879c6c7e8c24cff479ee4bcfe75da992fadf28ef1`  
		Last Modified: Tue, 11 Nov 2025 18:09:16 GMT  
		Size: 80.0 MB (79987981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e2a2edb9404eb16cf81f49ebfa0aef7839fe653010f61558ee7c9edfc099ff`  
		Last Modified: Wed, 12 Nov 2025 00:31:11 GMT  
		Size: 56.8 MB (56829499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:3e865f811261d55d63483028072374fceb2e57bf1237eaba2214e91569f7a98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40afd60d7ce6bb8de812083b4f510d507605a107d7df7f0900404108b2bc1c05`

```dockerfile
```

-	Layers:
	-	`sha256:4c55b6bbaadb26cdedd3db528abbd78f3635bf70365fe4d3ba29c72f3558dfdd`  
		Last Modified: Wed, 12 Nov 2025 02:48:51 GMT  
		Size: 6.4 MB (6409536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a727a2bfbef2d825fa3c880ce2be2d84195b2bc430236c7e26eaee325d187e85`  
		Last Modified: Wed, 12 Nov 2025 02:48:52 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:437387ca95553c1c0e42da8370978a10f227e58c41509ba57a464661f4cdd6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133104640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac997713e9f8c825ecfbf9180ecae3ac44d78e039197804b912e3a4db5215d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 03 Nov 2025 14:42:39 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:42:39 GMT
ENV container oci
# Mon, 03 Nov 2025 14:42:42 GMT
COPY dir:c22d670f25ba5cde2c2d8d1688af2de21ea1e374441f45369132bc4e5f49deb3 in /      
# Mon, 03 Nov 2025 14:42:42 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:42:42 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:42:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:42:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:42:43 GMT
COPY file:1d95fcc56c0aff87194ee5f83332302b3ada28688b0fd6b5cbc3a2fcea0dc72d in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:42:43 GMT
COPY file:1d95fcc56c0aff87194ee5f83332302b3ada28688b0fd6b5cbc3a2fcea0dc72d in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:42:43 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="00c43f8dc3947b5f7b934623bc5ac982b185c750" "org.opencontainers.image.revision"="00c43f8dc3947b5f7b934623bc5ac982b185c750" "build-date"="2025-11-03T14:42:16Z" "release"="1762180182"org.opencontainers.image.revision=00c43f8dc3947b5f7b934623bc5ac982b185c750
# Wed, 12 Nov 2025 00:29:54 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 12 Nov 2025 00:29:54 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 12 Nov 2025 00:29:54 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 12 Nov 2025 00:29:54 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 12 Nov 2025 00:29:54 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Wed, 12 Nov 2025 00:29:54 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Wed, 12 Nov 2025 00:29:54 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 12 Nov 2025 00:29:54 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 12 Nov 2025 00:29:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:cbe4d6f990609a3a7d77b5bbff294d941e5036b164ba7ffb504bd63bb950a096`  
		Last Modified: Tue, 11 Nov 2025 18:09:16 GMT  
		Size: 77.7 MB (77714391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ce5554ce9b1158e18b8f371be8371dc874d66835e50f07bdcd26b4a2e85da`  
		Last Modified: Wed, 12 Nov 2025 00:30:26 GMT  
		Size: 55.4 MB (55390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:340f261f2bcd38f2db80f3edcb0c1d99f4a3f94869512fd3f4c62bcf85a54997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc65514ccf482c290f99ab875ba0a40f5aace02633f12a9053e776e3cd0fd965`

```dockerfile
```

-	Layers:
	-	`sha256:e55e15161b059416102b46e35e00206c2424a1bca5bdce3316f1355e96b70928`  
		Last Modified: Wed, 12 Nov 2025 02:48:57 GMT  
		Size: 6.4 MB (6405339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0256018f15382e33287353b8a9b312bbb6707b3453fd03022513fb243a39f5`  
		Last Modified: Wed, 12 Nov 2025 02:48:58 GMT  
		Size: 11.6 KB (11554 bytes)  
		MIME: application/vnd.in-toto+json
