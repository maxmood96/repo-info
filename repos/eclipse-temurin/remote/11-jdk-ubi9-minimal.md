## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:f3143bc70a8aa363392512fa8f7a003c19e404b0ed2f98a0236cfb95c68c4fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fd865551b94c9baeb363cc2cc2d25304df359f460e6fd971ba5c205206d68310
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206994316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70732b752bb72217b6a343bb2b9cc864ad1d2c8ef89a802af8803c79650fc78e`
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
# Thu, 19 Oct 2023 02:51:36 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 19 Oct 2023 02:51:44 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:51:46 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:51:46 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:51:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 02:51:47 GMT
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
	-	`sha256:d8c66f8fce28c78d08411be967c06ffbda7d1ad659be8a531a8119b61ba52647`  
		Last Modified: Thu, 19 Oct 2023 02:57:19 GMT  
		Size: 141.3 MB (141285821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888cde5469e993c0b4742b31bd0bd3501a68b3198c565896a360ec5e2f202586`  
		Last Modified: Thu, 19 Oct 2023 02:57:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5542d79c3bbd37acf9965eb817fcbc256a1874ab43644f825b9923f756be2e8`  
		Last Modified: Thu, 19 Oct 2023 02:57:08 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6a4df45e3ecad6e813ea572623772eff5bdeb66d781587995d1a481f62a31297
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202481544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61920b7add76bda07740f68b2d6b1bf7ca8050a08ac9aefec8160a6dfc5d502b`
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
# Thu, 19 Oct 2023 03:05:24 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 19 Oct 2023 03:05:33 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 03:05:36 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 03:05:36 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 03:05:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 03:05:36 GMT
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
	-	`sha256:065e121beafde2a1c3465dbcccdfb1fc8d1a13703206ea6212e22ac9cf010343`  
		Last Modified: Thu, 19 Oct 2023 03:09:12 GMT  
		Size: 138.0 MB (138032516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134e4ce07a0cbd3f547b65cdda8493df5b3c17fb8604e62a7ed49f106bea288d`  
		Last Modified: Thu, 19 Oct 2023 03:09:02 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ded3c1622391f91105db79d0cd388b6ac21f3c0fcf76228bb388f862ff7d081`  
		Last Modified: Thu, 19 Oct 2023 03:09:02 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:00e3b4667abf7c8600f801a8163f5a22ac94734b91da75344f0d5f61b1f52df0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201219433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9bc6e23a6a40b43679a879da1c675db656155d5c14ae13ed363d3d0a196ac2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 10 Oct 2023 23:21:24 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 10 Oct 2023 23:21:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Oct 2023 23:21:31 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Tue, 10 Oct 2023 23:21:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Oct 2023 23:21:32 GMT
CMD ["jshell"]
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
	-	`sha256:ac47fe5cfac6b6f4f01aa3dee33dab51fad2fc84d1dcafae5cfae5fbe8dc9e35`  
		Last Modified: Tue, 10 Oct 2023 23:24:46 GMT  
		Size: 128.5 MB (128486016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91401b797262591cafa02c53220dae4e4892320dbf3848cd032642efd07015b7`  
		Last Modified: Tue, 10 Oct 2023 23:24:29 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582cb235251144336a77056537c55b9ac747076626719617473a76564115d082`  
		Last Modified: Tue, 10 Oct 2023 23:24:29 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:bd5303974b7788a3d9e82eecf49f071db999e836978611a77cd323aeb41ec1b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185594713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d123f904df175fc988b34b32ba73173bda58ae4f54efebbb17ffb102d8812d0`
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
# Thu, 19 Oct 2023 02:41:23 GMT
ENV JAVA_VERSION=jdk-11.0.20.1+1
# Thu, 19 Oct 2023 02:41:31 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='69d39682c4a2fac294a9eaacbf62c26d3c8a2f9123f1b5d287498a5472c6b672';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='b806f4bb526161bf9b2ffb37be4e1b77f56b4e726dc4d52c7902130a79e7d710';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a7efbe804a4616d38b6ac0def40cd9feacc04aee2bb89132191f4d33fc0a7c1e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='398a64bff002f0e3b0c01ecd24a1a32c83cb72a5255344219e9757d4ddd9f857';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1%2B1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:41:36 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:41:36 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:41:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 02:41:36 GMT
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
	-	`sha256:f4a1447a9a0298c89fff970148044f044fd0a94b44dc508408b9001d1d74624f`  
		Last Modified: Thu, 19 Oct 2023 02:44:13 GMT  
		Size: 121.5 MB (121544987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c709dc4a14949f1103b2df1a9a90eeb073fb0b80e645abf758a3c2145c5a2b`  
		Last Modified: Thu, 19 Oct 2023 02:44:04 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c975b24ba2bdf09d0640e5f74850d76d1107dc4a996d51e677911fda04da79`  
		Last Modified: Thu, 19 Oct 2023 02:44:04 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
