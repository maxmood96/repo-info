## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:269a61ab08988bc4383912b581865122316f8509765d017d0b5e512145f81cf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:29b25258e78dfb271ff76b655719acc5ceb66e1afd25b27bdae3c44d26dabd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1094611429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fa78b426b2337307c13c4e71e16d13c6222b4988bd11a59433e9bdb96409b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 28 May 2025 17:53:13 GMT
LABEL url="https://www.redhat.com"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 28 May 2025 17:53:13 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 28 May 2025 17:53:13 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 28 May 2025 17:53:13 GMT
ENV container oci
# Wed, 28 May 2025 17:53:13 GMT
COPY dir:b25666a2cecd4aabfea3117014fd574e02f36a49fdf092027d5fe0c6cb3df046 in / 
# Wed, 28 May 2025 17:53:13 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 28 May 2025 17:53:13 GMT
LABEL "build-date"="2025-06-24T17:30:37" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fbd8c9ae24dcadf38d1c0eed1a6e33267aea887e" "release"="1750786174"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:24431058b73728c387089e7665e6f7171089f9bc580b84b9be8d28f8923b96b6`  
		Last Modified: Tue, 24 Jun 2025 21:28:00 GMT  
		Size: 79.6 MB (79611064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a785372b99a78fff874923ea6f6a9ce52499cf40fe793eca9b3ef4f1957cd38`  
		Last Modified: Wed, 25 Jun 2025 20:28:00 GMT  
		Size: 124.4 MB (124390235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcd9042a6b13defe243d1dd84d563f45f7ead75c07d1598785319b0b77ba9a9`  
		Last Modified: Tue, 03 Jun 2025 20:30:52 GMT  
		Size: 890.6 MB (890609955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ec6e8aca3cd7f2ad82e372155abda15ce1ac11176ceec7a8863200160bee74`  
		Last Modified: Wed, 25 Jun 2025 18:04:38 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:f3c11114a5fef4ad3e6dca71d2f00a8cf219f969b3616057c6d08f4e1e839c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12977127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad4d400f02537ff654b741c1a931e34d0ae8e09bf32f53a35134151c078a84e`

```dockerfile
```

-	Layers:
	-	`sha256:e3c08478fd2f3a1768b47150f1313e308cb441b27691980bde9f6b5166be495b`  
		Last Modified: Wed, 25 Jun 2025 19:48:26 GMT  
		Size: 13.0 MB (12962668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d406d40f85cc4a6011be630d53e52f86ae73d70ebb7a8f5407f1119b6ec5ef2b`  
		Last Modified: Wed, 25 Jun 2025 19:48:26 GMT  
		Size: 14.5 KB (14459 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c15406ac872b560fccdb5b729968c965025a48d57fd656c7f3257fd3a59451fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1082740270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6d07144e29d377a19841c4530ebc44e99870f77a9c3ccfcef1fa4045557f2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Wed, 28 May 2025 17:53:13 GMT
LABEL url="https://www.redhat.com"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.6"       distribution-scope="public"
# Wed, 28 May 2025 17:53:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 28 May 2025 17:53:13 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 28 May 2025 17:53:13 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.expose-services=""
# Wed, 28 May 2025 17:53:13 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 28 May 2025 17:53:13 GMT
ENV container oci
# Wed, 28 May 2025 17:53:13 GMT
COPY dir:e8589066f7026a8ea1a777994a944e296915f585d9ba57a125edd9f5d3a74fac in / 
# Wed, 28 May 2025 17:53:13 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 28 May 2025 17:53:13 GMT
LABEL "build-date"="2025-06-24T17:35:37" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fbd8c9ae24dcadf38d1c0eed1a6e33267aea887e" "release"="1750786174"
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:5726a84ee9e369b359279109dbbe6b8d37bc8c7a1f84f175aea6a92a68b6e7d1`  
		Last Modified: Tue, 24 Jun 2025 22:16:20 GMT  
		Size: 77.3 MB (77303173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d98f95e312d24554d643ec8053096e8ae93326d9772f1811b80e3845b800b67`  
		Last Modified: Wed, 25 Jun 2025 23:24:37 GMT  
		Size: 118.1 MB (118077025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c0d074e38755136a9465305aafe08516ebba1fecf7d780eff797053a3359fa`  
		Last Modified: Wed, 04 Jun 2025 15:11:16 GMT  
		Size: 887.4 MB (887359898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a14a03f951dc4c2a26ca256d9c185abf36115e177ff5cbd31b21cee81470aee`  
		Last Modified: Wed, 25 Jun 2025 23:24:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:6e3db1ef6b074c6215411a67c53db1fd794c3b3b1e6ae4c0e14c63bc48195f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12850490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5271f4f8255f886bf9e0b6ea5ce821c6ebdf7b0af7fd11492d92cc0346dc86`

```dockerfile
```

-	Layers:
	-	`sha256:0296a74ee66aaa580976d42f16055e7ef6f354d5119bd23afbbf122ab794cc9c`  
		Last Modified: Thu, 26 Jun 2025 01:48:29 GMT  
		Size: 12.8 MB (12835915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44cf1606dba552320f9800b0be54b22e657a90bcdcdb8d7fe1203a78f5a2ed3d`  
		Last Modified: Thu, 26 Jun 2025 01:48:30 GMT  
		Size: 14.6 KB (14575 bytes)  
		MIME: application/vnd.in-toto+json
