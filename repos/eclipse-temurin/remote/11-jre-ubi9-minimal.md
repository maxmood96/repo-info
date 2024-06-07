## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:f8c76d015743ab9c98e1881f039279c4edc79bc7acfb69c2399a56ee0d4b5e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9e0f0428f406c2705750349adfb39afb14b82275b618686424fa46be034d61a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110217910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b3be7f782b70c2ebb03363e8d6179c05c6f770f8018c0bc8b5b62bedc59443`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 May 2024 13:35:45 GMT
ADD file:6b3c51c101388be0fae89df70c275c457df3109dd754e67aaa695ab57931a55a in / 
# Thu, 30 May 2024 13:35:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 30 May 2024 13:35:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 30 May 2024 13:35:46 GMT
ADD multi:10a5b9e3ab6a191968d4e9508eca8f1cb30ca8c8ff6681dd9ecbea964c42b6de in /etc/yum.repos.d/ 
# Thu, 30 May 2024 13:35:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 May 2024 13:35:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 30 May 2024 13:35:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 May 2024 13:35:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 May 2024 13:35:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 May 2024 13:35:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 May 2024 13:35:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 May 2024 13:35:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 May 2024 13:35:46 GMT
ENV container oci
# Thu, 30 May 2024 13:35:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 13:35:46 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 13:35:47 GMT
RUN rm -rf /var/log/*
# Thu, 30 May 2024 13:35:47 GMT
ADD file:2867968da940ee5c316f478f01298796b71b04357b6efbbbc1d7219d486e29b7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1717074713.json 
# Thu, 30 May 2024 13:35:47 GMT
ADD file:be47ef503ada1def84422c0f3cdaa00761a8066b1c6ebe894382ae45cbfaec35 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1717074713 
# Thu, 30 May 2024 13:35:47 GMT
LABEL "release"="949.1717074713" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-30T13:14:08" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1717074713"
# Thu, 30 May 2024 13:35:48 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3133872-373bc.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 30 May 2024 13:35:49 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 30 May 2024 13:35:50 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:428c4e67728c0398b6263211d375a9bebe8b3c56a76af661e5b3efe156886361`  
		Last Modified: Thu, 06 Jun 2024 08:39:56 GMT  
		Size: 38.9 MB (38880168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a267a3718add0549f6c943408831bee4dd962ad4ca6ad4f6da1c97c0344fbb6`  
		Last Modified: Fri, 07 Jun 2024 04:53:08 GMT  
		Size: 27.1 MB (27144160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e20119e2e95941998cc4f2a6d96064970039af5cb57cec55416b33450030cb0`  
		Last Modified: Fri, 07 Jun 2024 04:54:07 GMT  
		Size: 44.2 MB (44192743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f362b8b2f027c82ad3a205543714794ebdb259727bfc7332b57342aa3a9264`  
		Last Modified: Fri, 07 Jun 2024 04:54:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf886d4d6762cac289c81a9b14008d20d5dca3b3966222547bf62d4ed914814`  
		Last Modified: Fri, 07 Jun 2024 04:54:02 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9a6f70c247fc1ae19b3a0ed17bda0e952226476a4e94b6e57fdec7ee65259fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107234792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d0bb44e9099383c9a48e70d69b4069cb54b7d73aa747acc7e594fdb317260`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 May 2024 13:35:31 GMT
ADD file:3b70ca75f887cc972d131fb5caf99fff1fcf1808900d6017705a3b6b5815c57f in / 
# Thu, 30 May 2024 13:35:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 30 May 2024 13:35:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 30 May 2024 13:35:32 GMT
ADD multi:10a5b9e3ab6a191968d4e9508eca8f1cb30ca8c8ff6681dd9ecbea964c42b6de in /etc/yum.repos.d/ 
# Thu, 30 May 2024 13:35:32 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 May 2024 13:35:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 30 May 2024 13:35:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 May 2024 13:35:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 May 2024 13:35:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 May 2024 13:35:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 May 2024 13:35:32 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 May 2024 13:35:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 May 2024 13:35:32 GMT
ENV container oci
# Thu, 30 May 2024 13:35:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 13:35:32 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 13:35:33 GMT
RUN rm -rf /var/log/*
# Thu, 30 May 2024 13:35:33 GMT
ADD file:0c56a50d30c503011b2cd2ad620c8b42e23f9a7b3209387c1ac85014ea8e51e8 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1717074713.json 
# Thu, 30 May 2024 13:35:33 GMT
ADD file:3a9c01c5d61ee0a5b80c728e4e882d1de507083d557a30843ff3cd99eda21cfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1717074713 
# Thu, 30 May 2024 13:35:33 GMT
LABEL "release"="949.1717074713" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-30T13:14:08" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1717074713"
# Thu, 30 May 2024 13:35:34 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3133872-373bc.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 30 May 2024 13:35:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 30 May 2024 13:35:37 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2eb4a094086c55c8718178f8c03ee6268f662e2fe3ac281acbd7e5b4abd42768`  
		Last Modified: Thu, 06 Jun 2024 08:39:55 GMT  
		Size: 37.1 MB (37080678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd2f49759892a5d3183436d1c697f04322fe8391c3f4641c40c158a8b81333b`  
		Last Modified: Fri, 07 Jun 2024 04:19:01 GMT  
		Size: 27.6 MB (27591598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd94f58f12893e6f7720d99e18c9cfa9d03cc394c7ca3ee39f1f7c5188a112c`  
		Last Modified: Fri, 07 Jun 2024 04:19:59 GMT  
		Size: 42.6 MB (42561676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8926552a33eac26473b43da5d66105a2330795e0ff7cb35b3820c97c87469b4e`  
		Last Modified: Fri, 07 Jun 2024 04:19:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b1a23b4aeb233d8a3622b92962f8cdeefa1389af2ce8c602aa1b3185df8013`  
		Last Modified: Fri, 07 Jun 2024 04:19:54 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b9278be88b89bd2e5ba386045ccfc9803c0c9927fabf669c4ea19ac031072030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112634849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4d73229a7f0a3386693b56d06bde309a02f5d72b9ef5d161d1210d4a91dbc4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 May 2024 13:35:34 GMT
ADD file:8a11e8afe4fad68b45b505db6ac31e944034f6abdc60d8fcf7f1cdf0da538039 in / 
# Thu, 30 May 2024 13:35:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 30 May 2024 13:35:36 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 30 May 2024 13:35:36 GMT
ADD multi:10a5b9e3ab6a191968d4e9508eca8f1cb30ca8c8ff6681dd9ecbea964c42b6de in /etc/yum.repos.d/ 
# Thu, 30 May 2024 13:35:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 May 2024 13:35:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 30 May 2024 13:35:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 May 2024 13:35:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 May 2024 13:35:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 May 2024 13:35:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 May 2024 13:35:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 May 2024 13:35:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 May 2024 13:35:36 GMT
ENV container oci
# Thu, 30 May 2024 13:35:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 13:35:36 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 13:35:37 GMT
RUN rm -rf /var/log/*
# Thu, 30 May 2024 13:35:37 GMT
ADD file:ed5945e6ebaf6348f1150110cab2c41219c5e559c36670f43bdb732b8876972d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1717074713.json 
# Thu, 30 May 2024 13:35:38 GMT
ADD file:40f6a258d8800b05b75117f66c0badee4ba1b750d7c01f88a1d2eb56a09c0bfc in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1717074713 
# Thu, 30 May 2024 13:35:38 GMT
LABEL "release"="949.1717074713" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-30T13:14:08" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1717074713"
# Thu, 30 May 2024 13:35:39 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3133872-373bc.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 30 May 2024 13:35:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 30 May 2024 13:35:42 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e3f06c9962057a5cc6e14b55583c5cc376f23326466b1686e09163bcfed6781b`  
		Last Modified: Thu, 06 Jun 2024 18:11:46 GMT  
		Size: 43.4 MB (43361533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e301f455ae57f1531fab42be921a41103b0edae1296f0004d784b5f202e3125`  
		Last Modified: Fri, 07 Jun 2024 03:05:59 GMT  
		Size: 29.6 MB (29573602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f39f47589a941a0aaf88794a4dd07dca2040ef6bac02fb8837d6434ee6e8a69`  
		Last Modified: Fri, 07 Jun 2024 03:06:58 GMT  
		Size: 39.7 MB (39698876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40af08754c970b8f153bfdf2fe3a22ffa35b2679b0640fe1d72f9376f216923`  
		Last Modified: Fri, 07 Jun 2024 03:06:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68a59f6f7c448a1e21fc512d3aced02983402949bd25754c7f20b89df25bca5`  
		Last Modified: Fri, 07 Jun 2024 03:06:52 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:67a1caede54403a7b92682411777b3fe3068b0a1a69ad219fc3baea4d4a9c3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102073955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f16bb2a7a2d9c9494e1fe96ebbfa6a41b127c62a01dbbed5f4f02d58e09ad9d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 May 2024 13:35:33 GMT
ADD file:8b016c2ebd388f0eef3c74518d8a51d2d0f91f909a2c8dc0cf8e895d6a603e0d in / 
# Thu, 30 May 2024 13:35:34 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 30 May 2024 13:35:34 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 30 May 2024 13:35:34 GMT
ADD multi:10a5b9e3ab6a191968d4e9508eca8f1cb30ca8c8ff6681dd9ecbea964c42b6de in /etc/yum.repos.d/ 
# Thu, 30 May 2024 13:35:34 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 May 2024 13:35:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 30 May 2024 13:35:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 May 2024 13:35:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 May 2024 13:35:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 May 2024 13:35:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 May 2024 13:35:34 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 May 2024 13:35:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 May 2024 13:35:34 GMT
ENV container oci
# Thu, 30 May 2024 13:35:34 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 13:35:34 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 13:35:36 GMT
RUN rm -rf /var/log/*
# Thu, 30 May 2024 13:35:36 GMT
ADD file:7a4eab654b9ca109b4f2363c082defccf7202d379a2669fd35283e0b49c8f37d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1717074713.json 
# Thu, 30 May 2024 13:35:36 GMT
ADD file:71d4936b52982664ba7256d377f39f0b718aa884683e99d20ecab908615c7df4 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1717074713 
# Thu, 30 May 2024 13:35:36 GMT
LABEL "release"="949.1717074713" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-30T13:14:08" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1717074713"
# Thu, 30 May 2024 13:35:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3133872-373bc.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 30 May 2024 13:35:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 30 May 2024 13:35:40 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1380853393b36312aac70ccb4466a637b994f6a098d82d62044bfaf89ed2364e`  
		Last Modified: Thu, 06 Jun 2024 18:11:53 GMT  
		Size: 37.1 MB (37121384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a58bcf7f8ace53176f5346b83319201ec3703c0ad9dec581eb0b7c039c8af50`  
		Last Modified: Fri, 07 Jun 2024 02:24:15 GMT  
		Size: 27.2 MB (27181632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60090e33576659cb73d56ecdd6db6836ae3602679028d8decd76eb9400119d5d`  
		Last Modified: Fri, 07 Jun 2024 02:24:35 GMT  
		Size: 37.8 MB (37770100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad209a60837de9052c49f4e729cd422976efd5c69cd75f15e7d38ff8b939ed`  
		Last Modified: Fri, 07 Jun 2024 02:24:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb3f82efd7cb3dacddb271e02fdf2021ef2abcea4402a04124975aecc5036fc`  
		Last Modified: Fri, 07 Jun 2024 02:24:30 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
