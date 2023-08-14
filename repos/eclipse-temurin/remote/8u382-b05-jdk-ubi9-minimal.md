## `eclipse-temurin:8u382-b05-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:94040bdd8d42349c15488a0dea6e842fc3a31845e4a02d86f52c2b2ff670b339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u382-b05-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0de302d5452bf96aecbb71332a08a9b767083f7cabccf5d3993364a08601e473
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169275747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de223d897911c87683c862b992ed6d918acd9a7b5c5fb4ab463675e1e1f700e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 26 Jul 2023 14:57:46 GMT
ADD file:f3010bd586bc7794afba95160a7961e057f655d5b4f52d06b705e2a617017edd in / 
# Wed, 26 Jul 2023 14:57:47 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 26 Jul 2023 14:57:47 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 26 Jul 2023 14:57:48 GMT
ADD multi:75455514cbe77ce7631a7c71aa7d7e34aff7f5078c6874650e6f91efe6e4c042 in /etc/yum.repos.d/ 
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL io.openshift.expose-services=""
# Wed, 26 Jul 2023 14:57:48 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 26 Jul 2023 14:57:48 GMT
ENV container oci
# Wed, 26 Jul 2023 14:57:48 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 14:57:48 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 14:57:50 GMT
RUN rm -rf /var/log/*
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL release=717
# Wed, 26 Jul 2023 14:57:51 GMT
ADD file:b7b8ba930a63f130e5b521d20879b60b1bcaf936b24117776d0b51c2b48d2a4d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-717.json 
# Wed, 26 Jul 2023 14:57:51 GMT
ADD file:b4ab85020f52e63c65078dbea52129cc08eeebd3d7249aa486338819331ac9f4 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-717 
# Wed, 26 Jul 2023 14:57:51 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-07-26T14:47:44" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-717"
# Wed, 26 Jul 2023 14:57:52 GMT
RUN rm -f '/etc/yum.repos.d/repo-ede3e.repo' '/etc/yum.repos.d/repo-0937a.repo'
# Wed, 26 Jul 2023 14:57:54 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 26 Jul 2023 14:57:55 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 01 Aug 2023 23:26:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 23:26:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 23:26:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 01 Aug 2023 23:26:52 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 01 Aug 2023 23:26:52 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 23:26:58 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 01 Aug 2023 23:26:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:09:27 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:684e2f1d925d1b205883b677fc893b5275192cfc90efd1fa51a90e1da256c4e0`  
		Last Modified: Tue, 01 Aug 2023 12:07:07 GMT  
		Size: 37.8 MB (37822945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2828cc08e260989d3b1f2221bf07fc5e520511e23bc5b395498e083c91b1f6b`  
		Last Modified: Tue, 01 Aug 2023 23:30:20 GMT  
		Size: 27.9 MB (27866608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdb9fd56d15e42a39a1752fcd4bdbda15b442e8445b93f76351a1974381f58f`  
		Last Modified: Tue, 01 Aug 2023 23:30:25 GMT  
		Size: 103.6 MB (103585323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fc94c7ca61a41ece3fc78b2b5a6a3e08a4e7c4ecf3bc47ad6aea2c43642254`  
		Last Modified: Tue, 01 Aug 2023 23:30:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666b62c8c366b068df448db840359d3b9a738c799ed3941658bba2bd878de950`  
		Last Modified: Mon, 14 Aug 2023 18:13:36 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u382-b05-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c6b3351f6c86f0f9eae7c13d7f70f127fecaa8b87222fed8762f64dbc717535a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167112378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf75ba772351a1e24c2d676322b7fc498ca2ffbb533ec91b61419ca254f4611`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 26 Jul 2023 14:58:04 GMT
ADD file:8d7c0f622c108d1e429ca4709a9dda0c55a5dd4cf1e5e2870676045dce7caeba in / 
# Wed, 26 Jul 2023 14:58:05 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 26 Jul 2023 14:58:05 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 26 Jul 2023 14:58:05 GMT
ADD multi:75455514cbe77ce7631a7c71aa7d7e34aff7f5078c6874650e6f91efe6e4c042 in /etc/yum.repos.d/ 
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 26 Jul 2023 14:58:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 26 Jul 2023 14:58:05 GMT
ENV container oci
# Wed, 26 Jul 2023 14:58:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 14:58:05 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 14:58:07 GMT
RUN rm -rf /var/log/*
# Wed, 26 Jul 2023 14:58:07 GMT
LABEL release=717
# Wed, 26 Jul 2023 14:58:07 GMT
ADD file:14e3121d95013deb0e4913aeb325fcf7bbf604080f2fc69e396fcf1a88bc8897 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-717.json 
# Wed, 26 Jul 2023 14:58:07 GMT
ADD file:ba1f369d1b07d713c5215a52333de8398076c4ecb9e2b6628520422b2da2b65a in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-717 
# Wed, 26 Jul 2023 14:58:07 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-07-26T14:47:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-717"
# Wed, 26 Jul 2023 14:58:08 GMT
RUN rm -f '/etc/yum.repos.d/repo-ede3e.repo' '/etc/yum.repos.d/repo-0937a.repo'
# Wed, 26 Jul 2023 14:58:09 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 26 Jul 2023 14:58:11 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 02 Aug 2023 00:03:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Aug 2023 00:03:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Aug 2023 00:03:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Aug 2023 00:03:52 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 02 Aug 2023 00:03:52 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 02 Aug 2023 00:03:58 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 02 Aug 2023 00:03:59 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:08:59 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:08:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9624f58f605cb9332696a166f1617f4e6d7fb1060bba9b0ea2aac67daac0dc73`  
		Last Modified: Tue, 01 Aug 2023 12:07:13 GMT  
		Size: 36.1 MB (36130176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78179c51ffbc35adfff015fcabffcfccefa9d8913285f7c8e6fecba7de53d28b`  
		Last Modified: Wed, 02 Aug 2023 00:06:38 GMT  
		Size: 28.3 MB (28290560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5688ca81b276adbd2a812a456de033bc83f843ecc521733ae9ab05132320619`  
		Last Modified: Wed, 02 Aug 2023 00:06:43 GMT  
		Size: 102.7 MB (102690771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b183de4bcd9c49a0370a6513628863bcae7f807fd975bf77e3127f386db5e8c`  
		Last Modified: Wed, 02 Aug 2023 00:06:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d6f69486c2caa7b81770eda666b890db5d343f0137e2aaa47da0e3f0cb8646`  
		Last Modified: Mon, 14 Aug 2023 18:11:17 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u382-b05-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:c2f9663e99c11a396cbbbbde920a492735b3944dc98f18c4b714997dd3a67f09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173757617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62d97fbc45644cfcd99409c0fc4215ceef8828b940c898c347047e5bdd4bd40`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 26 Jul 2023 14:57:48 GMT
ADD file:0c441962aa29a3affc408ed5089865900d38e4b549824783248a665571d42ebf in / 
# Wed, 26 Jul 2023 14:57:50 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 26 Jul 2023 14:57:50 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 26 Jul 2023 14:57:50 GMT
ADD multi:75455514cbe77ce7631a7c71aa7d7e34aff7f5078c6874650e6f91efe6e4c042 in /etc/yum.repos.d/ 
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL io.openshift.expose-services=""
# Wed, 26 Jul 2023 14:57:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 26 Jul 2023 14:57:50 GMT
ENV container oci
# Wed, 26 Jul 2023 14:57:50 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 14:57:50 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 14:57:51 GMT
RUN rm -rf /var/log/*
# Wed, 26 Jul 2023 14:57:51 GMT
LABEL release=717
# Wed, 26 Jul 2023 14:57:51 GMT
ADD file:a666bb3210193c7a955c3cec15b42d917e019faddf36ddc2545c81fc7f9ee928 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-717.json 
# Wed, 26 Jul 2023 14:57:52 GMT
ADD file:688393c03d435532347f62afef64019a0b40f85408be8040970afc31de6816e2 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-717 
# Wed, 26 Jul 2023 14:57:52 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-07-26T14:47:44" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-717"
# Wed, 26 Jul 2023 14:57:53 GMT
RUN rm -f '/etc/yum.repos.d/repo-ede3e.repo' '/etc/yum.repos.d/repo-0937a.repo'
# Wed, 26 Jul 2023 14:57:54 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 26 Jul 2023 14:57:56 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 01 Aug 2023 23:16:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 23:16:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Aug 2023 23:16:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 01 Aug 2023 23:18:28 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Tue, 01 Aug 2023 23:18:48 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 01 Aug 2023 23:19:18 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='0951398197b7bef39ab987b59c22852812ee2c2da6549953eed7fced4c08e13d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='509c923c308d1f4f28fd0068831a59250a05b8ca173ca92fb2be2e2e1f9ff3f9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='789ad24dc0d9618294e3ba564c9bfda9d3f3a218604350e0ce0381bbc8f28db3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 01 Aug 2023 23:19:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:09:14 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8458a49a58a9ceefce8feddf47e6c6d5ac3416b39eddb7e6a86407b47b94d1cb`  
		Last Modified: Tue, 01 Aug 2023 12:07:20 GMT  
		Size: 42.3 MB (42290376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a2713fd75507be3000cb44286c34e36d1b211a49c77956a228a83323a08e1d`  
		Last Modified: Tue, 01 Aug 2023 23:26:03 GMT  
		Size: 30.4 MB (30421820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d3113fec5f370d8a6a8b5d3c067a51b07f86ee3a9106376c721774a148eeac`  
		Last Modified: Tue, 01 Aug 2023 23:26:12 GMT  
		Size: 101.0 MB (101044549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2e727d48f267433859304dafa5496b9a96a95ed2944c99ab53d32264f47af5`  
		Last Modified: Tue, 01 Aug 2023 23:25:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9309bf10c63a94a0c8b7e273465d38ca2b0881dfc25eb653b6653f9cf89bff85`  
		Last Modified: Mon, 14 Aug 2023 18:12:27 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
