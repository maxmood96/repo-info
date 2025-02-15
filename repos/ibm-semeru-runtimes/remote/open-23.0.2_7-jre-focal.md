## `ibm-semeru-runtimes:open-23.0.2_7-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:aaadad892430fc4e4518c3d9ad9cc0de7c14d79c8cae777ddec8a2ef8f639721
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `ibm-semeru-runtimes:open-23.0.2_7-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:1c740721c5ea75146dbc11fd11617e7b7c368c773042f20cefc9dd435f73639f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105001227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5864dcf885a82c0ee232073b88a839867beb4a4c2bea89f80c5b6aba03aa86f9`
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
# Thu, 13 Feb 2025 04:44:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Feb 2025 04:44:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_VERSION=jdk-23.0.2+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2fcef32e2bb56b232dbf90b470869ecfd737b2bc4954a8a92b690478af1a88c4';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d84a863e91920c2b924b74a8f40058ae6c53e031e15ccc47bcdda13d37645c99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e056f8d70387eae66994d57904ec02e47c5e6ba1fe0a655e0feafedcfd04ab60';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='b92f0bb3603ac86856c97e0d060b19b4efc21d9a349cc2cfe23654a4c332ce28';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25f2dc680e7ffc33313e10fa419e37f6af4e523251f5a32165e6fe8a4225039`  
		Last Modified: Sat, 15 Feb 2025 02:32:04 GMT  
		Size: 16.1 MB (16075901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4015e707d7241642308ab5f7a7b5bfd70277c994cba95d95bd504e82b5d0a873`  
		Last Modified: Sat, 15 Feb 2025 02:32:05 GMT  
		Size: 55.8 MB (55816492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183efeea84217d6428493a2eff5fa0e9adda104321cf301facf7162daeb8c54e`  
		Last Modified: Sat, 15 Feb 2025 02:32:04 GMT  
		Size: 5.6 MB (5597774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23.0.2_7-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a3a193fead395ed89f9b06588f2bcb5a9f493ee9c68e22b8c7c20ebf2f22e2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653c425dc071c3db5d123f183b74f3c581ac034eaeb1ec150fa5633e4a771d33`

```dockerfile
```

-	Layers:
	-	`sha256:8b576b3de26ac9d82c416b1878c4ba2ea283d3e9ca0ad374cea7b9b8cfedad74`  
		Last Modified: Fri, 14 Feb 2025 23:46:17 GMT  
		Size: 3.6 MB (3591554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc1d7aa3ede1042584a9e07db508f6d3106966669634fa019bb4d8101321d206`  
		Last Modified: Fri, 14 Feb 2025 23:46:17 GMT  
		Size: 24.1 KB (24108 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23.0.2_7-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:011120cb962d0cf12b88aa5528b7b18ecb34ef396960f3c30b2b45a85f7c4cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110369152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc7276f2db68a71d8e4c961207cf296984a371f36bfed2fd47e8f18bde1d82`
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
# Thu, 13 Feb 2025 04:44:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Feb 2025 04:44:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_VERSION=jdk-23.0.2+7_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2fcef32e2bb56b232dbf90b470869ecfd737b2bc4954a8a92b690478af1a88c4';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='d84a863e91920c2b924b74a8f40058ae6c53e031e15ccc47bcdda13d37645c99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e056f8d70387eae66994d57904ec02e47c5e6ba1fe0a655e0feafedcfd04ab60';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='b92f0bb3603ac86856c97e0d060b19b4efc21d9a349cc2cfe23654a4c332ce28';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.2%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_23.0.2_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 04:44:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.99/bin/apache-tomcat-9.0.99.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 13 Dec 2024 21:07:44 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55caf6c5ab5a2f4dd7778bf3241e397e7a5a65adbf72e89249f83424684d3d6b`  
		Last Modified: Sat, 15 Feb 2025 02:03:22 GMT  
		Size: 17.2 MB (17247743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13477a09d5f5ea1a3a3ad7082841c8eab258e8b9eda4597b65d9fe4fbaf8cf1`  
		Last Modified: Sat, 15 Feb 2025 02:49:27 GMT  
		Size: 56.8 MB (56802216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272738dc91d52b4478a637829ec0fdb2cfa24f210064cc7c7485699d4461df`  
		Last Modified: Sat, 15 Feb 2025 02:49:25 GMT  
		Size: 4.2 MB (4242687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23.0.2_7-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:33885424293c9c534e21c47520072c535d18c98ca8c5e6922a0d3f3fb4d5a22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c64e3ca4af7ea16e0ece3f25a6ac784dc44372afb1b9ffe4159094c6edc2f3`

```dockerfile
```

-	Layers:
	-	`sha256:53c89c74acdfadf7ff5494609fd317d9c22b3c8524c056c91de3b655724e52db`  
		Last Modified: Sat, 15 Feb 2025 05:46:05 GMT  
		Size: 3.6 MB (3593516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f5ba8bfa42098f931714b5e2a0c6a6659d66b031f039afdcc637eebca8a3d8`  
		Last Modified: Sat, 15 Feb 2025 05:46:06 GMT  
		Size: 24.1 KB (24144 bytes)  
		MIME: application/vnd.in-toto+json
