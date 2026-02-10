## `ibm-semeru-runtimes:open-11-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:c63557f32bc0ec4274d2363e482b1ac525e64b7041d1853feeb97b2c38fbdc7f
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

### `ibm-semeru-runtimes:open-11-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:fe1fa024ac8a3b56a8663ca7fa90b11ec815bee061a4cb33b495e33900c6484b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268355391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80acb22484c79f9d7d7e49edfa56eb028722d1ad274d94fd17796ae9d372dce9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:05:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:05:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:05:49 GMT
ENV JAVA_VERSION=jdk-11.0.30+7_openj9-0.57.0
# Mon, 09 Feb 2026 20:05:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b8a9013f033798fb33861df42e411fe557400ae6b3dac69d98f1c1347432d202';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d38ff59f1becb2f8b31ba0c5ff94bcf23dcbfefc80b079533b398d4e93bb3bae';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1306ed223443830c1e4c0d393c67c6eb5a32de33cddd684057290ce38916fea3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='ca807012f56589826bfe40947efde8c58f3652d97c07bd7aa9aec9d89c982e73';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:05:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:05:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:07:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 20:07:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a79d7926fd666f1e8377ce53ba81261ce979afb12410b6ab2ccc5f7656d482b`  
		Last Modified: Mon, 09 Feb 2026 20:07:22 GMT  
		Size: 12.2 MB (12171497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfde65c3225175724e514b0dbcd03acea590fd0294b0e2deb5a26dac8df68695`  
		Last Modified: Mon, 09 Feb 2026 20:07:30 GMT  
		Size: 221.3 MB (221273494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8d648726318d564ee2656952e30ee4c0a12fc0cccc0f9155a573fd2334a75`  
		Last Modified: Mon, 09 Feb 2026 20:07:21 GMT  
		Size: 5.4 MB (5373733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e1ce3689f36dd2e0c6950bc9fa59ff47650bc8fe756864b6bd1ea5c94fed8d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a35b68489669764346f5aad7a95bccd560cf897860c2dffb782e65df7901ac4`

```dockerfile
```

-	Layers:
	-	`sha256:52de562c76d3354751f7592e0c8da7c6c34764588e293c3b81d629dba43e87b2`  
		Last Modified: Mon, 09 Feb 2026 20:07:21 GMT  
		Size: 3.8 MB (3833211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a72e4d9d65e0e0aa04bde3a3e91a61a48f063fc20358327e1265c83ed25f458a`  
		Last Modified: Mon, 09 Feb 2026 20:07:21 GMT  
		Size: 25.6 KB (25555 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:e23fe0a159353b37ddf297cf6391a978319dac8e42cf2e3184934bc485256485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262879252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f3e6bc6e1448e3d7c638fbbe6052c356d2ca654a5ab9bb40c350862875077b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:06:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:06:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:06:11 GMT
ENV JAVA_VERSION=jdk-11.0.30+7_openj9-0.57.0
# Mon, 09 Feb 2026 20:06:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b8a9013f033798fb33861df42e411fe557400ae6b3dac69d98f1c1347432d202';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d38ff59f1becb2f8b31ba0c5ff94bcf23dcbfefc80b079533b398d4e93bb3bae';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1306ed223443830c1e4c0d393c67c6eb5a32de33cddd684057290ce38916fea3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='ca807012f56589826bfe40947efde8c58f3652d97c07bd7aa9aec9d89c982e73';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:06:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:06:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:07:26 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 20:07:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645f37defb4e06e98a6c467e00e58a4e1b3aa9fadecac004e4100450ab9f2c6`  
		Last Modified: Mon, 09 Feb 2026 20:07:46 GMT  
		Size: 12.1 MB (12136224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d2e376c8d779071a37f2f175a4eb542467d82eab425d0f516cf4e722d9ff0b`  
		Last Modified: Mon, 09 Feb 2026 20:07:50 GMT  
		Size: 218.1 MB (218134040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86594dd4b6229cb4d8a870ad959ce54bae9dfb09219b788973694ef426ed7c85`  
		Last Modified: Mon, 09 Feb 2026 20:07:45 GMT  
		Size: 5.2 MB (5225491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3b697b6586dfb1da033eaea040095a999e6d07b75cbe073914df793e5464dbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3856624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae17e4465569987e9e6229359be3f009ba19041ac7785bacae3480a372bac2e2`

```dockerfile
```

-	Layers:
	-	`sha256:6c0f25bc8c17af962a92b3326ae87c16871281088e25155ef08e7711dfc45632`  
		Last Modified: Mon, 09 Feb 2026 20:07:45 GMT  
		Size: 3.8 MB (3830960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c891729020a3e68a406f34ae1cff0fdbbc8bd924a2c2cf71b16faec321b31d6`  
		Last Modified: Mon, 09 Feb 2026 20:07:45 GMT  
		Size: 25.7 KB (25664 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:a4e607ffcb361706983e399b6f034ca24339bcba4e597074ad4c8bcaefa2f0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276816018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b06078057fc55d843da7373f10374f8f57d7fef0f101363be44ee56854e12e8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:34:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:34:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:34:04 GMT
ENV JAVA_VERSION=jdk-11.0.30+7_openj9-0.57.0
# Mon, 09 Feb 2026 20:36:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b8a9013f033798fb33861df42e411fe557400ae6b3dac69d98f1c1347432d202';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d38ff59f1becb2f8b31ba0c5ff94bcf23dcbfefc80b079533b398d4e93bb3bae';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1306ed223443830c1e4c0d393c67c6eb5a32de33cddd684057290ce38916fea3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='ca807012f56589826bfe40947efde8c58f3652d97c07bd7aa9aec9d89c982e73';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:36:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:36:30 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:37:35 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 20:37:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6692474891d89964ff7faedfdbaeec6433f0215c07a6a09d29d0ceb9f8395fb2`  
		Last Modified: Mon, 09 Feb 2026 20:38:19 GMT  
		Size: 12.9 MB (12893726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2819f2385d2f649616a7ac8182a7ce5c0ecadee0d9bce6446881536acd5bb2`  
		Last Modified: Mon, 09 Feb 2026 20:38:25 GMT  
		Size: 225.0 MB (224974820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e05bddd0ce112df83401d8bf186c011b5872b62af2ea04183f69c49358bd1b`  
		Last Modified: Mon, 09 Feb 2026 20:38:19 GMT  
		Size: 4.5 MB (4500510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:039ff7a0934016c92a3cd490547ea916d99f91d8a96b09ffa0e4d890a8b9f414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3863429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afb613930c52700ff784af1f26c2373145f5222eb4943da075966f1a2ee3e7d`

```dockerfile
```

-	Layers:
	-	`sha256:88f3adad20055fb14a048c32ff750d64f89027e802ec10197e06e525e38c7845`  
		Last Modified: Mon, 09 Feb 2026 20:38:19 GMT  
		Size: 3.8 MB (3837838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35ce83abe295986f856258ae5c3221ecea1bc02e7cbffac7979d62d73156a21b`  
		Last Modified: Mon, 09 Feb 2026 20:38:19 GMT  
		Size: 25.6 KB (25591 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-11-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:ea1ff672519dfc76773b418e033082165dbe8e12e95f53aa94c7fc082c679359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264879359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358969e3da4830c5ccc2f1c67a7397c702b77b96d81df3a131056bb2a4d78628`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:07:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:07:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:07:33 GMT
ENV JAVA_VERSION=jdk-11.0.30+7_openj9-0.57.0
# Tue, 10 Feb 2026 01:19:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b8a9013f033798fb33861df42e411fe557400ae6b3dac69d98f1c1347432d202';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d38ff59f1becb2f8b31ba0c5ff94bcf23dcbfefc80b079533b398d4e93bb3bae';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='1306ed223443830c1e4c0d393c67c6eb5a32de33cddd684057290ce38916fea3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='ca807012f56589826bfe40947efde8c58f3652d97c07bd7aa9aec9d89c982e73';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30%2B7_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30_7_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 10 Feb 2026 01:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 01:19:38 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 10 Feb 2026 01:20:43 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 10 Feb 2026 01:20:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cf131361351ec38b54320166821c427e6cdca9c3706dd28daccb4e229961c4`  
		Last Modified: Mon, 09 Feb 2026 20:12:40 GMT  
		Size: 12.2 MB (12220166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bbc1acadfe0e429e398c9eed6900427b411e7f8d9270dd808ca281e94eb1e6`  
		Last Modified: Tue, 10 Feb 2026 01:21:16 GMT  
		Size: 219.0 MB (219005191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2db259c7bbaccd5306e07e5561c03f47b8b3269d5bd669dfb0b8d5bce95aa4f`  
		Last Modified: Tue, 10 Feb 2026 01:21:12 GMT  
		Size: 5.7 MB (5650864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-11-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:42c14d20cff2e9a9628074f0cc5c993b099a2beff7e82dd85ab7aad853d648d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240a40807cf87288bfb46d3890386b05226cca7a1b63cd9994c0c885db18fb2e`

```dockerfile
```

-	Layers:
	-	`sha256:49e80dda2bf0ab3ebde30b5d12d4f34654bcbfd0df54e1b359089f2699ef3beb`  
		Last Modified: Tue, 10 Feb 2026 01:21:12 GMT  
		Size: 3.8 MB (3834803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b360cb4e9e93c28d1366d89feb43162d05cc90500ccf20f62b32ecb3a517ade`  
		Last Modified: Tue, 10 Feb 2026 01:21:12 GMT  
		Size: 25.6 KB (25554 bytes)  
		MIME: application/vnd.in-toto+json
