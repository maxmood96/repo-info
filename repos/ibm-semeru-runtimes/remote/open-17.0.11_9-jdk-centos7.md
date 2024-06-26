## `ibm-semeru-runtimes:open-17.0.11_9-jdk-centos7`

```console
$ docker pull ibm-semeru-runtimes@sha256:3fb4fce472dc62ae00d585f8cb3825d0b2436114914386048b22e65bd5b1db37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `ibm-semeru-runtimes:open-17.0.11_9-jdk-centos7` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:5c38253a476851f6dae1962406bc9ef1f22d59d10962be03b7fcdf9546aa569e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314012767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9daec347d405be8fb18d619178e9ed5809fb641e037d92ecef9cb420db27b7b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e33b5825b93b75b274c7fa3be33539683a25d76b7bbac51c6b24b66aee621222';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='61bf38e9005c286d55cc403eac3061bf9ebcb54af2f0475cde8261efe4effbec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='af07d5b5d8a980826a1edd8954b868361709c1a11ef3402b28fa246c55c4e415';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='eb2ade1453801b330a06abb32e4ecac13ccc7c03029fa5bbf9604b9e1a5c9a5c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bceb3830a3818579e969d1ddaa109e4a6b11a3658797590a6d82c0e9f610ea`  
		Last Modified: Tue, 25 Jun 2024 22:58:04 GMT  
		Size: 14.6 MB (14642701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2886663007058f2791eb565472d147d6c7ae05f585e70fbd6e89a616e537866f`  
		Last Modified: Tue, 25 Jun 2024 22:58:07 GMT  
		Size: 217.3 MB (217260613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa15c326640770e53d7590e767dee8b0987cd4747f74e0540b0572030988583`  
		Last Modified: Tue, 25 Jun 2024 22:58:04 GMT  
		Size: 6.0 MB (6012296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.11_9-jdk-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d903618b2a0fd2cd7410a74769f0856de366b717b6c0e3a6825fee6d8e72a01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5184149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de579d64e228bc6a819d2a551911c42ceb26daf95a1ef431e2bcdbf919715b`

```dockerfile
```

-	Layers:
	-	`sha256:92b0d05a1fbbd9acf673a0102248f468da9d58ef8a65abdbcecc8ad35939c83e`  
		Last Modified: Tue, 25 Jun 2024 22:58:04 GMT  
		Size: 5.2 MB (5161006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a741c61478d1ada52acce9c5667621714d9e885172aa96b0a3ad04b332b6bbfd`  
		Last Modified: Tue, 25 Jun 2024 22:58:04 GMT  
		Size: 23.1 KB (23143 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.11_9-jdk-centos7` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:47634e0b571f3e35f88b230213115e10d5088c9edd1985a60533537445f2c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336791826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea8d4d4016dca87e9090ed0e63bb6741c69cb0f54d01821f59e07dd9b5bb0bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 14 Feb 2022 19:39:36 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Mon, 14 Feb 2022 19:39:37 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Mon, 14 Feb 2022 19:39:38 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e33b5825b93b75b274c7fa3be33539683a25d76b7bbac51c6b24b66aee621222';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='61bf38e9005c286d55cc403eac3061bf9ebcb54af2f0475cde8261efe4effbec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='af07d5b5d8a980826a1edd8954b868361709c1a11ef3402b28fa246c55c4e415';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='eb2ade1453801b330a06abb32e4ecac13ccc7c03029fa5bbf9604b9e1a5c9a5c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d618285429c2bf62e795cf4222667658ce0dc51d7560e205d38445dbbd56a0e8`  
		Last Modified: Tue, 25 Jun 2024 23:04:41 GMT  
		Size: 14.2 MB (14167828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a378bc511d824364d1843b7fb66be2a6b22561260d740b576147a29c3e1b1d`  
		Last Modified: Tue, 25 Jun 2024 23:19:22 GMT  
		Size: 208.5 MB (208456584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3bbd9abfdfaede2455176cbe54b8283fbf3bc2f7fe5460b9b7071d2bb9b35`  
		Last Modified: Tue, 25 Jun 2024 23:19:16 GMT  
		Size: 5.8 MB (5792469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.11_9-jdk-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:00d5e821680c3b1e523e92bf6981e4606762db16bc7a0618f62b64140c42c706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6366016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01774b6353a7cf195ed5e25b5eb7fe4c4aa282068e171bdec74c9a057237488`

```dockerfile
```

-	Layers:
	-	`sha256:1255280cf18b78fd6876f1562a0bb3cfb71c2e926b05710cfe413885638d5a30`  
		Last Modified: Tue, 25 Jun 2024 23:19:16 GMT  
		Size: 6.3 MB (6342596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df48ee80c0152119401a5bc86ee5ba2c678b6f42cf1d080e8366e7a2edbb9000`  
		Last Modified: Tue, 25 Jun 2024 23:19:15 GMT  
		Size: 23.4 KB (23420 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.11_9-jdk-centos7` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:8e85124a7ee8d574cbe3aeb3ecc2a9fa59f6b563610bba63150f137645f4af8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319873148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305402f0fbe6a3bf1b8963ee3f8b5f6445c54df8a14696cfb4402ec2df1d39fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-17.0.11+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e33b5825b93b75b274c7fa3be33539683a25d76b7bbac51c6b24b66aee621222';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_aarch64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='61bf38e9005c286d55cc403eac3061bf9ebcb54af2f0475cde8261efe4effbec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_x64_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='af07d5b5d8a980826a1edd8954b868361709c1a11ef3402b28fa246c55c4e415';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='eb2ade1453801b330a06abb32e4ecac13ccc7c03029fa5bbf9604b9e1a5c9a5c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.11%2B9_openj9-0.44.0/ibm-semeru-open-jdk_s390x_linux_17.0.11_9_openj9-0.44.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991a61d82e75ea7116e8f0546b27c479f7364c780fcd07cd3ccc01bebb7f5dbb`  
		Last Modified: Tue, 25 Jun 2024 23:06:48 GMT  
		Size: 14.5 MB (14546231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbc8ad4ad3890de70cccb4e2a487b92e10cbb46adf7221eccb0b99b3bbed135`  
		Last Modified: Tue, 25 Jun 2024 23:25:59 GMT  
		Size: 219.9 MB (219936686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e517e2e8450389609a217e9f768d6a11c1703806d348f95f9dcb1b43aefef2f`  
		Last Modified: Tue, 25 Jun 2024 23:25:53 GMT  
		Size: 4.9 MB (4873771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.11_9-jdk-centos7` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8e45e51af2a96a7e9d5c2d7f1e9c0cc2f59ea9eb1aa893eade07a0afa09d7e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ebd8fd8db7f001cac9a635543592979d5ab54a14e004d863ff98769b0cc38a`

```dockerfile
```

-	Layers:
	-	`sha256:e9289630d1c34c014870c50d5c1b74e2d3ecccda357c97241410fcdca6ef9a4a`  
		Last Modified: Tue, 25 Jun 2024 23:25:53 GMT  
		Size: 5.2 MB (5167975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e729fba6dfe66dbcffb9016baf169fd213e51a0087620efebabab2dec83918`  
		Last Modified: Tue, 25 Jun 2024 23:25:53 GMT  
		Size: 23.2 KB (23173 bytes)  
		MIME: application/vnd.in-toto+json
