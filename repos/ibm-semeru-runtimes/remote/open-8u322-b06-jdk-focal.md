## `ibm-semeru-runtimes:open-8u322-b06-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:2e3125b9d291ce862f95a0bd18c2c9e6e1c5fc5269f86a271a9a47e46b307e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ibm-semeru-runtimes:open-8u322-b06-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:ce62b82db29fb5c17a598be33b808306814c8828ca91d7aa27fa8a92528d5b4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165611277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b111fa2b364af3b8b473c7e47bccda083a2df9e69680148bf550bccdad871b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:04:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 02:04:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:35:01 GMT
ENV JAVA_VERSION=jdk8u322-b06_openj9-0.30.0
# Fri, 22 Apr 2022 02:35:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42adfae1e175fa3b524b5f30ef335eb5b1e3b90ed3f1813acc58a3077c171a48';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_aarch64_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ba9a831d9de82874a9187e010d5a400665b8758c3f23b067ef67348e30197bc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_ppc64le_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        amd64|x86_64)          ESUM='78b149add83696695e37cf4e1b9747112e63a2e8f128335b919f9a412fc17503';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_x64_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        s390x)          ESUM='90e453ea9ad4f8b74adf3d4354f22eb6e00253f8de2898b32a4bd6a090420068';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_s390x_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:35:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:35:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 22 Apr 2022 02:35:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b11e2aa9202b3c11a943dfa8adc2bef4462ab2165124b84051d10250faff2a0`  
		Last Modified: Fri, 22 Apr 2022 02:08:16 GMT  
		Size: 16.0 MB (16030117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49105c775df5b2557e0a50e0ce732acfaafce575e09a3968d298e4a86c1d99d9`  
		Last Modified: Fri, 22 Apr 2022 02:43:14 GMT  
		Size: 116.7 MB (116716399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f531c1da8c88c94d317b6c1467e9800b48bd2df0fae57937c0c97c1707be69`  
		Last Modified: Fri, 22 Apr 2022 02:43:05 GMT  
		Size: 4.3 MB (4298763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8u322-b06-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:a10e8c49824947da2329dc9fc5f28c9e7a1d09bfe4d24f07fa30f39bfee939d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161285833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d49be90338958cc5ab86f4300bd036b41c65e0db4adf32360df9cf683bbf317`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:59 GMT
ADD file:113ba5e7bc74d50e8d35449f8a62712359e2f00146e03eee822c28c8c6f59368 in / 
# Tue, 05 Apr 2022 22:41:00 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 23:19:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 00:31:39 GMT
ENV JAVA_VERSION=jdk8u322-b06_openj9-0.30.0
# Wed, 06 Apr 2022 00:31:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42adfae1e175fa3b524b5f30ef335eb5b1e3b90ed3f1813acc58a3077c171a48';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_aarch64_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ba9a831d9de82874a9187e010d5a400665b8758c3f23b067ef67348e30197bc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_ppc64le_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        amd64|x86_64)          ESUM='78b149add83696695e37cf4e1b9747112e63a2e8f128335b919f9a412fc17503';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_x64_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        s390x)          ESUM='90e453ea9ad4f8b74adf3d4354f22eb6e00253f8de2898b32a4bd6a090420068';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_s390x_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 00:31:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 00:31:49 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Apr 2022 00:32:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:185e8a4c100571f111d924b5d4399d89f163bf95d71ce2c6a33f656a66c52f0a`  
		Last Modified: Tue, 05 Apr 2022 13:15:01 GMT  
		Size: 27.2 MB (27169393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749a2a96ed3e9b4226fb4f45f4fa06a3f157ad7780fa6da936d865439a01ad33`  
		Last Modified: Tue, 05 Apr 2022 23:25:07 GMT  
		Size: 15.9 MB (15895491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980a4869f18dc3eb7d8974614abcf6ca17b14c21449f3c7c6c8eab246f4b0b50`  
		Last Modified: Wed, 06 Apr 2022 00:39:00 GMT  
		Size: 114.2 MB (114177024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a2899cf1c0dea2574f56f30351533e1f260a5e5e0c5882a6816a065ae3edbd`  
		Last Modified: Wed, 06 Apr 2022 00:38:50 GMT  
		Size: 4.0 MB (4043925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8u322-b06-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:2b353080bcf0afe1a0bbf6cb339f2ab49281ea85212a4d14d19626ed52568b8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170792751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad4d0aee3039c738cebcb766703af52a1431bc42818470190328a606e818d41`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:53:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:55:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:21:34 GMT
ENV JAVA_VERSION=jdk8u322-b06_openj9-0.30.0
# Wed, 06 Apr 2022 05:22:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42adfae1e175fa3b524b5f30ef335eb5b1e3b90ed3f1813acc58a3077c171a48';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_aarch64_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ba9a831d9de82874a9187e010d5a400665b8758c3f23b067ef67348e30197bc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_ppc64le_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        amd64|x86_64)          ESUM='78b149add83696695e37cf4e1b9747112e63a2e8f128335b919f9a412fc17503';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_x64_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        s390x)          ESUM='90e453ea9ad4f8b74adf3d4354f22eb6e00253f8de2898b32a4bd6a090420068';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_s390x_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 05:22:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 05:22:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Apr 2022 05:23:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51134a7a9e0d0b603ce41f6ef7aa0f9d1a77696cb80e63a1e73b539ff51023b0`  
		Last Modified: Wed, 06 Apr 2022 05:08:30 GMT  
		Size: 17.2 MB (17204248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef8e68e1bccfe292105494651ab11f423deb37ced1469b6b5e5a8797ceccf18`  
		Last Modified: Wed, 06 Apr 2022 05:40:46 GMT  
		Size: 116.8 MB (116817406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4979d02e2c14331db2408244cfa24bfc75abb21da988a3e840d4006cadb585fd`  
		Last Modified: Wed, 06 Apr 2022 05:40:33 GMT  
		Size: 3.5 MB (3479288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8u322-b06-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:353fbf967c9122e1c45c9627050abc05edb80e846d742a872466065974fd5f6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162538813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f95d8fc1ed05d88ac6432f166729bf53271395f08f6bcf02249cf90f6b7655a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:54:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 01:55:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:05:05 GMT
ENV JAVA_VERSION=jdk8u322-b06_openj9-0.30.0
# Fri, 22 Apr 2022 02:05:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='42adfae1e175fa3b524b5f30ef335eb5b1e3b90ed3f1813acc58a3077c171a48';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_aarch64_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ba9a831d9de82874a9187e010d5a400665b8758c3f23b067ef67348e30197bc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_ppc64le_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        amd64|x86_64)          ESUM='78b149add83696695e37cf4e1b9747112e63a2e8f128335b919f9a412fc17503';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_x64_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        s390x)          ESUM='90e453ea9ad4f8b74adf3d4354f22eb6e00253f8de2898b32a4bd6a090420068';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u322-b06_openj9-0.30.0/ibm-semeru-open-jdk_s390x_linux_8u322b06_openj9-0.30.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:05:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:05:29 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 22 Apr 2022 02:06:04 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ad99882b01b0ab3e7045a65b2c93f1319b8763364d776de22578aaade5be51`  
		Last Modified: Fri, 22 Apr 2022 02:02:24 GMT  
		Size: 15.7 MB (15738876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1450e6ca8e40c8d152b2003fba3c4a4f11c5c52d568d5740b4b23c1c26c187`  
		Last Modified: Fri, 22 Apr 2022 02:16:04 GMT  
		Size: 115.4 MB (115369669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c67f364d6e487e8a03b6acf5161f3e4d030a7cc7541ac0b2efec6da73fb160`  
		Last Modified: Fri, 22 Apr 2022 02:15:56 GMT  
		Size: 4.3 MB (4344550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
