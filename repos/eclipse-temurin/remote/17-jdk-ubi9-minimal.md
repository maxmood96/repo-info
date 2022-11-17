## `eclipse-temurin:17-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:f19af504b43d5e826ce6b3d9858c10b8658d615fe68f28eba50aaee6450c2c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c222b7e9ffbe0e5c9c25a6c9cb2f9ced2a1b7ed505fcc88b98772e7ff3eb8322
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260043975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828d51b7ccb0a42d73249dd336760c63071965ef4b42e32455fd2502a85e92b0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 09 Nov 2022 13:44:42 GMT
ADD file:7b3aab3c25c29047a9bd11941a3e9ccfde01adc9bbbbf15bbdd780231892edc1 in / 
# Wed, 09 Nov 2022 13:44:42 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 09 Nov 2022 13:44:42 GMT
ADD multi:30ff6a02e0f899d3bc68d3fabc66b2b79dc0a64adc0f1b34ed26fe13df185b90 in /etc/yum.repos.d/ 
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 09 Nov 2022 13:44:42 GMT
ENV container oci
# Wed, 09 Nov 2022 13:44:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Nov 2022 13:44:42 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 13:44:43 GMT
RUN rm -rf /var/log/*
# Wed, 09 Nov 2022 13:44:43 GMT
LABEL release=1656
# Wed, 09 Nov 2022 13:44:44 GMT
ADD file:2ee23fa79b125669153ba526f3027c406136fcda77f38f5b972b6909b03bd62b in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.json 
# Wed, 09 Nov 2022 13:44:44 GMT
ADD file:cba9034625dcd3d13a92da2b903766954a174dea51345b8298bf1b82d79d01be in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656 
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-09T13:34:12" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656"
# Wed, 09 Nov 2022 13:44:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-f4c1a.repo' '/etc/yum.repos.d/repo-33b3b.repo'
# Wed, 09 Nov 2022 13:44:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 17 Nov 2022 00:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Nov 2022 00:20:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Nov 2022 00:20:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Nov 2022 00:20:24 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 17 Nov 2022 00:21:45 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 17 Nov 2022 00:21:54 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c26c0e09f1641a666d6740d802beb81e12180abaea07b47c409d30c7f368109';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a426a4e2cbc29f46fa686bea8b26613f7b7a9a772a77fed0d40dfe05295be883';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6fc21601d3cf08584e698d676249a91b6a9e790c8fc7c4d9f294628562e16273';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='482180725ceca472e12a8e6d1a4af23d608d78287a77d963335e2a0156a020af';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 00:21:57 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Nov 2022 00:21:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:370b922a565a4b8fc293d71dfab1a9b03877e7981e294fb4d032629cff2908ea`  
		Last Modified: Wed, 16 Nov 2022 03:31:29 GMT  
		Size: 37.9 MB (37924180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4a315172de5e471c299b202c75ad450791e6a58aafc696280fdde7bf9de66a`  
		Last Modified: Thu, 17 Nov 2022 00:25:05 GMT  
		Size: 29.7 MB (29681415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b167a15a90796fdad8d8c69c757078a2d44a997c8a3af04b30ff896f52c499`  
		Last Modified: Thu, 17 Nov 2022 00:26:47 GMT  
		Size: 192.4 MB (192438204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488e4c7e3e31bfbaa654074cb321b64ec6092885f979fe82e33f498a5bb51111`  
		Last Modified: Thu, 17 Nov 2022 00:26:33 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6751e780240cb684dafc61daddee2a5c5a76347eb2fb13008d9ad682c33a3948
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257403195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18dac31534bcc8e460e0104fa25605820afbfd1aa9fbba376cfdfe977e1c1bb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 09 Nov 2022 13:44:44 GMT
ADD file:4bdffe661347b90e953f55c24556c3b4f4e5ba3f83e11ba255b6991fc4388f0d in / 
# Wed, 09 Nov 2022 13:44:44 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 09 Nov 2022 13:44:44 GMT
ADD multi:30ff6a02e0f899d3bc68d3fabc66b2b79dc0a64adc0f1b34ed26fe13df185b90 in /etc/yum.repos.d/ 
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 09 Nov 2022 13:44:44 GMT
ENV container oci
# Wed, 09 Nov 2022 13:44:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Nov 2022 13:44:44 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 13:44:45 GMT
RUN rm -rf /var/log/*
# Wed, 09 Nov 2022 13:44:45 GMT
LABEL release=1656
# Wed, 09 Nov 2022 13:44:46 GMT
ADD file:92a16ecbaa8d380506f46b78ebac1017789d726f830c1562f9310d3e5dbec611 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.json 
# Wed, 09 Nov 2022 13:44:46 GMT
ADD file:01629bc17614a262eab3033c276469803729534b11886fd19242e772ccb80ca8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656 
# Wed, 09 Nov 2022 13:44:46 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-09T13:34:12" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656"
# Wed, 09 Nov 2022 13:44:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-f4c1a.repo' '/etc/yum.repos.d/repo-33b3b.repo'
# Wed, 09 Nov 2022 13:44:49 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 16 Nov 2022 23:39:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Nov 2022 23:39:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 23:39:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Nov 2022 23:40:00 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 16 Nov 2022 23:41:23 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Wed, 16 Nov 2022 23:41:29 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c26c0e09f1641a666d6740d802beb81e12180abaea07b47c409d30c7f368109';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a426a4e2cbc29f46fa686bea8b26613f7b7a9a772a77fed0d40dfe05295be883';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6fc21601d3cf08584e698d676249a91b6a9e790c8fc7c4d9f294628562e16273';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='482180725ceca472e12a8e6d1a4af23d608d78287a77d963335e2a0156a020af';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Wed, 16 Nov 2022 23:41:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 16 Nov 2022 23:41:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:017404579d24b362f0902de606e00d1778350beb20d740b3d5a93e9fce757028`  
		Last Modified: Wed, 16 Nov 2022 03:31:28 GMT  
		Size: 36.1 MB (36113178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9c397b088b3d30bce459b5efbcc1ca184b7cceeeca6ef7742a3d5a65d9cf86`  
		Last Modified: Wed, 16 Nov 2022 23:44:11 GMT  
		Size: 30.1 MB (30068286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5897451502d10b9e534ea815860ba81b71082d0be2aae5f9bf694f8fdd2e9a`  
		Last Modified: Wed, 16 Nov 2022 23:45:34 GMT  
		Size: 191.2 MB (191221555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1feaa042e8b67a3f6e26bebac8fae53a9e3b4fc383a1375e6a0ad2133d084af`  
		Last Modified: Wed, 16 Nov 2022 23:45:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5287071411a739a6bf7003d06e97f7cd43674d42237214107e780ae09324ac95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265080713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9b75d9748e01b914e78515d15c0fdd852c745540b295bea3f6d7246fea4e84`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 09 Nov 2022 13:44:29 GMT
ADD file:b7fa848956dba9d5b7e47ce28fe09611e7916334adb166f4d923d2acc3b62dfa in / 
# Wed, 09 Nov 2022 13:44:29 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 09 Nov 2022 13:44:30 GMT
ADD multi:30ff6a02e0f899d3bc68d3fabc66b2b79dc0a64adc0f1b34ed26fe13df185b90 in /etc/yum.repos.d/ 
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 09 Nov 2022 13:44:30 GMT
ENV container oci
# Wed, 09 Nov 2022 13:44:30 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Nov 2022 13:44:30 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 13:44:32 GMT
RUN rm -rf /var/log/*
# Wed, 09 Nov 2022 13:44:32 GMT
LABEL release=1656
# Wed, 09 Nov 2022 13:44:32 GMT
ADD file:67f707548ff6615b646dd023e0a11ef26064bb17ff187cf60508cfd387c8dd94 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.json 
# Wed, 09 Nov 2022 13:44:33 GMT
ADD file:4ddcfe8ebb6a1157eb414014a1ed71157dfc0268903635f6ab7da5807eb88547 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656 
# Wed, 09 Nov 2022 13:44:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-09T13:34:12" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656"
# Wed, 09 Nov 2022 13:44:34 GMT
RUN rm -f '/etc/yum.repos.d/repo-f4c1a.repo' '/etc/yum.repos.d/repo-33b3b.repo'
# Wed, 09 Nov 2022 13:44:37 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 17 Nov 2022 01:13:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Nov 2022 01:13:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Nov 2022 01:13:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Nov 2022 01:13:30 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 17 Nov 2022 01:16:12 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 17 Nov 2022 01:16:37 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c26c0e09f1641a666d6740d802beb81e12180abaea07b47c409d30c7f368109';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a426a4e2cbc29f46fa686bea8b26613f7b7a9a772a77fed0d40dfe05295be883';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6fc21601d3cf08584e698d676249a91b6a9e790c8fc7c4d9f294628562e16273';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='482180725ceca472e12a8e6d1a4af23d608d78287a77d963335e2a0156a020af';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 01:16:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Nov 2022 01:16:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f67e11af6c0f957f8aaf4aa1c82d719ae236aea00d1ce0b61e682e04bbf8f8f8`  
		Last Modified: Wed, 16 Nov 2022 12:27:18 GMT  
		Size: 40.8 MB (40829227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5281831dd83348105313170c050e6e082e67c269bbc07976066171a271af40cc`  
		Last Modified: Thu, 17 Nov 2022 01:22:08 GMT  
		Size: 32.4 MB (32431799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4698d18ebb9f7953acbb81e3d82d8f479fe2a8042b094fd6027763d2ff6a99c2`  
		Last Modified: Thu, 17 Nov 2022 01:24:27 GMT  
		Size: 191.8 MB (191819511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1aa67296f689e3c4834d7f31352c6fa3f9d66d0606acc0b4b5f682a0bb6850e`  
		Last Modified: Thu, 17 Nov 2022 01:24:02 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:8bd4eef163ee4a0e15b8355e4977f1f85e7816ec1732995c236caa85697a79a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252078064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11beb6563b5362b47e09cd01dc743b9ab52512d7153d0b67ca2df5c147dfd53`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 09 Nov 2022 13:45:00 GMT
ADD file:c696a6975b26d0bc58510e6f82144dd22f1da20d6144a50ea8acfbcf6c722471 in / 
# Wed, 09 Nov 2022 13:45:01 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 09 Nov 2022 13:45:01 GMT
ADD multi:30ff6a02e0f899d3bc68d3fabc66b2b79dc0a64adc0f1b34ed26fe13df185b90 in /etc/yum.repos.d/ 
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 09 Nov 2022 13:45:01 GMT
ENV container oci
# Wed, 09 Nov 2022 13:45:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Nov 2022 13:45:01 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 13:45:03 GMT
RUN rm -rf /var/log/*
# Wed, 09 Nov 2022 13:45:03 GMT
LABEL release=1656
# Wed, 09 Nov 2022 13:45:04 GMT
ADD file:d59ff54c102e6e4131f19b9acc93224b25457c4205967321323811051c1b9360 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.json 
# Wed, 09 Nov 2022 13:45:04 GMT
ADD file:a669e390d7b1390e068b1d844ee5b8733c2383a9853cba6cbc831aca94110042 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656 
# Wed, 09 Nov 2022 13:45:04 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-09T13:34:12" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656"
# Wed, 09 Nov 2022 13:45:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-f4c1a.repo' '/etc/yum.repos.d/repo-33b3b.repo'
# Wed, 09 Nov 2022 13:45:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 16 Nov 2022 23:59:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Nov 2022 23:59:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 23:59:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Nov 2022 23:59:42 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 17 Nov 2022 00:00:47 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 17 Nov 2022 00:00:56 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c26c0e09f1641a666d6740d802beb81e12180abaea07b47c409d30c7f368109';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.5_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a426a4e2cbc29f46fa686bea8b26613f7b7a9a772a77fed0d40dfe05295be883';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.5_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6fc21601d3cf08584e698d676249a91b6a9e790c8fc7c4d9f294628562e16273';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.5_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='482180725ceca472e12a8e6d1a4af23d608d78287a77d963335e2a0156a020af';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 00:01:02 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Nov 2022 00:01:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1551d58b2309089dfc342db62ee900f5b92a06b0a749d6b8700e31e9fb5f0d8`  
		Last Modified: Wed, 16 Nov 2022 12:27:26 GMT  
		Size: 36.2 MB (36198583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdb8f863ee656899ec04a324225fe008cc6737be0bdf34580d6e057d74cb1df`  
		Last Modified: Thu, 17 Nov 2022 00:04:36 GMT  
		Size: 35.6 MB (35623466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d5a02b3906a0b99f994db689d0f3f377360be2d01fd96f6c031d73e0dbde27`  
		Last Modified: Thu, 17 Nov 2022 00:05:23 GMT  
		Size: 180.3 MB (180255838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f15f6a2113e393f7a82fc8fcc263753a33618f0e65a650b70f4fe9f9688cff2`  
		Last Modified: Thu, 17 Nov 2022 00:05:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
