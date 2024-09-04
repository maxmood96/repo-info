## `eclipse-temurin:8u422-b05-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:ab87dd6cae54183ebde4d645bba6e3eb108eb7f9285c19e2ba696e059bf7a104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u422-b05-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:30ff67d6f825d4bd6228806f09fc7a5a74bff968e639616878168a2cc83bfb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108807805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844237a692face46d88734f66f4648718ade911c88170c63177697920b05ad7a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 14:03:11 GMT
ADD file:28a4a75a9aeca0a5843143d1d87f7e6aefda81bdf346196d22398dee9b7df3d3 in / 
# Tue, 27 Aug 2024 14:03:11 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 27 Aug 2024 14:03:12 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 27 Aug 2024 14:03:12 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Aug 2024 14:03:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 27 Aug 2024 14:03:12 GMT
ENV container oci
# Tue, 27 Aug 2024 14:03:12 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 14:03:12 GMT
CMD ["/bin/bash"]
# Tue, 27 Aug 2024 14:03:13 GMT
RUN rm -rf /var/log/*
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL release=1227
# Tue, 27 Aug 2024 14:03:13 GMT
ADD file:0b1fee39b7bed921468ebab3ffc98a2ab087629c37a0e3e3cb03b93101e57ebb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.json 
# Tue, 27 Aug 2024 14:03:13 GMT
ADD file:200862b6d11d841a68f9e14872cdabb79746d525114364781cdd4db91dd45267 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227 
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:56:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227"
# Tue, 27 Aug 2024 14:03:14 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Tue, 27 Aug 2024 14:03:14 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 27 Aug 2024 14:03:16 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        ppc64le)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        x86_64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c0ca389759b542396e6b30afcb100a3823d3b343bc847eee7f60d609a106f674`  
		Last Modified: Wed, 04 Sep 2024 07:33:30 GMT  
		Size: 39.2 MB (39158889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c410b6202d1bff60f5ab50a19c7298d4bcc51744f626dd1a29b47e7e183594d7`  
		Last Modified: Wed, 04 Sep 2024 21:54:24 GMT  
		Size: 27.8 MB (27763649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4253fea76e24952507383bd369c31c3972e30e632048e3c36e719523e66ee526`  
		Last Modified: Wed, 04 Sep 2024 21:54:43 GMT  
		Size: 41.9 MB (41883025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea41894fe0bc43dc418d0aafe0bfb3d6c4dd625e3a11488dd7cdc5bf5303509`  
		Last Modified: Wed, 04 Sep 2024 21:54:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56387288fc9ce29777f6cd699a1633f1ac37780c46b4390679af5cf03721469`  
		Last Modified: Wed, 04 Sep 2024 21:54:39 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u422-b05-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d57e49277a9ddf50850b3f7dfd7f23d1dadade87142a588e0aa1401ee9b740d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106384952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f414b21eccc36568027080cecbbd88f73d55cc4e0b2eabc0cde5e6d629fa34c0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 14:03:11 GMT
ADD file:9a5f39ba1f98c406e15a468dde96a97890537c615e6855d570753065003706c9 in / 
# Tue, 27 Aug 2024 14:03:12 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 27 Aug 2024 14:03:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 27 Aug 2024 14:03:13 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Aug 2024 14:03:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 27 Aug 2024 14:03:13 GMT
ENV container oci
# Tue, 27 Aug 2024 14:03:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 14:03:13 GMT
CMD ["/bin/bash"]
# Tue, 27 Aug 2024 14:03:14 GMT
RUN rm -rf /var/log/*
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL release=1227
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:34b7dbe1b5044530865977e137b95f472d40aa5287f2d845e436e943ed292fb0 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.json 
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:f2f42168d45968aaf5ad1ce77e9c21e661944f67624f2f1bb4e37bb2da84056a in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227 
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:56:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227"
# Tue, 27 Aug 2024 14:03:15 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Tue, 27 Aug 2024 14:03:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 27 Aug 2024 14:03:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        ppc64le)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        x86_64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:83e0d15826a8ceb224771cdacee673e782c6608cbaa3de01e33c5d01dc968d1a`  
		Last Modified: Wed, 04 Sep 2024 12:09:37 GMT  
		Size: 37.3 MB (37301947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c871629d0a973b06c6adf6069361a497c516de2dfbfb55881f24eb42c03592`  
		Last Modified: Wed, 04 Sep 2024 21:51:11 GMT  
		Size: 28.2 MB (28229634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03283786dabe41483a51fc8fae323c853c2adc093e88e07c160ccf1d36c1ad4`  
		Last Modified: Wed, 04 Sep 2024 21:51:28 GMT  
		Size: 40.9 MB (40851128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a425ad00a8d5d166380a26fafb91ec8461be6f86263c32d66a07d5ae6184951`  
		Last Modified: Wed, 04 Sep 2024 21:51:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec73a2b5f42473fea3c4b0118cd3e5ec5ba42e222c48e49447c0c48346baab5e`  
		Last Modified: Wed, 04 Sep 2024 21:51:24 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u422-b05-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:43ea3e63d22bcd5c4f3df87e5df859342e1edd32a02a17b7ba60886cbfd764a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115128087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74925c819113de4a7965d7f24685355c31dbfb73ead33fc54ce1cad09ceaefd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Aug 2024 14:03:12 GMT
ADD file:f007a60e32e08d43c550a97c16f972f39506988b7e247bd6627599e91c17323f in / 
# Tue, 27 Aug 2024 14:03:14 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 27 Aug 2024 14:03:14 GMT
ADD multi:b7aa4ff38ab5ea75bf6e77e6baa757897a071e6d87e5b1b50d0beab3143be0b8 in /etc/yum.repos.d/ 
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 27 Aug 2024 14:03:14 GMT
ENV container oci
# Tue, 27 Aug 2024 14:03:14 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 14:03:14 GMT
CMD ["/bin/bash"]
# Tue, 27 Aug 2024 14:03:15 GMT
RUN rm -rf /var/log/*
# Tue, 27 Aug 2024 14:03:15 GMT
LABEL release=1227
# Tue, 27 Aug 2024 14:03:16 GMT
ADD file:a5f8a4fe76e7d622a09fcbcca3627d47677c86bd786397d064531d01811fcdb0 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.json 
# Tue, 27 Aug 2024 14:03:16 GMT
ADD file:a3679a8847d919079839b3a73f96cc68368baad49ccd60dcbe5305759aba49b8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227 
# Tue, 27 Aug 2024 14:03:16 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:56:46" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227"
# Tue, 27 Aug 2024 14:03:17 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Tue, 27 Aug 2024 14:03:18 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 27 Aug 2024 14:03:21 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8fbefff2c578f73d95118d830347589ddc9aa84510200a5a5001901c2dea4810';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        ppc64le)          ESUM='2991edbedee448c0f1edf131beca84b415dac64ea97365b9bfd85bc2f39893bb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        x86_64)          ESUM='0ac516cc1eadffb4cd3cfc9736a33d58ea6a396bf85729036c973482f7c063d9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jre_x64_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5591fa6d9bf998094d14bbf292637dc73858269f63d69d897a1a64df35d25765`  
		Last Modified: Wed, 04 Sep 2024 12:09:42 GMT  
		Size: 43.6 MB (43628240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4ce08d6eb5ec512eb0e847a5a03bd92ab817cc08e181f01d83186106754432`  
		Last Modified: Wed, 04 Sep 2024 21:30:01 GMT  
		Size: 30.3 MB (30250600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2977e07be8d9127440b3dc7893a7f35375d98002dfcb1c652080ef2e7ffaa0ae`  
		Last Modified: Wed, 04 Sep 2024 21:30:22 GMT  
		Size: 41.2 MB (41247005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d197e843a65f1203b338a864f3ecb806cb72ab035b46786c972f2ce66e89e3c`  
		Last Modified: Wed, 04 Sep 2024 21:30:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7532681ea5d764ca14ea9e1135491c99fd9ab04ab33f273f852a5536fb0d75`  
		Last Modified: Wed, 04 Sep 2024 21:30:16 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
