## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:c2784999ab841756896aa120345d29c5b710a7b8b6d032307d7b77cf24a8998f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:61e9ccc0b9f60dbe0a471d24d46bd08ca4c05348a8bb63c5f17cde2526af6266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211125387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16c6e1d644b3c7fc88d72c43f16c38a3d311a6e5f193a194e13332b0684eed6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
	-	`sha256:428c4e67728c0398b6263211d375a9bebe8b3c56a76af661e5b3efe156886361`  
		Last Modified: Thu, 06 Jun 2024 08:39:56 GMT  
		Size: 38.9 MB (38880168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a267a3718add0549f6c943408831bee4dd962ad4ca6ad4f6da1c97c0344fbb6`  
		Last Modified: Fri, 07 Jun 2024 04:53:08 GMT  
		Size: 27.1 MB (27144160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0613a30d711955a029dadd6dc363097e32e1f68411d627fa77777c521838ed61`  
		Last Modified: Fri, 07 Jun 2024 04:54:29 GMT  
		Size: 145.1 MB (145100203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08148dbc3ced659762bad4777d4e09f8119933c755dd5a0d617b274c9669d8fd`  
		Last Modified: Fri, 07 Jun 2024 04:54:18 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41072e39014c5a451a988b8b4aedd877613e4f5f52c6e696fbd79aa4a21bd426`  
		Last Modified: Fri, 07 Jun 2024 04:54:18 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:930428e34aad8cebe5b960f34dfb29206ee9a8b2626c27696f34a15a14990576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208569767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d964a097748b6e13bf732bed62b2e9bd4078d2c9889dd9e423c078b1c22955f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
	-	`sha256:2eb4a094086c55c8718178f8c03ee6268f662e2fe3ac281acbd7e5b4abd42768`  
		Last Modified: Thu, 06 Jun 2024 08:39:55 GMT  
		Size: 37.1 MB (37080678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd2f49759892a5d3183436d1c697f04322fe8391c3f4641c40c158a8b81333b`  
		Last Modified: Fri, 07 Jun 2024 04:19:01 GMT  
		Size: 27.6 MB (27591598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9e4ea0cdcd3d9c0928fc9d90895052b94457f6982e44f2e317c961339338b3`  
		Last Modified: Fri, 07 Jun 2024 04:20:21 GMT  
		Size: 143.9 MB (143896636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afac66215c73e458c88d68554b445cc696432c3dd5eeba7b1f13db0e6da9bfdb`  
		Last Modified: Fri, 07 Jun 2024 04:20:11 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750dc3673cb0c806480ea1a9f0743f2bcf7c1b30dc755aa7f016a68862bac92b`  
		Last Modified: Fri, 07 Jun 2024 04:20:11 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4b85df0f1c5cf41e555915246018c0a16b76c70dad429f99533a590f41aae66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217744083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734245ae1ac81bc78fe45cad29f1121dde76f860006a732f635470c5b171a4e2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
	-	`sha256:e3f06c9962057a5cc6e14b55583c5cc376f23326466b1686e09163bcfed6781b`  
		Last Modified: Thu, 06 Jun 2024 18:11:46 GMT  
		Size: 43.4 MB (43361533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e301f455ae57f1531fab42be921a41103b0edae1296f0004d784b5f202e3125`  
		Last Modified: Fri, 07 Jun 2024 03:05:59 GMT  
		Size: 29.6 MB (29573602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8580320932476a7accc7548ed28e70f2f958fbfd4d67d39ff17eea33b232c8`  
		Last Modified: Fri, 07 Jun 2024 03:07:22 GMT  
		Size: 144.8 MB (144808092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69cf5c4777f37008052085f5982473862a5bdc0e98be8c4e5a9ed3c8aebdfec`  
		Last Modified: Fri, 07 Jun 2024 03:07:08 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3079ed80b55d3f7c8386ba0fe97e1c031407721e562496b147b4ec86ad1d7a`  
		Last Modified: Fri, 07 Jun 2024 03:07:08 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:231ade0d719e8ac324372e13693bc596931ea703f512117c935aa2fa57f1ccb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198634306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92152065f4c6aacbccb32ebbc9234d552391feda9969a09b8cadc87c19930ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
	-	`sha256:1380853393b36312aac70ccb4466a637b994f6a098d82d62044bfaf89ed2364e`  
		Last Modified: Thu, 06 Jun 2024 18:11:53 GMT  
		Size: 37.1 MB (37121384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a58bcf7f8ace53176f5346b83319201ec3703c0ad9dec581eb0b7c039c8af50`  
		Last Modified: Fri, 07 Jun 2024 02:24:15 GMT  
		Size: 27.2 MB (27181632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0ae1c979cb60867763958ba4d8053ee41de92764747a2d5d378d518f99fb0`  
		Last Modified: Fri, 07 Jun 2024 02:24:53 GMT  
		Size: 134.3 MB (134330434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50016ca3fd9ef7bbeeafe8f9d2d9e1c96ce0d16ba023875c4ec5dda91bd89c5f`  
		Last Modified: Fri, 07 Jun 2024 02:24:43 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c348364d3472ab7b82c69e8427c4ffcfef2abf2f32f7d64f52bdf625b9b9128`  
		Last Modified: Fri, 07 Jun 2024 02:24:43 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
