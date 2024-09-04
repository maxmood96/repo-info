## `eclipse-temurin:22-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:06ebce63611c42bb6bfb7884d6e987d2e2b0bd299883fd22e63e54145143e618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:22-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3542f367f9453f024f0101257da43f8ec981e1e3da4ff69c26518e23c48d292c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119598733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3023aec5abe93d302590a60df157da9d5364ae687706f6ad91741e60aba9e18b`
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
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='7cf494b51625505d1843ad032677d885bd8000a80d0d38396685f25acbdb5708';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64le)          ESUM='132191d6f23ad1ac558de67e3e9913d047db07efd979eb84bf5dc20a651ffe61';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='4d9bc998c29fffcbbf752e9d0bf32391928a9e7a46edb1c5706e0f55b34a0c56';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='41e401f287e1850631b259b483929462217ac6b1cc3c7359d80b1cc01ee5a666';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:4dac323619d78cbd7a90057fe19a62ed7ff139102595e427b006d47e3716dbae`  
		Last Modified: Wed, 04 Sep 2024 21:57:18 GMT  
		Size: 52.7 MB (52673951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65821d91edd00e9b0d26219d3fc3cb9d8417cacc9378bb447846d2020241c0aa`  
		Last Modified: Wed, 04 Sep 2024 21:57:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d0469a77ec18626abb7619c7caa3ebc0adb4c7ce46dab3a9e3d15231a5f33b`  
		Last Modified: Wed, 04 Sep 2024 21:57:11 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1cddbf716bbec0be56b9a2842babeca2dd2c69883364b66db065c6bc74200192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117267133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d495efca272a1eec57e879cff2d169772d20a5228cce90f8f70b35c9c25c25f3`
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
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='7cf494b51625505d1843ad032677d885bd8000a80d0d38396685f25acbdb5708';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64le)          ESUM='132191d6f23ad1ac558de67e3e9913d047db07efd979eb84bf5dc20a651ffe61';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='4d9bc998c29fffcbbf752e9d0bf32391928a9e7a46edb1c5706e0f55b34a0c56';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='41e401f287e1850631b259b483929462217ac6b1cc3c7359d80b1cc01ee5a666';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:6482647a927bb3eeffb41f2a4656f11598eec27fff867e1733afa3a792672f10`  
		Last Modified: Wed, 04 Sep 2024 21:53:52 GMT  
		Size: 51.7 MB (51733309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5587acd90678e5b0879304c892ed5f6a60e75dd85ff96ab36721236c7de92607`  
		Last Modified: Wed, 04 Sep 2024 21:53:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026e83d39080986ace907962fd7031299655ec441b85ba233cdef5916feabe9d`  
		Last Modified: Wed, 04 Sep 2024 21:53:45 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9f4456d562c8925336d14e2e69da7d1082d9b336df65eaa996ecce31b0873e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126496148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea27151fbdcbb0ad2fec46f95593619898689c3bef8094ad58e0d984a802c8ec`
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
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='7cf494b51625505d1843ad032677d885bd8000a80d0d38396685f25acbdb5708';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64le)          ESUM='132191d6f23ad1ac558de67e3e9913d047db07efd979eb84bf5dc20a651ffe61';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='4d9bc998c29fffcbbf752e9d0bf32391928a9e7a46edb1c5706e0f55b34a0c56';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='41e401f287e1850631b259b483929462217ac6b1cc3c7359d80b1cc01ee5a666';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:0db2baf978c335c7070fc52de7087aebc1312f05ba9f3b242183382e063fd077`  
		Last Modified: Wed, 04 Sep 2024 21:33:12 GMT  
		Size: 52.6 MB (52615064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f765a9bc51798cc033b05f69cc1e685cbdf597c5b69194aff4a6fcb44ebf642`  
		Last Modified: Wed, 04 Sep 2024 21:33:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510d0997856671842ef4c3240014f8c2a93de63e8d18f1cdf6d2fac7406dd1e1`  
		Last Modified: Wed, 04 Sep 2024 21:33:03 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:4fd0048a6b73e7e0884abf5fb9489e1636dc0364dcd78dc27d3030a82842d2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114028315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0c140fcb193f8158b74d2470bb5039d847a58dcbe76cf4dc80f13941bc1656`
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
ENV JAVA_VERSION=jdk-22.0.2+9
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='7cf494b51625505d1843ad032677d885bd8000a80d0d38396685f25acbdb5708';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_aarch64_linux_hotspot_22.0.2_9.tar.gz';          ;;        ppc64le)          ESUM='132191d6f23ad1ac558de67e3e9913d047db07efd979eb84bf5dc20a651ffe61';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_ppc64le_linux_hotspot_22.0.2_9.tar.gz';          ;;        s390x)          ESUM='4d9bc998c29fffcbbf752e9d0bf32391928a9e7a46edb1c5706e0f55b34a0c56';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_s390x_linux_hotspot_22.0.2_9.tar.gz';          ;;        x86_64)          ESUM='41e401f287e1850631b259b483929462217ac6b1cc3c7359d80b1cc01ee5a666';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.2%2B9/OpenJDK22U-jre_x64_linux_hotspot_22.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:faf37d1c90782a184e500e5cbbd7c1ad873f77ffa1bcdd49a8921ec28ebc9115`  
		Last Modified: Wed, 24 Jul 2024 23:04:30 GMT  
		Size: 49.1 MB (49136772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40773dc429ddc25ace1d1e10a7903fcecfde744ebd898ed71571e163c2049cb8`  
		Last Modified: Wed, 24 Jul 2024 23:04:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c972fac911c38a785c158977a991d6a531907714ea93fb1fc5144124608c769`  
		Last Modified: Fri, 23 Aug 2024 19:49:44 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
