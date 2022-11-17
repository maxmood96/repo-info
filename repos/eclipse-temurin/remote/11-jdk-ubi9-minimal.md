## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:0d390916f41d834d2de94d1f89178af6a42df6ea831fc4f18cb5f188cbef6809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:829f5e6e6304580438044a56d18bea08c4a7a71be2718b16f1e6c69dea9abd39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262534611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59f85d03039bfb1871e50bc3e73d54f27bb2dd5d9bcff4ea54705152714ceba`
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
# Thu, 17 Nov 2022 00:21:01 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Thu, 17 Nov 2022 00:21:14 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d18b5dd73fce9edd5c58f623a1173f9ee2d45023836b8753b96beae51673a432';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='18c636bd103e240d29cdb30d7867720ea9fb9ff7c645738bfb4d5b8027269263';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eb861db1433ddc1b89f170b789fafde282f137218d6d985fb5c2003e4ff44984';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b8d46ed08ef4859476fe6421a7690d899ed83dce63f13fd894f994043177ef3c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 00:21:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Nov 2022 00:21:17 GMT
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
	-	`sha256:dfb84c91d63d03434ebd2bc2adf8f2c332a521afae1579995327b496b42a25a1`  
		Last Modified: Thu, 17 Nov 2022 00:25:58 GMT  
		Size: 194.9 MB (194928839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3566155a4313f2cc44f5f4ad9143885caaab8aecd68c7ffe755a27e1ac5bd2c2`  
		Last Modified: Thu, 17 Nov 2022 00:25:44 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e7ea4ec084e77f86334fa73a6aaf913999f376f9a87d491646271f7522fee19d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257863082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe6410b19b08f3c1e348ed0184b6a0ffe7ae02937e16597afcb153faa0b01fe`
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
# Wed, 16 Nov 2022 23:40:32 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Wed, 16 Nov 2022 23:40:52 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d18b5dd73fce9edd5c58f623a1173f9ee2d45023836b8753b96beae51673a432';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='18c636bd103e240d29cdb30d7867720ea9fb9ff7c645738bfb4d5b8027269263';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eb861db1433ddc1b89f170b789fafde282f137218d6d985fb5c2003e4ff44984';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b8d46ed08ef4859476fe6421a7690d899ed83dce63f13fd894f994043177ef3c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Wed, 16 Nov 2022 23:40:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 16 Nov 2022 23:40:55 GMT
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
	-	`sha256:29a6aa1f6e46d936907f509ae6a8024276921f403b3c7ca5b4feef443b6000e3`  
		Last Modified: Wed, 16 Nov 2022 23:44:53 GMT  
		Size: 191.7 MB (191681440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8cc88a694fac445833cf4b011f37805fc584f5746ae57dde44e1930485d24b`  
		Last Modified: Wed, 16 Nov 2022 23:44:42 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1c3ecdf81e099ae11fd7998f292fb63a7441a8fd18c284e4a976f58500d95532
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250186445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664df04580cb42be2c57dc79f83474d033c5221eec45d986d84122f1e9d5501f`
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
# Thu, 17 Nov 2022 01:14:46 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Thu, 17 Nov 2022 01:15:13 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d18b5dd73fce9edd5c58f623a1173f9ee2d45023836b8753b96beae51673a432';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='18c636bd103e240d29cdb30d7867720ea9fb9ff7c645738bfb4d5b8027269263';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eb861db1433ddc1b89f170b789fafde282f137218d6d985fb5c2003e4ff44984';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b8d46ed08ef4859476fe6421a7690d899ed83dce63f13fd894f994043177ef3c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 01:15:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Nov 2022 01:15:20 GMT
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
	-	`sha256:b17a2da7358f600ed5c344fb1be90d7b545adc0b43302b7b1e8d1c1e34f3036c`  
		Last Modified: Thu, 17 Nov 2022 01:23:19 GMT  
		Size: 176.9 MB (176925242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa894fbe9fd12b00f095a9f6b666394935055d9450a9c541f61e0b0b4b5f64a`  
		Last Modified: Thu, 17 Nov 2022 01:22:57 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:d960f8e969dfabf587220f00885999d330312e0ea326f94d1dfe9b6d7572f36a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240145440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec85f6d3fee766e15e962aa7637172b2f91c3c2ca9bc2488555bd628c75f52c`
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
# Wed, 16 Nov 2022 23:59:43 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Wed, 16 Nov 2022 23:59:52 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d18b5dd73fce9edd5c58f623a1173f9ee2d45023836b8753b96beae51673a432';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='18c636bd103e240d29cdb30d7867720ea9fb9ff7c645738bfb4d5b8027269263';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eb861db1433ddc1b89f170b789fafde282f137218d6d985fb5c2003e4ff44984';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b8d46ed08ef4859476fe6421a7690d899ed83dce63f13fd894f994043177ef3c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Wed, 16 Nov 2022 23:59:57 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 16 Nov 2022 23:59:57 GMT
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
	-	`sha256:fc364ce63f57cb92c67b015b41d5ba675cbeec7208d7d479c855dd2b6c8c8c5d`  
		Last Modified: Thu, 17 Nov 2022 00:04:42 GMT  
		Size: 168.3 MB (168323215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf631e269fcef1136aec3cbd7f42c3f2333ae94b004349c6ca6e72ee871e3a8`  
		Last Modified: Thu, 17 Nov 2022 00:04:31 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
