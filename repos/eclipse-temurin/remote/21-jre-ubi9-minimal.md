## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1aefc798c5931dcaf1094476bfbb06bdc8ce44904cd093ad8c3d44a3f1e2bad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f5d79a32d99f2f2c94f36be10f97316a54389dad3afee31779af15405af8df96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119515618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea4028907b9f43e709037730bede0ce3197cdd8ed461f154ee0a9ada0969b6c`
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:913f6ab9509f078a6abce4d967500f7268fc1ab95638524cda776355b7b7be58`  
		Last Modified: Thu, 02 May 2024 23:56:33 GMT  
		Size: 53.5 MB (53466188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133f3d7fd4bb17c6d7ff9044f12334090904bdf39b8b0a3c2e056b36a948c6dd`  
		Last Modified: Thu, 02 May 2024 23:56:26 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be7419c579c034476363389c061c9ae5dce8499f36e85417986ad137130313c`  
		Last Modified: Thu, 02 May 2024 23:56:26 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:37180c8f01c22809676206e890435e0dc35b0fef321d1994aab7b6a04e704e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117329158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cb55666e5a2288c0ed9d437afd3cb27a6f12ed0214cc6eec8f6bdf33220c29`
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:54ac88b6cf29af1bd8c592457d620610b6412433c291207776230967d5a6f229`  
		Last Modified: Fri, 03 May 2024 00:06:00 GMT  
		Size: 52.6 MB (52594983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07865560dca862affe22e6f22d6612f6e0a00ec03d312618ec63793dfbc34423`  
		Last Modified: Fri, 03 May 2024 00:05:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28baff090ead9307c523ede9a93a6ba6829a3b5e5c57923cbbd1185db588b7b3`  
		Last Modified: Fri, 03 May 2024 00:05:53 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9aaa0f49f444a38a7e6a0f3468792d79e664d491fc2b2a9537ddbade75e411b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126473435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173890f3906b932cdd41f9a5a33d7691e11d24803d60eb6105e1b42b09bf00d9`
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:204334df88c245c4e1d066917a97a17578edc8ffdf733569284cd240b662f6cf`  
		Last Modified: Fri, 03 May 2024 00:32:56 GMT  
		Size: 53.5 MB (53535799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0cfb76a63961a7918c471a01fff56e75fa4b262fd653041e991995bd46fd72`  
		Last Modified: Fri, 03 May 2024 00:32:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564948deb8b42f5fbed86b48da300d2c1464580d22cbdafd2742a9b4e0e0e0b`  
		Last Modified: Fri, 03 May 2024 00:32:47 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:9b75676e34ebe8cf2d7ce2dcfd37b1fb19217e2644da8a950c2bc9a3afcbba7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113968621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc23b01783949d56d5df1774ac8ae1c619ceffa0693904fb41ca5f063a94a46a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Apr 2024 18:01:40 GMT
ADD file:cb8d9fd5d29227fbcd15dc49f1730d3e9399b92d95fc5497f890f4efc962ff34 in / 
# Tue, 23 Apr 2024 18:01:41 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 23 Apr 2024 18:01:41 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 23 Apr 2024 18:01:42 GMT
ADD multi:1d3a84f6d9bb78a456d5b38854fbf0421ebc2fd9f63ad2a332e4ba315d308fef in /etc/yum.repos.d/ 
# Tue, 23 Apr 2024 18:01:42 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Apr 2024 18:01:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 23 Apr 2024 18:01:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Apr 2024 18:01:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Apr 2024 18:01:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Apr 2024 18:01:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Apr 2024 18:01:42 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Apr 2024 18:01:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Apr 2024 18:01:42 GMT
ENV container oci
# Tue, 23 Apr 2024 18:01:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 18:01:42 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 18:01:43 GMT
RUN rm -rf /var/log/*
# Tue, 23 Apr 2024 18:01:43 GMT
LABEL release=949
# Tue, 23 Apr 2024 18:01:43 GMT
ADD file:f29e34a839f2a70a433dd3e2ce30f4de55580d52e1b6d708541405a74156cfa3 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.json 
# Tue, 23 Apr 2024 18:01:44 GMT
ADD file:1b7963c92b0eafd2b95a572f11eca641db149fc7b6e8412c54de443a206192f6 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949 
# Tue, 23 Apr 2024 18:01:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-04-23T17:54:13" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949"
# Tue, 23 Apr 2024 18:01:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-813f3.repo' '/etc/yum.repos.d/repo-5c289.repo'
# Tue, 23 Apr 2024 18:01:46 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 23 Apr 2024 18:01:48 GMT
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e7fecff8180ea0c68896643598445fcb719f009b0f6161b0596bc28b3554a324`  
		Last Modified: Tue, 30 Apr 2024 18:09:41 GMT  
		Size: 37.1 MB (37142835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a3d9e9e6c9ba5b0a1648736d69fa017a9cfd3388225bb3669def9197add8f`  
		Last Modified: Fri, 03 May 2024 00:09:23 GMT  
		Size: 27.2 MB (27200525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e28eb6176185b49eb56eb322d9285914a0283947a4303784d1b93f5f5809ba8`  
		Last Modified: Fri, 03 May 2024 00:10:54 GMT  
		Size: 49.6 MB (49624389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb991da9e4898b8db96f684dd68c1daec4eeb6ba21d52710111359c050ee35`  
		Last Modified: Fri, 03 May 2024 00:10:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9c97162cf8c422a7b78e7ae7fe08bc12f555730507dcd10db19a30a5b1c4c9`  
		Last Modified: Fri, 03 May 2024 00:10:47 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
