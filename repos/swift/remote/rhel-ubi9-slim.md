## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:8ee8786210216bfb840dfa3b18ec83a0196ab993c82d5ae35e7ccdc67bfecae3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:310157bf56638466c0a016f02d618612b407a9b221f3110199ce7fb08ffae7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143232965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedb59dc678559ba4b3e8d60b627ee11ff969e7d7cedd8d8840f071a01a1f3f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 12 Dec 2024 07:44:15 GMT
ENV container oci
# Thu, 12 Dec 2024 07:44:15 GMT
COPY dir:5bb879c94b3c2ff1570d6397a19e735efa694941fe59a0d69caa3c2a8d60e461 in / 
# Thu, 12 Dec 2024 07:44:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL "build-date"="2025-02-04T04:39:49" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4371344f505f230dd8b447590dba1946ab022b7" "build-date"="2025-02-04T04:32:30Z" "release"="1738643550"
# Thu, 12 Dec 2024 07:44:15 GMT
RUN /bin/sh
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:d4cb20dd5cad1ea19f0e857b56614f8b02eb977288e4f1a49f5bbbef8ff64b43`  
		Last Modified: Tue, 04 Feb 2025 05:22:17 GMT  
		Size: 88.5 MB (88497912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d117d635acf411b6b4106c39d1cdcadbe7b7b49d48995c3585269733701f6a`  
		Last Modified: Tue, 04 Feb 2025 05:22:06 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba79f56fbe870745ccb90148bbb1c8d308d181d3b52e7b9aed9898006095403c`  
		Last Modified: Tue, 04 Feb 2025 20:35:07 GMT  
		Size: 54.7 MB (54734591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:1c35f921a0408b35496483f52b8c32492da2f78e3787943f9ebb7822dfe9931e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde4e1609d182c9aef8472151f91f83526bde24f3340637c668ea17c3d50080f`

```dockerfile
```

-	Layers:
	-	`sha256:aec03d46c5a47929ffd862c86a8f3d474de6b59ad05902f0d3570863d4e6808d`  
		Last Modified: Tue, 04 Feb 2025 20:35:06 GMT  
		Size: 7.5 MB (7473242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6280865cfac6a05be464328fcd4110ca5fccd5dd4deefd77264cdc0086ef6f4f`  
		Last Modified: Tue, 04 Feb 2025 20:35:06 GMT  
		Size: 11.8 KB (11807 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:761d0e86492f2291c41548dbcfcbd02174c595b4daa2eddc95e4191c19977457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139876759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c245606cc282d630c3020a54498733de42b09fb2c75dc36056621c20bad0a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 12 Dec 2024 07:44:15 GMT
ENV container oci
# Thu, 12 Dec 2024 07:44:15 GMT
COPY dir:3ca43e73148a468ad8a46c2eba62ef2a6a5d7be81a9c91017df4efecdbca008f in / 
# Thu, 12 Dec 2024 07:44:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL "build-date"="2025-01-09T06:38:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d029ef1bed7f4b1258ff0991bfd682219c5c5b1a" "build-date"="2025-01-09T06:27:16Z" "release"="1736404036"
# Thu, 12 Dec 2024 07:44:15 GMT
RUN /bin/sh
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=ubi9
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:17f7af7a37d4b6da17d2725f33537953d09fe9cf30df676b1d1dd561e35971ab`  
		Last Modified: Thu, 09 Jan 2025 09:08:04 GMT  
		Size: 86.2 MB (86220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f999dbdae714d45c5dfdb9663ce8a4dacdeb39839c23fbdee19edd1ce2645e53`  
		Last Modified: Thu, 09 Jan 2025 09:08:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dc1a976a29bb05709b8d2838f01b95a962067c108988a5292872bda6e27a81`  
		Last Modified: Sat, 11 Jan 2025 01:51:48 GMT  
		Size: 53.7 MB (53655625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:0cc03e06da5a17fb103349833a9710c9490288a38cdf0445e7884698dff875f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2786ffa7c761204ff787e0fc133020de9ce2152eb34b7424c0889fc3d07837dc`

```dockerfile
```

-	Layers:
	-	`sha256:438fc85006363722199aa89b71e399fbbb1d640ac48c27c3f4d2a6cf8f38ba0f`  
		Last Modified: Sat, 11 Jan 2025 01:51:47 GMT  
		Size: 7.5 MB (7469033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b69a58abd0bde5aae4b991cc15da1eb13b4e12130aaefe9ec904039b47020e5`  
		Last Modified: Sat, 11 Jan 2025 01:51:46 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.in-toto+json
