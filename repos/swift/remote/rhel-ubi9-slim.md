## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:cafeb9a6c167fda767c053deebaf82771d1a7e912abebe965fb3ca70cc795900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:fc33d32e0b71ea96eef5338a0ef9b40baccf90249d46e0baa12c567d4bcb8ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137595197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f571c67e65a77aa641d9a3b489e2506e39674fecf93cd65fe5b5792e4023fea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 May 2026 09:01:01 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:01:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:01:01 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 09:01:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:01:01 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 12 May 2026 09:01:01 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:01:01 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:01:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 12 May 2026 09:01:01 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:01:01 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 12 May 2026 09:01:01 GMT
ENV container oci
# Tue, 12 May 2026 09:01:03 GMT
COPY dir:dc2903ccadfb17708e4f3606c837c7a2dcaefcf45e7650b8e21eaa8685308f51 in /      
# Tue, 12 May 2026 09:01:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:01:03 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:01:03 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:01:03 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:01:03 GMT
COPY file:b5436b9382ece22e983fc2ba25df27bf2a379c73c669aa0a75af228b6c9148f3 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:01:03 GMT
COPY file:b5436b9382ece22e983fc2ba25df27bf2a379c73c669aa0a75af228b6c9148f3 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:01:04 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa4fa8db6226e15f9e1c73bc3815043f0c0a439d" "org.opencontainers.image.revision"="aa4fa8db6226e15f9e1c73bc3815043f0c0a439d" "build-date"="2026-05-12T09:00:42Z" "org.opencontainers.image.created"="2026-05-12T09:00:42Z" "release"="1778576335"org.opencontainers.image.revision=aa4fa8db6226e15f9e1c73bc3815043f0c0a439d,org.opencontainers.image.created=2026-05-12T09:00:42Z
# Tue, 12 May 2026 23:37:09 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 12 May 2026 23:37:09 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 12 May 2026 23:37:09 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 12 May 2026 23:37:09 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 12 May 2026 23:37:09 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Tue, 12 May 2026 23:37:09 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Tue, 12 May 2026 23:37:09 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 May 2026 23:37:09 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 12 May 2026 23:37:09 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:b66ab30abd6c3aa6e70bb84e4b3f0025035459b0fa3fc0d28bb37e057cde7b50`  
		Last Modified: Tue, 12 May 2026 10:09:26 GMT  
		Size: 80.0 MB (79954768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a6e5ee42125aac8b6d4a19347f24b42fe7c7e6b8732b4ebf9e1db626763790`  
		Last Modified: Tue, 12 May 2026 23:37:24 GMT  
		Size: 57.6 MB (57640429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d7c2b50e48a41dd20528e15cdbfcb0a3c58ec7a7ac2536f896cea4258985bb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6417846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5145d5e5321ac75a2b7673d581031be1659043d90bd164c7fd87bd1e88b3adaa`

```dockerfile
```

-	Layers:
	-	`sha256:aa910ad764f1bb9f58dddbf4fa8154ae860d80b60824bc92d98f80e26ca037a0`  
		Last Modified: Tue, 12 May 2026 23:37:22 GMT  
		Size: 6.4 MB (6406378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4e2c709a3b1f9a52c8558cd070a5619eed1d9e76e36923fb48420c69b5718e`  
		Last Modified: Tue, 12 May 2026 23:37:22 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:45946118c9331a120358b6613863cf4ee4834bd2093d5126d7d32920fe348e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133710560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1f20b7537b9e43c51bc329f8712627879ab6ee174092f902aaab96a13098b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 May 2026 09:02:53 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:02:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:02:54 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 09:02:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:02:54 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 12 May 2026 09:02:54 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:02:54 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:02:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 12 May 2026 09:02:54 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:02:54 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 12 May 2026 09:02:54 GMT
ENV container oci
# Tue, 12 May 2026 09:02:57 GMT
COPY dir:79843c7a11b82518bdac5c3918cb04f59fa9fd5e588d4ad937331cdae04daaf1 in /      
# Tue, 12 May 2026 09:02:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:02:57 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:02:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:02:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:02:57 GMT
COPY file:09ce45df509134aee3aee77e0b739651c99a05567d56c48d6dfcbc2b68737b85 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:02:57 GMT
COPY file:09ce45df509134aee3aee77e0b739651c99a05567d56c48d6dfcbc2b68737b85 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:02:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa4fa8db6226e15f9e1c73bc3815043f0c0a439d" "org.opencontainers.image.revision"="aa4fa8db6226e15f9e1c73bc3815043f0c0a439d" "build-date"="2026-05-12T09:02:37Z" "org.opencontainers.image.created"="2026-05-12T09:02:37Z" "release"="1778576335"org.opencontainers.image.revision=aa4fa8db6226e15f9e1c73bc3815043f0c0a439d,org.opencontainers.image.created=2026-05-12T09:02:37Z
# Wed, 13 May 2026 18:06:12 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:06:12 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:06:12 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:06:12 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 13 May 2026 18:06:12 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:06:12 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:06:12 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:06:12 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:06:12 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:66c47a7ff47768837c084e8a7889a768b3f736f72ddb31d8896c4c5112926914`  
		Last Modified: Tue, 12 May 2026 10:02:33 GMT  
		Size: 77.7 MB (77744299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b9706c477392330f02c740e144f915380fd3eeb58c7bb7466c769daccdf37`  
		Last Modified: Wed, 13 May 2026 18:06:28 GMT  
		Size: 56.0 MB (55966261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:131a74cef892a1ce939df1678a57e91881697cf1a8cff18b69d8effb24eac931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bcf8f3f03db228b01160b8003d7819daf56d46d6316be54f1bea9ed44234b5`

```dockerfile
```

-	Layers:
	-	`sha256:a324018fc429f86ffc32dd3acdda93e3d843d4ad06123994efef424329d38f4b`  
		Last Modified: Wed, 13 May 2026 18:06:27 GMT  
		Size: 6.4 MB (6402177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3eabf546b452a44cee67e0e66ee61feecd3f3843957609dc81fdbf6ff3c1a3`  
		Last Modified: Wed, 13 May 2026 18:06:26 GMT  
		Size: 11.6 KB (11554 bytes)  
		MIME: application/vnd.in-toto+json
