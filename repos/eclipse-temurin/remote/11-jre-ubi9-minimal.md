## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:08c5d37ea4c2f95bc0deff8c6038275f5a528b3d315ab97ce9aca9ab3aea886e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:29cd07b67eb7fbfdb7f16f38eb293cf92f9ba17754576b621fe961d781892765
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109585563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cdb0ef2b4f5e448422c4c4242b88fa08f2cc2d389066df881f711f066d763a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 17 Oct 2023 10:15:12 GMT
ADD file:0c5d05879b5d7d32f930c1beaf8ad9f6db37bec6c7bb91fecf0b158bf70803f0 in / 
# Tue, 17 Oct 2023 10:15:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 17 Oct 2023 10:15:13 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 17 Oct 2023 10:15:13 GMT
ADD multi:4e5954f068a55d1448054f27ac557b6ddfb05f27a96a5b66e3c3e0e18b1ebf30 in /etc/yum.repos.d/ 
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Oct 2023 10:15:13 GMT
ENV container oci
# Tue, 17 Oct 2023 10:15:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Oct 2023 10:15:13 GMT
CMD ["/bin/bash"]
# Tue, 17 Oct 2023 10:15:14 GMT
RUN rm -rf /var/log/*
# Tue, 17 Oct 2023 10:15:14 GMT
ADD file:86286d94d563bf0adbc7d26edbd283bab3299216732a58412c76ee497d74627e in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1697534106.json 
# Tue, 17 Oct 2023 10:15:14 GMT
ADD file:73acdbc48477957e28c9fe2847b511144adf0dec06ff8516416b1e2520432e1e in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1697534106 
# Tue, 17 Oct 2023 10:15:14 GMT
LABEL "release"="750.1697534106" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-17T10:03:30" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1697534106"
# Tue, 17 Oct 2023 10:15:15 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2451840-29300.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Tue, 17 Oct 2023 10:15:15 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 17 Oct 2023 10:15:17 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 19 Oct 2023 02:50:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Oct 2023 02:50:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 02:50:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Oct 2023 02:50:43 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 19 Oct 2023 02:51:36 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 19 Oct 2023 02:52:09 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:52:10 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:52:10 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:52:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5f093fe9a5aa441cd3cc59f19cbf324af431653a8fde63fefd31a3d40c4135d1`  
		Last Modified: Wed, 18 Oct 2023 07:45:30 GMT  
		Size: 37.8 MB (37848955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146714005ffcbd9ac36c8b25681c3a9417c7bf3d45886dce27194a4dd0a0d5f4`  
		Last Modified: Thu, 19 Oct 2023 02:55:50 GMT  
		Size: 27.9 MB (27858655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5df9c0935856c7f36b9d8b443999ca3d1ac337149ad75de16a2a2ac55617c4`  
		Last Modified: Thu, 19 Oct 2023 02:57:54 GMT  
		Size: 43.9 MB (43877081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee168b5d7ceb5e7220cdc8740f30d92008f38f3103d7a8a5a463a4059c927bd8`  
		Last Modified: Thu, 19 Oct 2023 02:57:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a08bc95a1d2fabbd2f6f8a5f474511d2084b97fe408a44a13432d5822b1a21`  
		Last Modified: Thu, 19 Oct 2023 02:57:48 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:dd2e25a19d2742682b7c7ae7ff3ccc6f04af2f81e5d2e278fcdcab04f2daa765
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106651765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6118837f8d5b5b861660e47691b7d8dd26d2d2c76dcc5282be0ac63ac76718`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 17 Oct 2023 10:15:10 GMT
ADD file:d0c7268244afb53087c24f01c8a41771779e732f4be085164138f4687a39457f in / 
# Tue, 17 Oct 2023 10:15:11 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 17 Oct 2023 10:15:11 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 17 Oct 2023 10:15:11 GMT
ADD multi:4e5954f068a55d1448054f27ac557b6ddfb05f27a96a5b66e3c3e0e18b1ebf30 in /etc/yum.repos.d/ 
# Tue, 17 Oct 2023 10:15:11 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Oct 2023 10:15:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Tue, 17 Oct 2023 10:15:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Oct 2023 10:15:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Oct 2023 10:15:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Oct 2023 10:15:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Oct 2023 10:15:11 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Oct 2023 10:15:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Oct 2023 10:15:11 GMT
ENV container oci
# Tue, 17 Oct 2023 10:15:11 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Oct 2023 10:15:11 GMT
CMD ["/bin/bash"]
# Tue, 17 Oct 2023 10:15:12 GMT
RUN rm -rf /var/log/*
# Tue, 17 Oct 2023 10:15:12 GMT
ADD file:4fa75a5b2d4ea1cd5e7a376cc6c1a4749572edee3cf9300bfca2ae93c638daba in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1697534106.json 
# Tue, 17 Oct 2023 10:15:13 GMT
ADD file:929f709aa03324ed2eedd8f9c44343f1e609c4158c744e385b0fc479aa1ffe97 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1697534106 
# Tue, 17 Oct 2023 10:15:13 GMT
LABEL "release"="750.1697534106" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-17T10:03:30" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1697534106"
# Tue, 17 Oct 2023 10:15:14 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2451840-29300.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Tue, 17 Oct 2023 10:15:15 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 17 Oct 2023 10:15:16 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 19 Oct 2023 03:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Oct 2023 03:04:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 03:04:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Oct 2023 03:04:58 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 19 Oct 2023 03:05:24 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 19 Oct 2023 03:05:46 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 03:05:46 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 03:05:47 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 03:05:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7f17f66a889d79eed8f010709b6c1b6fd3553b8f1d641d0ae5cb20c00b2b8af5`  
		Last Modified: Wed, 18 Oct 2023 07:45:27 GMT  
		Size: 36.2 MB (36163686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87565c5945684348fc6c29d6b9817f04c4a213b3460fb22c1975a6800477f47d`  
		Last Modified: Thu, 19 Oct 2023 03:08:29 GMT  
		Size: 28.3 MB (28284452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0f610f411ffca051c7dac23befde7e4a3a1e7d5fcada79e67ddac01517e5bd`  
		Last Modified: Thu, 19 Oct 2023 03:09:31 GMT  
		Size: 42.2 MB (42202757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8190503d0bc5bedec10ff59a9389c9c5cb24353169197db75d255d5104d586aa`  
		Last Modified: Thu, 19 Oct 2023 03:09:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f426c3133650f6ae7747370009e2e1d2db7318a046e17848f44ec62634cfdf2`  
		Last Modified: Thu, 19 Oct 2023 03:09:26 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:a8b02e243abcdc5403164a8839a0ef7238b51c639186626bbded2adbde06d5be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112077193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25861153645d06cc22e9b4db5cae5f40815c31bccd5ceb847629dd7424a6bef6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 05 Oct 2023 14:38:58 GMT
ADD file:6d1fa1dd4f82effa3edd3df36cb6be0e361553a9a4ceb44387ec3c39709e1113 in / 
# Thu, 05 Oct 2023 14:38:59 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 05 Oct 2023 14:38:59 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 05 Oct 2023 14:38:59 GMT
ADD multi:983c894e8a29f7d84811b8480f8cb94a942803f65be70fbae4914c9f2a20c5e7 in /etc/yum.repos.d/ 
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Oct 2023 14:38:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Oct 2023 14:38:59 GMT
ENV container oci
# Thu, 05 Oct 2023 14:38:59 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 14:38:59 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 14:39:01 GMT
RUN rm -rf /var/log/*
# Thu, 05 Oct 2023 14:39:01 GMT
ADD file:328ddeb1ec18f23aacb0d0a2878c45c71ef674135124723e62d867c8005005f2 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1696515534.json 
# Thu, 05 Oct 2023 14:39:01 GMT
ADD file:d7126bc8d11f5a5c0794401215ed55d7754bdb3563355e4d1cfcc331f47c63e8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1696515534 
# Thu, 05 Oct 2023 14:39:01 GMT
LABEL "release"="750.1696515534" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-05T14:27:14" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1696515534"
# Thu, 05 Oct 2023 14:39:03 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2414592-d4ca5.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Thu, 05 Oct 2023 14:39:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 05 Oct 2023 14:39:06 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 10 Oct 2023 23:19:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Oct 2023 23:19:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Oct 2023 23:19:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 10 Oct 2023 23:20:17 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 10 Oct 2023 23:21:10 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Tue, 10 Oct 2023 23:21:52 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:21:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 10 Oct 2023 23:21:55 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:21:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:571735d1e71e07b1fa3a2fb676b0fb08b6139607cc00c69743cd5c964836cff8`  
		Last Modified: Mon, 09 Oct 2023 12:07:33 GMT  
		Size: 42.3 MB (42311719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cc747d263fea66ad8cdd4604f369660ef4ac8e363da97fcd971689c41886c8`  
		Last Modified: Tue, 10 Oct 2023 23:23:48 GMT  
		Size: 30.4 MB (30420809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed27e241f4348b1a98c1f38b3e8d0854cc1377c37012deed33b2daee394782e`  
		Last Modified: Tue, 10 Oct 2023 23:25:09 GMT  
		Size: 39.3 MB (39343794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abb32d89b5b07b0c159a66a8ee24f95d43a7af0d08e111cf1b3e80a3afb186`  
		Last Modified: Tue, 10 Oct 2023 23:25:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75b8ea98a50c0463fa565b9af4262aa0f89248858f0f2682b4eadc6f61ad67a`  
		Last Modified: Tue, 10 Oct 2023 23:25:00 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:7dcc01035f11dd40dbd630b61e048e2b56be049d24b44e432019b6efbd943194
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101657429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4dd1642082a64705fbf5e590f1db581c126ccba24a0d3dbb757b19ef498771`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 17 Oct 2023 10:15:41 GMT
ADD file:3775d4f4bbc749574049d3c7e5949ca724e6c88a35f97ea6671c3fd414a22d00 in / 
# Tue, 17 Oct 2023 10:15:45 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 17 Oct 2023 10:15:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 17 Oct 2023 10:15:48 GMT
ADD multi:4e5954f068a55d1448054f27ac557b6ddfb05f27a96a5b66e3c3e0e18b1ebf30 in /etc/yum.repos.d/ 
# Tue, 17 Oct 2023 10:15:48 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Oct 2023 10:15:48 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Tue, 17 Oct 2023 10:15:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Oct 2023 10:15:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Oct 2023 10:15:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Oct 2023 10:15:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Oct 2023 10:15:48 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Oct 2023 10:15:48 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Oct 2023 10:15:48 GMT
ENV container oci
# Tue, 17 Oct 2023 10:15:48 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Oct 2023 10:15:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Oct 2023 10:15:52 GMT
RUN rm -rf /var/log/*
# Tue, 17 Oct 2023 10:15:53 GMT
ADD file:54ce42a8f7ad919429422b5d5004e8585179b50d3748ab78b826e978e5be42f1 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1697534106.json 
# Tue, 17 Oct 2023 10:15:54 GMT
ADD file:f0c00156432f9cb07b294312fb15869b31232c6bb4b2a5122b915da1861070c8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1697534106 
# Tue, 17 Oct 2023 10:15:54 GMT
LABEL "release"="750.1697534106" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-17T10:03:30" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1697534106"
# Tue, 17 Oct 2023 10:15:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2451840-29300.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Tue, 17 Oct 2023 10:15:58 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 17 Oct 2023 10:16:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 19 Oct 2023 02:41:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Oct 2023 02:41:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 02:41:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Oct 2023 02:41:21 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 19 Oct 2023 02:41:23 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 19 Oct 2023 02:42:02 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f69f5c05cb7fb2804be3735ed31ce92acff1a51ef29be544b89f83c90d2ea2a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='7963580e5c3abe55e6b9d2297f2e2cde7b227d28204497bec5f17bb37762c7b7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf7fa0f0291687ebcb5f87f5db3a8d94525fd65832adc636c4c6e1f3174d9997';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bc6ed047e50b09611b419c878e4ea3ea36594bd79f64001a5b53decf72669d33';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:42:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:42:06 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:42:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d3ec0d1563ef1c7109fbca7e95dcd9c27363a7425f34c2b0088a396e4b1cfc2b`  
		Last Modified: Wed, 18 Oct 2023 12:07:15 GMT  
		Size: 36.1 MB (36145178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea7ebd6a1c9bd934e799f2d96765bdef84a09fce624d6c5c9d21e37769c7e8`  
		Last Modified: Thu, 19 Oct 2023 02:44:07 GMT  
		Size: 27.9 MB (27903662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097eaf745c3c1b7f39052a0c5d1e2f92b49ab71b76be85648bd8e7df10ea7495`  
		Last Modified: Thu, 19 Oct 2023 02:44:30 GMT  
		Size: 37.6 MB (37607718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f056d97b4e01a0514ce1ef40eed96265374d766ce456611a1dce3431a6aa0f99`  
		Last Modified: Thu, 19 Oct 2023 02:44:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e26fe1efaf9318a7a6a39e887db53ac3940008b5e84f98fae23e74602274109`  
		Last Modified: Thu, 19 Oct 2023 02:44:25 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
