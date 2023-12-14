## `eclipse-temurin:21-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:36eae1e63968fe741da3be15e70b214fe1ead9159c2c3dfc6397800e881a07b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:747d555bdc2100902627e7359bc10263cf7a25a2706e5f28596a0d6aa2aaab9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224239803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfd641c2925b76bbd3a8eb67e1fbb489bc985393fecf37435e7a45bd8911d8f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Dec 2023 04:19:06 GMT
ADD file:3b29fba5e73efe9ec5cf915f4a12bcfc1233baf57b701cd7f46462ebf85c5421 in / 
# Thu, 07 Dec 2023 04:19:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 07 Dec 2023 04:19:07 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 07 Dec 2023 04:19:08 GMT
ADD multi:8257bc82024891d335e91a6d5e44bb825bdb87abe8bc1d2ee3fcfb9e8cbecea1 in /etc/yum.repos.d/ 
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Dec 2023 04:19:08 GMT
ENV container oci
# Thu, 07 Dec 2023 04:19:08 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 04:19:08 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 04:19:08 GMT
RUN rm -rf /var/log/*
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL release=1475
# Thu, 07 Dec 2023 04:19:09 GMT
ADD file:2f91406cebe76f5a68d0aed7a9142410aa2ad41c096c1c117a8b580e3b56e55c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1475.json 
# Thu, 07 Dec 2023 04:19:09 GMT
ADD file:8af5a93a05a5b30bf94d83167bac0b48e41ee4f966d909ff7d9660196be34c4c in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1475 
# Thu, 07 Dec 2023 04:19:09 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-12-07T04:10:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1475"
# Thu, 07 Dec 2023 04:19:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-84783.repo' '/etc/yum.repos.d/repo-186d3.repo'
# Thu, 07 Dec 2023 04:19:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 07 Dec 2023 04:19:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 14 Dec 2023 01:49:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Dec 2023 01:49:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 01:49:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Dec 2023 01:49:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Thu, 14 Dec 2023 01:51:48 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 14 Dec 2023 01:51:56 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='e184dc29a6712c1f78754ab36fb48866583665fa345324f1a79e569c064f95e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1a6fa8abda4c5caed915cfbeeb176e7fbd12eb6b222f26e290ee45808b529aa1';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9574828ef3d735a25404ced82e09bf20e1614f7d6403956002de9cfbfcb8638f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 14 Dec 2023 01:51:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Thu, 14 Dec 2023 01:51:58 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 14 Dec 2023 01:51:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Dec 2023 01:51:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6e98c874e21bf68ae62db244603d751054b20b94888bfb1adb157827cd38c92`  
		Last Modified: Wed, 13 Dec 2023 17:00:23 GMT  
		Size: 37.7 MB (37721982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2ae6a725bd5e58600f85d2090852440f19f984fb02a57124291673e262a11b`  
		Last Modified: Thu, 14 Dec 2023 01:53:18 GMT  
		Size: 27.9 MB (27883877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4204b52ba1994da7f001c736616d473a67245055f1fdc708b8cd39366558a9`  
		Last Modified: Thu, 14 Dec 2023 01:55:25 GMT  
		Size: 158.6 MB (158633055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfff51b9e71250bf65eadce178f370eb85e5f73d78dc5aff143eb595fde30a7`  
		Last Modified: Thu, 14 Dec 2023 01:55:13 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e22250e941a89845185059e5f628277aaffc65ecdd8c70281ca31d0ce4cd8e4`  
		Last Modified: Thu, 14 Dec 2023 01:55:13 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:9cfeacd830b56e271151466f4b39e5d74a45f5bf0dfcc60155570a771bc6c04e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221204730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1728599d1212a8267480530fc0e43f77c7081ccb49ba37ebc05ca40d03cc34e0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Dec 2023 04:19:06 GMT
ADD file:7ba972e538cfd486a9ead8e6c555a813a0fdd8c971fece26107d633360ca400e in / 
# Thu, 07 Dec 2023 04:19:08 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 07 Dec 2023 04:19:08 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 07 Dec 2023 04:19:08 GMT
ADD multi:8257bc82024891d335e91a6d5e44bb825bdb87abe8bc1d2ee3fcfb9e8cbecea1 in /etc/yum.repos.d/ 
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Dec 2023 04:19:08 GMT
ENV container oci
# Thu, 07 Dec 2023 04:19:08 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 04:19:08 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 04:19:09 GMT
RUN rm -rf /var/log/*
# Thu, 07 Dec 2023 04:19:09 GMT
LABEL release=1475
# Thu, 07 Dec 2023 04:19:09 GMT
ADD file:81f4709f6c901cfae1353cf48b313f40bcb74c28a4a486b53e093a5b3d4a8b47 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1475.json 
# Thu, 07 Dec 2023 04:19:09 GMT
ADD file:1ff4ce5b17d000737bdcb251e3ecc8506100fc38c8fdd75265dcf2699f35103c in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1475 
# Thu, 07 Dec 2023 04:19:09 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-12-07T04:10:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1475"
# Thu, 07 Dec 2023 04:19:11 GMT
RUN rm -f '/etc/yum.repos.d/repo-84783.repo' '/etc/yum.repos.d/repo-186d3.repo'
# Thu, 07 Dec 2023 04:19:12 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 07 Dec 2023 04:19:13 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 14 Dec 2023 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Dec 2023 01:51:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 01:51:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Dec 2023 01:51:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Thu, 14 Dec 2023 01:52:54 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 14 Dec 2023 01:53:03 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='e184dc29a6712c1f78754ab36fb48866583665fa345324f1a79e569c064f95e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1a6fa8abda4c5caed915cfbeeb176e7fbd12eb6b222f26e290ee45808b529aa1';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9574828ef3d735a25404ced82e09bf20e1614f7d6403956002de9cfbfcb8638f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 14 Dec 2023 01:53:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Thu, 14 Dec 2023 01:53:07 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 14 Dec 2023 01:53:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Dec 2023 01:53:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4849aa241c326e575522a63046cad5e53ec51b8e918d232021fc78d31e146fa`  
		Last Modified: Wed, 13 Dec 2023 17:00:20 GMT  
		Size: 36.0 MB (36010908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07d5d8f482e628787b0283e4b5bf1bb77ed91bf99882fd31d18c4a369503b37`  
		Last Modified: Thu, 14 Dec 2023 01:54:13 GMT  
		Size: 28.3 MB (28317176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ccbedd20c8d40d00e881a6c365e2ea1aa9049e3119666f6a743d728a00b320`  
		Last Modified: Thu, 14 Dec 2023 01:56:09 GMT  
		Size: 156.9 MB (156875760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb490b5221cb4b12a23056538465ea8fb3b663d1aabb46d988bd47798c7176`  
		Last Modified: Thu, 14 Dec 2023 01:55:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54207c8dea6d681b73691ccd19fb3cf657bca64c90c14f48ba722f7f5aff09e`  
		Last Modified: Thu, 14 Dec 2023 01:55:59 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:599ee584d3050feda17aa408f781a07eaa0dc2940e132cb74c1a12fbb7fa0e0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230819520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8384ea02e98fd2ed7994f0969a0748ea629b0576a3aa6fe77fd8c2b9491352cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Dec 2023 04:19:10 GMT
ADD file:82b0903051ac27f66d120ca59a87f8b5bfc31c8e4f19f88d41b7e189dd5f9848 in / 
# Thu, 07 Dec 2023 04:19:11 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 07 Dec 2023 04:19:11 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 07 Dec 2023 04:19:11 GMT
ADD multi:8257bc82024891d335e91a6d5e44bb825bdb87abe8bc1d2ee3fcfb9e8cbecea1 in /etc/yum.repos.d/ 
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Dec 2023 04:19:11 GMT
ENV container oci
# Thu, 07 Dec 2023 04:19:11 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 04:19:11 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 04:19:13 GMT
RUN rm -rf /var/log/*
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL release=1475
# Thu, 07 Dec 2023 04:19:13 GMT
ADD file:d551330fb95bb45b70652e0761f50eba42eb6aa5681123b038c37fdca6bad444 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1475.json 
# Thu, 07 Dec 2023 04:19:13 GMT
ADD file:a493a33c479aa9eca7d6a43f9973055b7d838c41bd3ed43d03df6d30f8078ba0 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1475 
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-12-07T04:10:36" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1475"
# Thu, 07 Dec 2023 04:19:14 GMT
RUN rm -f '/etc/yum.repos.d/repo-84783.repo' '/etc/yum.repos.d/repo-186d3.repo'
# Thu, 07 Dec 2023 04:19:16 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 07 Dec 2023 04:19:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 14 Dec 2023 02:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Dec 2023 02:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 02:22:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Dec 2023 02:23:36 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Thu, 14 Dec 2023 02:26:22 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 14 Dec 2023 02:26:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='e184dc29a6712c1f78754ab36fb48866583665fa345324f1a79e569c064f95e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1a6fa8abda4c5caed915cfbeeb176e7fbd12eb6b222f26e290ee45808b529aa1';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9574828ef3d735a25404ced82e09bf20e1614f7d6403956002de9cfbfcb8638f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 14 Dec 2023 02:26:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Thu, 14 Dec 2023 02:26:47 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 14 Dec 2023 02:26:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 14 Dec 2023 02:26:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c721e8705d331953b5dcba6f470f14a60df884f6177622562d6d4fed0fe02d41`  
		Last Modified: Wed, 13 Dec 2023 18:09:18 GMT  
		Size: 42.1 MB (42148257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cd525af4bd813e8ef5d4e2fa0475beee9b649b527b923a3a810516e15fc635`  
		Last Modified: Thu, 14 Dec 2023 02:28:15 GMT  
		Size: 30.4 MB (30432228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e7eda70d0ddff2e6adbc93bb3a006be3297f55c252e0cd0ebc74472c8e233`  
		Last Modified: Thu, 14 Dec 2023 02:30:33 GMT  
		Size: 158.2 MB (158238144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbf53f50b62de677347d7f65b69c03d665815c050056e9309f45d6e239b6e0a`  
		Last Modified: Thu, 14 Dec 2023 02:30:18 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e981d675da6df2766a6477d88951eaeaa15fa623c85c400fed91ec75c8c73a`  
		Last Modified: Thu, 14 Dec 2023 02:30:18 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
