## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:57530176e6ea13eac4236605e1cb819f23a603772d6eb05824aa7e94d360a237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:68082580dfa1bdfc451d6a6e5df419a8730d3d683acdaacdb5088658c667ed0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138769695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e80df48ddfe61dc422e673b7d1eb0c08a80bc7233fa29a826f96b5dafddec8e`
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
# Tue, 30 Jun 2026 18:57:26 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:57:26 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:57:26 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:57:26 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 30 Jun 2026 18:57:26 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:57:26 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:57:26 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:57:26 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:57:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:a65b1d5fa71f2275b83830542c74d937ba4151138631910bd375d577f8ceeed8`  
		Last Modified: Thu, 25 Jun 2026 06:10:13 GMT  
		Size: 80.5 MB (80532710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ad7885f5bfc8679da72e47912c92139e63ef98007f542f4da40649d5fde3d`  
		Last Modified: Tue, 30 Jun 2026 18:57:42 GMT  
		Size: 58.2 MB (58236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:e18ecbc0ccbac5aed96c1df02481083eec2c4f8936c9e1b36f04841370bc8d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6419361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04f1fc1e343068d75431a5df361872dcc68c6b3ab6156927b7894c7fca6347d`

```dockerfile
```

-	Layers:
	-	`sha256:334b4a259ea19e86bcecb4c148cc27b5d2933097e9153c43ec66c35c9ae4a37c`  
		Last Modified: Tue, 30 Jun 2026 18:57:41 GMT  
		Size: 6.4 MB (6407893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778b7652d5c8c4b5f31fd49db1cd40d357dfe454fed7712bd5c6f1a72c1b68e9`  
		Last Modified: Tue, 30 Jun 2026 18:57:40 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b9c2b9c9c83985221a66c088d2c73dc44faac7ecef5f1ac06352dc80b6cbd4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134638589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2270b883722524eeceb0e885a2d48bd913bd4dfc9492edd43e19b5589bfcd9`
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
# Tue, 30 Jun 2026 18:57:11 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:57:11 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:57:11 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:57:11 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 30 Jun 2026 18:57:11 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:57:11 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:57:11 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:57:11 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:57:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:f00a3ea30fea862d594c88740f011c234eb0b745138910c83abb92b28517593d`  
		Last Modified: Thu, 25 Jun 2026 06:10:23 GMT  
		Size: 78.1 MB (78143463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701c77bfdb175f62b0b8fd742964abf203f8ffd24ce1fbdb8624ce067d378d19`  
		Last Modified: Tue, 30 Jun 2026 18:57:27 GMT  
		Size: 56.5 MB (56495126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:dcc4b55ef65a1aaf01c66b5db0b29f4448bfa7ba86f3f47cbda074f1181ba6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6415245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92ac799fa8b301412eeaa1093f4a75c611bcf10c27a3099cb41733e03a0e9c5`

```dockerfile
```

-	Layers:
	-	`sha256:3bc4665e4e212970e77c494d419bfef71a515bd7c8d9cd96efd707489f9c4503`  
		Last Modified: Tue, 30 Jun 2026 18:57:25 GMT  
		Size: 6.4 MB (6403692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03e6511a1cbfaa27977b99b6cffd7fedb89d9f56e5d76d5f96154fa141adf49`  
		Last Modified: Tue, 30 Jun 2026 18:57:25 GMT  
		Size: 11.6 KB (11553 bytes)  
		MIME: application/vnd.in-toto+json
