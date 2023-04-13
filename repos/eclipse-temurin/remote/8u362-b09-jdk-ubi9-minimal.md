## `eclipse-temurin:8u362-b09-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:f01de4960dee156fc4bf256f21e0734d3bbf5455705e7e0a58871c398793f821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u362-b09-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4e0a505ec33351bb68a9511b1042d31e19d38516ae554b246b8b7a1de34696ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121415173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ddaa05e6f7fc2e8a82dd42f8665e0d897bf7a26b1751b815243ad092907d3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Apr 2023 13:07:33 GMT
ADD file:905b849da3572ece24997970bc5f8f41e7174ca401655a93b42989192f52bce7 in / 
# Tue, 04 Apr 2023 13:07:34 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 04 Apr 2023 13:07:34 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Tue, 04 Apr 2023 13:07:35 GMT
ADD multi:b69fbca1cffcb1fb28acb34486e2a3bc449bb345809fd618d7d6606c2a083b31 in /etc/yum.repos.d/ 
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Apr 2023 13:07:35 GMT
ENV container oci
# Tue, 04 Apr 2023 13:07:35 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Apr 2023 13:07:35 GMT
CMD ["/bin/bash"]
# Tue, 04 Apr 2023 13:07:35 GMT
RUN rm -rf /var/log/*
# Tue, 04 Apr 2023 13:07:35 GMT
LABEL release=1829
# Tue, 04 Apr 2023 13:07:36 GMT
ADD file:cf3eeb2e912ec7d5452258305aa3941508d6411e0f118883b2f48fd05b560585 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1829.json 
# Tue, 04 Apr 2023 13:07:36 GMT
ADD file:e6349894ce1fac0ce2388a5e758ebb3154dba47fc5ff70ebb97c6f8cb831f391 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1829 
# Tue, 04 Apr 2023 13:07:36 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-04-04T12:58:00" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1829"
# Tue, 04 Apr 2023 13:07:37 GMT
RUN rm -f '/etc/yum.repos.d/repo-6b42c.repo' '/etc/yum.repos.d/repo-8e12e.repo'
# Tue, 04 Apr 2023 13:07:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 04 Apr 2023 13:07:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 13 Apr 2023 00:00:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Apr 2023 00:00:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Apr 2023 00:00:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Apr 2023 00:00:11 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 13 Apr 2023 00:00:11 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Thu, 13 Apr 2023 00:00:17 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Thu, 13 Apr 2023 00:00:17 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:7bffb309b4e88826a3c7dc629c1ebd7b3aa6ad861157f4acea7c4f8057fa30d5`  
		Last Modified: Wed, 12 Apr 2023 00:12:26 GMT  
		Size: 37.9 MB (37857227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f333d7fe9465a3809d1f6e8b8e23215ec312598f7bb283afb16aff784e52e9`  
		Last Modified: Thu, 13 Apr 2023 00:03:03 GMT  
		Size: 28.9 MB (28922011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8baaa43bad9397f21b7379f62cbe631027b036f48c0285cceb670fd207afb0`  
		Last Modified: Thu, 13 Apr 2023 00:03:05 GMT  
		Size: 54.6 MB (54635775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141b3e8a60e4408dbac6be6eb65a83b2d123a9ea704bcc1e5c1b5f7121f6847d`  
		Last Modified: Thu, 13 Apr 2023 00:02:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u362-b09-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1eb0ad76994c509f1ba17cfb0f849f3810cd165f8bde5a7d997297953486f495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119228819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f843d5d588d7a3cddecafe2d118b063958aebffca250ed03138fd3dce3340e65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Apr 2023 13:07:33 GMT
ADD file:afa1c5c010e4cadc5caa512540bfe7a19a2119f5a23c11699f1fc5ebc3791570 in / 
# Tue, 04 Apr 2023 13:07:34 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 04 Apr 2023 13:07:34 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Tue, 04 Apr 2023 13:07:34 GMT
ADD multi:b69fbca1cffcb1fb28acb34486e2a3bc449bb345809fd618d7d6606c2a083b31 in /etc/yum.repos.d/ 
# Tue, 04 Apr 2023 13:07:34 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Apr 2023 13:07:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Tue, 04 Apr 2023 13:07:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Apr 2023 13:07:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Apr 2023 13:07:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Apr 2023 13:07:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Apr 2023 13:07:34 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Apr 2023 13:07:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Apr 2023 13:07:34 GMT
ENV container oci
# Tue, 04 Apr 2023 13:07:34 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Apr 2023 13:07:34 GMT
CMD ["/bin/bash"]
# Tue, 04 Apr 2023 13:07:36 GMT
RUN rm -rf /var/log/*
# Tue, 04 Apr 2023 13:07:36 GMT
LABEL release=1829
# Tue, 04 Apr 2023 13:07:36 GMT
ADD file:eeb46db8ece74b6067d83e79285bc2792da01bf3b91d21f47ba014c45d95d345 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1829.json 
# Tue, 04 Apr 2023 13:07:36 GMT
ADD file:fa9a9550d67d7b0c75e5937adbdb8e9c5e69c7db36b0059436a49607b7a5ab77 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1829 
# Tue, 04 Apr 2023 13:07:36 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-04-04T12:58:00" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1829"
# Tue, 04 Apr 2023 13:07:37 GMT
RUN rm -f '/etc/yum.repos.d/repo-6b42c.repo' '/etc/yum.repos.d/repo-8e12e.repo'
# Tue, 04 Apr 2023 13:07:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 04 Apr 2023 13:07:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 12 Apr 2023 21:01:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 21:01:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 21:01:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Apr 2023 21:01:21 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 12 Apr 2023 21:01:21 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 12 Apr 2023 21:01:26 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 12 Apr 2023 21:01:27 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f5f2c7a71685ec0f59198b120b1eeb1b4156a8e348e3278e9af113dbfd938c63`  
		Last Modified: Wed, 12 Apr 2023 00:12:36 GMT  
		Size: 36.2 MB (36175114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae77f5963c85da26562df7a2bf14b3d03b5142a01dc25b3dae1448566af62f8`  
		Last Modified: Wed, 12 Apr 2023 21:03:41 GMT  
		Size: 29.3 MB (29325370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ba10027329b4ec9a4fe6116aa40d16e594d87ac253be957407a609030c6a58`  
		Last Modified: Wed, 12 Apr 2023 21:03:53 GMT  
		Size: 53.7 MB (53728175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415b42059a28ebcad53eb5a23518a2f9269011ffcd06f0584ff121c60e5c1369`  
		Last Modified: Wed, 12 Apr 2023 21:03:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u362-b09-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b949c322c8b2916587f2075d20d9b7ccec53d74c3bc1fd8f677f7fb7326395d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124641537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7aa2ed3a98aa3823597df8241f18c78dcbe73722fc2725fee7668a64c9a615`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Apr 2023 13:07:54 GMT
ADD file:d95a1c9a5bbb0497cd30daf349083a943c7474b5ce4727538b0f3af948d62548 in / 
# Tue, 04 Apr 2023 13:07:56 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 04 Apr 2023 13:07:57 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Tue, 04 Apr 2023 13:07:57 GMT
ADD multi:b69fbca1cffcb1fb28acb34486e2a3bc449bb345809fd618d7d6606c2a083b31 in /etc/yum.repos.d/ 
# Tue, 04 Apr 2023 13:07:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Apr 2023 13:07:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Tue, 04 Apr 2023 13:07:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Apr 2023 13:07:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Apr 2023 13:07:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Apr 2023 13:07:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Apr 2023 13:07:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Apr 2023 13:07:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Apr 2023 13:07:57 GMT
ENV container oci
# Tue, 04 Apr 2023 13:07:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Apr 2023 13:07:57 GMT
CMD ["/bin/bash"]
# Tue, 04 Apr 2023 13:07:59 GMT
RUN rm -rf /var/log/*
# Tue, 04 Apr 2023 13:07:59 GMT
LABEL release=1829
# Tue, 04 Apr 2023 13:08:00 GMT
ADD file:f8f74c34929680c686c32b2da846a19db607deeb99250ddbec9124c941503991 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1829.json 
# Tue, 04 Apr 2023 13:08:01 GMT
ADD file:c0f35b2d0f64fe7063d1d3fe631133c801d5bc9101f713dab560dfc4ed2f29fc in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1829 
# Tue, 04 Apr 2023 13:08:01 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-04-04T12:58:00" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1829"
# Tue, 04 Apr 2023 13:08:03 GMT
RUN rm -f '/etc/yum.repos.d/repo-6b42c.repo' '/etc/yum.repos.d/repo-8e12e.repo'
# Tue, 04 Apr 2023 13:08:05 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 04 Apr 2023 13:08:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 12 Apr 2023 22:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 22:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 22:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Apr 2023 22:59:52 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 12 Apr 2023 22:59:55 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 12 Apr 2023 23:00:10 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 12 Apr 2023 23:00:18 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5fef3fbf7e4557a50ffaf81313edae4a5a4c17a3cae0fa15adff1b82be55c646`  
		Last Modified: Wed, 12 Apr 2023 00:12:47 GMT  
		Size: 40.9 MB (40860934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9b68e5a13516c526c59005ee43ec07496b956cecfb1f5ada5c01f9efda5a6c`  
		Last Modified: Wed, 12 Apr 2023 23:04:54 GMT  
		Size: 31.7 MB (31670593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7ad230ab65d2149bf15dd278ece401dd5b42471c38057553d2196b532b1ae`  
		Last Modified: Wed, 12 Apr 2023 23:04:57 GMT  
		Size: 52.1 MB (52109849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9493c4020f111283525f950db0608648dd14901edd298c2a7efc4308475e1b`  
		Last Modified: Wed, 12 Apr 2023 23:04:44 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
