## `ibm-semeru-runtimes:open-23-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:2a5d0a6646756d3e126b6ecea638dd08780ed532a5f493740ce7681b89959266
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

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:6e62d159c305b9c2d0188ac8bd833c8d1414d1f5d84e78562de997cbff53eae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286830591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd0db7b3578bb852aa69941abb693d54f6283f4800860dd5f1bfd40efe1b4ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0437f4c210c7c75bf47e3693431227d6b4e37deccfe6cfabf734a403d429f68`  
		Last Modified: Mon, 04 Nov 2024 22:05:13 GMT  
		Size: 16.1 MB (16082611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba88c2a5d124f670b49bb83c01322fbdabac3eae1bbec79b15bc35e7dc0f0467`  
		Last Modified: Mon, 04 Nov 2024 22:05:18 GMT  
		Size: 236.5 MB (236532678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5aced5662dc510c4b912aea01a6dc0e19cfbcf7c2c61fba37e1846c89380599`  
		Last Modified: Mon, 04 Nov 2024 22:05:13 GMT  
		Size: 6.7 MB (6704242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7504eae7f24aede65eb6704fc2154ab2b79e489d170aca1f8bf34fdfc4e880c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3698171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f7c46a6cb0a0cd53e0363308b957ee1810f095654a58f77297030b7581b54a`

```dockerfile
```

-	Layers:
	-	`sha256:7d5b7ce5e3ac7c57d45c7cc1c106dc95e13588c2ce253985fbe4406b0ee7c2e5`  
		Last Modified: Mon, 04 Nov 2024 22:05:12 GMT  
		Size: 3.7 MB (3674126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c83fd8063b7fd5d27b45835793e78c41360991c94fe87459aa121db4555db749`  
		Last Modified: Mon, 04 Nov 2024 22:05:12 GMT  
		Size: 24.0 KB (24045 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:a7e86c77a00162c49f74d10c57c37a1e1aa86cc77d9729182b5fdc2f3c42cf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276557273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567343fd552126c7d0d7d233feeeb286e75e31228b0ca7d3ec6e20053a0fca7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c87aac1d4ce7ba28204a4f8c7ccbc4da254cdd092097b48a1bbda757f24ae4c`  
		Last Modified: Mon, 04 Nov 2024 22:06:02 GMT  
		Size: 15.9 MB (15945006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4707dcbc4bc961dee7d8782663e758bc154758646992459892fff2bda217f12a`  
		Last Modified: Mon, 04 Nov 2024 22:34:16 GMT  
		Size: 228.2 MB (228229263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f5bd80c667b65793716424e24aba15f791c86f2f2bdda395425e14a2e7f5c7`  
		Last Modified: Mon, 04 Nov 2024 22:34:11 GMT  
		Size: 6.4 MB (6409176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c22c12346dfe620b7df5bc544043284a1d5acf09913b0c11155ee544c1de1897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bc35aac62914eb49aa5cb9b29d33ffda8c687d0617c5016f056e0245fdfacd`

```dockerfile
```

-	Layers:
	-	`sha256:885fa8f8d40ce6bdbe8f688e686861891a4481aea533a603357feae287c6252d`  
		Last Modified: Mon, 04 Nov 2024 22:34:11 GMT  
		Size: 3.7 MB (3666815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3dcb2eb4bbfc6da68293964039bd005d4db485f81ea0a31a38fe0ec83bab07`  
		Last Modified: Mon, 04 Nov 2024 22:34:10 GMT  
		Size: 24.2 KB (24155 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:5d3c3e88e593281c42e0dbb6f91fab7f98cf64b615213724e085c50922c36646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294456739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5139d0f4a39c96789d00cd6d08a5411ff632e43b18a5549077d5f4c425bf8b83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c03062ba6cc89d48fbed8c001c307b5b41e0a5f776a5ecb43457bcbf48b0c0d`  
		Last Modified: Mon, 04 Nov 2024 22:05:24 GMT  
		Size: 17.3 MB (17256542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce751f8c5e856ee91a307fff84ef7dc983f44319a09bfcd4ce84ad343d87c5eb`  
		Last Modified: Mon, 04 Nov 2024 22:47:53 GMT  
		Size: 239.7 MB (239670485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f00b9db38288b7c99c45cff97c519ae4e7bf73bbfead6808b31b179f4ec263`  
		Last Modified: Mon, 04 Nov 2024 22:47:47 GMT  
		Size: 5.5 MB (5453206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a0a26a5243f5acc3c9cac48c10438c11ebe1efaf485c383829036980c0c39aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3702642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0633ff7f3ea92a3463cea64e9f03a53139a246a2867bb637ec4668509f0c70`

```dockerfile
```

-	Layers:
	-	`sha256:03f9f35947a314f9c973823a4fbf0bbbf1f94d8be7ba906376e4d76d72fda0cb`  
		Last Modified: Mon, 04 Nov 2024 22:47:47 GMT  
		Size: 3.7 MB (3678561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3283bb8b76433c4a2e510f56fa6099dc7c5ab8326a904b694878884a4d8f0742`  
		Last Modified: Mon, 04 Nov 2024 22:47:46 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:a29d2ce796c01726661a94211e5991d349513221d1b0a23361b0338839b92e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283597620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b220bba80f9b2f83ce6e0fbdc44c05469c4804c1fa251c831c8c65a2aa2c7b6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f6b14778eb4fed5cbb0bd80eea19d48526571f3b2dfa0196faf63f42fdb8c6c2`  
		Last Modified: Fri, 11 Oct 2024 04:41:53 GMT  
		Size: 26.4 MB (26365979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae76440d6755e318199681b6d987a4b8660d5945e0ea29db0a034c2ad4c00548`  
		Last Modified: Mon, 04 Nov 2024 22:07:59 GMT  
		Size: 15.8 MB (15773072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a01b7a2a6415fa41a16c25de87f0c61f20cb418936ad775d6208c7180c9dae`  
		Last Modified: Mon, 04 Nov 2024 22:45:10 GMT  
		Size: 234.6 MB (234626057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a70f67c83b8d3a81dc0a82ae49a60f43b600c653dc16762bdea39079229b9f2`  
		Last Modified: Mon, 04 Nov 2024 22:45:07 GMT  
		Size: 6.8 MB (6832512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3c40c9ec7d1c0d7e6601772beef630b059bcf52bbc55263c88c1fe83a9619f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3699591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b062c8640d179e12bd16492784e7525ada046d485a83c1c2dc790991bf6fead`

```dockerfile
```

-	Layers:
	-	`sha256:c10ada82262267c2789cb1a449ab5a314e9a4d3933f4bb3d2c38e22f1b5d0f36`  
		Last Modified: Mon, 04 Nov 2024 22:45:07 GMT  
		Size: 3.7 MB (3675547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6858eaacd5eccacbec13a8021d2093f879e34b3975bb393d2abe219e40d7b06f`  
		Last Modified: Mon, 04 Nov 2024 22:45:07 GMT  
		Size: 24.0 KB (24044 bytes)  
		MIME: application/vnd.in-toto+json
