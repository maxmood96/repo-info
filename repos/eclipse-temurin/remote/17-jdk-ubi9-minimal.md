## `eclipse-temurin:17-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:6df0c670a6bfc338c64056cd19aedcf229c1f5ca4c0867d0b88fd7abf839f188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4814332eeda1c36e3dbd476a7865ef4f895be8679d54bb1cea1714fb53384cc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259221272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2820687912df95fef2ada2bdf7f0379ac8c1093438f9a18003b791ae8320abcd`
-	Default Command: `["jshell"]`

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
# Tue, 24 Jan 2023 18:46:29 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 24 Jan 2023 18:46:37 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Tue, 24 Jan 2023 18:46:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 24 Jan 2023 18:46:40 GMT
CMD ["jshell"]
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
	-	`sha256:5a205b3d7f4ed2a59e24cbd33750355e98ff0990886fed431bbf82d6a9e2338f`  
		Last Modified: Tue, 24 Jan 2023 18:55:04 GMT  
		Size: 192.4 MB (192439693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab3c894391da44b96d2902075fc5841c9e35e4c9440fd654e1ff6e65e766759`  
		Last Modified: Tue, 24 Jan 2023 18:54:49 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b05a60ad1c1038f65ed69ff97b5653b415ee1b7c721804953bab2eed9be090ab
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256688088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570391b65edcfbff63ffe10b03680c3d76b0a3459a0ec657f631d5543c04d4d8`
-	Default Command: `["jshell"]`

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
# Fri, 10 Feb 2023 20:10:34 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Fri, 10 Feb 2023 20:10:48 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 20:10:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 10 Feb 2023 20:10:51 GMT
CMD ["jshell"]
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
	-	`sha256:9e15d79ea3e154da304356ce2e8050b81fe21d4d4e2d3ce12c0eaefa71a91c0f`  
		Last Modified: Fri, 10 Feb 2023 20:15:18 GMT  
		Size: 191.3 MB (191265464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0be04cb9540ff358317f55a13ed92149257b964b973ff1e703747ab0f0918f`  
		Last Modified: Fri, 10 Feb 2023 20:15:06 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:2d2a712ff418f63a35c1d9eb5665cf1aef0c3dd0c248da9743637b632c755218
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264319958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d78bf304028822d0657e122f38f542a8041b13c7e5d8a4da485eab22c51c3b`
-	Default Command: `["jshell"]`

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
# Fri, 10 Feb 2023 19:58:54 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Fri, 10 Feb 2023 19:59:21 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 19:59:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 10 Feb 2023 19:59:29 GMT
CMD ["jshell"]
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
	-	`sha256:5494412d38b0bc931ec8d647ed8dea1acac53ca0cd30117fffc10657b3093794`  
		Last Modified: Fri, 10 Feb 2023 20:07:32 GMT  
		Size: 191.8 MB (191818845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e122efc2f975e3d1b9a3440ea0a0e4572bd4c25646068c337c67cdef00f926`  
		Last Modified: Fri, 10 Feb 2023 20:07:07 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:56f64b45e42b9b6b734345121da2b0e7ee2b0d2189799cc1d029d55d734032e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251286342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe09d375c13d7e18176fc7f8625e5ae1fdc3bd0bd73c3a481f6e09cf1a721ac`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 07 Feb 2023 17:12:28 GMT
ADD file:cb6c2adde8b97cea587e9a8db464fc01bdc9f0b673b0ad2e0e2678122252d92b in / 
# Tue, 07 Feb 2023 17:12:30 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 07 Feb 2023 17:12:30 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Tue, 07 Feb 2023 17:12:31 GMT
ADD multi:6893bb0509c7aae7bc271b3e27ee01082fe34bd3f5e8d8e4ad49d547e73ac56f in /etc/yum.repos.d/ 
# Tue, 07 Feb 2023 17:12:31 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 07 Feb 2023 17:12:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Tue, 07 Feb 2023 17:12:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 07 Feb 2023 17:12:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 07 Feb 2023 17:12:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 07 Feb 2023 17:12:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 07 Feb 2023 17:12:31 GMT
LABEL io.openshift.expose-services=""
# Tue, 07 Feb 2023 17:12:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 07 Feb 2023 17:12:31 GMT
ENV container oci
# Tue, 07 Feb 2023 17:12:31 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Feb 2023 17:12:31 GMT
CMD ["/bin/bash"]
# Tue, 07 Feb 2023 17:12:32 GMT
RUN rm -rf /var/log/*
# Tue, 07 Feb 2023 17:12:32 GMT
ADD file:78585b6515461a96d7b0c2eba9ff34a70fabfd23be248af79ac46b32df635372 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1760.1675784957.json 
# Tue, 07 Feb 2023 17:12:33 GMT
ADD file:fd4561208b14fefd702eec93980ad5cba7b7fd20966762594227a4ec0b1538be in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1760.1675784957 
# Tue, 07 Feb 2023 17:12:33 GMT
LABEL "release"="1760.1675784957" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-02-07T16:25:34" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1760.1675784957"
# Tue, 07 Feb 2023 17:12:34 GMT
RUN rm -f '/etc/yum.repos.d/odcs-1774985-d0e8e.repo' '/etc/yum.repos.d/gitweb-1077d.repo'
# Tue, 07 Feb 2023 17:12:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 07 Feb 2023 17:12:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 10 Feb 2023 21:01:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Feb 2023 21:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Feb 2023 21:01:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 10 Feb 2023 21:02:08 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Fri, 10 Feb 2023 21:02:59 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Fri, 10 Feb 2023 21:03:08 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='9e0e88bbd9fa662567d0c1e22d469268c68ac078e9e5fe5a7244f56fec71f55f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cb772c3fdf3f9fed56f23a37472acf2b80de20a7113fe09933891c6ef0ecde95';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='32e53321dd3e724e111e5445fbdcbcefde893e59055cc1f102d20fa3bb62ccc3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a0b1b9dd809d51a438f5fa08918f9aca7b2135721097f0858cf29f77a35d4289';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 21:03:12 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 10 Feb 2023 21:03:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d5757b3a020addebbf3ea062c1bdebe1597a8a7fa7e6b7857030d5dec4afe0c`  
		Last Modified: Thu, 09 Feb 2023 08:51:50 GMT  
		Size: 36.1 MB (36142353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae97706e9b35f25eeb9e3eb6acf9e5dbb2a4ac0ead4b1f7394468612ad8513ce`  
		Last Modified: Fri, 10 Feb 2023 21:06:34 GMT  
		Size: 34.9 MB (34865115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290ab305a20fb3f0b5fe72111a3d218f49b47ccdbed95950ab377725f7481788`  
		Last Modified: Fri, 10 Feb 2023 21:07:20 GMT  
		Size: 180.3 MB (180278701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5006879785e11237e07822aa6be53b0702e5921a3894b8da515fe7f9f3d9f356`  
		Last Modified: Fri, 10 Feb 2023 21:07:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
