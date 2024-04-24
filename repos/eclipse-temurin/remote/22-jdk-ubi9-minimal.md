## `eclipse-temurin:22-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:b5544cfa1ec3a8ca385d0a1ae6cccc3a1dae72788c674e3b1ee3d9f1470b489b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:22-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bd585fb257863ebeaa65f34e4b40f24c15845fbb65129e441123538d45b38025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223028130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2963ec8d00b7cdb3f43d892b26ef1cc1ee70d2af07013609c0dc0392f3fe8f48`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
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
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440448b8b996ac596b9214d68c607662000c8e74ad26b922b0283d11eb829154`  
		Last Modified: Mon, 15 Apr 2024 18:58:06 GMT  
		Size: 28.6 MB (28612828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c392693b42e331884d8c6534424b9b79d8e9a60c8224c3945e534a4a06289b7`  
		Last Modified: Wed, 24 Apr 2024 19:19:00 GMT  
		Size: 156.7 MB (156719225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032b7e25fb03ae2562104616c5a860339b9377865f4c278f8c6e731af2dbae89`  
		Last Modified: Wed, 24 Apr 2024 19:18:48 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832565889b9e64ae706875a2174f3391f2b4bcb47081b952861a8799f0d13db7`  
		Last Modified: Wed, 24 Apr 2024 19:18:47 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:971923554f5016c4a8d1492e011baaf6a04d75c07ab3695eef8d3e94a37c7da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219780169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1668a0d2a3c432b6754b6dfa86f9536fc53c7669b68021989d273b426680b61`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
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
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1833003c62adc51f6cc3c367fb7787c6e8b6bdc508130c0ef4323e9e4806e3f`  
		Last Modified: Mon, 15 Apr 2024 18:50:59 GMT  
		Size: 29.0 MB (29049830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e128c9c85f0ce47b81f5e310b09f3da569f9714f79f546574cda68228addaba1`  
		Last Modified: Wed, 24 Apr 2024 18:03:03 GMT  
		Size: 154.7 MB (154745661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6b90c3c17ddc5d75d9703cad6c246fa143caf7b265cfc7e8521b3c1810a9d1`  
		Last Modified: Wed, 24 Apr 2024 18:02:52 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59ae9b297c5325ec72a4626c98fe08c9afafdb6bf72a5e8223dc227ab92f16`  
		Last Modified: Wed, 24 Apr 2024 18:02:53 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e3d2f5c64d8b007347d53dba760711c63401ce3e771c7f8e7091731d0fd69c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (229954808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e563aed909442ec077782b69ef7d9f91c4998d4751b540c220378612f4535b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:e100ce295764ee5bd8795041bb4862d3fb9f62818b8b8e7b65a32cee1fce1afa in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:47 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:48 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:48 GMT
ADD file:b6e7a73897a55184357ba915feb05b8bf7c348344fa75e8c843db12ccaec3e21 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:48 GMT
ADD file:3c70a25705cace759733fff14c8b2d0e1dc0f21628fff6d121c38656560f65c4 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:50 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:51 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:53 GMT
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
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:c77c514a1cb5c6b968ce2a99c2b9cdd751b585456e06761249027a93afab424f`  
		Last Modified: Fri, 15 Mar 2024 10:54:10 GMT  
		Size: 42.1 MB (42080689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba206225c418784da485680a1a4d57d824add72e88c85419005f79fb4f7b5e`  
		Last Modified: Mon, 15 Apr 2024 19:31:58 GMT  
		Size: 31.2 MB (31174818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420425ee46dfb624ecde4ec11100c86b2e39b33143fa8357ea2438d9ff94da7c`  
		Last Modified: Wed, 24 Apr 2024 17:52:02 GMT  
		Size: 156.7 MB (156698414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf575e4893c4594232eee00087006278ede5c3fb949e6babb8c62e5969c53024`  
		Last Modified: Wed, 24 Apr 2024 17:51:46 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7543b54077e5c31c35c4599c92db5b1a1724a755e70afbf5ca57b6109e347f63`  
		Last Modified: Wed, 24 Apr 2024 17:51:47 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
