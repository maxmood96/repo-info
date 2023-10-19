## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:08f999de37d3234a007558ba02e119cc17b1838e1f0f9a99d5d394f949c079ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2246ceac61ac171294b1cb4c784f1515cd2026fbe351829aaf54449fc876df87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119196576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61db023b6dfe577d4533f1ac8759faadc789bd949e35cd99956da3f622e2a4f9`
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
# Thu, 19 Oct 2023 02:53:30 GMT
ENV JAVA_VERSION=jdk-21+35
# Thu, 19 Oct 2023 02:54:02 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a36cde2956749aaad502e1df6729072e5483265fce142230516261da9a391db';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_aarch64_linux_hotspot_21_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='080a53a3f75b94450779199f09c8d91b53637d315f128c58a4f160fb6272502d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_x64_linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:54:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:54:03 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:54:03 GMT
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
	-	`sha256:40e7286c0fe1c82329b93e855071a7993eeb78ccb4b73f5e1785f77c970ba74a`  
		Last Modified: Thu, 19 Oct 2023 03:00:47 GMT  
		Size: 53.5 MB (53488098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03357b3336a6878a7f073bd8b9d2dd24c2667bf4b6f6f4a15f86a8f2ea1b021`  
		Last Modified: Thu, 19 Oct 2023 03:00:39 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11f133f1b294656e2b50ffeb559e1379510cbbe39c43458edca22b7e4c730ed`  
		Last Modified: Thu, 19 Oct 2023 03:00:39 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:26073effd7334089b22491187a7d69d32800860bf7899944828e006a5cc11e2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117107984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa28fcc9c6cdae73d5d09ea8b96b505d18f60366e0b9ceb92324da3a9e199324`
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
# Thu, 19 Oct 2023 03:06:39 GMT
ENV JAVA_VERSION=jdk-21+35
# Thu, 19 Oct 2023 03:07:06 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a36cde2956749aaad502e1df6729072e5483265fce142230516261da9a391db';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_aarch64_linux_hotspot_21_35.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='080a53a3f75b94450779199f09c8d91b53637d315f128c58a4f160fb6272502d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jre_x64_linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 03:07:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 03:07:08 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 03:07:08 GMT
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
	-	`sha256:6f049b4d8f6f71cddf04b65c2bf5d7362c9b95ea7ed55deb32738fdd8900d5fc`  
		Last Modified: Thu, 19 Oct 2023 03:11:34 GMT  
		Size: 52.7 MB (52658975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ac48d1d4c7d99fcc10489aeefd37481cb8d1b9afb2b3e5fc57e6357177d301`  
		Last Modified: Thu, 19 Oct 2023 03:11:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb1e168ed734245dc77792e98f52bb0ff609b274e491d3b389dbf31fb8334d7`  
		Last Modified: Thu, 19 Oct 2023 03:11:28 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
