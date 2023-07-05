## `ibm-semeru-runtimes:open-20-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:c5cc3614f7f5e1e12a1ce4d93aa56fbab0be81673bb79b1a8395d5959ca7c41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ibm-semeru-runtimes:open-20-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:531af25149c93c152365323c2089ded0b74409dd09cfd1d02443d3a4d05942fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269165046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641e3ae658718d1b76dc97b30b840895cc3ad7f6a852859af6875cfac995a9bf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 09:59:08 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:59:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:59:08 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:59:10 GMT
ADD file:12f97b7b044d0d1166dd59408c67f5610a764127aa8a01bc57db23bee48911af in / 
# Wed, 28 Jun 2023 09:59:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 19:17:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 19:17:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 19:28:07 GMT
ENV JAVA_VERSION=jdk-20.0.1+9_openj9-0.39.0
# Tue, 04 Jul 2023 19:28:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='803ebb8ddf06e5408b0f26020e42b7d0b65bd8a82f62d2b633c49323fe46b441';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_aarch64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        amd64|x86_64)          ESUM='aef46e2a06b8671369783c85a473aefd586fffb720abf654f45e4940b2c81df2';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_x64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='62aa89c2c8921e143f30e3d951cdc58c6af894f713dea2340778b691ea9de3ab';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_ppc64le_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        s390x)          ESUM='3b496071093249d9a6d3e750181c316cd333dfe3d61dc340013362761e98f821';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_s390x_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 04 Jul 2023 19:28:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 19:28:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jul 2023 19:28:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 04 Jul 2023 19:28:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0fb668748fc8bb961f4580895692ae741be788857ac2e8220adc2265ffb38e10`  
		Last Modified: Wed, 28 Jun 2023 18:43:28 GMT  
		Size: 28.6 MB (28580012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d88f120128b937df427a0eaedb1e7567b8c1fae920b7bda63bc2e0e1363bc7`  
		Last Modified: Tue, 04 Jul 2023 19:32:27 GMT  
		Size: 16.1 MB (16057533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62802e856a8c800963d93891756c94d15044e3ab5ed57e9e3e8690305b0523c`  
		Last Modified: Tue, 04 Jul 2023 19:36:18 GMT  
		Size: 218.5 MB (218476303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fb53c5725398264ab6af90e3976ded34e4fc49ca3cf2d03ddab3225f8f5aa0`  
		Last Modified: Tue, 04 Jul 2023 19:36:04 GMT  
		Size: 6.1 MB (6051198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-20-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:9e7ac7a24db9376f8f41b4293ed0a824a28c66eb82091f07d65e1d91d2da5366
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262994195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67347fb0521be156e40b2041bd590987c1ebb631cfdc70b7216c6ca5ea3cc0f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 09:54:46 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:54:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:54:46 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 09:54:48 GMT
ADD file:a6db9f7789e57b7119f68e4e4ec9ec5aab8c3c8bd53fd932f3c59c54b1c20a26 in / 
# Wed, 28 Jun 2023 09:54:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:59:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 16:00:05 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:09:25 GMT
ENV JAVA_VERSION=jdk-20.0.1+9_openj9-0.39.0
# Tue, 04 Jul 2023 16:09:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='803ebb8ddf06e5408b0f26020e42b7d0b65bd8a82f62d2b633c49323fe46b441';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_aarch64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        amd64|x86_64)          ESUM='aef46e2a06b8671369783c85a473aefd586fffb720abf654f45e4940b2c81df2';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_x64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='62aa89c2c8921e143f30e3d951cdc58c6af894f713dea2340778b691ea9de3ab';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_ppc64le_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        s390x)          ESUM='3b496071093249d9a6d3e750181c316cd333dfe3d61dc340013362761e98f821';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_s390x_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 04 Jul 2023 16:09:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 16:09:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jul 2023 16:10:11 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 04 Jul 2023 16:10:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e77eb131c5c9032ce8e6e512f601714ce7ba48e296f5b7a5191703bdcbc904d`  
		Last Modified: Tue, 04 Jul 2023 04:05:23 GMT  
		Size: 27.2 MB (27198330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b09734daedc0304878798a71791219640fa2ef7b562635c4ca5be781b33a7f`  
		Last Modified: Tue, 04 Jul 2023 16:13:21 GMT  
		Size: 15.9 MB (15925683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2d8df1e5275ebd6e6ee70978b9b4e79f9a2e4a6f37a83d809b7ba94ab20af2`  
		Last Modified: Tue, 04 Jul 2023 16:16:48 GMT  
		Size: 214.1 MB (214096326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d19fb063f8509334107d91567cbd5802056a5e16fef1077bda39c93ceb7817`  
		Last Modified: Tue, 04 Jul 2023 16:16:37 GMT  
		Size: 5.8 MB (5773856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-20-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:f80268384026ebcf4f8280c9e1a049762ddf49de55ebab0de62d68767d34a5b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275948789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051f068fdc99c0d226ac9ffa5a1f9810f900ef0d225d5da095888fe369ba7086`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 10:04:43 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:04:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:04:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:04:46 GMT
ADD file:df651ead0b69eb261098e765354dbdf5ffca51275c037d8881fedcaa1c91c36d in / 
# Wed, 28 Jun 2023 10:04:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:34:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Jul 2023 01:35:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:42:39 GMT
ENV JAVA_VERSION=jdk-20.0.1+9_openj9-0.39.0
# Wed, 05 Jul 2023 01:43:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='803ebb8ddf06e5408b0f26020e42b7d0b65bd8a82f62d2b633c49323fe46b441';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_aarch64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        amd64|x86_64)          ESUM='aef46e2a06b8671369783c85a473aefd586fffb720abf654f45e4940b2c81df2';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_x64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='62aa89c2c8921e143f30e3d951cdc58c6af894f713dea2340778b691ea9de3ab';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_ppc64le_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        s390x)          ESUM='3b496071093249d9a6d3e750181c316cd333dfe3d61dc340013362761e98f821';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_s390x_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jul 2023 01:43:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 01:43:08 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jul 2023 01:43:47 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Jul 2023 01:43:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e95615eadb7a0d90a47ca15a5c0693371494902f54d8d78a50d53e89e7a20de`  
		Last Modified: Tue, 04 Jul 2023 04:40:49 GMT  
		Size: 33.3 MB (33308759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f03d8ba34db8491f122cbcdef5a82c067f29a6968d5b43a3b214b10fa5e715`  
		Last Modified: Wed, 05 Jul 2023 01:45:49 GMT  
		Size: 17.2 MB (17232724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d422977342e83750c1a2d20232be36868d9996350b771f6d202e4304f7391584`  
		Last Modified: Wed, 05 Jul 2023 01:49:11 GMT  
		Size: 220.4 MB (220378812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b007ccc9d3774c0322a73490d9252f5ee1fed8ba1cf305504351dd309d4e2d`  
		Last Modified: Wed, 05 Jul 2023 01:48:47 GMT  
		Size: 5.0 MB (5028494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-20-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:b4e3536cd1de15fdc974afeccdc65afe5d5b4e2e3d7d0db965833d8db3d8f9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265117241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc2303af601d85a4938c0b17b133ba2239961531aab30fed60cac3ecd31ea65`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 10:01:13 GMT
ARG RELEASE
# Wed, 28 Jun 2023 10:01:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 10:01:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 10:01:14 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 28 Jun 2023 10:01:15 GMT
ADD file:777fd71e798b91bf768b21e1ca4403f388db9936ef55ef68b4b019cb167fa707 in / 
# Wed, 28 Jun 2023 10:01:15 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:30:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jul 2023 16:30:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:41:55 GMT
ENV JAVA_VERSION=jdk-20.0.1+9_openj9-0.39.0
# Tue, 04 Jul 2023 16:42:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='803ebb8ddf06e5408b0f26020e42b7d0b65bd8a82f62d2b633c49323fe46b441';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_aarch64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        amd64|x86_64)          ESUM='aef46e2a06b8671369783c85a473aefd586fffb720abf654f45e4940b2c81df2';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_x64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='62aa89c2c8921e143f30e3d951cdc58c6af894f713dea2340778b691ea9de3ab';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_ppc64le_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        s390x)          ESUM='3b496071093249d9a6d3e750181c316cd333dfe3d61dc340013362761e98f821';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jdk_s390x_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 04 Jul 2023 16:42:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 16:42:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jul 2023 16:42:43 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 04 Jul 2023 16:42:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5ebe8481b30a6d3b710b0efdec29843cca805811e3be1a4e375761725c40e5a`  
		Last Modified: Tue, 04 Jul 2023 13:07:41 GMT  
		Size: 27.0 MB (27013645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3461070d67e6bed4ebdf68c9d0c7a7474d2ade2a95d5ad8c42b27ad6188e582`  
		Last Modified: Tue, 04 Jul 2023 16:46:29 GMT  
		Size: 15.8 MB (15754151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae2a1c882ffbed40c0152fce195766c5628982de15158889ce80c8d6ea7203f`  
		Last Modified: Tue, 04 Jul 2023 16:49:43 GMT  
		Size: 216.2 MB (216188540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7878ec02d3af87f6ccaef42e14492f995b77a8ed0718c735f46d88f309faf2f7`  
		Last Modified: Tue, 04 Jul 2023 16:49:29 GMT  
		Size: 6.2 MB (6160905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
