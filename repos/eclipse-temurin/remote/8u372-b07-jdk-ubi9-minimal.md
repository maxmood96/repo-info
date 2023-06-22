## `eclipse-temurin:8u372-b07-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:d82d922696d58a0b8efe82e588e33d8fc33845a63c6bb61a0bf13acede88d2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u372-b07-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0c091d27cd25e1ba71227690b9fdbf1f601b8134c29128b5d8b23fafdca550f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120340604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce58b2d3bed95092aa82f614047b3cac3b84d89f083b1183937d419ed53ca09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 01:53:36 GMT
ADD file:80304e0bef72b7ea92e51e210b2106f2c76929c20237bda1e2504ed5f08a797b in / 
# Thu, 15 Jun 2023 01:53:37 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:53:37 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:53:38 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 15 Jun 2023 01:53:38 GMT
ENV container oci
# Thu, 15 Jun 2023 01:53:38 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:53:38 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:53:39 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:53:39 GMT
LABEL release=691
# Thu, 15 Jun 2023 01:53:39 GMT
ADD file:f9ce97cb03af747b91e8159962dd1fafb4875a94fd8e03fa1bea1e9a7c1ba028 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-691.json 
# Thu, 15 Jun 2023 01:53:39 GMT
ADD file:2ff83eb5063de7c62bc86b57ae37130f3c49c5f7d6920bc96b44baad3134fcb8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-691 
# Thu, 15 Jun 2023 01:53:39 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-691"
# Thu, 15 Jun 2023 01:53:40 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:53:41 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:53:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 01:08:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jun 2023 01:08:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 01:08:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Jun 2023 01:08:25 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 22 Jun 2023 01:08:25 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 22 Jun 2023 01:08:30 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Thu, 22 Jun 2023 01:08:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:62742f27dce5ebff467a57ad6bfa680820f3bc534cc313627f8113246276bf0f`  
		Last Modified: Wed, 21 Jun 2023 18:10:35 GMT  
		Size: 37.8 MB (37833161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89fad3074e960a219b14c1d9389a3f59012f3496f87a126808d6aef4ac84ee`  
		Last Modified: Thu, 22 Jun 2023 01:11:48 GMT  
		Size: 27.9 MB (27864943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d422fcdd9181982e0fc6066b94d06de688fe64f27af2a348829e0cb29481e09`  
		Last Modified: Thu, 22 Jun 2023 01:11:49 GMT  
		Size: 54.6 MB (54642341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913586a5122b4219db58eb89b07472895edd62c77bd44fb3af5a0581b2116e80`  
		Last Modified: Thu, 22 Jun 2023 01:11:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u372-b07-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8783fd08962c77ad2986b8c818e35c61e9c1f89ca2bcf624012fc02bdd901900
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118176886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b9fb5ed06ec08e006260107e189caf42b05a84df9d0e0f84f0dc9701ad09c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 01:53:37 GMT
ADD file:2ddf47843f2f56bf055d8a2d5a986816d35279705fd72a482cc996e557eb4d0d in / 
# Thu, 15 Jun 2023 01:53:38 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:53:38 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:53:38 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 15 Jun 2023 01:53:38 GMT
ENV container oci
# Thu, 15 Jun 2023 01:53:38 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:53:38 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:53:39 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:53:39 GMT
LABEL release=691
# Thu, 15 Jun 2023 01:53:39 GMT
ADD file:266cf5a0a08ad49bce286a2a6e6ed92bb75eaeccf0647ce1785fde528a6e4ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-691.json 
# Thu, 15 Jun 2023 01:53:39 GMT
ADD file:fd14cf6ab7b729a931fbee6ca52647a4566540b77950a20a9e14019b02a75ae8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-691 
# Thu, 15 Jun 2023 01:53:39 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-691"
# Thu, 15 Jun 2023 01:53:41 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:53:42 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:53:43 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 01:22:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jun 2023 01:22:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 01:22:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Jun 2023 01:22:29 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 22 Jun 2023 01:22:29 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 22 Jun 2023 01:22:34 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Thu, 22 Jun 2023 01:22:35 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4933b799093955850acfb98487d4801e9a478436ebdbe4db2585569f7dfc7a73`  
		Last Modified: Wed, 21 Jun 2023 18:10:47 GMT  
		Size: 36.1 MB (36137191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221abf6c7eabaab989c2b30a6ba34fbf0d167b44ff1c2c8ad78d55925af18fe9`  
		Last Modified: Thu, 22 Jun 2023 01:25:14 GMT  
		Size: 28.3 MB (28296608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fafc5bee4907f6d98edd1f3ac491eed81028632de77c1e40ee6ab1eacaf487`  
		Last Modified: Thu, 22 Jun 2023 01:25:15 GMT  
		Size: 53.7 MB (53742927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933cbedb9d3be272f9cd91261f350b1de49c05a74dc1c9f98cb830dcbeb58e1b`  
		Last Modified: Thu, 22 Jun 2023 01:25:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u372-b07-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:24870822e6a6950b99e8e8946fb5ca070de8cc7a2382d77a9949834fd779b4f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124818394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ee4e555df084b021b14f4bdc59640ece295dfc2fd012f96b9984a9b3d56602`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 01:54:23 GMT
ADD file:c1d758c5131eb31c12267045c3ab457513fcf413dda42a4641fa6e60cf265fd3 in / 
# Thu, 15 Jun 2023 01:54:24 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:54:24 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:54:24 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 15 Jun 2023 01:54:24 GMT
ENV container oci
# Thu, 15 Jun 2023 01:54:24 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:54:24 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:54:26 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:54:26 GMT
LABEL release=691
# Thu, 15 Jun 2023 01:54:26 GMT
ADD file:0eda173520172f76a0b725b37803c57a32c1391cda8419639363f4c2b7f4ac18 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-691.json 
# Thu, 15 Jun 2023 01:54:26 GMT
ADD file:5a376fbc447f597f91a76df815d29f894dce397f746be88bd73c0c852bd868aa in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-691 
# Thu, 15 Jun 2023 01:54:26 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:07" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-691"
# Thu, 15 Jun 2023 01:54:27 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:54:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:54:30 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 01:15:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jun 2023 01:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 01:15:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Jun 2023 01:15:54 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 22 Jun 2023 01:15:56 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 22 Jun 2023 01:16:07 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='195808eb42ab73535c84de05188914a52a47c1ac784e4bf66de95fe1fd315a5a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_aarch64_linux_hotspot_8u372b07.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='bb85303848fe402d4f1004f748f80ccb39cb11f356f50a513555d1083c3913b8';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u372b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='78a0b3547d6f3d46227f2ad8c774248425f20f1cd63f399b713f0cdde2cc376c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jdk_x64_linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Thu, 22 Jun 2023 01:16:10 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:e3f3a1bf0aa97991a0413fbe9daa5105fc285b24b4e2ac14458522802ff4e0ec`  
		Last Modified: Wed, 21 Jun 2023 18:11:05 GMT  
		Size: 42.3 MB (42261485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76b5a334e3072ec76c9e2fa0cbaea07673b1437abfa3bdd3c23ed0eca21d193`  
		Last Modified: Thu, 22 Jun 2023 01:19:16 GMT  
		Size: 30.4 MB (30423134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf9187634621332c329b7190a97c95df4903b229adf69a4f2e60d8900ef28ee`  
		Last Modified: Thu, 22 Jun 2023 01:19:19 GMT  
		Size: 52.1 MB (52133615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec42622bcfd6fa2b1fa5ea78794e154adafd909ab7ab300aa4d3026ace72e61b`  
		Last Modified: Thu, 22 Jun 2023 01:19:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
