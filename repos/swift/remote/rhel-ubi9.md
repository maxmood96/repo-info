## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:51be0607e15e3bd3d351a75b2d63e16295c1cbc1eef3f7b8e68d2b401dda1695
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:36d6f7987c9783fe84a66594fcc48abe2bb1e605064887dad3e13e70f1c2db81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1227131598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c596441cf31da60df37ad5653babdc79cbe22776dcf43cf0ae6868b503b2c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:51 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 03 Dec 2025 20:39:51 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:53 GMT
COPY dir:e028f696326f03cd7252c4c349f445b8770570e8560a604b425cd138de4f6500 in /      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:53 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:53 GMT
COPY file:3510fe100acabb01d1f82e20899ef080183d1fa839353ecc75b35a4f9f617700 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:54 GMT
COPY file:3510fe100acabb01d1f82e20899ef080183d1fa839353ecc75b35a4f9f617700 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:54 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "org.opencontainers.image.revision"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "build-date"="2025-12-03T20:39:28Z" "org.opencontainers.image.created"="2025-12-03T20:39:28Z" "release"="1764794285"org.opencontainers.image.revision=6ab6aed6d7cb84504700f3d038e41e8b4b3c3116,org.opencontainers.image.created=2025-12-03T20:39:28Z
# Tue, 09 Dec 2025 17:39:29 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:39:29 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:39:29 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 09 Dec 2025 17:39:29 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:39:29 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 09 Dec 2025 17:39:29 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:39:29 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:39:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:29 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:40:06 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 09 Dec 2025 17:40:06 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:d9ce76bfbf66102c69a90574796db9749bc7ac51bea111e75112291f6c0326c5`  
		Last Modified: Wed, 03 Dec 2025 21:13:53 GMT  
		Size: 80.0 MB (80040124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47b38d4a630d0b0d22fb5138c9f74c81832b3924c3fa0e6d9153218a3dc8418`  
		Last Modified: Tue, 09 Dec 2025 17:42:54 GMT  
		Size: 124.7 MB (124711724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c927a14f743d9c57642f67106f7edfd1772177e40f664ffc79768b3311511048`  
		Last Modified: Tue, 09 Dec 2025 17:42:59 GMT  
		Size: 1.0 GB (1022379576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c737d8e050cec7c4b431e14282fa533bd97606129f60a2bb10fb52ccbebffb6d`  
		Last Modified: Tue, 09 Dec 2025 17:42:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:170fd8381176e03b14aa656e3b4671ababe77732734cdaf01df5b102d98a7593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (13002612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7c0d33f960ea7c6305f960cbe5a6b9c3d73e0f71096d53df717d9a649a55cb`

```dockerfile
```

-	Layers:
	-	`sha256:9d6fba1dd0d2ed40254f7da1885aad5fd8a6fd3558dc6c1a1117dc6d5bba336a`  
		Last Modified: Tue, 09 Dec 2025 20:48:53 GMT  
		Size: 13.0 MB (12988170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb6a8e6a5d9130f538080aa849b2a58dee09a1ea6a70683fb2654ef2ae4a683`  
		Last Modified: Tue, 09 Dec 2025 20:48:54 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ce428d846c01994ccd5573f98f0e02d6994b265806ca8c257fafb1992b450172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1214511063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af97d8d483917256ff0cbe8911f6c451c7be859442ae420dd7cc176999188bfd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:44:54 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 03 Dec 2025 20:44:54 GMT
ENV container oci
# Wed, 03 Dec 2025 20:44:57 GMT
COPY dir:eb9bf5494000bc25c9b7b9c079b1fafa2372042b89728acc56982ccb84aecd0f in /      
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:44:57 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:44:57 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:44:58 GMT
COPY file:f4709671a5a80ff0d54c4f0107ef89c6244ef4daa403ef182c946f77eda0aa0f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:44:58 GMT
COPY file:f4709671a5a80ff0d54c4f0107ef89c6244ef4daa403ef182c946f77eda0aa0f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:44:58 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "org.opencontainers.image.revision"="6ab6aed6d7cb84504700f3d038e41e8b4b3c3116" "build-date"="2025-12-03T20:44:35Z" "org.opencontainers.image.created"="2025-12-03T20:44:35Z" "release"="1764794285"org.opencontainers.image.revision=6ab6aed6d7cb84504700f3d038e41e8b4b3c3116,org.opencontainers.image.created=2025-12-03T20:44:35Z
# Tue, 09 Dec 2025 17:39:34 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:39:34 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:39:34 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Tue, 09 Dec 2025 17:39:34 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:39:34 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 09 Dec 2025 17:39:34 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:39:34 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:39:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:34 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:40:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 09 Dec 2025 17:40:14 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:04818a5cef267e6e003591a4574d021a2141ec6ef8efc36216cf70aac950e30b`  
		Last Modified: Wed, 03 Dec 2025 21:16:16 GMT  
		Size: 77.7 MB (77711266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47509ab9113714ba23eb81b69b571e6001899a9b8dab9dfc3c5c334522dae964`  
		Last Modified: Tue, 09 Dec 2025 17:42:53 GMT  
		Size: 118.2 MB (118210315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0be021800d08ec3a81683ff183270fb610f0626b3476b25c44961a5d9d16a2d`  
		Last Modified: Tue, 09 Dec 2025 17:43:01 GMT  
		Size: 1.0 GB (1018589308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f293129ab292d2c497e4dc3eb1cb451eb1415eb2657dde9b14bff9e2566db865`  
		Last Modified: Tue, 09 Dec 2025 17:42:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:b8fd8fed67587ef16559c51c211e34b15e8a2de8093d532de637c808f4c9efae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12875971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbddcd2bc80614b9ce688f237c717ae66d30d4cae3d66b93dc38bdebccd0234`

```dockerfile
```

-	Layers:
	-	`sha256:b802256f7cd9563f492a01e6896944237b089c4156336efcbf0be31b8e122541`  
		Last Modified: Tue, 09 Dec 2025 20:49:05 GMT  
		Size: 12.9 MB (12861413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:956db75231965103a50027125d17073844d143e33d9a1dd2f9d95d9bf29c7c75`  
		Last Modified: Tue, 09 Dec 2025 20:49:06 GMT  
		Size: 14.6 KB (14558 bytes)  
		MIME: application/vnd.in-toto+json
