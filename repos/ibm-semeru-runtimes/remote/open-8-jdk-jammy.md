## `ibm-semeru-runtimes:open-8-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:f5d91be5074f4456217f0c6ad6a07b62da2da598d1c938406028b909a4c762cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `ibm-semeru-runtimes:open-8-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:74e4eeb15fba9f2f19f373a741461234a4a1af9370a4cbbc71dabddbcd94501f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163610490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7391224330796ef87c9525c1eca819fa09e587d98a861497b4140f67774ef999`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:21:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:21:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 01:34:52 GMT
ENV JAVA_VERSION=jdk8u362-b09_openj9-0.36.0
# Wed, 01 Mar 2023 01:34:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='502b13e9ff9dae3984633ef1560b642d9836b8a0e7f5d84baf2d4a438d375360';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_aarch64_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='783730b95fdcd0742393751b296c5b9d9d2e8317de85e4f027dbdc128df3e8c5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_ppc64le_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        amd64|x86_64)          ESUM='4c956f08cbe02d43a06536e9eae888925cc495a669bd024606389bec5ea6964a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_x64_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        s390x)          ESUM='b137500de20ff1a733e9c4ff28cb4ee585cd01f8cd9a50636fe0d22b86ba502e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_s390x_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 01 Mar 2023 01:34:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 01:34:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 01 Mar 2023 01:35:34 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:10ac4908093d4325f2c94b2c9a571fa1071a17a72dd9c21c1ffb2c86f68ca028`  
		Last Modified: Thu, 26 Jan 2023 08:46:26 GMT  
		Size: 30.4 MB (30429004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a2e3d5e01bb2e259616c0ff1606d8392779478b294aa443c0115968d9677e4`  
		Last Modified: Tue, 31 Jan 2023 18:36:29 GMT  
		Size: 12.1 MB (12082422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f2f6f2fb4fde2629eeb625528bcdd96936f33528d511012a390169d5dd4e24`  
		Last Modified: Wed, 01 Mar 2023 01:50:43 GMT  
		Size: 116.9 MB (116850954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c57d15557e0327f848403c149e2ae9d94c38498a83bf6c9cd9c9146a924052`  
		Last Modified: Wed, 01 Mar 2023 01:50:34 GMT  
		Size: 4.2 MB (4248110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:ddb5a11b8d7cc5944c146882f3b945f8a8e9ec1d44ac9f5db6b3602bae5a0dfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158790228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5943be00d97fc0a2b45799520443cfd660f77fea7744c9476c1cfeb8603cadc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:47:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:48:01 GMT
ADD file:cf91de9ab30abab112d58c0a7f3bbb35853a02b2e406c65c89430ff049573c47 in / 
# Wed, 01 Mar 2023 04:48:01 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:45:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:45:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:45:22 GMT
ENV JAVA_VERSION=jdk8u362-b09_openj9-0.36.0
# Thu, 02 Mar 2023 02:45:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='502b13e9ff9dae3984633ef1560b642d9836b8a0e7f5d84baf2d4a438d375360';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_aarch64_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='783730b95fdcd0742393751b296c5b9d9d2e8317de85e4f027dbdc128df3e8c5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_ppc64le_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        amd64|x86_64)          ESUM='4c956f08cbe02d43a06536e9eae888925cc495a669bd024606389bec5ea6964a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_x64_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        s390x)          ESUM='b137500de20ff1a733e9c4ff28cb4ee585cd01f8cd9a50636fe0d22b86ba502e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_s390x_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 02 Mar 2023 02:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:45:28 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 02 Mar 2023 02:46:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:986c4f6be3072d9528a459c780295bd053806536d2295a6de6aad327eaf19fad`  
		Last Modified: Wed, 01 Mar 2023 09:02:52 GMT  
		Size: 28.4 MB (28387922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd8756a0aa8766f884b553de90ddaa01cd4b1e4412a4ef3678e8197ab2f2153`  
		Last Modified: Thu, 02 Mar 2023 02:59:32 GMT  
		Size: 12.0 MB (12048288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37eb11a54c8ee24bec3a30fcfa6854708ad9231c7fd883e88c146c2eee3752e`  
		Last Modified: Thu, 02 Mar 2023 02:59:39 GMT  
		Size: 114.3 MB (114303582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fde094670ebb363901f93d0f553f961ac516ed28025fb81f05c73e2e5ad337b`  
		Last Modified: Thu, 02 Mar 2023 02:59:31 GMT  
		Size: 4.1 MB (4050436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:96b03159f055f5bdddb2150c7ddd43664f55cad66bd52b9fc21b737acd6d2ed9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161271511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f683c7c27a55f033770a2f69048b3e2d39e9ce7638a84f6b22ba8ed53eded492`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:10:39 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:41 GMT
ADD file:db14dc9a9d330115a6699be3c4a344f5fe366ec17e7d3649c4ecb2711605e52b in / 
# Wed, 01 Mar 2023 05:10:41 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:39:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:40:00 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:40:01 GMT
ENV JAVA_VERSION=jdk8u362-b09_openj9-0.36.0
# Thu, 02 Mar 2023 02:40:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='502b13e9ff9dae3984633ef1560b642d9836b8a0e7f5d84baf2d4a438d375360';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_aarch64_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='783730b95fdcd0742393751b296c5b9d9d2e8317de85e4f027dbdc128df3e8c5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_ppc64le_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        amd64|x86_64)          ESUM='4c956f08cbe02d43a06536e9eae888925cc495a669bd024606389bec5ea6964a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_x64_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        s390x)          ESUM='b137500de20ff1a733e9c4ff28cb4ee585cd01f8cd9a50636fe0d22b86ba502e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u362-b09_openj9-0.36.0/ibm-semeru-open-jdk_s390x_linux_8u362b09_openj9-0.36.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 02 Mar 2023 02:40:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:40:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 02 Mar 2023 02:40:46 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:905ef75a23211c85ea45c3aa7f7e77bc95a94ff8c250e03412ef8c50b5fb9f49`  
		Last Modified: Thu, 02 Mar 2023 02:23:13 GMT  
		Size: 28.6 MB (28647596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e3b14143abc6139bc75b388db80e25ba28725ecbcc60811eb5b95d1bff9f24`  
		Last Modified: Thu, 02 Mar 2023 02:57:11 GMT  
		Size: 12.1 MB (12133769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1177d30a226c932f1154f8242b167f4408f8fa4a250788d1dae73bafd170d6`  
		Last Modified: Thu, 02 Mar 2023 02:57:18 GMT  
		Size: 116.2 MB (116172558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6356af13235b8cf52587dc457d1f8e6d24c2624af913a809bfa309b3c2b5de1d`  
		Last Modified: Thu, 02 Mar 2023 02:57:10 GMT  
		Size: 4.3 MB (4317588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
