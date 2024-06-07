## `eclipse-temurin:21-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:e16aa36e91cf474dfe7483c914ad7abff8754ec370cfd1d82660aa9a37a4f196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3cddb2324ad32964a0538581543a25701edade66943ea8f9d1b80ed32c6edc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224531551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279aa690282c43d0d708fc49b3b7899d8211b52378298c152dd580002a4f75c`
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:e17e7a657cb31fe76235a113caf97ada63daf2924210d77482dce63993d0559e`  
		Last Modified: Fri, 07 Jun 2024 04:55:11 GMT  
		Size: 158.5 MB (158506368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6abd2c7abc055082d9b0f9d3a39fab2edb53e8d195b790c3354ace078c87b39`  
		Last Modified: Fri, 07 Jun 2024 04:54:59 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efd40289fb9c87101f552391d87e3d6e01cd9be3e8a75ccb0ebaf92ff5a016d`  
		Last Modified: Fri, 07 Jun 2024 04:54:59 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5c2adc7feddb8b1240cdef65a141f4e0b61db042bbb9f3917e068a263f5f3034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221347141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a18a50a05b953773cebc2cce101c4788aaec00fbef7bae8c06f4502bebef3c`
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:5e7a4ed8a9a4cc28fae1f25343533e35b6e4950d45a9ec80ee3acab80746dc5b`  
		Last Modified: Fri, 07 Jun 2024 04:20:59 GMT  
		Size: 156.7 MB (156674010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94178f2132c763a0480926f87eb54ceb5aff076f12d01400e4a470ae6318d27d`  
		Last Modified: Fri, 07 Jun 2024 04:20:49 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949f9e5ee90e6e1f509d41f5424fd31532ab0fff1a0060a24a5145078586b9d3`  
		Last Modified: Fri, 07 Jun 2024 04:20:49 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0ee3bb4d1ef669543c0c00f8452de06f74f2866a1c05d8e8bcedd9640bc3d5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231681102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b4959a8f8e41c0832a8b9add5ee322fb4d8241b999984a4ffec46674c6be5a`
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:760a7a6741d29aea54443d0817110fa73a9e04c5381162bf3e0f2336144db4c0`  
		Last Modified: Fri, 07 Jun 2024 03:08:04 GMT  
		Size: 158.7 MB (158745111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aa0bae4ccc3741142261593a8a9bff37487485d9bf148ec8da424e6ababb55`  
		Last Modified: Fri, 07 Jun 2024 03:07:49 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c78dce5bd6ab5ddb2afab4d93d0be13dc3b2d37d7cd02c48d3f1512ff1c4c4`  
		Last Modified: Fri, 07 Jun 2024 03:07:49 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:952a34a35d49cad7cb0120ef64dd5821a508ca0085240ad19cb66401cfc6b49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211278991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f903eeab41b5ec24ee9abe664bc4f7a7592f84fa068f9e813c0122fde9119c`
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='7d3ab0e8eba95bd682cfda8041c6cb6fa21e09d0d9131316fd7c96c78969de31';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fffa52c22d797b715a962e6c8d11ec7d79b90dd819b5bc51d62137ea4b22a340';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9a1079d7f0fc72951fdc9a0029e49a15f6ba114683aee626f882ee2c761f1d57';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='f57a078d417614e5d78c07c77a6d8a04701058cf692c8e2868d593582be92768';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:4549d27ace92efd14c498ac960e78213c280ed893a648dad595232990b2d2491`  
		Last Modified: Fri, 07 Jun 2024 02:25:26 GMT  
		Size: 147.0 MB (146975119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f815bb383758d8dff7c10b63349a750b7172f573006bf9851854852aff1d5ba`  
		Last Modified: Fri, 07 Jun 2024 02:25:15 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0274d297226e6b080ec846d4196e14b6b4968b1fb965a9b2e50285a871059b65`  
		Last Modified: Fri, 07 Jun 2024 02:25:15 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
