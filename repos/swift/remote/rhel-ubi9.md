## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:769b7ba74f3f846e156200681b1884377b3578009e42ac61aa4662f9e2ff735a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:9e248c3e086c590a42250816d61c2780d7cc23b1373a946621eecc368c49113b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1225579215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99db71d65bf35f32f2841c4b0c188009677ca5b1ecc4e53f7ca608aec520fff6`
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
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:35d6a5cce6a146ea7213377edde7d1d27f34dda18ce9fac98ea2ab40a6b110f6`  
		Last Modified: Mon, 13 Oct 2025 08:55:32 GMT  
		Size: 79.6 MB (79593305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e4f71f0f4ffcbb3f538a2f262d2fd7bd7925ad8eab76170934063c4c8131f9`  
		Last Modified: Tue, 14 Oct 2025 18:00:35 GMT  
		Size: 124.3 MB (124324344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9348d67c88b9ff0d2041c46628e479c6747b4e7fa3419d1caab88e65c3205b7`  
		Last Modified: Tue, 16 Sep 2025 20:42:52 GMT  
		Size: 1.0 GB (1021661394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd9720355e48042ed115c66a490459f373281eaa13541407b2f969cfde40547`  
		Last Modified: Tue, 14 Oct 2025 18:00:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:b04131e6a1c6e3d4b92c1611ca5e0632892ffac00206d62fb7a3d493be119788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12987225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3710d41f26a43809506ac0dd8e26fdb0aecbff8d1b7b65a948f82cc29ac7819f`

```dockerfile
```

-	Layers:
	-	`sha256:9d0a3ee1227ad41c2e7a1aa0c1547f79cba1c36574c3afb4d3d99473cf8c2535`  
		Last Modified: Tue, 14 Oct 2025 19:48:48 GMT  
		Size: 13.0 MB (12972752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf06d20c22be70165af3f67713e39dffe8779b5c3fc4b42ff3deb22a35c4850`  
		Last Modified: Tue, 14 Oct 2025 19:48:49 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3c02babf64afb7a936f21a485a079b9991018b0b55de0c301a9e12e148443f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1213230366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94884d55ff88b6140c013b7f582a3f1f185e32ccf3252a7e819ef669fa7f45a`
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
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:47c325a0b847affaa9b64f57de793eff43b8d44ae93c70c8f50b53cc15ac6046`  
		Last Modified: Mon, 13 Oct 2025 12:10:12 GMT  
		Size: 77.3 MB (77323400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c4d326be4e67d093f81216d0a22293be3cd3439b5223acff083e7bed37dd0c`  
		Last Modified: Tue, 14 Oct 2025 18:00:36 GMT  
		Size: 118.0 MB (117994179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e173220e447556c365792852e7b4bdbe7b0b10015a0e8083371296e522e16db5`  
		Last Modified: Tue, 16 Sep 2025 20:43:04 GMT  
		Size: 1.0 GB (1017912612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3bbe710c1203575163b68d6e7b3dbfa030a610eb76951a9cb452eaa8f49838`  
		Last Modified: Tue, 14 Oct 2025 18:00:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:259dcf616b2000fac854941898f55f0b8c769539e22ef004c4ff982fbfe1e266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12860588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3927720b68eb6e0ac8e9a22363a29b9679244e9ff5443c18295855302c84e18`

```dockerfile
```

-	Layers:
	-	`sha256:1f9d074c91b37064ec1a75b0895b37e4c3ae929f07f7ecb7df374db72872b3f0`  
		Last Modified: Tue, 14 Oct 2025 19:49:00 GMT  
		Size: 12.8 MB (12845999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4096c04426b94000f62a429a43eab83c1ce34ef6ffefc266973c7ba7dc0ca20`  
		Last Modified: Tue, 14 Oct 2025 19:49:01 GMT  
		Size: 14.6 KB (14589 bytes)  
		MIME: application/vnd.in-toto+json
