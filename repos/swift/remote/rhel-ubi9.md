## `swift:rhel-ubi9`

```console
$ docker pull swift@sha256:5da14a9f45b74c37ab8f4422b8d584bd2f7f871b8e10bdb82ec31004b8127973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9` - linux; amd64

```console
$ docker pull swift@sha256:e5f43acc38827de0d23970e110684f7620830f956d300c0c16b1575d8284f799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1023032018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af504dba473cdda9f8f5c29bb2f7febb724ef45f90836e87bdf787c63ff94b0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL url="https://www.redhat.com"
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Nov 2024 14:34:16 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 28 Nov 2024 14:34:16 GMT
ENV container oci
# Thu, 28 Nov 2024 14:34:17 GMT
COPY dir:6e388bec01400ec35da0a5b5a2596b41da834e86ca148940cbc732afde5a8f48 in / 
# Thu, 28 Nov 2024 14:34:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Nov 2024 14:34:17 GMT
CMD ["/bin/bash"]
# Thu, 28 Nov 2024 14:34:18 GMT
LABEL "build-date"="2024-11-28T14:33:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2c6dc24323bfe846cd1fe51f2a65994655ca3068" "build-date"="2024-11-28T14:28:08Z" "release"="1732804088"
# Thu, 28 Nov 2024 14:34:34 GMT
RUN /bin/sh
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:d1626b5b9f7a59add02f7c14fb670e63a729a8b70a53b95f56bf7f5ee8dc12d8`  
		Last Modified: Thu, 28 Nov 2024 16:08:27 GMT  
		Size: 88.5 MB (88473716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a73aee7e570194d6ace6157d6693b5439c872acf23a01d32c79489f3192264f`  
		Last Modified: Thu, 28 Nov 2024 16:08:24 GMT  
		Size: 113.7 KB (113737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9cc24e1d510a151015f25a9f199b82af5b9af6cb1e5868e61075dc81a407f1`  
		Last Modified: Thu, 12 Dec 2024 22:37:28 GMT  
		Size: 134.2 MB (134167062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becb7870dcf6d647e51c7c441149215366fec01a7644653ad7f9dc8baebabdb5`  
		Last Modified: Thu, 12 Dec 2024 22:37:40 GMT  
		Size: 800.3 MB (800277307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c153d132a4f0b5bd2686d50fed87d10be4b45190fb8995367cf26a8842daea7`  
		Last Modified: Thu, 12 Dec 2024 22:37:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:2e7c48784219c03f04b319135bf3c023cee1127274cc24107e2d909440b341a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14022617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81281b0051f300266edbd219a43196c2105b5fbc317ebccad8da7ba0bdf3d28e`

```dockerfile
```

-	Layers:
	-	`sha256:c790fd63875b514ea1b34e27ec2038fdcb69f58c9b562a7c181ee4fc2788863e`  
		Last Modified: Thu, 12 Dec 2024 22:37:26 GMT  
		Size: 14.0 MB (14007531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a558124f35aae2b1f6563ed9bc57f6d7a2119b5e875e5d5f501e54fe6729d7d`  
		Last Modified: Thu, 12 Dec 2024 22:37:25 GMT  
		Size: 15.1 KB (15086 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:922d660e17f89491c1d127ddd14928c73489d72e0088c1ecbf87dcb11badfa55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1010789443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b8e9f21458709049894ca5a9e745c5d60f22913cd4f91231546dbe8e8a7888`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL url="https://www.redhat.com"
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Nov 2024 14:37:42 GMT
LABEL io.openshift.tags="base rhel9"
# Thu, 28 Nov 2024 14:37:42 GMT
ENV container oci
# Thu, 28 Nov 2024 14:37:46 GMT
COPY dir:f9ac93ad8ddd076435cbb4ae20a3638777ab7ede3558d32697445bfd75fb40d9 in / 
# Thu, 28 Nov 2024 14:37:46 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 28 Nov 2024 14:37:46 GMT
CMD ["/bin/bash"]
# Thu, 28 Nov 2024 14:37:47 GMT
LABEL "build-date"="2024-11-28T14:36:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2c6dc24323bfe846cd1fe51f2a65994655ca3068" "build-date"="2024-11-28T14:28:08Z" "release"="1732804088"
# Thu, 28 Nov 2024 14:38:18 GMT
RUN /bin/sh
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
RUN yum -y install   git                 gcc-c++             libcurl-devel       libedit-devel       libuuid-devel       libxml2-devel       ncurses-devel       python3-devel       rsync               sqlite-devel        unzip               zip # buildkit
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
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:d2722a26089ce7ded66c7ce945d1b8c06782b041a5cd8f503e73b093aef3dd87`  
		Last Modified: Thu, 28 Nov 2024 16:08:16 GMT  
		Size: 86.2 MB (86194931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19df96f61f206bf06c52174829d709ad815251fc970317345df86e49ea173fa`  
		Last Modified: Thu, 28 Nov 2024 16:08:18 GMT  
		Size: 113.7 KB (113734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0721bac6cc3653ccbabbe1c457ae9e8f6ffeb5fcc5d1751deef3ff66fdc261`  
		Last Modified: Fri, 13 Dec 2024 00:30:21 GMT  
		Size: 128.0 MB (128007066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f936313db041fe3dee46ad15cc3dda672e3ec8f43c577c59bd936fefae706a1a`  
		Last Modified: Fri, 13 Dec 2024 00:30:33 GMT  
		Size: 796.5 MB (796473513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208d9d4fe15d80043336d331957959a283fd56923a7adf3069d5f88b17b0c35`  
		Last Modified: Fri, 13 Dec 2024 00:30:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9` - unknown; unknown

```console
$ docker pull swift@sha256:88d2b78badb4442ebac69b16af6750dcc242d863c638818cf8ac7d3e08161abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13895718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e55c3749557880ac3a046bb7ed29bdeddfba14ac55056427d4a17ab12f8176`

```dockerfile
```

-	Layers:
	-	`sha256:43c11297f65320886df176e9de1e1262f8540991210ea2706fdd4eda625b0748`  
		Last Modified: Fri, 13 Dec 2024 00:30:18 GMT  
		Size: 13.9 MB (13880515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f527072dc7c7ebd34e3d6f8f7254aa9b312a222a3da553f720ebda66db10b2`  
		Last Modified: Fri, 13 Dec 2024 00:30:17 GMT  
		Size: 15.2 KB (15203 bytes)  
		MIME: application/vnd.in-toto+json
