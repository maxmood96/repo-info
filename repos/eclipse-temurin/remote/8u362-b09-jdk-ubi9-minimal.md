## `eclipse-temurin:8u362-b09-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:3913211e6c436915686a5257b42f86ecd2b30598c180b853af6c3135828a7068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u362-b09-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:12521acb3c867ea86b091c42c5992107e2abe6f9d7b6b9d2fae4a11f2101ad81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121447429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3420d3962005d61ed744f024d2ab421ebf976437019bee114cb356a7a28771`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 07 Feb 2023 17:12:52 GMT
ADD file:7f3dba2b8944352969f2190e0eaa7f634665cb0f837adb2418465697663b7dd0 in / 
# Tue, 07 Feb 2023 17:12:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 07 Feb 2023 17:12:53 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Tue, 07 Feb 2023 17:12:53 GMT
ADD multi:6893bb0509c7aae7bc271b3e27ee01082fe34bd3f5e8d8e4ad49d547e73ac56f in /etc/yum.repos.d/ 
# Tue, 07 Feb 2023 17:12:53 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 07 Feb 2023 17:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Tue, 07 Feb 2023 17:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 07 Feb 2023 17:12:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 07 Feb 2023 17:12:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 07 Feb 2023 17:12:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 07 Feb 2023 17:12:53 GMT
LABEL io.openshift.expose-services=""
# Tue, 07 Feb 2023 17:12:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 07 Feb 2023 17:12:53 GMT
ENV container oci
# Tue, 07 Feb 2023 17:12:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Feb 2023 17:12:53 GMT
CMD ["/bin/bash"]
# Tue, 07 Feb 2023 17:12:54 GMT
RUN rm -rf /var/log/*
# Tue, 07 Feb 2023 17:12:54 GMT
ADD file:3033ccd9e61e6dce208eda3c72b9a1b32bc6d9f9b494d81d1614587d6c0077f3 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1760.1675784957.json 
# Tue, 07 Feb 2023 17:12:54 GMT
ADD file:a8e380d1abf7420577ace8ed0d26087daf587430895ca4a8d7d407d1b4420812 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1760.1675784957 
# Tue, 07 Feb 2023 17:12:54 GMT
LABEL "release"="1760.1675784957" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-02-07T16:25:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1760.1675784957"
# Tue, 07 Feb 2023 17:12:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-1774985-d0e8e.repo' '/etc/yum.repos.d/gitweb-1077d.repo'
# Tue, 07 Feb 2023 17:12:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 07 Feb 2023 17:12:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 11 Feb 2023 04:37:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Feb 2023 04:37:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 04:37:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 11 Feb 2023 04:37:14 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Sat, 11 Feb 2023 04:37:14 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Sat, 11 Feb 2023 04:37:23 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9290a8beefd7a94f0eb030f62d402411a852100482b9c5b63714bacc57002c2a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u362b09.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='69658dd316c6a160915655971573179766e19c6610ea03880c1e578a0e518f74';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u362b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1486a792fb224611ce0cd0e83d4aacd3503b56698549f8e9a9f0a6ebb83bdba1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Sat, 11 Feb 2023 04:37:24 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4a23d2a9ea05cf85aaee9749dfb13c60e0272f4313d17833f62f53ebde12a710`  
		Last Modified: Thu, 09 Feb 2023 08:52:06 GMT  
		Size: 37.9 MB (37897058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf3cc054da9b94c8d7623d8d1362262c1bc1142e7f43e01d9552f5d5877fa24`  
		Last Modified: Sat, 11 Feb 2023 04:41:39 GMT  
		Size: 28.9 MB (28914412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1817242d0ccab7ca1a289b2621ee8ec63af83a8e9a29cb37b3c8e18bd103ed`  
		Last Modified: Sat, 11 Feb 2023 04:41:42 GMT  
		Size: 54.6 MB (54635798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afe37faa008443a88f8f0e06f9266ced18eb48fb281e4d00bb84cffdc0270f4`  
		Last Modified: Sat, 11 Feb 2023 04:41:35 GMT  
		Size: 161.0 B  
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
