## `eclipse-temurin:19-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:6cb264ce053a8d8a7ed9aa9d46427dbffe6a0db7d07f2de175b90a8124c7e236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:19-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:df138d5f75e540a3a471ac6210b7a2e29f98a9757e47ba68ea2e127d1acc04a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116222581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e923ab31d0e7ac84517cea372690ea1e6c21777f5c63586ff6af2d19d3e4475a`
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
# Wed, 25 Jan 2023 19:23:08 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Wed, 25 Jan 2023 19:24:01 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='3653f9e5ad21e4744e5a655e243fba2895651029bee23f3d2366d5debc41a736';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a30203431c7c21602227d39368c5af6e7abd19000d6da5562de7f3f5c57cbad5';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='59463543feb858dc2eabeea344491897806da5d09c3cbf5b7c93e86269e32a02';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7386e10c74f00a4382be0540bc0494854804ad79427d8a50ac77a4c7208ff348';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 25 Jan 2023 19:24:02 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:f66fd7a8e0c5116a4e6cadc2488fbaa190520fc0cea7c69261192b2927e50949`  
		Last Modified: Wed, 25 Jan 2023 19:32:06 GMT  
		Size: 49.4 MB (49441020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97d5fe3e90ee22d48a40b7e665aa8426225153984be4b86471b3adbbd9a7c75`  
		Last Modified: Wed, 25 Jan 2023 19:31:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3a1707b5527a663b1f8463ab6cbd0aeb91c18cf5c82a583c1f120b7eac342ab5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114319150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5ed5db4bbdcf6b8a5e9d6e8f59c94ac5ec7c9bd2b66fe83fe06972d136292a`
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
# Fri, 10 Feb 2023 20:11:13 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Fri, 10 Feb 2023 20:12:03 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='3653f9e5ad21e4744e5a655e243fba2895651029bee23f3d2366d5debc41a736';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a30203431c7c21602227d39368c5af6e7abd19000d6da5562de7f3f5c57cbad5';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='59463543feb858dc2eabeea344491897806da5d09c3cbf5b7c93e86269e32a02';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7386e10c74f00a4382be0540bc0494854804ad79427d8a50ac77a4c7208ff348';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 20:12:05 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:ee43d3034b0e8484a8f1b500026abbeb8a8e772a6f38abc68e38269aa5f6b93c`  
		Last Modified: Fri, 10 Feb 2023 20:16:24 GMT  
		Size: 48.9 MB (48896543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590c3a66a9162319eb3ab4e2a5c158cfcf862ca8e541964b2537a899db4fcff4`  
		Last Modified: Fri, 10 Feb 2023 20:16:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:27a55ae371214cda4debb34516da6b811235eb9dad1394055d429113b83a0525
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121683294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61331c074655a53b1c9b1b7f6cac7ac25d40ebf73bc06924a675723732029642`
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
# Fri, 10 Feb 2023 20:00:22 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Fri, 10 Feb 2023 20:01:28 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='3653f9e5ad21e4744e5a655e243fba2895651029bee23f3d2366d5debc41a736';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a30203431c7c21602227d39368c5af6e7abd19000d6da5562de7f3f5c57cbad5';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='59463543feb858dc2eabeea344491897806da5d09c3cbf5b7c93e86269e32a02';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7386e10c74f00a4382be0540bc0494854804ad79427d8a50ac77a4c7208ff348';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 20:01:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:ae22c3125d6bb305ef6030f50330ec133afe46d7979e7d8cd196b52092e2d477`  
		Last Modified: Fri, 10 Feb 2023 20:09:22 GMT  
		Size: 49.2 MB (49182199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6262b759cb587c2aa42a8a9fe2d5df2073d50f738aeaf72715db6839548789fc`  
		Last Modified: Fri, 10 Feb 2023 20:09:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c8460e7588a1f8024d067eb69077a4a10cdf2b41d24a69b39fa4275489993178
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117026411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d9a73d71925fa73eb4676434c6c7906060c130ccc1121445d396630aeafefb`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 10 Feb 2023 21:04:27 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='3653f9e5ad21e4744e5a655e243fba2895651029bee23f3d2366d5debc41a736';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_aarch64_linux_hotspot_19.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a30203431c7c21602227d39368c5af6e7abd19000d6da5562de7f3f5c57cbad5';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_ppc64le_linux_hotspot_19.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='59463543feb858dc2eabeea344491897806da5d09c3cbf5b7c93e86269e32a02';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_s390x_linux_hotspot_19.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7386e10c74f00a4382be0540bc0494854804ad79427d8a50ac77a4c7208ff348';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.2%2B7/OpenJDK19U-jre_x64_linux_hotspot_19.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Fri, 10 Feb 2023 21:04:29 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:ae9dc98b92d69ddb33109e411e79ced81397185ba3efad4714eadcfe2885ec18`  
		Last Modified: Fri, 10 Feb 2023 21:08:22 GMT  
		Size: 46.0 MB (46018783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72abce0159ad183ca9efebbf1c99269dbed06e4291d6f4ad02b42b7577c5ffd`  
		Last Modified: Fri, 10 Feb 2023 21:08:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
