## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:587d1621f196e982f06a1dc9a2a3ad870eaf3adf3db9a2ff48607f605edd5d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:749527dce5f8cd882bf83d61fe3486e785345eb83ed840192e109c2571710236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136426894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c6839daa90bc2c4d294a9736d8975b35025d6e08b7d126b0a0c444e37d85c7`
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
# Thu, 04 Dec 2025 19:50:04 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 04 Dec 2025 19:50:04 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 04 Dec 2025 19:50:04 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 04 Dec 2025 19:50:04 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 04 Dec 2025 19:50:04 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Thu, 04 Dec 2025 19:50:04 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Thu, 04 Dec 2025 19:50:04 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 Dec 2025 19:50:04 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 Dec 2025 19:50:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:d9ce76bfbf66102c69a90574796db9749bc7ac51bea111e75112291f6c0326c5`  
		Last Modified: Wed, 03 Dec 2025 21:13:53 GMT  
		Size: 80.0 MB (80040124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a503d991f16659b0c57e19c3e84c8abb2b35946f0685c4483166139fb8379c`  
		Last Modified: Thu, 04 Dec 2025 19:50:34 GMT  
		Size: 56.4 MB (56386770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:86f0596c6139d564f63dc44098a68c1404e3a57211926dce5dc1505b79165811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6421032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf5402415c1ed0c4b450f3fc68ba912c1156d679b847972585f612d41c15454`

```dockerfile
```

-	Layers:
	-	`sha256:74f41fafa6cc1f8646a0c5672a865417b16654bac3f8bb7748372a07b6d95344`  
		Last Modified: Thu, 04 Dec 2025 20:48:48 GMT  
		Size: 6.4 MB (6409564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841bee55a7f47836a26e4256fa73504649ce20282b4e35cf95fe788cfb033652`  
		Last Modified: Thu, 04 Dec 2025 20:48:49 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c340281dbd3aa70f33c6f542ca4779b0ae7ba4f11f45036011057bbe776d9d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132648636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dcf0957bfd26ea4d2b818604046ed3e30c04e8559d310c728173e0f4f86518`
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
# Thu, 04 Dec 2025 19:50:27 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 04 Dec 2025 19:50:27 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 04 Dec 2025 19:50:27 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 04 Dec 2025 19:50:27 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 04 Dec 2025 19:50:27 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Thu, 04 Dec 2025 19:50:27 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Thu, 04 Dec 2025 19:50:27 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 Dec 2025 19:50:27 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 Dec 2025 19:50:27 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:04818a5cef267e6e003591a4574d021a2141ec6ef8efc36216cf70aac950e30b`  
		Last Modified: Wed, 03 Dec 2025 21:16:16 GMT  
		Size: 77.7 MB (77711266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f761bdd24460fbb7d7591dd4f7e719a88974329582cfc744a34b339ce9ef6c9f`  
		Last Modified: Thu, 04 Dec 2025 19:50:54 GMT  
		Size: 54.9 MB (54937370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:183bc5febdcdd44c799bfe01e6f6b894deab16c197691dc050ea1ccbcbb1b6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063768a7a10848109f539d5d285595ea9088b3d16505fa24faa9730f050d4379`

```dockerfile
```

-	Layers:
	-	`sha256:bf5d6a3831d23d2a9d2ecaa587a44fc017995e932dfedc45a67878bf4f0fa890`  
		Last Modified: Thu, 04 Dec 2025 20:48:56 GMT  
		Size: 6.4 MB (6405367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253f4b1d5558134361bd572ea10294bceecee851a3d7e3b4cd858e618ac741cc`  
		Last Modified: Thu, 04 Dec 2025 20:48:57 GMT  
		Size: 11.6 KB (11554 bytes)  
		MIME: application/vnd.in-toto+json
