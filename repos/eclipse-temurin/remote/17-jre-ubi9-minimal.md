## `eclipse-temurin:17-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:fe651a8ec8d0dc04cfcc24fd025a03401d7a32933e5b09c2a9a09f33f9178dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4a509b34e7ad76b4e705a9718b08f948a38d895815a93415ddd9595547bd6634
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96481541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda82c561bd8b39ac420d736ff8cd0ac9248cdbe91fd2618101a1584ab2526ae`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 26 Jan 2024 01:58:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Jan 2024 01:58:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:58:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Jan 2024 01:58:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Fri, 26 Jan 2024 01:59:48 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 26 Jan 2024 02:00:16 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 26 Jan 2024 02:00:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 26 Jan 2024 02:00:17 GMT
COPY file:80168d55afbbfdfea820e78ae2e1141fd21095cf26d68a4715fadfae5beb9e0b in /__cacert_entrypoint.sh 
# Fri, 26 Jan 2024 02:00:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac79c30eef6754f3d5aa78581ea68cc4242943acadd0ebea4f8b9dc1c5914ab7`  
		Last Modified: Fri, 26 Jan 2024 02:02:02 GMT  
		Size: 11.6 MB (11597577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b72ee28e589667720fd082997ed243b453c1dc34d8fa1fd99d4452fce5d9d97`  
		Last Modified: Fri, 26 Jan 2024 02:03:58 GMT  
		Size: 47.2 MB (47161321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b485bd7079907cff6f690d5fa77550e946dc8e9641ed7f699846c2dbdce51`  
		Last Modified: Fri, 26 Jan 2024 02:03:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac50a76615913048dffceafca724c2da794f4e1ae63313780a0082f36867471`  
		Last Modified: Fri, 26 Jan 2024 02:03:51 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e40f59ee9bf3f267e7750fb8972c91662f7ceeb9a60f2c3bf455fd87d9217c5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94837179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76228ee20a8f16ab2787cf3a22910003f6e7ef2650631a100ca5799386f8790`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 26 Jan 2024 02:26:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Jan 2024 02:26:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 02:26:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Jan 2024 02:26:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Fri, 26 Jan 2024 02:27:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 26 Jan 2024 02:27:57 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 26 Jan 2024 02:27:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 26 Jan 2024 02:27:58 GMT
COPY file:80168d55afbbfdfea820e78ae2e1141fd21095cf26d68a4715fadfae5beb9e0b in /__cacert_entrypoint.sh 
# Fri, 26 Jan 2024 02:27:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57606f358ad8d4841542a3025b1feab6d2bb1033c0d6c82d16f908db04722c10`  
		Last Modified: Fri, 26 Jan 2024 02:29:08 GMT  
		Size: 12.2 MB (12152132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930e5b814a722ace38cb2ffd31da7d331e04512123f6fe29b7e8649e2d6bcc8d`  
		Last Modified: Fri, 26 Jan 2024 02:30:50 GMT  
		Size: 46.6 MB (46635124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4d5ba145acb8e83da79b44bafe828630e202d2dce082567c9da784fe1edeea`  
		Last Modified: Fri, 26 Jan 2024 02:30:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4021718977d6af0de416d3289ca2d82a3505d250f4ff4e9ce9e336b15c422c44`  
		Last Modified: Fri, 26 Jan 2024 02:30:45 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:41496b3ed9e38c95e8abd50a728cec768045909207569661b53e6c72dacb8875
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102352026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b434f97fe46881734f5cd65302ef027f690c7539c52f5c650d7186312c488a0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 17 Jan 2024 19:19:03 GMT
ADD file:df0617a0702d6fcc11ee30e344357a75c6c91c5e5eb174951aad6c5cef0e845b in / 
# Wed, 17 Jan 2024 19:19:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:19:06 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:19:07 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:19:07 GMT
ENV container oci
# Wed, 17 Jan 2024 19:19:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:19:07 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:19:10 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:19:10 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:19:10 GMT
ADD file:3f468e77179542afdf211420f105b5678cd54f2e899d127556bc80a014fbae6a in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:19:10 GMT
ADD file:aeb01c9a1302a02244512fc6820189c5bc5001c9a42470420da268fb1cee5295 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:19:10 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:19:13 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:19:16 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:19:21 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 26 Jan 2024 01:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Jan 2024 01:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 26 Jan 2024 01:19:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Fri, 26 Jan 2024 01:21:38 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 26 Jan 2024 01:22:16 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 26 Jan 2024 01:22:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 26 Jan 2024 01:22:20 GMT
COPY file:80168d55afbbfdfea820e78ae2e1141fd21095cf26d68a4715fadfae5beb9e0b in /__cacert_entrypoint.sh 
# Fri, 26 Jan 2024 01:22:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d8e558e99693b636a7ac64b024a003c505239316a353b7663603283057bcb110`  
		Last Modified: Thu, 25 Jan 2024 18:08:23 GMT  
		Size: 42.1 MB (42101515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab6b507b188b61e86e6d9bf2ce8006fd8cc5527c9d7d6b27da38d404facf278`  
		Last Modified: Fri, 26 Jan 2024 01:24:06 GMT  
		Size: 13.2 MB (13227731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2f0b2ceba3f79c5f9f0f9b400db9c5de510f804cab1500fa71a8a484502eb8`  
		Last Modified: Fri, 26 Jan 2024 01:26:04 GMT  
		Size: 47.0 MB (47021909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246428f077e46730792ef35636cda956801b19ff130038f2acd477abad9d6cd9`  
		Last Modified: Fri, 26 Jan 2024 01:25:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f0bd3c8945bf896e2dc49ceaf968554035c83d61267bc8919bec2ee37a5dda`  
		Last Modified: Fri, 26 Jan 2024 01:25:56 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:a1e28488fcf8f1f184bc51ae6ac5841afbfecf48fe69c52932f7c2bbef3573f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92485966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e5cc2a8c255fdf20128bf2c8f50afe677a759d832c0103d7e0eab029540056`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 07 Dec 2023 04:19:12 GMT
ADD file:f28428576778c7445b6d84f230feb4cf5f485c09878c17b5308e66f47e60dd6b in / 
# Thu, 07 Dec 2023 04:19:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 07 Dec 2023 04:19:13 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 07 Dec 2023 04:19:13 GMT
ADD multi:8257bc82024891d335e91a6d5e44bb825bdb87abe8bc1d2ee3fcfb9e8cbecea1 in /etc/yum.repos.d/ 
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Dec 2023 04:19:13 GMT
ENV container oci
# Thu, 07 Dec 2023 04:19:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 04:19:13 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 04:19:15 GMT
RUN rm -rf /var/log/*
# Thu, 07 Dec 2023 04:19:15 GMT
LABEL release=1475
# Thu, 07 Dec 2023 04:19:15 GMT
ADD file:c3f990a430d6edcbf823d30c7448598ff08ec2c99ea64ed8f5e7267948f7744e in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1475.json 
# Thu, 07 Dec 2023 04:19:15 GMT
ADD file:2ce5db9476b24b8df5425d0980e82ff5904b59022728f19b59a69df51a56dd68 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1475 
# Thu, 07 Dec 2023 04:19:15 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-12-07T04:10:36" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1475"
# Thu, 07 Dec 2023 04:19:16 GMT
RUN rm -f '/etc/yum.repos.d/repo-84783.repo' '/etc/yum.repos.d/repo-186d3.repo'
# Thu, 07 Dec 2023 04:19:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 07 Dec 2023 04:19:19 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 14 Dec 2023 01:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Dec 2023 01:58:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 01:58:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 17:22:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Thu, 25 Jan 2024 17:30:54 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Thu, 25 Jan 2024 17:35:06 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 25 Jan 2024 17:35:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 17:35:09 GMT
COPY file:80168d55afbbfdfea820e78ae2e1141fd21095cf26d68a4715fadfae5beb9e0b in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 17:35:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c5417d2c3fb20ae8c25c21a43ae726873ed44925368ac0d8ffb5a7414ecaad64`  
		Last Modified: Wed, 13 Dec 2023 18:09:23 GMT  
		Size: 36.0 MB (36005795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077660e2d57b125e1efc1c3a441b89379f61c1cb9a92e8be7681198d9ab2eef7`  
		Last Modified: Thu, 25 Jan 2024 17:43:37 GMT  
		Size: 12.7 MB (12717874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4840ff34f40d95127def68b1bde55acd872332afaff0fceec2dab601faab0318`  
		Last Modified: Thu, 25 Jan 2024 17:45:55 GMT  
		Size: 43.8 MB (43761427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3e28fccbf21fb6c6637ad2e6c849019a58893aa47b68d08c45a650a744a924`  
		Last Modified: Thu, 25 Jan 2024 17:45:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074cd0647fad7b42b4bf1c1e9d6266aad904a0e8c7f6990384ab7dc9aca9d4fe`  
		Last Modified: Thu, 25 Jan 2024 17:45:49 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
