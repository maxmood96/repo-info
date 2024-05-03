## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:8c987789ffe88dd31f5028a235bd5640b40358edd3fa8223eb678f2a9a8a32d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f8734a783e7d09b12b1e2a5b7c0fb19ddad43aff33d8d57439f0d0b3af5b92a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107923469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdb951aa2d712ce2528603fd2b57bacb923313f2fcd1abe3ec01054d2b46fdb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Apr 2024 18:01:38 GMT
ADD file:272a54c4ff2458766f95510a6275659ae29451ca133d92e47fcaa3a4a18775ae in / 
# Tue, 23 Apr 2024 18:01:39 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 23 Apr 2024 18:01:39 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 23 Apr 2024 18:01:39 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Apr 2024 18:01:39 GMT
ENV container oci
# Tue, 23 Apr 2024 18:01:39 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 18:01:39 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 18:01:40 GMT
RUN rm -rf /var/log/*
# Tue, 23 Apr 2024 18:01:40 GMT
LABEL release=949
# Tue, 23 Apr 2024 18:01:40 GMT
ADD file:514a0e96fc8d9f5ebda74914cf507d7ef22d83d438d1bcd476ab173ce0924966 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Tue, 23 Apr 2024 18:01:40 GMT
ADD file:a20b9d381f9f0687b9334e8127977b5011dc44aba28ab1989ce5117dfc501e24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Tue, 23 Apr 2024 18:01:40 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Tue, 23 Apr 2024 18:01:41 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Tue, 23 Apr 2024 18:01:41 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 23 Apr 2024 18:01:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c74421934803b3366e2cc6538ee64f78f065ffab29c0b8cbe898ce0785a30ab5`  
		Last Modified: Tue, 30 Apr 2024 15:07:32 GMT  
		Size: 38.9 MB (38885484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933d79ac4ff99dfe879bb01a2a29cb330d94f6be8715f660faa18a8834d3a664`  
		Last Modified: Thu, 02 May 2024 23:54:06 GMT  
		Size: 27.2 MB (27163072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3297cc2be80ded30361fafaeb54c3846b527d082a0b5425210bf6741f9a373ae`  
		Last Modified: Thu, 02 May 2024 23:54:29 GMT  
		Size: 41.9 MB (41874041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e069ec5c2ea932ae88f6fb87103ee1490dc8939ca0f332c4d814c5205e6fa1`  
		Last Modified: Thu, 02 May 2024 23:54:24 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3be4b5bb21d16d74423f0d4956101668a57c11705787012db749472517ed64`  
		Last Modified: Thu, 02 May 2024 23:54:24 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:77a0e4e881eb990985eb80a446c55cad91e33f427042f4db4102f1a573337dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105583071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3685737d8d62e0bcb87a807cdf79ce63eb2c3d2cc4b2f6724f3623d6b043337`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Apr 2024 18:01:37 GMT
ADD file:e1b0b107488b07d74943f44442065a4e4ae7797d17ded1cd89b5b5ee28e49026 in / 
# Tue, 23 Apr 2024 18:01:38 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 23 Apr 2024 18:01:38 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 23 Apr 2024 18:01:39 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Apr 2024 18:01:39 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Apr 2024 18:01:39 GMT
ENV container oci
# Tue, 23 Apr 2024 18:01:39 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 18:01:39 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 18:01:40 GMT
RUN rm -rf /var/log/*
# Tue, 23 Apr 2024 18:01:40 GMT
LABEL release=949
# Tue, 23 Apr 2024 18:01:40 GMT
ADD file:82f223ec5eb8d3cbb061ccbc7b61239980c69fa8c13fd4cc5af690a8271af210 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Tue, 23 Apr 2024 18:01:40 GMT
ADD file:1e4512520b98a9369be1a1031d807df5dae244da98a1dc941241697db22f5fe9 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Tue, 23 Apr 2024 18:01:40 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Tue, 23 Apr 2024 18:01:41 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Tue, 23 Apr 2024 18:01:43 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 23 Apr 2024 18:01:44 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e8c814ef5b6acaf7bfd8f6e716458093dba2f51c1314fa33595896a381eaa4b`  
		Last Modified: Tue, 30 Apr 2024 15:27:44 GMT  
		Size: 37.1 MB (37131582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50d79e983b7c5a509dcfd45139a5fd195b6c7a0552fefb2a123c979e17227fe`  
		Last Modified: Fri, 03 May 2024 00:03:38 GMT  
		Size: 27.6 MB (27601722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47320f386adc7703e54244db266f51e5863fb3caa990566b54011639a0fdb718`  
		Last Modified: Fri, 03 May 2024 00:04:00 GMT  
		Size: 40.8 MB (40848896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e8569fe2994f699ddef0932de8daacb152c6cb76b8de14b8ec5bc1de4d5d56`  
		Last Modified: Fri, 03 May 2024 00:03:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4e0c0c6727aa721f0e887e9fa87e3cb9e829294228962d4ac47798c7e51c7e`  
		Last Modified: Fri, 03 May 2024 00:03:56 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:56af5457d0d513ae0d39fd37eccf227b75e471fa8d1bb61aaf7d69658c037eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114171487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3836789b713e0ebfef2f6ef5c53418a2c739b0dc63e0ea72b99011c390fedf04`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Apr 2024 18:01:41 GMT
ADD file:ef1b6c4fb319052ccf9a6af0cbdd4542b604923875397207a2ae5fc8b7597d67 in / 
# Tue, 23 Apr 2024 18:01:42 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 23 Apr 2024 18:01:42 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 23 Apr 2024 18:01:43 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Apr 2024 18:01:43 GMT
ENV container oci
# Tue, 23 Apr 2024 18:01:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 18:01:43 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 18:01:44 GMT
RUN rm -rf /var/log/*
# Tue, 23 Apr 2024 18:01:44 GMT
LABEL release=949
# Tue, 23 Apr 2024 18:01:44 GMT
ADD file:a70c907dbd57c95c46099f0c1f094e654c82044bcf37976dfc60f355a4c9a927 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Tue, 23 Apr 2024 18:01:45 GMT
ADD file:e23471b4e177d691d3a63444ffa51995d47b2fe910bc4f870715bf4c63415036 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Tue, 23 Apr 2024 18:01:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Tue, 23 Apr 2024 18:01:46 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Tue, 23 Apr 2024 18:01:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 23 Apr 2024 18:01:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f1f41ebd152776a91a1b2f3927cda0e63f2b56ce502c07af9492b43acfb6eb0c`  
		Last Modified: Tue, 30 Apr 2024 18:09:28 GMT  
		Size: 43.3 MB (43345637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47eb6ed7aaab1fecfac6461d67f8ff241e3c27df45b56b1f5a24245d067d008`  
		Last Modified: Fri, 03 May 2024 00:30:20 GMT  
		Size: 29.6 MB (29591128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421ad141ad5db9b41d929a270cabc6cb9ce4ce77f6dfb049fa03b105ddf47984`  
		Last Modified: Fri, 03 May 2024 00:30:44 GMT  
		Size: 41.2 MB (41233851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2951e6f0d9b2598c823e7963c0ec41496b85db1ee15dabcd1d9133bd0f052b`  
		Last Modified: Fri, 03 May 2024 00:30:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308dc900f76c73111c9418d005003aca8e6e9bea65289e8d49976eb11ba01d0c`  
		Last Modified: Fri, 03 May 2024 00:30:39 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
