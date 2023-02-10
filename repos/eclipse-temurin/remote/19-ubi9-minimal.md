## `eclipse-temurin:19-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:71841dc1e1c85cbaa722f8e48d99de5eefb712c28ad074bea8dc88f6306fc9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:19-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d5e099da1309ad8a66db9bde0470f69f737a921a97562cbc7626fd777a69af58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267902656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63be15e3c54aa1af7702d1f3a96e0e8fa05582d8044035f604a217c854f3f34`
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
# Wed, 25 Jan 2023 19:23:08 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Wed, 25 Jan 2023 19:23:17 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 25 Jan 2023 19:23:19 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 25 Jan 2023 19:23:19 GMT
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
	-	`sha256:1b9d3367fa8f4f7473b327cba5e0f810f8688bde6ba57632bf7340cba25d16a0`  
		Last Modified: Wed, 25 Jan 2023 19:30:44 GMT  
		Size: 201.1 MB (201121078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94240c179795cb22a1a635ac1c3f9313b7ed5c77e45e02d321576778e4aecd2`  
		Last Modified: Wed, 25 Jan 2023 19:30:28 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:10d15761c3f6d0ade523f1f79a4a4a6c58aab14e84bc67b9a7915c910f484437
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265281173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1b6436c47ae605ed08afcda4362bab7ca7f81e9a852963cc79ab17cc23c62f`
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
# Fri, 10 Feb 2023 20:11:13 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Fri, 10 Feb 2023 20:11:48 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 20:11:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 10 Feb 2023 20:11:51 GMT
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
	-	`sha256:ccc70b29b7888dd426f2b98597753a79af501fa5403dc164689aa13ca68ac2e1`  
		Last Modified: Fri, 10 Feb 2023 20:16:04 GMT  
		Size: 199.9 MB (199858548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0896aed0007dc697cf794d4777b51e7488106f4b78510fde4ceffc4c4e854861`  
		Last Modified: Fri, 10 Feb 2023 20:15:51 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:6d94fd87c0a643990cfcf5598e65790513c7fd19eb4840fa5a1446b7dd00f267
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272789471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3cbfdbe66b26877d34b1206b64904c7a0f3717619d63837b213f18e43d7166`
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
# Fri, 10 Feb 2023 20:00:22 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Fri, 10 Feb 2023 20:00:47 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 20:00:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 10 Feb 2023 20:00:56 GMT
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
	-	`sha256:ee007ffbcab9ac95c4b870d505307367d0244ea249dd79039b04db6a85e28e26`  
		Last Modified: Fri, 10 Feb 2023 20:08:51 GMT  
		Size: 200.3 MB (200288359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d43e3562fba312976e8e148b8d10f8a2b683b0bddbda358c5d45e0d2a61bfa1`  
		Last Modified: Fri, 10 Feb 2023 20:08:23 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3f768b0fd9dc7cead30aa6db5ba05005e1f204ed7de04710093914c4aa9bd5cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259505122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147e875c641265d8d37d26966dffd0a99a7a1b1cce0ec4c0d1ceb19c158562d0`
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
# Fri, 10 Feb 2023 21:03:52 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Fri, 10 Feb 2023 21:04:01 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='1c4be9aa173cb0deb0d215643d9509c8900e5497290b29eee4bee335fa57984f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='173d1256dfb9d13d309b5390e6bdf72d143b512201b0868f9d349d5ed3d64072';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f2512f9a8e9847dd5d3557c39b485a8e7a1ef37b601dcbcb748d22e49f44815c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a3ba7a3f8c3a5999e2c91ea1dca843435a0d1c43737bd2f6822b2f02fc52165';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jdk_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 21:04:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 10 Feb 2023 21:04:06 GMT
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
	-	`sha256:74576df30d716c87b26d2510651a7da20735bcc187a8d7fa7425bbd887183410`  
		Last Modified: Fri, 10 Feb 2023 21:08:03 GMT  
		Size: 188.5 MB (188497480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb40c520995e4265c3c4f750070735cbeda866224f457183082ed8fd0dd0adf`  
		Last Modified: Fri, 10 Feb 2023 21:07:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
