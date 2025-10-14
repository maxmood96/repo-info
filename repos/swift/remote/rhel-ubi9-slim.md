## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:bbb26afae838af28751f257e6e406d3ab46365f4e77a5b5cb021264f6fa2bab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:71b12d143b418ad701c87c035ad197fe74713580dbfaf176778a235e1166ae37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135571799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb59515e3bd6a5aea340a0dd69bf260d0e38bcadeb47d536877064679965dd26`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 15 Sep 2025 22:15:37 GMT
ENV container oci
# Mon, 15 Sep 2025 22:15:37 GMT
COPY dir:91d00d24ce3ba29551746ee5faca2e3a563eef65ecd488882ee5f2d4f984589d in /      
# Mon, 15 Sep 2025 22:15:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Sep 2025 22:15:37 GMT
CMD ["/bin/bash"]
# Mon, 15 Sep 2025 22:15:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Sep 2025 22:15:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Sep 2025 22:15:37 GMT
COPY file:a782d4cd79a0c61643bc1cbf3cd5798a42f1495fe330dde8598373d62cac62dd in /root/buildinfo/labels.json      
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="60d587d1286655c5e777e63959aaae224123ea95" "org.opencontainers.image.revision"="60d587d1286655c5e777e63959aaae224123ea95" "build-date"="2025-10-13T07:36:46Z" "release"="1760340943"org.opencontainers.image.revision=60d587d1286655c5e777e63959aaae224123ea95
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:35d6a5cce6a146ea7213377edde7d1d27f34dda18ce9fac98ea2ab40a6b110f6`  
		Last Modified: Mon, 13 Oct 2025 08:55:32 GMT  
		Size: 79.6 MB (79593305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da113cdb58a1bf592b8f682dcb5293978f76cc551438afe998fe28042ce4f9ab`  
		Last Modified: Tue, 14 Oct 2025 17:58:17 GMT  
		Size: 56.0 MB (55978494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:8a601d16b5880792951dc0029758d0440006ec7460cbefb2f24ca5f1d1d9f5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6412754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7b49746e2dc0f1d4764d5168b05732afb33830e8d35e33dd044548c6f1489`

```dockerfile
```

-	Layers:
	-	`sha256:e7fb52b512961fcb4ec9bd61ea7a3c6b71ecff258fc4330a2af4fad4aca2b4c5`  
		Last Modified: Tue, 14 Oct 2025 19:48:55 GMT  
		Size: 6.4 MB (6401251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c292805a52df651e9b8d7d59f42cc18e98400afa3d40469d740e30e07c13ff`  
		Last Modified: Tue, 14 Oct 2025 19:48:56 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d2c33c804552966911d67418a33fb9ad1ce94b099588b8624b5ce94216bd42e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (131984425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747dc5b858de4cc40deed2680d1e6dceca43dac5062f0de5803d064a6114c6ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9/ubi"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL io.openshift.tags="base rhel9"
# Mon, 15 Sep 2025 22:15:37 GMT
ENV container oci
# Mon, 15 Sep 2025 22:15:37 GMT
COPY dir:b9ca9ee30ad427ffb29be1a6c8e68d7dfc3fa9352a21a6a76346c5782783c7a9 in /      
# Mon, 15 Sep 2025 22:15:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Sep 2025 22:15:37 GMT
CMD ["/bin/bash"]
# Mon, 15 Sep 2025 22:15:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Sep 2025 22:15:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Sep 2025 22:15:37 GMT
COPY file:d2bf1cf35fa0b6f9865b8418d392585e592bd0e3566050282498c9984d00cc1b in /root/buildinfo/labels.json      
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="60d587d1286655c5e777e63959aaae224123ea95" "org.opencontainers.image.revision"="60d587d1286655c5e777e63959aaae224123ea95" "build-date"="2025-10-13T07:41:49Z" "release"="1760340943"org.opencontainers.image.revision=60d587d1286655c5e777e63959aaae224123ea95
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_PLATFORM=ubi9
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:47c325a0b847affaa9b64f57de793eff43b8d44ae93c70c8f50b53cc15ac6046`  
		Last Modified: Mon, 13 Oct 2025 12:10:12 GMT  
		Size: 77.3 MB (77323400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35111aed409d9d31ccc183c6827ef44101c9db87bc3cba891bd34924975bcec`  
		Last Modified: Tue, 14 Oct 2025 17:58:16 GMT  
		Size: 54.7 MB (54661025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:283d0ff0f67eb15b53a36fdc37f49d8927c7f8327dc47547c812dd9911845761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6408643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807857e228448a593d60f8249936bc575877fef914d4c6a1bcc7322254167db`

```dockerfile
```

-	Layers:
	-	`sha256:d073a6ddc0f79303234c639bc83edb81747f847a578989bf78bd34d64fe09130`  
		Last Modified: Tue, 14 Oct 2025 19:49:02 GMT  
		Size: 6.4 MB (6397054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d227ab0781c744d68e4b2fc3bcbb402ae2d538d6f3f4fca796ca53a7ad4d7eba`  
		Last Modified: Tue, 14 Oct 2025 19:49:03 GMT  
		Size: 11.6 KB (11589 bytes)  
		MIME: application/vnd.in-toto+json
