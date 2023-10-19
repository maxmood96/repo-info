## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:038dd79d60295526172e27df9623858f2fd4b462f7735d09ab0ecef8cf1bc569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:77c751dc8eee9dd3ac51cc6bf3d2ea660f1e108707f21acacf6eaf144b7555d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107553540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a7561a51cd2146a2c863f2a3bdf9d0096b6c60b4fb8b206e9b1239a5ae14f3`
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
# Thu, 19 Oct 2023 02:50:43 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Thu, 19 Oct 2023 02:51:12 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:51:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 19 Oct 2023 02:51:13 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:51:13 GMT
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
	-	`sha256:981201f36f6fe3db9d57793bd9a52bb8c967c8f1611a77aace193d9a2af07a88`  
		Last Modified: Thu, 19 Oct 2023 02:56:31 GMT  
		Size: 41.8 MB (41845060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc6184e426404b84a886eebed6a7979c0c6c953e7d1b0a87872c219da96498a`  
		Last Modified: Thu, 19 Oct 2023 02:56:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aa522a72a05b68e61f637b0951793ca829d65bdb336fc5a958fa16bd45ad2b`  
		Last Modified: Thu, 19 Oct 2023 02:56:26 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:23785eca822fd6c37a5ec21d6cfee4b7e278669a3d595e15f8c4df91afda0e2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105292649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd2d44b09f8dd9c1dcba206b2e994cc7069055008a1c8f3d82631a3002aa09a`
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
# Thu, 19 Oct 2023 03:04:58 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Thu, 19 Oct 2023 03:05:18 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 03:05:18 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 19 Oct 2023 03:05:18 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 03:05:19 GMT
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
	-	`sha256:c4d5dd9350ad723bc240afb6743f48dc35441b656efd3bdda12a118e80f581e6`  
		Last Modified: Thu, 19 Oct 2023 03:08:51 GMT  
		Size: 40.8 MB (40843639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4531f7b885ffb05974a66c37dc34d3b056bc977b11f008c04272c846f3fad7`  
		Last Modified: Thu, 19 Oct 2023 03:08:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8f0fa80703664914e2f12ce7156bd7ec4e8c2e4e63c02ef5f55b59dc7a441a`  
		Last Modified: Thu, 19 Oct 2023 03:08:47 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:697b6092fdadf06c381e6ac93d657c29ddd37e200753f1873fa60d8dfbaf2415
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113929924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe3fae5e980a796fdb2b0193ac7a884bb6f3f5bdcbf8992ffbcd809fc443f92`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 17 Oct 2023 10:15:18 GMT
ADD file:39b25f6ce9dd05293dbcda68469f644d68b73faf4bfc17284a86ea944282b8bb in / 
# Tue, 17 Oct 2023 10:15:21 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 17 Oct 2023 10:15:21 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 17 Oct 2023 10:15:22 GMT
ADD multi:4e5954f068a55d1448054f27ac557b6ddfb05f27a96a5b66e3c3e0e18b1ebf30 in /etc/yum.repos.d/ 
# Tue, 17 Oct 2023 10:15:22 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Oct 2023 10:15:22 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Tue, 17 Oct 2023 10:15:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Oct 2023 10:15:22 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Oct 2023 10:15:22 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Oct 2023 10:15:22 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Oct 2023 10:15:22 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Oct 2023 10:15:22 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Oct 2023 10:15:22 GMT
ENV container oci
# Tue, 17 Oct 2023 10:15:22 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Oct 2023 10:15:22 GMT
CMD ["/bin/bash"]
# Tue, 17 Oct 2023 10:15:24 GMT
RUN rm -rf /var/log/*
# Tue, 17 Oct 2023 10:15:25 GMT
ADD file:02f700680dab6adbc8aba2d7225bc348db7089e6fe3cf33ffd66bcea88aedf03 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-750.1697534106.json 
# Tue, 17 Oct 2023 10:15:26 GMT
ADD file:eded54a1ad36d1100b251f9a46d59ae86b22ad74ba49f4277f7d4d1d694ca356 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-750.1697534106 
# Tue, 17 Oct 2023 10:15:26 GMT
LABEL "release"="750.1697534106" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-17T10:03:30" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-750.1697534106"
# Tue, 17 Oct 2023 10:15:29 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2451840-29300.repo' '/etc/yum.repos.d/gitweb-a7836.repo'
# Tue, 17 Oct 2023 10:15:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 17 Oct 2023 10:15:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 19 Oct 2023 07:25:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Oct 2023 07:25:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 07:25:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Oct 2023 07:25:51 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 19 Oct 2023 07:25:52 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Thu, 19 Oct 2023 07:26:19 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 07:26:21 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Thu, 19 Oct 2023 07:26:21 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 07:26:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5d7198cdfc86d1b6204763c2bec33fff4e40622c0ccf9811420a3f2135f3edd8`  
		Last Modified: Wed, 18 Oct 2023 12:06:55 GMT  
		Size: 42.3 MB (42282358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b35f1ab6dffccc9a7b4e6854f71cb98255e955e22eba616c7dd942b9c783740`  
		Last Modified: Thu, 19 Oct 2023 07:28:36 GMT  
		Size: 30.4 MB (30420591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08baaa27e00244dd814dc937dc580af6bf49b34decac60256999577304e6544c`  
		Last Modified: Thu, 19 Oct 2023 07:29:00 GMT  
		Size: 41.2 MB (41226104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b3d200313d5a2d3e48773520ab3596d7a5aca4d5c4ee41f0045658c7afd59`  
		Last Modified: Thu, 19 Oct 2023 07:28:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d150c8892370455e3b1f7765de89918b0ed40541d8ade041417bca5671fa1f`  
		Last Modified: Thu, 19 Oct 2023 07:28:54 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
