## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:3a9dc208a6ac3ebf59603d4aa48dd6190a8901ef1207656de9dd16e0ad7bb390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:884e3924ec98a5aa38685af0132ad901c4080f33365e14d35b119d76dee93e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120435459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669de0de61d69225bc416d5b58e450899e4f8cac4d291f74fae801abc92f0a8c`
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:217f3732b43843b9b2c0106ad6bc868df8d97a0dcba97e8a83e94a66754eac77`  
		Last Modified: Wed, 04 Sep 2024 21:56:39 GMT  
		Size: 53.5 MB (53510678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44be210d62b62c7c93685cca908a53b7f6b154578a7d1d71de6bf5fb941f4f5`  
		Last Modified: Wed, 04 Sep 2024 21:56:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278f56e813de4be2b7e71da5513f6f1de3f3c2a5b230cee0b7d9389834c942fa`  
		Last Modified: Wed, 04 Sep 2024 21:56:32 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c6c007e36dbb7ef937e18fbf764121d6b435c0c0c3dbe9fc6fbb233aaf330e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118169939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207ed9b384b3232baeb90272b7f064af88ce34234164248a6620105525929828`
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:ed7c1f0042ca69d41856ece9f295af105dfd8f4a2e7c79f2fa7f6fc691924f54`  
		Last Modified: Wed, 04 Sep 2024 21:53:15 GMT  
		Size: 52.6 MB (52636115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db3c722e25c8d4382050efa6b405a73de3a5315e68bc0ce06f5c9cb34245f2e`  
		Last Modified: Wed, 04 Sep 2024 21:53:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af97ca9cc1e6fe6d627c881161e1f5a6923b0022c9fe02b103fd5b804abfb474`  
		Last Modified: Wed, 04 Sep 2024 21:53:09 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e198a6b77e9265ae11fb33b3bae49673f630c62f27da20d122866b74f5a49178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127452542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220fe15f5ad5479df5a3dee57a888228be7a32cdd6d4de3cc4447583d6f9d782`
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
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
	-	`sha256:adac6fb721a4c62692aa7a5d79caf7f17c32ae675528381a848b0a32c685b6fc`  
		Last Modified: Wed, 04 Sep 2024 21:32:30 GMT  
		Size: 53.6 MB (53571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b89b01d533515e78b36e830c83d277d2647a42702ec9a138db5c5da817179c9`  
		Last Modified: Wed, 04 Sep 2024 21:32:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846f276c6b1946b8117c2a8000f79d53244c3651f5b1a453f9dd1edf1a82da5e`  
		Last Modified: Wed, 04 Sep 2024 21:32:21 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c46a17e5f2602e7b6b10d26f0aca7e05e6525e193f9473e316bd86a68564ee10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114559658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726e67732efdbcf580c81db95b89ad051d9364a69cd86ed164648679575a2e7c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Jul 2024 16:02:12 GMT
ADD file:1a0498fcbd53ea6a4cce5caa1a166c86ab5a3d63fb2e6f1005f6229cd3fd8ddc in / 
# Thu, 18 Jul 2024 16:02:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:02:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:02:13 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:02:13 GMT
ENV container oci
# Thu, 18 Jul 2024 16:02:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:02:13 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:02:14 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:02:14 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:02:15 GMT
ADD file:260b735774b29b332765c57758623137b24eea7dfd0749ddc4f622d177cc9a81 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:02:15 GMT
ADD file:6c5a2a1a67a074079cab4ce304a1b74e6ebbcec0d31479580388db97c242c818 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:02:15 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:02:16 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:02:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:02:18 GMT
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:503bb890315f555a5f9d7cf50d5a90a092481d25c9c474822b5e12c758ad6065`  
		Last Modified: Wed, 24 Jul 2024 00:09:55 GMT  
		Size: 37.1 MB (37116517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067abbd59221a137019fc8775d8224b3867a3583ecfaf2af6a4d69582b0d7643`  
		Last Modified: Wed, 24 Jul 2024 23:02:44 GMT  
		Size: 27.8 MB (27772786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efadea03d3fcfd92604c5d51a80781f889d7de4cafb2784f359e8b5ef352546`  
		Last Modified: Wed, 24 Jul 2024 23:04:00 GMT  
		Size: 49.7 MB (49668113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e8a5005cfae8a015ea60bc284b61d8d3d75bcf9d3ab4e782627ee1587773f4`  
		Last Modified: Wed, 24 Jul 2024 23:03:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd973d88e9cef74e279f6aceb9f258d99645e4797d8a4ee99de9ad8b7477b51d`  
		Last Modified: Fri, 23 Aug 2024 19:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
