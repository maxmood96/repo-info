## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:19c66566a0a802df5674301b223683ffbcf56cf18488a37a21d53e3d09df57d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:42cd0e031dd5061999705d6e178481691b9b0ea821c922d5ef48e68aaa23c338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211149487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38dc9398adcaa85da8f1e57d96eaa1179c52820b4fd6d4458b57a405820bbe04`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
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
	-	`sha256:6278ab099c9d4f72446b1b8a44b60bf0a1b056e7b8020c8f5b0b9fe9d5fb023e`  
		Last Modified: Thu, 02 May 2024 23:55:33 GMT  
		Size: 145.1 MB (145100043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076f939e32799b89cef4d7c1b44aa11acb6ad2ae787cf02c6274e7631fa01581`  
		Last Modified: Thu, 02 May 2024 23:55:22 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aace44b678aa836d656313c8c2dc0b716ee3d211ee1db2b5777427ae417f5e15`  
		Last Modified: Thu, 02 May 2024 23:55:22 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:cf011f15ed730192a6df8bb1e576125ddf986cb7f13e8837196296645b65db00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208630879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f53d91f8c8e5bbdd5060523c07ac59a03321361ac904d4e2e3fbcd8d4d733df`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
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
	-	`sha256:56859df285014e60fb6bcb4867fdae1182bbaaba686c8be9c3ed98a30174565b`  
		Last Modified: Fri, 03 May 2024 00:05:00 GMT  
		Size: 143.9 MB (143896688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5179249b4a100328bb49c6ea29ef1fab05cf3aae2bb7d34505a235db48feb5d7`  
		Last Modified: Fri, 03 May 2024 00:04:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4223920e73337ccd245b7242d2cdba284476b8aed4d485c091e75a7798e3c73`  
		Last Modified: Fri, 03 May 2024 00:04:50 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:6ece7416cbb1adaadb9676e9f387ac1e97bd9741d79e88ab59caf47d9ba22eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217745809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3e18713113e043f325ebf3f8b692b0f057256450b77f48ac352e386052f311`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
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
	-	`sha256:fe95232fb83b76e7d10129bf792c183a2b880313637644a9b2da31ec34106012`  
		Last Modified: Fri, 03 May 2024 00:31:50 GMT  
		Size: 144.8 MB (144808156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab942c9e2cda3b1517e259f7e116657529fec171b7e32c9c1c08d7b87b5594a3`  
		Last Modified: Fri, 03 May 2024 00:31:37 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851b055cb254a232e457e2c8ccfbd2ec57483dc62ada6fb28f3f7dfc742151f2`  
		Last Modified: Fri, 03 May 2024 00:31:37 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3b4f80ca2a0542e77e6c9ce494fc0053eb22e8ca785bd8eb12c159df3bb36a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198674634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33aefc0b78999c4a508ea2e51438f800e0ca84d99a1b982f91ac32d3a87e17a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='a900acf3ae56b000afc35468a083b6d6fd695abec87a8abdb02743d5c72f6d6d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='aa7fb6bb342319d227a838af5c363bfa1b4a670c209372f9e6585bd79da6220c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='44bdd662c3b832cfe0b808362866b8d7a700dd60e6e39716dee97211d35c230f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='af3f33c14ed3e2fcd85a390575029fbf92a491f60cfdc274544ac8ad6532de47';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
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
	-	`sha256:80dcc3019c681dc371d0c7e3b7a7d3755bee05917f042aa968575552b702d2c3`  
		Last Modified: Fri, 03 May 2024 00:10:05 GMT  
		Size: 134.3 MB (134330386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d88aba2572236c228f801567fc106259c813ecee90daf222409970974f2056`  
		Last Modified: Fri, 03 May 2024 00:09:54 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff52235d1f9007dce7005ec6aa369f9eb70a7d9b1a2363755fbd2fc870d39f34`  
		Last Modified: Fri, 03 May 2024 00:09:54 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
