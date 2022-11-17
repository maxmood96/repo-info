## `eclipse-temurin:8u352-b08-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:0d75e8b97ff89195e1a47b84cd14bb4b395cfa9e1b1d7f5736764561c0fad234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u352-b08-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4fa7fdcf570d1a20d15dea48dec1335007184220597b45dfc5ea78d706d60ab5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171136712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16ec7bc7165daccd6bd73e1b9f54208b863b2f0400b6e8ce0ac71320d577647`
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
# Thu, 17 Nov 2022 00:20:30 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 00:20:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:9b96aef62aea8a7403c0ce64134282572587b624524836733eec2a5e76885950`  
		Last Modified: Thu, 17 Nov 2022 00:25:10 GMT  
		Size: 103.5 MB (103530957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbab13beb393ec2091f6b34f927ce06006afe7b0a5e235e785e72b42456070b`  
		Last Modified: Thu, 17 Nov 2022 00:25:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u352-b08-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:634dc20f697a9ffcd908cbd5dca3b7f8bc54b07a5b2bd374228b20f3cc1d0226
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168808490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5419fa8bbc006135c80ebd555319758b8f13d34fe046bfbf88283c6a27d5ce3`
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
# Wed, 16 Nov 2022 23:40:09 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Wed, 16 Nov 2022 23:40:11 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:d7bbfc6d97ec94b873e5a62630e1e80d5e7a29329e9fe14f4c2b6c0bb0064806`  
		Last Modified: Wed, 16 Nov 2022 23:44:15 GMT  
		Size: 102.6 MB (102626864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47c6bc71f6b3a70661498a92034e9804992308d41e6441f1f780f2cc987ba79`  
		Last Modified: Wed, 16 Nov 2022 23:44:08 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u352-b08-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7dfad567d479d4a72830940776a6235c700e525443118deea6e64e7605de6685
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174290180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c23a3657188116a9d77eb06600a55ff6db5de1852c41d537ec864e23ba8b03`
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
# Thu, 17 Nov 2022 01:13:47 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a70768968bbcccccf977f036e87e545c3b080ed6c44072a01e9dadb94051c454';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u352b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='863791dd8e0536a678f5e439c9c67199a0f3f18c76138a8e242775dfe1784009';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u352b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1633bd7590cb1cd72f5a1378ae8294451028b274d798e2a4ac672059a2f00fee';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 01:13:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:f8f0a6b1729383b3a6d18bdb8c1e38214542646ff9f964a9031d1bc31e23e4da`  
		Last Modified: Thu, 17 Nov 2022 01:22:14 GMT  
		Size: 101.0 MB (101028994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a5236eaa09928abc2ccb8044a2b840937f3145958ebbdbfbd71f03d2b759e3`  
		Last Modified: Thu, 17 Nov 2022 01:21:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
