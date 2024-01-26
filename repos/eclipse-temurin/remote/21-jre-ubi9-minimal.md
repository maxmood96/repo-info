## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:25e86776a12a74dca5de01cec69c5f3b770438c35db455493875c592af9ffa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:35eb0814160848e2ed20ecd39abc200a0d86f74c21cb29e2b2e196f2391f2141
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103305192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6118941e39436d3138afd922808dc4368c9a32f89ed33e849e1c66fca346700d`
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
# Fri, 26 Jan 2024 02:00:25 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Fri, 26 Jan 2024 02:00:49 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 26 Jan 2024 02:00:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 26 Jan 2024 02:00:50 GMT
COPY file:80168d55afbbfdfea820e78ae2e1141fd21095cf26d68a4715fadfae5beb9e0b in /__cacert_entrypoint.sh 
# Fri, 26 Jan 2024 02:00:50 GMT
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
	-	`sha256:d035e3aace383ce5f642e748ece64b81262ed0cae6642ca310b2e9843b353caa`  
		Last Modified: Fri, 26 Jan 2024 02:04:40 GMT  
		Size: 54.0 MB (53984972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7d1051b29a385382e0d904cf239ba7340df5a9329ed918c9e9d1df0bf7080a`  
		Last Modified: Fri, 26 Jan 2024 02:04:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbc405fffec61846a8b005629a5bbc96cef1eff6c1345920cd520bf4864c008`  
		Last Modified: Fri, 26 Jan 2024 02:04:32 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d262133f049b3771d62146a31f0104510cb212724d2590f9f3f7cb61c1f7512e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102061638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c3fe589642e081449f01288dd771448e4ee3779e1984a64619eeaa1a1d44d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Wed, 24 Jan 2024 20:40:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Wed, 24 Jan 2024 20:44:38 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 20:45:10 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 24 Jan 2024 20:45:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:45:12 GMT
COPY file:80168d55afbbfdfea820e78ae2e1141fd21095cf26d68a4715fadfae5beb9e0b in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:45:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f4849aa241c326e575522a63046cad5e53ec51b8e918d232021fc78d31e146fa`  
		Last Modified: Wed, 13 Dec 2023 17:00:20 GMT  
		Size: 36.0 MB (36010908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6626cc88fdf97382d2d21503deed9146ccdce0dd6bdafd076d981d7e29b4179`  
		Last Modified: Wed, 24 Jan 2024 20:47:08 GMT  
		Size: 12.9 MB (12914665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e879d4d5043a79bffdc954e68d81618afc9a89750014d054726d314fedf859f0`  
		Last Modified: Wed, 24 Jan 2024 20:54:45 GMT  
		Size: 53.1 MB (53135195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb25830af837858464e9dec1957d6d51d8fd53883e56b0ece78fbe6d945cb502`  
		Last Modified: Wed, 24 Jan 2024 20:54:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d750dc354605632ff82e822531225e89faf60c868b498ee44be3b417a7548ee0`  
		Last Modified: Wed, 24 Jan 2024 20:54:39 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7b99ba93704bf09d0fe60ab3264602eae61dbbc228e6d84a7eba67fa40e9123f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109122169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08d955abab529bb16e452061a65f6fdcfa3e347bccc5fa650467b272767e48f`
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
# Fri, 26 Jan 2024 01:22:27 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Fri, 26 Jan 2024 01:23:05 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 26 Jan 2024 01:23:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 26 Jan 2024 01:23:08 GMT
COPY file:80168d55afbbfdfea820e78ae2e1141fd21095cf26d68a4715fadfae5beb9e0b in /__cacert_entrypoint.sh 
# Fri, 26 Jan 2024 01:23:09 GMT
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
	-	`sha256:2de33a8133e92365f201a723b8a76caae6bcff01416e89e2ac49cad5dc19dd34`  
		Last Modified: Fri, 26 Jan 2024 01:26:50 GMT  
		Size: 53.8 MB (53792052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96942193ca847de4b30f4f084d3354f87c70188df252b102d0eca441c5ede471`  
		Last Modified: Fri, 26 Jan 2024 01:26:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357e1cedf79449ab5bfd9c3b06f8cedcd20348e1e84cae951e74f9def9c01e0c`  
		Last Modified: Fri, 26 Jan 2024 01:26:41 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b152b60c553d61a5e342aa3a03956e88d0e9ee2b0a7b8c771f207e0c50774492
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98562657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de85e7582553899c8e29515d69cafd887673830af0d0dec9d51944c0da8e8e93`
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
# Thu, 25 Jan 2024 17:37:50 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Thu, 25 Jan 2024 17:40:50 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 25 Jan 2024 17:40:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 17:40:53 GMT
COPY file:80168d55afbbfdfea820e78ae2e1141fd21095cf26d68a4715fadfae5beb9e0b in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 17:40:53 GMT
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
	-	`sha256:0c5df86ebbd2189e91c19e13a85f44d2e83a744020aa27684cf03b439b2c50fc`  
		Last Modified: Thu, 25 Jan 2024 17:47:04 GMT  
		Size: 49.8 MB (49838118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81219bebb3dfcfa3d8a5d4428fc3d7e3c1d35ae94e07f59837807058e07d0cab`  
		Last Modified: Thu, 25 Jan 2024 17:46:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b5e279005d80b3775e3803834528edcda4e19840a8d0b3a6d06a3b767171ca`  
		Last Modified: Thu, 25 Jan 2024 17:46:57 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
