## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:f39bcac470db9fc4e8487e486e070c6a975f66367348a12cd316d92cd0a3fb6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:df4ca4cd510c2f3101256a35b4e4ef546b31359f57110e72598e615e2193a17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148557645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8492e5c475a98c26ff72b4098063184dfacda82ade0a9edcc218ec5ba5e5a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 21:36:31 GMT
ADD file:0067eb9f2ee25ab2d666a7639a85fe707b582902a09242761abf30c53664069b in / 
# Wed, 18 Sep 2024 21:36:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:36:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:36:32 GMT
ADD multi:7a67822d03b1a3ddb205cc3fcf7acd9d3180aef5988a5d25887bc0753a7a493b in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:36:32 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 18 Sep 2024 21:36:32 GMT
ENV container oci
# Wed, 18 Sep 2024 21:36:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:36:32 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:36:33 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:36:34 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 18 Sep 2024 21:36:35 GMT
ADD file:ed34e436a5c2cc729eecd8b15b94c75028aea1cb18b739cafbb293b5e4ad5dae in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1726694543.json 
# Wed, 18 Sep 2024 21:36:35 GMT
ADD file:d56bb1961538221b52d7e292418978f186bf67b9906771f38530fc3996a9d0d4 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1726694543 
# Wed, 18 Sep 2024 21:36:35 GMT
LABEL "release"="1214.1726694543" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:30" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1726694543"
# Wed, 18 Sep 2024 21:36:36 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496925-3b364.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:36:37 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:36:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:40049f9dc50417693bf704b63a02d64347b23867b33ac7776be3fae4a2d178b0`  
		Last Modified: Mon, 23 Sep 2024 14:28:12 GMT  
		Size: 79.6 MB (79592786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb520556cd9786ce17d7aad34d9c9515a710415dc9fff5d3209f36551a436e6`  
		Last Modified: Thu, 26 Sep 2024 22:57:35 GMT  
		Size: 69.0 MB (68964859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:3843ff5d596f148aba20c5ba41ffebc4615215d71a5f2635f7a62d70bfeff491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6391597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca5ffba79885584bdf9b0c13dc703961316753c847bc0c5c4eff4beab7bc986`

```dockerfile
```

-	Layers:
	-	`sha256:046213461fb1af6cabae58fe21c501fff3f17d04addbce794272a834f958340e`  
		Last Modified: Thu, 26 Sep 2024 22:57:34 GMT  
		Size: 6.4 MB (6380120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e74796a39e5190168cefd0b5324bd9edf3204d17c606e96137be988486da86ec`  
		Last Modified: Thu, 26 Sep 2024 22:57:34 GMT  
		Size: 11.5 KB (11477 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2b211e349b673ed868657e7789ab1a650931fe6296f38b03dbb5d46d8ef8341f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145217308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b1f04adc9a3a68b465a1bbdb7c4099014ef5aaa09b7cc9ef428dacfa20766b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 21:36:27 GMT
ADD file:d6101aaaa0ea140d84b6346291651ad4d2bce8c444478e1fc83508b02136ec0f in / 
# Wed, 18 Sep 2024 21:36:28 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Sep 2024 21:36:28 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 18 Sep 2024 21:36:28 GMT
ADD multi:7a67822d03b1a3ddb205cc3fcf7acd9d3180aef5988a5d25887bc0753a7a493b in /etc/yum.repos.d/ 
# Wed, 18 Sep 2024 21:36:28 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Sep 2024 21:36:28 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.4"
# Wed, 18 Sep 2024 21:36:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Sep 2024 21:36:28 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Wed, 18 Sep 2024 21:36:28 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Sep 2024 21:36:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Wed, 18 Sep 2024 21:36:28 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Sep 2024 21:36:28 GMT
LABEL io.openshift.tags="base rhel9"
# Wed, 18 Sep 2024 21:36:28 GMT
ENV container oci
# Wed, 18 Sep 2024 21:36:28 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 21:36:28 GMT
CMD ["/bin/bash"]
# Wed, 18 Sep 2024 21:36:29 GMT
RUN rm -rf /var/log/*
# Wed, 18 Sep 2024 21:36:30 GMT
RUN mkdir -p /var/log/rhsm
# Wed, 18 Sep 2024 21:36:31 GMT
ADD file:6744b3d23896832934836f8b77190150a7f9f836065a064436c5b9dc47a95425 in /root/buildinfo/content_manifests/ubi9-container-9.4-1214.1726694543.json 
# Wed, 18 Sep 2024 21:36:31 GMT
ADD file:19c58e8e8129cd749e0ec129d64db36f9eb2b3729bc034e6755ab07ad478a419 in /root/buildinfo/Dockerfile-ubi9-9.4-1214.1726694543 
# Wed, 18 Sep 2024 21:36:31 GMT
LABEL "release"="1214.1726694543" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:30" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e309397d02fc53f7fa99db1371b8700eb49f268f" "io.k8s.description"="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9/images/9.4-1214.1726694543"
# Wed, 18 Sep 2024 21:36:32 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496925-3b364.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Wed, 18 Sep 2024 21:36:33 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Sep 2024 21:36:34 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubi9
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:642dd3de0a7ba3fef28a56da54f6c6b620e3bdff1c55b20751a3029bea383326`  
		Last Modified: Mon, 23 Sep 2024 14:28:14 GMT  
		Size: 77.4 MB (77352301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4f3832a9f78a33ba40c992e0490c4c2f819735fe11ab101bb3d4ee7d29ce2b`  
		Last Modified: Fri, 27 Sep 2024 10:06:52 GMT  
		Size: 67.9 MB (67865007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:01fd2d3f2331c5c73336e5aa28e830d561f72fcd31e969a630db962f50e45cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723f614c0e97f251e0e820a25a188bd7487d88fd18e425936c1b249a22dd35e6`

```dockerfile
```

-	Layers:
	-	`sha256:8693de7ed17c59df3bb0c0ec844fcb566e8e562af9466727449f37d86ca36541`  
		Last Modified: Fri, 27 Sep 2024 10:06:49 GMT  
		Size: 6.4 MB (6377819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2136f98e31bd32ecfb59a50c3f21f8c056d1760afe6d031638e9fe133650e03`  
		Last Modified: Fri, 27 Sep 2024 10:06:48 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json
