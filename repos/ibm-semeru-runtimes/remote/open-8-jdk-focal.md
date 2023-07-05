## `ibm-semeru-runtimes:open-8-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:dd0fb1b3a027bed96c2f7d6abc92849161696b66894086319fabc4e2846103c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ibm-semeru-runtimes:open-8-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:e86d4aa732fbe52678b9c6bac765744adc2102fdc721cad021d9b161bfc9429e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165773134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c167d0ba85e32c4efac68e0619f11440cccd1318715edfda6642c1991967e8`
-	Default Command: `["\/bin\/bash"]`

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
# Tue, 04 Jul 2023 19:17:30 GMT
ENV JAVA_VERSION=jdk8u372-b07_openj9-0.38.0
# Tue, 04 Jul 2023 19:17:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7b9225c7a968242210effe261ee12f01c03259ab8403147b43ac35697fa5c2f4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_aarch64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='23924d0e8f50a87f2e51c77ee0c19364e97cb68df47baf9352c100387feff172';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_ppc64le_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='dd1edee0a50ac6766268feeaac2a4e95eca83d30d1e0dea7c1e199dc9048f1c0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_x64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='c0b354b2f4823cb542843214a153c93e2ee5ac09893fd0a594074766f68d70d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_s390x_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 04 Jul 2023 19:17:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 19:17:38 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jul 2023 19:18:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
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
	-	`sha256:f7497fa8a4705f7749457b4356ebaea3632bed19c97bb046136c7a3b9de8f07f`  
		Last Modified: Tue, 04 Jul 2023 19:32:34 GMT  
		Size: 116.9 MB (116933507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04946943979f21fd6455c876efa111ae0ace8e20e39ff8d7b3f73b1fbe84e2e0`  
		Last Modified: Tue, 04 Jul 2023 19:32:25 GMT  
		Size: 4.2 MB (4202082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:680ccb409f01fb7fe0b97f4f68880cfde4e04862403d9d491647143fadd39e2c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162238157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ae52f1e683c48a81b1c56e838c7c9d03921ffc4240e60e623d1aee958d4faa`
-	Default Command: `["\/bin\/bash"]`

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
# Tue, 04 Jul 2023 16:00:05 GMT
ENV JAVA_VERSION=jdk8u372-b07_openj9-0.38.0
# Tue, 04 Jul 2023 16:00:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7b9225c7a968242210effe261ee12f01c03259ab8403147b43ac35697fa5c2f4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_aarch64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='23924d0e8f50a87f2e51c77ee0c19364e97cb68df47baf9352c100387feff172';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_ppc64le_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='dd1edee0a50ac6766268feeaac2a4e95eca83d30d1e0dea7c1e199dc9048f1c0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_x64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='c0b354b2f4823cb542843214a153c93e2ee5ac09893fd0a594074766f68d70d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_s390x_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 04 Jul 2023 16:00:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 16:00:12 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jul 2023 16:00:46 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
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
	-	`sha256:ea7efcb04fe4ccfa43b51b9e82ae751e6fc24a80d17636b492fe51252e30aa91`  
		Last Modified: Tue, 04 Jul 2023 16:13:27 GMT  
		Size: 115.1 MB (115099052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536e2c5b6e3e5070d3f81df7713c4ca55b60c8fd63ebe24c405a318d961f44f2`  
		Last Modified: Tue, 04 Jul 2023 16:13:20 GMT  
		Size: 4.0 MB (4015092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:f8a81418bc971046237ac2158c06664a89393697c117ad7483b5fd23f1a95cce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171139541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74957019d84077d43c02a1fa54de3ab016dd86e5ab8798a102cb92632e52462`
-	Default Command: `["\/bin\/bash"]`

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
# Wed, 05 Jul 2023 01:35:32 GMT
ENV JAVA_VERSION=jdk8u372-b07_openj9-0.38.0
# Wed, 05 Jul 2023 01:36:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7b9225c7a968242210effe261ee12f01c03259ab8403147b43ac35697fa5c2f4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_aarch64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='23924d0e8f50a87f2e51c77ee0c19364e97cb68df47baf9352c100387feff172';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_ppc64le_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='dd1edee0a50ac6766268feeaac2a4e95eca83d30d1e0dea7c1e199dc9048f1c0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_x64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='c0b354b2f4823cb542843214a153c93e2ee5ac09893fd0a594074766f68d70d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_s390x_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Jul 2023 01:36:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 01:36:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Jul 2023 01:36:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
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
	-	`sha256:830a4350fc52fce75da5819033c6c894f2c3845aaeb49fefcd8a93ee701d1e5c`  
		Last Modified: Wed, 05 Jul 2023 01:46:01 GMT  
		Size: 117.0 MB (117047515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0028cbb1a1534314d3462321dac9d3d8af086b8bc390c7560b4ad88f113f4fa2`  
		Last Modified: Wed, 05 Jul 2023 01:45:46 GMT  
		Size: 3.6 MB (3550543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:010741e0f1b52a0a2abc878683592e4bc52c5a4e9be4207d624ff391b51f7aba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163302590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935e0e2d119199fabc48286e8b5755b810903f8128afd3d53fe61cf357f33f59`
-	Default Command: `["\/bin\/bash"]`

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
# Tue, 04 Jul 2023 16:30:56 GMT
ENV JAVA_VERSION=jdk8u372-b07_openj9-0.38.0
# Tue, 04 Jul 2023 16:31:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7b9225c7a968242210effe261ee12f01c03259ab8403147b43ac35697fa5c2f4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_aarch64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='23924d0e8f50a87f2e51c77ee0c19364e97cb68df47baf9352c100387feff172';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_ppc64le_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='dd1edee0a50ac6766268feeaac2a4e95eca83d30d1e0dea7c1e199dc9048f1c0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_x64_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='c0b354b2f4823cb542843214a153c93e2ee5ac09893fd0a594074766f68d70d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u372-b07_openj9-0.38.0/ibm-semeru-open-jdk_s390x_linux_8u372b07_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 04 Jul 2023 16:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 16:31:07 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jul 2023 16:31:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
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
	-	`sha256:c66a59a60dc6eb9741250f9a34816bd4d8a3a2f1ca671d99714a0b1a32d90259`  
		Last Modified: Tue, 04 Jul 2023 16:46:35 GMT  
		Size: 116.3 MB (116252317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58274078d3fa61e2d439a5b7d0805475ce37c22004d0174b8977786f0baae1db`  
		Last Modified: Tue, 04 Jul 2023 16:46:27 GMT  
		Size: 4.3 MB (4282477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
