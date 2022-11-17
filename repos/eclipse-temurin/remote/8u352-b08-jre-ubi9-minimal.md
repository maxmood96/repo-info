## `eclipse-temurin:8u352-b08-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:4d0b4d82540d0bd20f48001f41544d8d748ef8563bcf607772433e33552554aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u352-b08-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6b0805e1b7b7d8a57200afc4be459eea20b8cf4b1ca4e0f016819fa4f8bce5a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109417642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb46bdeff7cb0f0843f36962ef224f09e425ceeb1373fa65f55561707a66401`
-	Default Command: `["\/bin\/bash"]`

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
# Thu, 17 Nov 2022 00:20:24 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Thu, 17 Nov 2022 00:20:48 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 00:20:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:cff40e9a7b4257f4c8365f3e8c75910ad9a693aa47ae04e33407526d25ef53aa`  
		Last Modified: Thu, 17 Nov 2022 00:25:28 GMT  
		Size: 41.8 MB (41811887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69a89a3fef56dde66dde7ea39de458951897de2ab150e9a520a5d1223f9ed69`  
		Last Modified: Thu, 17 Nov 2022 00:25:23 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u352-b08-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:667faa3501b3d82964cf62d1538628be2e044e9dffd8526f64b0ea0d97f603d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106984172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e3b2b97864abdb2d941dea08e890a5b1cdc5503e91a52a50d9cb0ae47d3283`
-	Default Command: `["\/bin\/bash"]`

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
# Wed, 16 Nov 2022 23:40:00 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Wed, 16 Nov 2022 23:40:23 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Wed, 16 Nov 2022 23:40:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:4c4b182bc2236505ee805039cc03c0b3b0740e996fb38e79579e05ef991973ee`  
		Last Modified: Wed, 16 Nov 2022 23:44:31 GMT  
		Size: 40.8 MB (40802547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293c1f795e8da75299fcbe90b8a4810129aada6802a697e9b9a82b659ffaa309`  
		Last Modified: Wed, 16 Nov 2022 23:44:27 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u352-b08-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9dad199ed3363bae7f61fb6f80524b36a6cada336607c7962ba310ebacd3a96d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114476473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67999b34938ce6275ed6735de71e7ce71efa2dde2539c12613cebfcc3221f69`
-	Default Command: `["\/bin\/bash"]`

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
# Thu, 17 Nov 2022 01:13:32 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Thu, 17 Nov 2022 01:14:23 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='cce4db7c4311378d8d2a174b2cf680d57b52a4036f37c995b14f936b6fc1141a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='5649672dab65b3519ec16653fb2f154da90a7cd2afc568da03f3bff5c6b30a90';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='40b6b4c3d8f7332ea479527b530413bf0dbc13cff3c0ed9fcadf1ca053bed106';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 01:14:25 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:b0959d7b6237de5c69b5f6dce51603fc8d07d152010ab02ee3a0d2333689145c`  
		Last Modified: Thu, 17 Nov 2022 01:22:40 GMT  
		Size: 41.2 MB (41215287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce86568ddfaf01099c944391b2b8eefe15148ee79702d9f57c266bca92ff88`  
		Last Modified: Thu, 17 Nov 2022 01:22:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
