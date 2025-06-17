## `ibm-semeru-runtimes:open-21-jre-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:1e729f74550a3f2092e7075e98400dce5c5ca99fb893468d51bd20cca21419c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibm-semeru-runtimes:open-21-jre-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:3364176962b55febe51926d9ae5b7fa55d5204491f5c764a6ba94a8c34067687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103251080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9016f3c6a9acd746be80213c598eac3cf18c94d83fec94bc0b92cd9d36a76c1e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk-21.0.7+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8a140dc3806d8e0ae23ca37cff6b4cf225eea45bc82b0749c05ad5f05b9cff36';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1c439bacc90f3a119edc3a7f313512b49b21d583a960cb318094974fe5006246';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c3e5287710e9a30a905e82cd0bb67a114cec08fc4a03f82798e76d22a1a7137e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='8c2ba94ac14dce46c68a7d46d600bee1685862299926a5462754a9dece5607cc';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75939cbec7cd5b3e9fe0e551664d4c64a44bc21150e3fc31c4140d04fa6f7fa4`  
		Last Modified: Tue, 17 Jun 2025 17:12:36 GMT  
		Size: 12.2 MB (12172111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd5daf8336ee731759f75a5c5865b89c52c065dda876deafd62c279f3949237`  
		Last Modified: Tue, 17 Jun 2025 17:12:40 GMT  
		Size: 56.4 MB (56428931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25712399fa02c4f56c5565ce68e73680f847cf2d150c08b50aaa421ea159be26`  
		Last Modified: Tue, 17 Jun 2025 17:12:35 GMT  
		Size: 5.1 MB (5117035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:85469d878580421340b49193cdeb8e3f3098ae764fc4a3a01b4cf45ef23f3d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3756237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8503dc8d360142f3e1d10b0d26f0c16e951d262ae0b119f15227f03ccccbf47a`

```dockerfile
```

-	Layers:
	-	`sha256:e89fc46dccea3417efa702ab39945a95417560a3d2758269341fc1b95f0dc849`  
		Last Modified: Tue, 17 Jun 2025 19:47:07 GMT  
		Size: 3.7 MB (3730969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f6d01a992bfea9055851a8e3c358314e95ea9bc7f01dedcc9a56657e8894417`  
		Last Modified: Tue, 17 Jun 2025 19:47:08 GMT  
		Size: 25.3 KB (25268 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:1c27186ddefbe19a21db7c07b0f4d559993afe8f8eb43c1f3f4d7fbae5a62662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97257823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be57f8137c01b2c31bb9e052f712ab0b50353704c5a13ffbf24d9409a02d1da3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk-21.0.7+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8a140dc3806d8e0ae23ca37cff6b4cf225eea45bc82b0749c05ad5f05b9cff36';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1c439bacc90f3a119edc3a7f313512b49b21d583a960cb318094974fe5006246';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c3e5287710e9a30a905e82cd0bb67a114cec08fc4a03f82798e76d22a1a7137e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='8c2ba94ac14dce46c68a7d46d600bee1685862299926a5462754a9dece5607cc';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbff14187feb7082a330fc6604f5d950114fba77a27a3564014bdeb0c0a7e399`  
		Last Modified: Tue, 17 Jun 2025 17:39:17 GMT  
		Size: 12.1 MB (12129302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9323a2d5a69f46ec3164a1bf82ccaf862d6b46b45c181ba640b79715ab1f7f`  
		Last Modified: Tue, 17 Jun 2025 17:55:25 GMT  
		Size: 52.9 MB (52850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973df58e7ca816d4e5aa6e8954313bd1f687fcc69806cef3144614498933bc80`  
		Last Modified: Tue, 17 Jun 2025 17:55:21 GMT  
		Size: 4.9 MB (4922939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6fa0f191edbffba83f1dbba8e9c76de4337ca85dc72426e136fc751f87c6ae25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9778d286cf88d464c6a4cd600cdcf03fd70c4b4ce1ec16e029d07cfb1c784ff`

```dockerfile
```

-	Layers:
	-	`sha256:8b5646f18cae35037dc2788f5c96df0ed819d7db9bad8ad72816b59e8226cd79`  
		Last Modified: Tue, 17 Jun 2025 19:47:13 GMT  
		Size: 3.7 MB (3724315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74cd6764ed2d74a453215e64788f19b44f4fdbb9bbbbe43935b4898fce2230e9`  
		Last Modified: Tue, 17 Jun 2025 19:47:13 GMT  
		Size: 25.4 KB (25379 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:a6a38d5bbdf28fae7d85c883707e8be84cdc669358fdc314a50de5719f7058b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109414125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8142bb96ad660906f7c990fb572e8eb24586e519a16f32f34993270c56e1bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk-21.0.7+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8a140dc3806d8e0ae23ca37cff6b4cf225eea45bc82b0749c05ad5f05b9cff36';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1c439bacc90f3a119edc3a7f313512b49b21d583a960cb318094974fe5006246';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c3e5287710e9a30a905e82cd0bb67a114cec08fc4a03f82798e76d22a1a7137e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='8c2ba94ac14dce46c68a7d46d600bee1685862299926a5462754a9dece5607cc';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c0a1fca7ea07c8c5a127826c7981b2bbb00fab8901f776e93777f6b6e7e19f`  
		Last Modified: Tue, 17 Jun 2025 17:55:19 GMT  
		Size: 12.9 MB (12893311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007fc60cbf48bcd7717123ae1538a088a752a00b0dce41384d3ceb8e3adb41a2`  
		Last Modified: Tue, 17 Jun 2025 18:15:32 GMT  
		Size: 58.1 MB (58105367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becd2204fa1bcb1c77d0373c4373ea5334bda20efb3f3b21b60cfbb752b75b60`  
		Last Modified: Tue, 17 Jun 2025 18:15:19 GMT  
		Size: 4.0 MB (3975090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:69a262fce512c6a7353e006ee8820147d4cd165cf8c984bb1626c16d5e67b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dcd593828e827f355479576ffeb837c8bf5f9f1b44d466aa7884f55b69628a`

```dockerfile
```

-	Layers:
	-	`sha256:0a09046abda5661437082edfb1ce2ee4e2ca8ef49817f7ff6db9f40761f91c48`  
		Last Modified: Tue, 17 Jun 2025 19:47:18 GMT  
		Size: 3.7 MB (3735596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89fd7cbff535bf0b73ecc18c994e655fcf59e0adaec949a462ee157223ccb142`  
		Last Modified: Tue, 17 Jun 2025 19:47:19 GMT  
		Size: 25.3 KB (25305 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21-jre-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:25ac3f47ec1a25c2bc4183f8eabcbff67495e71d9bb0d87c31c70257ef04882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101343932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a582176fc3d4a9ddae1535c7c1fdd64ec7d70bb4d93dc72c51904d64b1f7b163`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 30 May 2025 22:31:10 GMT
ARG RELEASE
# Fri, 30 May 2025 22:31:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:31:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:31:10 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:31:12 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Fri, 30 May 2025 22:31:12 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk-21.0.7+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8a140dc3806d8e0ae23ca37cff6b4cf225eea45bc82b0749c05ad5f05b9cff36';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1c439bacc90f3a119edc3a7f313512b49b21d583a960cb318094974fe5006246';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c3e5287710e9a30a905e82cd0bb67a114cec08fc4a03f82798e76d22a1a7137e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='8c2ba94ac14dce46c68a7d46d600bee1685862299926a5462754a9dece5607cc';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a592dff2b7023a1eb4d0588791417d7ab44efe41ce34295948fbb1653b7e87`  
		Last Modified: Tue, 17 Jun 2025 17:51:35 GMT  
		Size: 12.2 MB (12219457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a2ec063dae7d9583d3b298ff3cb7bd4822933ceef4a931fb4fe6a09e5e8d77`  
		Last Modified: Tue, 17 Jun 2025 18:29:05 GMT  
		Size: 55.8 MB (55761213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc1ce918958409fe3e744933ddfac1b82bab0a0d84e8adc24f93a7e6b72ccbf`  
		Last Modified: Tue, 17 Jun 2025 18:28:59 GMT  
		Size: 5.4 MB (5362662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:66697c391396789f1afe8ee1ec7e781f6510fd16bc81a8fb87212e8909a25c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f90b994fb8001f73dbf0f4fd846b8fd8d05dde2725ba58ffa08fb60022f2f`

```dockerfile
```

-	Layers:
	-	`sha256:1f7b774ca78ad4b7620e54761484831acac4e8ea6a358734f029de69680828ac`  
		Last Modified: Tue, 17 Jun 2025 19:47:23 GMT  
		Size: 3.7 MB (3733187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915a98ea22c55405e2f7d80a1fdc044d9e52a361e2a1a556fed0280fc487872d`  
		Last Modified: Tue, 17 Jun 2025 19:47:24 GMT  
		Size: 25.3 KB (25269 bytes)  
		MIME: application/vnd.in-toto+json
