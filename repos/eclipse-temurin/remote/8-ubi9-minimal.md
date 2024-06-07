## `eclipse-temurin:8-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:12a742949ced74d2fdc58946a69d8b8e2f0da7887bbe38baf2eaebaafa7fd500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:064394ce86a4c21345c3222d0266c939bd8a932e684880839320aebfc544c7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169625649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0030fb9f9ca99c5580c5112c5ee59e9f6844fc8831fa41bd0971a0d74135af11`
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:4c94e25d6c0a3166f141beb39e046daf6ae7717b89cdce9058b423e587088ae0`  
		Last Modified: Fri, 07 Jun 2024 04:53:13 GMT  
		Size: 103.6 MB (103600482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cc312a9d10cd023ecea3c7a639c61ab2d66b9cd629dd59efadfe362ee89216`  
		Last Modified: Fri, 07 Jun 2024 04:53:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaa419a4e4c0c78ac786efb485c826d588d1a601d45545b740790bb78a3a028`  
		Last Modified: Fri, 07 Jun 2024 04:53:04 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:790b7a14a77e378e155e4b23cf4a87e01d2489fa446756ea9321685d923786b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167373460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a296b7923c3f5357dce195a8e6df15cb4359bd67a5a68292cee523b229c78b`
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:e6a0b4171f2f46eef121b5727b253741048ee13d78947b3fd3e9572dc628265c`  
		Last Modified: Fri, 07 Jun 2024 04:19:04 GMT  
		Size: 102.7 MB (102700346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9691e572040ed8d995b9ac29834ed6cc11cb15481e76b23b1171afdbbb2778`  
		Last Modified: Fri, 07 Jun 2024 04:18:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b105f85d88028564d19faa561584134a5b52d00f8f896f303ff071475030694`  
		Last Modified: Fri, 07 Jun 2024 04:18:58 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e3cca21beec9cd0803c924bae3d6c2d7ddaa65f7dee3fb631b3f30f4c46c7bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.0 MB (174004311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcf8f8a6379165697e13d89a2295b780cc0d863e50d4a145d11d20929f3cf22`
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='3504d748a93f23cac8c060bd33231bd51e90dcb620f38dadc6239b6cd2a5011c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b9884a96f78543276a6399c3eb8c2fd8a80e6b432ea50e87d3d12d495d1d2808';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u412b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='6b7ed7996788075e182dd33349288346240fbce540e50fd77aecfc309a5ada19';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:f3007927b5ea09fa5171ab21f4c2b3e664d26e6642d5c86b97b239637d6f0bae`  
		Last Modified: Fri, 07 Jun 2024 03:06:03 GMT  
		Size: 101.1 MB (101068339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d2867fa835faa2823dc7568aec615696ed247cdf9c59c9ee99e41c43493b4`  
		Last Modified: Fri, 07 Jun 2024 03:05:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361ea7cf3b830d65377b123595cbed8275a4210b813a2e819605ff249f3cca05`  
		Last Modified: Fri, 07 Jun 2024 03:05:54 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
