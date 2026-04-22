## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:3560a17cf36f26bc4779563cf0183c81ef99a99d7c550b98a17e4c245d4c29c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:7a3482086e63b6e03d9c3677692c0eb8dce108c5690c7fe56f69e0f645bb71e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137600829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d658fdaae59ccc3aca1c02aa4d69928bc34d377d23fac920f3fa58befe01881`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:03:07 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 22 Apr 2026 05:03:07 GMT
ENV container oci
# Wed, 22 Apr 2026 05:03:09 GMT
COPY dir:3ff2d39ae06fb20eccb68f3beaa79fe1e9823a8c7eb1e60e613146e57008c0d4 in /      
# Wed, 22 Apr 2026 05:03:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:03:09 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:03:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:03:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:03:09 GMT
COPY file:3a9736838f6dce34051adcc517f0e1bb8bb71915214cae605d0267eddbd9e63b in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:03:10 GMT
COPY file:3a9736838f6dce34051adcc517f0e1bb8bb71915214cae605d0267eddbd9e63b in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:03:10 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0809ab29dc0248030bc33288f153b9d237dc704c" "org.opencontainers.image.revision"="0809ab29dc0248030bc33288f153b9d237dc704c" "build-date"="2026-04-22T05:02:44Z" "org.opencontainers.image.created"="2026-04-22T05:02:44Z" "release"="1776834047"org.opencontainers.image.revision=0809ab29dc0248030bc33288f153b9d237dc704c,org.opencontainers.image.created=2026-04-22T05:02:44Z
# Wed, 22 Apr 2026 18:20:30 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 22 Apr 2026 18:20:30 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 22 Apr 2026 18:20:30 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 22 Apr 2026 18:20:30 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 22 Apr 2026 18:20:30 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Wed, 22 Apr 2026 18:20:30 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Wed, 22 Apr 2026 18:20:30 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 18:20:30 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 18:20:30 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:15ff23c3b2e178cb3ea1caa12f6fbe9ba23536bf0d0c938ef17359ac61bb5174`  
		Last Modified: Wed, 22 Apr 2026 05:54:32 GMT  
		Size: 80.0 MB (79952719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04cafd6fba8435516b6a99453aaceedf3f9db0970063134edda45c72a1aec1d`  
		Last Modified: Wed, 22 Apr 2026 18:20:46 GMT  
		Size: 57.6 MB (57648110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:bd6fb5b8bc7e05bf86efff44b0888d95454ea8c18ab668f9774927d9e67f6f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6417836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3192db66c69d37d80979a96a0fb9ef9456b8609b753235a62e718a5064cd67`

```dockerfile
```

-	Layers:
	-	`sha256:cbcdea5a681fefafe92bb527d2d8c425d16ab3cd56fe8b35f81ee80b16586d2b`  
		Last Modified: Wed, 22 Apr 2026 18:20:44 GMT  
		Size: 6.4 MB (6406368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d35f23978e34eccef9908a53fa4a50aba11b2887a280d3058d2f3d0d41cb12`  
		Last Modified: Wed, 22 Apr 2026 18:20:43 GMT  
		Size: 11.5 KB (11468 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:65127c3f88c292a4363cb33cf8e9d167fa2f2062d970288b3b56b3c771e02d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133741313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a601809780891711fa57cfd8048c13ecc7e71f85158743b315c2c20e7fa88c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:05:04 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 22 Apr 2026 05:05:04 GMT
ENV container oci
# Wed, 22 Apr 2026 05:05:07 GMT
COPY dir:fe2980062460e3bd4a122856fdac1c3ffa44768921f36afe9a319714831cf225 in /      
# Wed, 22 Apr 2026 05:05:07 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:05:07 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:05:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:05:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:05:08 GMT
COPY file:5a90691d0ef9b2fd3584bc1f13654e876db73891f849088e105da14b4e634263 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:08 GMT
COPY file:5a90691d0ef9b2fd3584bc1f13654e876db73891f849088e105da14b4e634263 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:09 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0809ab29dc0248030bc33288f153b9d237dc704c" "org.opencontainers.image.revision"="0809ab29dc0248030bc33288f153b9d237dc704c" "build-date"="2026-04-22T05:04:47Z" "org.opencontainers.image.created"="2026-04-22T05:04:47Z" "release"="1776834047"org.opencontainers.image.revision=0809ab29dc0248030bc33288f153b9d237dc704c,org.opencontainers.image.created=2026-04-22T05:04:47Z
# Wed, 22 Apr 2026 18:19:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 22 Apr 2026 18:19:55 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 22 Apr 2026 18:19:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 22 Apr 2026 18:19:55 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 22 Apr 2026 18:19:55 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Wed, 22 Apr 2026 18:19:55 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Wed, 22 Apr 2026 18:19:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 18:19:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 18:19:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:3bec630204a194f3a0b7caaca2685445f836c478dcaeab77c747628d52fb567c`  
		Last Modified: Wed, 22 Apr 2026 05:57:16 GMT  
		Size: 77.7 MB (77690700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135924beb78717841bcd1ca5c00da4677a4ce548cbc509051bb31779a2f2b3ee`  
		Last Modified: Wed, 22 Apr 2026 18:20:13 GMT  
		Size: 56.1 MB (56050613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:acc4fd6340a3d5848508d1df47416e2e298db8c15f2ea82a152fb3154d6268eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6413721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b207113c3e48a37f9eb7289455261d1edb27e34e9b06a4a56bda082e4af4dff`

```dockerfile
```

-	Layers:
	-	`sha256:cd4fc459a5b905558495e35e48eff1c0582711fd60cb26eafc96baea3faeaa67`  
		Last Modified: Wed, 22 Apr 2026 18:20:10 GMT  
		Size: 6.4 MB (6402167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bc8bef6728ece8e934725cefe2d207018c479236fd815eddb09f8600e1d802`  
		Last Modified: Wed, 22 Apr 2026 18:20:10 GMT  
		Size: 11.6 KB (11554 bytes)  
		MIME: application/vnd.in-toto+json
