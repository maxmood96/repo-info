## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:69e43cddd4a3efa2c55f38d6effa87c0e22f0e81cd5c58889dc3f67bc8f1e798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:11f79817ff00dec3d783d3aad9b744e73fe9a5f4dddfab238e3c78da49db76e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208932184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f775ff88d33394854dc7f33a5a942942cc9e9345ad39d49cca19f212c323265d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
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
	-	`sha256:674a035412bd301bfa587aa0778bdbfccb798927552775bb9fe52d9ab24aa6ff`  
		Last Modified: Wed, 04 Sep 2024 21:55:04 GMT  
		Size: 142.0 MB (142007387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887c3882cc2b78cf9cfafe43011cbebaf830a75ec9bffa7fc81b2d8c7f54c82b`  
		Last Modified: Wed, 04 Sep 2024 21:54:53 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a61ae0aa8949ba839c044fb80cd659d26bde42f5381c59787a3ba26d0a118a`  
		Last Modified: Wed, 04 Sep 2024 21:54:53 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:12a1eb6fac376241c7db9ca460304868b085782c93c6c3d890487dbdb38bb43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204348000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92c6cae9396f4eb5c23fd4ad3c16ea51409836c6cf37501bbffbfd678e7d89`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
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
	-	`sha256:cc4edede495c8981c0e93aeb52521be93a78c79b2c830f182e8ac41660621e5f`  
		Last Modified: Wed, 04 Sep 2024 21:51:48 GMT  
		Size: 138.8 MB (138814161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4095a331bf7f8179e814c418ac049cde674209265f48e5822c8a3a39079f90`  
		Last Modified: Wed, 04 Sep 2024 21:51:39 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea288ff39e3f52d0764f8bcb9d4af0d5d2dcff1d331937393872d8bc9bea8fe6`  
		Last Modified: Wed, 04 Sep 2024 21:51:39 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:a80799358d122be85e36c406bfd43163fb43f82d395d77f0af3b42ed8b37617f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203133105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aea0c1377e5a108093f1a31db8d54a89f6c29b991ff49cd57a5f1a465cdb627`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
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
	-	`sha256:f455912d6f5149e9d99ae119f19360c9f4c84e7b5aabd1d531733b9b0768c3e3`  
		Last Modified: Wed, 04 Sep 2024 21:30:43 GMT  
		Size: 129.3 MB (129252005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fef2695c6b507e24c74bbb342eeccceb7416f38c0a0ea8a9d01edc9c8e045c`  
		Last Modified: Wed, 04 Sep 2024 21:30:31 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05325c7818f1af3b2ab491a9cb43e50e9ab1fc60d14350e2aa6a01dc62c577e3`  
		Last Modified: Wed, 04 Sep 2024 21:30:31 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:7dc3ef638526197f9467e0da379a908c3e88ee5aa9144a752d5cb1258bc4f178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187124198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0706ad02f914f9cba17e438d9b509ff610cea66c9339366dc378b3be99ca403d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 14:03:11 GMT
ADD file:3be9883ece0ff5165cc24f0c588e3b42dc016404a82d559b5b886dd6a5b2dd6b in / 
# Tue, 27 Aug 2024 14:03:12 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 27 Aug 2024 14:03:12 GMT
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
ADD file:0be936f502a287e8906580e1bf6c9e7ab2575d33a1f300d26347c5ede4e5741c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.json 
# Tue, 27 Aug 2024 14:03:14 GMT
ADD file:09261f6eece8b1a99ffeb75f49833c204551e89b3ba163ce849889c560d99a24 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227 
# Tue, 27 Aug 2024 14:03:14 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-08-27T13:56:46" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227"
# Tue, 27 Aug 2024 14:03:15 GMT
RUN rm -f '/etc/yum.repos.d/repo-ecaf9.repo' '/etc/yum.repos.d/repo-c70d8.repo'
# Tue, 27 Aug 2024 14:03:16 GMT
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb313ca4b0a99db95fc46c5cc693c9716554d0679ba03a2afd9303df30894b6a`  
		Last Modified: Wed, 04 Sep 2024 12:09:47 GMT  
		Size: 37.4 MB (37402801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135f4e569ebfcc39dffd5ba3440ec9b9b142ae9199b1c3d226aa2186f476fb43`  
		Last Modified: Thu, 05 Sep 2024 00:24:11 GMT  
		Size: 27.8 MB (27791172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083cc6698514936ca8949783ecb923503e9d8617e91dd95fc6e82ec73a9b9471`  
		Last Modified: Thu, 05 Sep 2024 00:24:15 GMT  
		Size: 121.9 MB (121927965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1ae46b9d9820968adaba5caf48bf88e89182fb5f1946edc98be862d152b543`  
		Last Modified: Thu, 05 Sep 2024 00:24:11 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baccade0e22597406d44c5f2397b98ad9745ad95bc29fd738164bb2f350059ed`  
		Last Modified: Thu, 05 Sep 2024 00:24:11 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
