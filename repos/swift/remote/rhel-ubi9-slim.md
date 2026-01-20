## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:796e1b6b4a10cf82251a5dcc7833c9088e4d6f280922f2b6d83aa88e1d362cc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:a583d1e61264ebaef95776aaaa4447972ef3d7f2e0f5425193f52bc9c7650817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136443718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cbf736c554bd7d02429a2598782b5a4ea31ffab85854943c35f64c3f321be5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 06 Jan 2026 04:47:12 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 06 Jan 2026 04:47:12 GMT
ENV container oci
# Tue, 06 Jan 2026 04:47:14 GMT
COPY dir:318c5e01a98580bc429e98aaa90e4f574ec5db7328fe112be4269f43263e9ad8 in /      
# Tue, 06 Jan 2026 04:47:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 06 Jan 2026 04:47:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 04:47:14 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 06 Jan 2026 04:47:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 06 Jan 2026 04:47:15 GMT
COPY file:5940939e34801a2e8eafa07a5abd899f478da8f42ff30032cfba5bdfd20ff925 in /usr/share/buildinfo/labels.json      
# Tue, 06 Jan 2026 04:47:15 GMT
COPY file:5940939e34801a2e8eafa07a5abd899f478da8f42ff30032cfba5bdfd20ff925 in /root/buildinfo/labels.json      
# Tue, 06 Jan 2026 04:47:16 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3e794df56e99dd97dc87933feb0fbd960b8c9ca7" "org.opencontainers.image.revision"="3e794df56e99dd97dc87933feb0fbd960b8c9ca7" "build-date"="2026-01-06T04:46:51Z" "org.opencontainers.image.created"="2026-01-06T04:46:51Z" "release"="1767674301"org.opencontainers.image.revision=3e794df56e99dd97dc87933feb0fbd960b8c9ca7,org.opencontainers.image.created=2026-01-06T04:46:51Z
# Tue, 06 Jan 2026 19:01:48 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 06 Jan 2026 19:01:48 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 06 Jan 2026 19:01:48 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 06 Jan 2026 19:01:48 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 06 Jan 2026 19:01:48 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Tue, 06 Jan 2026 19:01:48 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Tue, 06 Jan 2026 19:01:48 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 06 Jan 2026 19:01:48 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 06 Jan 2026 19:01:48 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:34b5c851d9cf523f162ceb72c260f1c6d1e556f8f4422e15258572766f2afc28`  
		Last Modified: Tue, 06 Jan 2026 10:48:16 GMT  
		Size: 80.0 MB (80022799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d552fdfe27ed8fb43afb05be10d899be8f74d914e34e0b5e17312ac16297bd5`  
		Last Modified: Tue, 06 Jan 2026 19:02:03 GMT  
		Size: 56.4 MB (56420919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:2f8b2eece556567cbe412e82ee46f62d6f79157952ec6c4584b11024c3591916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6417700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300630dff9058009e2ef860afcd04f697e07df517ccb1f418d3c5b8125b2a521`

```dockerfile
```

-	Layers:
	-	`sha256:d69479c2283e4cc907a81b6ccdafff292ec72289a01ac1b583d219392e5934a6`  
		Last Modified: Tue, 06 Jan 2026 19:02:02 GMT  
		Size: 6.4 MB (6406232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eee83706f942e98f5af375c1ed7ca91d3ba0a3eafea1a23e5c027b50aeb0804`  
		Last Modified: Tue, 06 Jan 2026 20:48:54 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:7108797acbb717acd4dda6b3a94364578bbf4f4ddd0d4a7d6ff4b408b86ebb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132749513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a07de1818ebf954f3c4c59c9b2de52ea6db71bf686dcaff16994bbdb882d56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL io.openshift.expose-services=""
# Tue, 06 Jan 2026 05:02:25 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 06 Jan 2026 05:02:25 GMT
ENV container oci
# Tue, 06 Jan 2026 05:02:28 GMT
COPY dir:2a54c6bf5f67e50c61d6298985c7326aff278b3739d27bbd8cc6d9ae452931aa in /      
# Tue, 06 Jan 2026 05:02:28 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 06 Jan 2026 05:02:28 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 05:02:28 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 06 Jan 2026 05:02:28 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 06 Jan 2026 05:02:28 GMT
COPY file:2e088c8cf0985c3349b36361db393a050efdd599df5c058f5c3a73f85710c570 in /usr/share/buildinfo/labels.json      
# Tue, 06 Jan 2026 05:02:28 GMT
COPY file:2e088c8cf0985c3349b36361db393a050efdd599df5c058f5c3a73f85710c570 in /root/buildinfo/labels.json      
# Tue, 06 Jan 2026 05:02:29 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3e794df56e99dd97dc87933feb0fbd960b8c9ca7" "org.opencontainers.image.revision"="3e794df56e99dd97dc87933feb0fbd960b8c9ca7" "build-date"="2026-01-06T05:02:04Z" "org.opencontainers.image.created"="2026-01-06T05:02:04Z" "release"="1767674301"org.opencontainers.image.revision=3e794df56e99dd97dc87933feb0fbd960b8c9ca7,org.opencontainers.image.created=2026-01-06T05:02:04Z
# Tue, 06 Jan 2026 18:58:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 06 Jan 2026 18:58:43 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 06 Jan 2026 18:58:43 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 06 Jan 2026 18:58:43 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 06 Jan 2026 18:58:43 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Tue, 06 Jan 2026 18:58:43 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Tue, 06 Jan 2026 18:58:43 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 06 Jan 2026 18:58:43 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 06 Jan 2026 18:58:43 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:6cc4ae3ba77de579b57b6f5412fd695aeeaea1941ffa7497e25c0821c0d54c93`  
		Last Modified: Tue, 06 Jan 2026 09:04:12 GMT  
		Size: 77.8 MB (77769327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5a7d478507b54fcb924659f481250b81485d2fc6e08db2466099b7e1022602`  
		Last Modified: Tue, 06 Jan 2026 18:59:13 GMT  
		Size: 55.0 MB (54980186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:2f7f34908989a472708ad4d889bd70a1de96c346de078c88268b848ced4592e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65bf34d490571677a11d2651607c67172db2eccf69ce5429b13093108a14f2f`

```dockerfile
```

-	Layers:
	-	`sha256:79b498e0003d25820243bcd4db78204abc1269b7b90605a959e272712bc481db`  
		Last Modified: Tue, 06 Jan 2026 18:58:58 GMT  
		Size: 6.4 MB (6402031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03ca6a86bf03128ecd67f73afea188192720dfd47fb2a6ae16c17b67095f760`  
		Last Modified: Tue, 06 Jan 2026 20:49:03 GMT  
		Size: 11.6 KB (11554 bytes)  
		MIME: application/vnd.in-toto+json
