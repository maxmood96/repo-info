## `eclipse-temurin:17-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:775ccdc8041e3c185482007deea6a071bdd2ad305791c13c44f6378f64dc3a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7c2116ce502ed18922008ee998c349b16041c882752e51b32119dbb41ea42174
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210490219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87cbec5bd144384fd8f722fc3b57c25671225b2019ca51833b638116a05ef3d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Thu, 19 Oct 2023 02:52:34 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 19 Oct 2023 02:52:42 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:52:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:52:44 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:52:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 02:52:44 GMT
CMD ["jshell"]
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
	-	`sha256:7788b8da264d4c1f7b66b9f588760053c7303d410500b62c25b97e74f1300d45`  
		Last Modified: Thu, 19 Oct 2023 02:58:42 GMT  
		Size: 144.8 MB (144781722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5650a7c40dbab251c90b0b259c048c5917e7d78c23062bb72b4dc0582eaaa336`  
		Last Modified: Thu, 19 Oct 2023 02:58:31 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf02187207d450034244f5b68ec2391429239869ac71e65ec4c725f162e4aac`  
		Last Modified: Thu, 19 Oct 2023 02:58:31 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b0171b7c4c6e87c6c2ea6b317a91cc3eb28bc26d45c95cacde132d1912213e02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207997996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d79f8880189f14ae8034404767a53fcf548da89c8ef36bb8530dc6b080de62c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Thu, 19 Oct 2023 03:05:53 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 19 Oct 2023 03:06:02 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 03:06:05 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 03:06:05 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 03:06:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 03:06:06 GMT
CMD ["jshell"]
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
	-	`sha256:9ce041427eae86afa44e091931fe7054065561db1fbb6c327761241347fe9646`  
		Last Modified: Thu, 19 Oct 2023 03:09:55 GMT  
		Size: 143.5 MB (143548970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad91fc9f02aed01b6e3dfe15fad9cb57eb20ec0c893fddf17c3479d4b8c65a86`  
		Last Modified: Thu, 19 Oct 2023 03:09:45 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec364ad8b17a253174e4a3f70f37755233a535afbae56fc811d36b8bf48d8c5`  
		Last Modified: Thu, 19 Oct 2023 03:09:45 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d5b3901e4db4dd3dee23ddfc3d2e926d307a1374824b7ff97aa66ee919eeb3d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217216604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6de6781ce4876a49de0dca11e15d2f615218078e696cb694e12a9cccb2a229`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Thu, 19 Oct 2023 07:27:14 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 19 Oct 2023 07:27:26 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 07:27:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 07:27:31 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 07:27:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 07:27:32 GMT
CMD ["jshell"]
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
	-	`sha256:ce9bd9f48ca898b29f311bd4de44266412fd749208db6cb3a5c62733bfba1f46`  
		Last Modified: Thu, 19 Oct 2023 07:30:12 GMT  
		Size: 144.5 MB (144512768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab1fbc045a6f169233b8479545b826998831153352148a3a5b7c47289e79f2`  
		Last Modified: Thu, 19 Oct 2023 07:29:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9d0bf73d5f543d54af7c631a15d89a1020ede78fb2c382af0a9fb9683dca38`  
		Last Modified: Thu, 19 Oct 2023 07:29:59 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:11b2934beb6a91c880e51a0f579bc4f96bfc7a3a073c158768fa30ae42815e9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198265368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913addfa41fa2c6a6c56b78a721545fd9e16b2c6c4a22a9eba7610037dc7b4b5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Thu, 19 Oct 2023 02:42:25 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 19 Oct 2023 02:42:35 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eefd3cf3b3dd47ff269fa5b5c10b5e096b163f4e9c1810023abdbc00dc6cc304';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='00a4c07603d0218cd678461b5b3b7e25b3253102da4022d31fc35907f21a2efd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ffacba69c6843d7ca70d572489d6cc7ab7ae52c60f0852cedf4cf0d248b6fc37';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c25dfbc334068a48c19c44ce39ad4b8427e309ae1cfa83f23c102e78b8a6dcc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jdk_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:42:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:42:41 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:42:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 02:42:41 GMT
CMD ["jshell"]
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
	-	`sha256:ec6fa0fd43bd0b2b561f3ed1244896ad4998a0a146f1d5b1f723e1286b7b3359`  
		Last Modified: Thu, 19 Oct 2023 02:44:51 GMT  
		Size: 134.2 MB (134215643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f7412d097b4b707bb4b23ad3398ae4fb00a5627e406105f943da08289c6e0e`  
		Last Modified: Thu, 19 Oct 2023 02:44:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32db4bf182ad116f890fbbc302885ad0ee678234ea9d47d0bb5216e8a7431520`  
		Last Modified: Thu, 19 Oct 2023 02:44:40 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
