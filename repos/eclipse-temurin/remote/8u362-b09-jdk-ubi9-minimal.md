## `eclipse-temurin:8u362-b09-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:840a86f280dbcb3133c2c22bfb35b4b4776fc26b195ee2ccf493b8bc4b656b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u362-b09-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9b93293b4cabf2e9c292152b0a4f1e7f08e7fa2d3ac4123ed2b335c8a271358a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121417349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57233d9ff0bb7878f92d0cc5a08535329643f5ed857c94316d739ee954022f2f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Jan 2023 08:31:49 GMT
ADD file:cec23c8fbf16faebe415d9da27af234f476046de04a58fcd5c12596ca22053b4 in / 
# Tue, 17 Jan 2023 08:31:49 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Tue, 17 Jan 2023 08:31:50 GMT
ADD multi:41c7e0f932074ee6ab1584deadf29d960d57d75d1c101ce2209eff05b1a3e756 in /etc/yum.repos.d/ 
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Jan 2023 08:31:50 GMT
ENV container oci
# Tue, 17 Jan 2023 08:31:50 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jan 2023 08:31:50 GMT
CMD ["/bin/bash"]
# Tue, 17 Jan 2023 08:31:50 GMT
RUN rm -rf /var/log/*
# Tue, 17 Jan 2023 08:31:50 GMT
LABEL release=1760
# Tue, 17 Jan 2023 08:31:51 GMT
ADD file:f66581c13a3419d0ae04b2e10b800e53882f091321f55e851165a68c6908bdd9 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1760.json 
# Tue, 17 Jan 2023 08:31:51 GMT
ADD file:49a69232a0b4ae6f0ead42deb08bd00c74ba6474cc1f3ad8f89a43a6b6628c29 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1760 
# Tue, 17 Jan 2023 08:31:51 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-01-17T08:21:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1760"
# Tue, 17 Jan 2023 08:31:52 GMT
RUN rm -f '/etc/yum.repos.d/repo-b9156.repo' '/etc/yum.repos.d/repo-9b4cd.repo'
# Tue, 17 Jan 2023 08:31:53 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 24 Jan 2023 02:17:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 02:17:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 02:17:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 24 Jan 2023 02:17:41 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 25 Jan 2023 19:20:23 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 25 Jan 2023 19:20:28 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 25 Jan 2023 19:20:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:42df1cb831d12cb5122714b5a527807bf78729a544ae05eacc9ab8f82da8dad9`  
		Last Modified: Mon, 23 Jan 2023 18:08:50 GMT  
		Size: 37.9 MB (37856368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d71014b709775b87982103131d6162788201fd81c42f56eb70fc963192c5ad`  
		Last Modified: Tue, 24 Jan 2023 02:21:47 GMT  
		Size: 28.9 MB (28925033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e0cda9b9a863ebcb90dcf5f66dd58c2f3fe847eaf7ba26b8f9e06d4f581a38`  
		Last Modified: Wed, 25 Jan 2023 19:27:01 GMT  
		Size: 54.6 MB (54635786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd92e25929f714b9d6cec54ea591f71a6103082c060b46e5713466f2a6fae733`  
		Last Modified: Wed, 25 Jan 2023 19:26:54 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u362-b09-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ef6644f1bde695698632c81f163f2335ef0a9b2b8d369784e76588c14c463dac
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119150764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aaacfc5855d75d9bc6febe8e988ad19be031c8605c5a913a0eaec70b4e700fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 07 Feb 2023 17:12:25 GMT
ADD file:6eed9add4d102afab754f79cdd4236e76a60d0339232718e614809ce5c0ce94a in / 
# Tue, 07 Feb 2023 17:12:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 07 Feb 2023 17:12:26 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Tue, 07 Feb 2023 17:12:26 GMT
ADD multi:6893bb0509c7aae7bc271b3e27ee01082fe34bd3f5e8d8e4ad49d547e73ac56f in /etc/yum.repos.d/ 
# Tue, 07 Feb 2023 17:12:26 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 07 Feb 2023 17:12:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Tue, 07 Feb 2023 17:12:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 07 Feb 2023 17:12:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 07 Feb 2023 17:12:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 07 Feb 2023 17:12:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 07 Feb 2023 17:12:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 07 Feb 2023 17:12:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 07 Feb 2023 17:12:26 GMT
ENV container oci
# Tue, 07 Feb 2023 17:12:26 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Feb 2023 17:12:26 GMT
CMD ["/bin/bash"]
# Tue, 07 Feb 2023 17:12:27 GMT
RUN rm -rf /var/log/*
# Tue, 07 Feb 2023 17:12:27 GMT
ADD file:08ef57526cd88ed3537baebed5ed35184b5cda5e894d32b8a65f70597201d4e7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1760.1675784957.json 
# Tue, 07 Feb 2023 17:12:28 GMT
ADD file:2c15695afde4652d5154aef781f535601c28bed5bd22f0396a46bbb39a7e27d4 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1760.1675784957 
# Tue, 07 Feb 2023 17:12:28 GMT
LABEL "release"="1760.1675784957" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-02-07T16:25:34" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1760.1675784957"
# Tue, 07 Feb 2023 17:12:29 GMT
RUN rm -f '/etc/yum.repos.d/odcs-1774985-d0e8e.repo' '/etc/yum.repos.d/gitweb-1077d.repo'
# Tue, 07 Feb 2023 17:12:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 07 Feb 2023 17:12:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 10 Feb 2023 20:09:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Feb 2023 20:09:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Feb 2023 20:09:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Feb 2023 20:09:23 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Fri, 10 Feb 2023 20:09:23 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Fri, 10 Feb 2023 20:09:33 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 20:09:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3d6e338d0c59eb147bc19de6d1eee742a337331f97cf64c20fb62a190f217932`  
		Last Modified: Thu, 09 Feb 2023 08:52:27 GMT  
		Size: 36.1 MB (36113628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5729043cdd7250c6f7a92949ec61244b450289abaacce1ce1bc358e0810131`  
		Last Modified: Fri, 10 Feb 2023 20:13:51 GMT  
		Size: 29.3 MB (29308819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7c7017066177ac8d5197025abc045c3c319b08b82e78ee9eddfdb27bebd630`  
		Last Modified: Fri, 10 Feb 2023 20:13:53 GMT  
		Size: 53.7 MB (53728155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b9e0b73c8f4904de0cbc3f72cbb8fb8b6a488c9fe76b047a880d17769a859`  
		Last Modified: Fri, 10 Feb 2023 20:13:47 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u362-b09-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:30921e7103c7199b8bdd731dde2da32eee3ca6101da2f6355563899509d55a61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124610966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1622b40d7b5f80333461b96f837fcebcfbd5a547d98a7c28ba8cad217127540d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 07 Feb 2023 17:12:57 GMT
ADD file:a4ae30568dcee90136c3634fd94e34722344b5eb6d3fa5ca289e754b3f81eda9 in / 
# Tue, 07 Feb 2023 17:13:02 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 07 Feb 2023 17:13:02 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Tue, 07 Feb 2023 17:13:03 GMT
ADD multi:6893bb0509c7aae7bc271b3e27ee01082fe34bd3f5e8d8e4ad49d547e73ac56f in /etc/yum.repos.d/ 
# Tue, 07 Feb 2023 17:13:03 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 07 Feb 2023 17:13:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Tue, 07 Feb 2023 17:13:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 07 Feb 2023 17:13:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 07 Feb 2023 17:13:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 07 Feb 2023 17:13:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 07 Feb 2023 17:13:03 GMT
LABEL io.openshift.expose-services=""
# Tue, 07 Feb 2023 17:13:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 07 Feb 2023 17:13:03 GMT
ENV container oci
# Tue, 07 Feb 2023 17:13:03 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Feb 2023 17:13:03 GMT
CMD ["/bin/bash"]
# Tue, 07 Feb 2023 17:13:08 GMT
RUN rm -rf /var/log/*
# Tue, 07 Feb 2023 17:13:10 GMT
ADD file:c0515ee7277707a9bf1008f70bd623183ce69d84580ea50469a70b5415f05aa4 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1760.1675784957.json 
# Tue, 07 Feb 2023 17:13:10 GMT
ADD file:a5ae5174997880dbcde1f80706d909a5675d725820996a4d17bbd750f2ec54cc in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1760.1675784957 
# Tue, 07 Feb 2023 17:13:10 GMT
LABEL "release"="1760.1675784957" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-02-07T16:25:34" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1760.1675784957"
# Tue, 07 Feb 2023 17:13:19 GMT
RUN rm -f '/etc/yum.repos.d/odcs-1774985-d0e8e.repo' '/etc/yum.repos.d/gitweb-1077d.repo'
# Tue, 07 Feb 2023 17:13:23 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 07 Feb 2023 17:13:29 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 10 Feb 2023 19:54:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Feb 2023 19:54:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Feb 2023 19:54:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Feb 2023 19:55:40 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Fri, 10 Feb 2023 19:55:44 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Fri, 10 Feb 2023 19:56:03 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 19:56:07 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:85e5f0c37394f1c59d7e3270feef7dc13df3628f3afaa453124d6363656d8a73`  
		Last Modified: Fri, 10 Feb 2023 00:09:59 GMT  
		Size: 40.8 MB (40836851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5644e41b2311e4ce47e609eb31a20930d85ced2b755984e3946fc3857768bba8`  
		Last Modified: Fri, 10 Feb 2023 20:05:07 GMT  
		Size: 31.7 MB (31664084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66a3c5643725fb6b3212140aad85a5fdc6efd9f8614bd1df06abb3e69dfd87b`  
		Last Modified: Fri, 10 Feb 2023 20:05:10 GMT  
		Size: 52.1 MB (52109871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58df486fbfc06c7c327e9c5d3624e4d797e767aaf425620abb9dd7bfee6d3849`  
		Last Modified: Fri, 10 Feb 2023 20:04:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
