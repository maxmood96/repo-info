## `ibm-semeru-runtimes:open-22.0.2_9-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:09f6896e375b1f9b36e40261defb7fe63fcfe7ccb79a60a7a46f0c48977ac15b
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

### `ibm-semeru-runtimes:open-22.0.2_9-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:72cc9a42fd8e1e8ccfdc2ebabb3f922321b61947b433dd80f57a21497b1ea4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104132111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8c01b722394088f966a6da8318fc8453642ee6159441b1998ae25534731589`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79de3ae29e9407d13c0a2e8717425ad11c076db9390c983c50467fc0c8e10e11';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='94b0a0dcf87eda1bc739c827bdd69710569f816d9fad83698e14658d9da9402a';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='cb5fe1e7761c7dd689cfb11ce20017456b174562e64670896d5d00faf4825da0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='bc6b0af0d378fd1ee52ccfc4d8767e276abeb7a1d0e4a59b785114ae914dc504';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82545a671372b621d80566a3e2b60e8e667229d573fa5af5e58113579fc386d7`  
		Last Modified: Sat, 17 Aug 2024 02:05:01 GMT  
		Size: 16.1 MB (16061036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ac331c1208cf9546297664100c75ab80829206f51f5ae3eb42cf1f31d42d0`  
		Last Modified: Sat, 17 Aug 2024 02:05:01 GMT  
		Size: 55.3 MB (55324758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c9e0a0efff365f7729804cb63b7a800eeb711e1534c7ffb161a2a310ac5c78`  
		Last Modified: Sat, 17 Aug 2024 02:05:01 GMT  
		Size: 5.2 MB (5234548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:b5ceb3f168c08e2b38ff30e65dd557bbece9d2701433c3d05fa48b56b8fd80fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1680e22ef572f23bbc8aa0b363eb8f9128153ddd802a78cf58b98eeacbdbf7e4`

```dockerfile
```

-	Layers:
	-	`sha256:5576b3a4eaf16aef79e9d4e187d7006b2d97b0fbf94f5e6ff080e2c267632617`  
		Last Modified: Sat, 17 Aug 2024 02:05:00 GMT  
		Size: 3.5 MB (3463693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7400dc36fa805e2ac3028a5673f51d4d5f0d84cf92b8a676103f5a438c3b5e88`  
		Last Modified: Sat, 17 Aug 2024 02:05:00 GMT  
		Size: 23.7 KB (23718 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:28bf158cd5dbeef46fa2aa1c5379a9679ae0277a6e30d673ff2b7f8ad369cebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98549987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4776ecdc22638690e6ac664d00eb0390c8fb1bca5cd69e441f2449246765fff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79de3ae29e9407d13c0a2e8717425ad11c076db9390c983c50467fc0c8e10e11';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='94b0a0dcf87eda1bc739c827bdd69710569f816d9fad83698e14658d9da9402a';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='cb5fe1e7761c7dd689cfb11ce20017456b174562e64670896d5d00faf4825da0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='bc6b0af0d378fd1ee52ccfc4d8767e276abeb7a1d0e4a59b785114ae914dc504';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32447b8d1d57938895b10ad9b2309236208473c6fb3255b4549476e77fb29e2`  
		Last Modified: Mon, 12 Aug 2024 17:59:36 GMT  
		Size: 15.9 MB (15924034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20da5ea6102d1be677af9aa7e4113cc13a00591136a804e1a5aada831b23bd66`  
		Last Modified: Sat, 17 Aug 2024 02:49:17 GMT  
		Size: 51.7 MB (51691583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd0555ca904e5b75b34813453ed318a3b8fcf96f80e6b51d8971b27967421cd`  
		Last Modified: Sat, 17 Aug 2024 02:49:15 GMT  
		Size: 5.0 MB (4960153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7eb3baa63bfef38957a79ad7336e9734f803064881eada0f51c8380e6fd87a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b203abb8738d48ece34ca0d0d1d318b0596d3523e6764d20de91038cbc2f88a4`

```dockerfile
```

-	Layers:
	-	`sha256:e6bcff871945c3a5034b0c5a45b7dbcca07590859b7986691450589a2198c574`  
		Last Modified: Sat, 17 Aug 2024 02:49:15 GMT  
		Size: 3.5 MB (3463939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:180507dc933bc39f7f1d516d0e334621f8c98e36824383a52562e2143ab387ec`  
		Last Modified: Sat, 17 Aug 2024 02:49:15 GMT  
		Size: 24.0 KB (23995 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:c3926aed4edd65c1e535432ca084eb1dfd2f27453fa0bd9fa29ccf71791fb238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110275038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb5787be658dcad71572a29bddc256db83125b22ed2afc6b7eeda1655fb924f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79de3ae29e9407d13c0a2e8717425ad11c076db9390c983c50467fc0c8e10e11';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='94b0a0dcf87eda1bc739c827bdd69710569f816d9fad83698e14658d9da9402a';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='cb5fe1e7761c7dd689cfb11ce20017456b174562e64670896d5d00faf4825da0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='bc6b0af0d378fd1ee52ccfc4d8767e276abeb7a1d0e4a59b785114ae914dc504';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695549a4136bb16b902bceb966443542642f9c9131abb21acd5bd8417bdb51c7`  
		Last Modified: Mon, 12 Aug 2024 18:01:30 GMT  
		Size: 17.2 MB (17242215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca11348481e2ca9b88f3ec5d1b82763c42eefc3d8e0fcf809d15f6ff015465d1`  
		Last Modified: Sat, 17 Aug 2024 01:36:10 GMT  
		Size: 56.9 MB (56938712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625afc6a69539d8103829f593bd461b338ba6e3ac3e9c2946e492d58df4950b`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 4.0 MB (4016971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:cdd8d3372556f36aed2a612a0f30ff0126c10a7fcfd1f8345527cba82fb82c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba32cf8febe5b192d31592b6121075f76e537e69126a0126ac7e0a26b9d2da9e`

```dockerfile
```

-	Layers:
	-	`sha256:02509d73e4150873bf33f0f46417f96cb8d8365adec695f9f8df6c30868f601d`  
		Last Modified: Sat, 17 Aug 2024 01:36:08 GMT  
		Size: 3.5 MB (3468128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a745e4dd82bdbb7253e0df44ad56c11e2e52d5d7ad4439583777fd1322f65426`  
		Last Modified: Sat, 17 Aug 2024 01:36:07 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:05003a9ced3507c0968f5149175dc68175337107541f4dddb5079ad3d68ad054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102136012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe274851fd9aafe46064f9716b6cd24e9a794b94b8e4e3712a46ffc92ff305e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='79de3ae29e9407d13c0a2e8717425ad11c076db9390c983c50467fc0c8e10e11';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='94b0a0dcf87eda1bc739c827bdd69710569f816d9fad83698e14658d9da9402a';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='cb5fe1e7761c7dd689cfb11ce20017456b174562e64670896d5d00faf4825da0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='bc6b0af0d378fd1ee52ccfc4d8767e276abeb7a1d0e4a59b785114ae914dc504';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b93975e5d2fc73ed41c077a1d77fbf02d2aa8bdc632d27ffbfa396e568a20ab`  
		Last Modified: Sat, 17 Aug 2024 02:02:42 GMT  
		Size: 15.8 MB (15753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b719cc6a9e4e29a545d0e384c4f0a34c2917d2cdd87991b9ed794dd2600714dd`  
		Last Modified: Sat, 17 Aug 2024 02:29:36 GMT  
		Size: 54.7 MB (54656860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853bd2b93f08f5f5d1b487fe1a29a96b452524bc7c38718d3a66a6f66f18db8`  
		Last Modified: Sat, 17 Aug 2024 02:29:36 GMT  
		Size: 5.4 MB (5358295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:54b9aeee2e36d4ec0c0db0125ede82711c9fb64008ad0dbcb845abdf58792eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff58ba10a9cc144cf9282c0d75e05d9fcfc8d4f6afd5d4fe315239fdbbf5bf05`

```dockerfile
```

-	Layers:
	-	`sha256:6cead50f1049a476a29db0716a826c61031a52c0c91f3b37b194bd6bf8b95ff7`  
		Last Modified: Sat, 17 Aug 2024 02:29:36 GMT  
		Size: 3.5 MB (3464019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79da09b4596d553272675b9a063b6f01641a702ce16a18c93f9416d61b2e6977`  
		Last Modified: Sat, 17 Aug 2024 02:29:35 GMT  
		Size: 23.7 KB (23717 bytes)  
		MIME: application/vnd.in-toto+json
