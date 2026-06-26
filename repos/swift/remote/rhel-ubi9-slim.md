## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:c83367d3dcfdeb905ab13854c43d73f636d03a37fda61b0c3d1925cf73d0d219
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:7cb72c85a1d93c900a57fa225807ec736cf7a030ffae4b2c72da5a85b60211ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138747398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a235e947f2fb645abbbebc1b98404cd01ea9cd4ee00506c5652322068019c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:38:43 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 25 Jun 2026 05:38:43 GMT
ENV container oci
# Thu, 25 Jun 2026 05:38:45 GMT
COPY dir:45515cc5ec4c8c670413a5c6b236985cfad9a25da303502cddf18e5647660bcc in /      
# Thu, 25 Jun 2026 05:38:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:38:45 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:38:45 GMT
COPY dir:20961462c5205530b67f6f5f7c5374ed5e9ac3b372062cbe2067844563d2515d in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:38:45 GMT
COPY dir:20961462c5205530b67f6f5f7c5374ed5e9ac3b372062cbe2067844563d2515d in /root/buildinfo/      
# Thu, 25 Jun 2026 05:38:46 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:38:13Z" "org.opencontainers.image.revision"="5f0052ae5ad6e692325f20b47f9a15830ba43ef2" "build-date"="2026-06-25T05:38:13Z" "architecture"="x86_64" "vcs-ref"="5f0052ae5ad6e692325f20b47f9a15830ba43ef2" "vcs-type"="git" "release"="1782365825"org.opencontainers.image.created=2026-06-25T05:38:13Z,org.opencontainers.image.revision=5f0052ae5ad6e692325f20b47f9a15830ba43ef2
# Thu, 25 Jun 2026 23:29:03 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 25 Jun 2026 23:29:03 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 25 Jun 2026 23:29:03 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 25 Jun 2026 23:29:03 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 25 Jun 2026 23:29:03 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Thu, 25 Jun 2026 23:29:03 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Thu, 25 Jun 2026 23:29:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 25 Jun 2026 23:29:03 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 25 Jun 2026 23:29:03 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:a65b1d5fa71f2275b83830542c74d937ba4151138631910bd375d577f8ceeed8`  
		Last Modified: Thu, 25 Jun 2026 06:10:13 GMT  
		Size: 80.5 MB (80532710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f406dfdba0ba04614676f01114da8af86ac583d376726a254ea6272cd863c750`  
		Last Modified: Thu, 25 Jun 2026 23:29:19 GMT  
		Size: 58.2 MB (58214688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:080acc8f4a97853fcc909381941982bdca94b781b4d8dabbf31b77c008f4ec93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ff8f87271a5c843a22733e1d8076e852a2a54bc7d00d3ba0911243a1f98dcb`

```dockerfile
```

-	Layers:
	-	`sha256:6a7304acf3844188c43c9559ad17aeee363626ee97285b786542a777b45829c9`  
		Last Modified: Thu, 25 Jun 2026 23:29:16 GMT  
		Size: 6.4 MB (6407893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3ad91290268d94015a26e8960295a3d8317f53f16c55d75b57fe41452bfcaf`  
		Last Modified: Thu, 25 Jun 2026 23:29:16 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:e272a72668d5f33e200f40e477f8abb3ed6ca7db5ed1c7f8d3e5c67124df2719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134654125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116cff749d56f8d5b653cebb4931544999b8398f6c522a929d64ed9cb4af3f5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:41:43 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 25 Jun 2026 05:41:43 GMT
ENV container oci
# Thu, 25 Jun 2026 05:41:46 GMT
COPY dir:9ffdd7d31cae6d6146f0e7f752e4ce86c9534ba4a8482cdc1e39e03d277ebb93 in /      
# Thu, 25 Jun 2026 05:41:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:41:46 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:41:46 GMT
COPY dir:aa6784c3342804d758e3d58961fa212cb8d9e1ad20a025c6ff09d109c60fc18c in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:41:46 GMT
COPY dir:aa6784c3342804d758e3d58961fa212cb8d9e1ad20a025c6ff09d109c60fc18c in /root/buildinfo/      
# Thu, 25 Jun 2026 05:41:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:41:19Z" "org.opencontainers.image.revision"="5f0052ae5ad6e692325f20b47f9a15830ba43ef2" "build-date"="2026-06-25T05:41:19Z" "architecture"="aarch64" "vcs-ref"="5f0052ae5ad6e692325f20b47f9a15830ba43ef2" "vcs-type"="git" "release"="1782365825"org.opencontainers.image.created=2026-06-25T05:41:19Z,org.opencontainers.image.revision=5f0052ae5ad6e692325f20b47f9a15830ba43ef2
# Thu, 25 Jun 2026 23:28:48 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 25 Jun 2026 23:28:48 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 25 Jun 2026 23:28:48 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 25 Jun 2026 23:28:48 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 25 Jun 2026 23:28:48 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Thu, 25 Jun 2026 23:28:48 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Thu, 25 Jun 2026 23:28:48 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 25 Jun 2026 23:28:48 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 25 Jun 2026 23:28:48 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:f00a3ea30fea862d594c88740f011c234eb0b745138910c83abb92b28517593d`  
		Last Modified: Thu, 25 Jun 2026 06:10:23 GMT  
		Size: 78.1 MB (78143463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa132c88521e7c01d63ab0be8ed62e7ef125254f3fa5c0759772941d63606c35`  
		Last Modified: Thu, 25 Jun 2026 23:29:05 GMT  
		Size: 56.5 MB (56510662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:770f345be05d5f159379d9d85f2b5f1a7bd4003e52d75b1768f2ecead90ead83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6415246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d728184e26df6cfeeaeb2f60ec73d44ca5670c9faf9bee0d4551219b51687f1`

```dockerfile
```

-	Layers:
	-	`sha256:a844c029ce4ccced5c99224dc5728f43bc9c05ff48744ac10a74e0d53e3cb690`  
		Last Modified: Thu, 25 Jun 2026 23:29:03 GMT  
		Size: 6.4 MB (6403692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66e53d02004b1ec4c63143b5b291fd10fc812144b666797e01a6087dbed8828`  
		Last Modified: Thu, 25 Jun 2026 23:29:02 GMT  
		Size: 11.6 KB (11554 bytes)  
		MIME: application/vnd.in-toto+json
