## `ibm-semeru-runtimes:open-8u442-b06-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:31b5ba190dad81feda539ec93f1d2fd7a1c329a9dcb7a091e1e4501d1f75c5dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `ibm-semeru-runtimes:open-8u442-b06-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:c983a74b208128a55578754877892319b7d436ec3cb202fed75488708f944a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164554287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b71ba18632675f8a5c8141b36ede65f4dce2c84270346c9af226c674641219c`
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
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='619dca885ed8e86ea5ce0c64c4242c4fba3846117304b88c7aa54363c148d2e7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='155ea4b99fedec6a38dfaf7825ecf7275f0a13f6a80f7169d6bff70ce72493b1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a6be6d9b7adf04d46448356e88128fe8c634215ff7816e023e7e94c98c35b763';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='f516bac072670a6bffb18ddf4cc6bfd4736dff830bfd545f27744409f3702dbc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:413d8d02325c5d74f2c5a0c74c4930f899863368bf3adf3e505b30e798e041e3`  
		Last Modified: Sat, 15 Feb 2025 03:13:29 GMT  
		Size: 16.1 MB (16075895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a30a5be39fb530cd2263a0f5734490e9cacc2f71311a19fbe473c9d85a326f1`  
		Last Modified: Sat, 15 Feb 2025 03:13:35 GMT  
		Size: 116.7 MB (116665615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c7500a14cf7bc95b1e830fe5ca573540d538475b4f09302a4589f56f523b32`  
		Last Modified: Sat, 15 Feb 2025 03:13:29 GMT  
		Size: 4.3 MB (4301717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u442-b06-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:65c67f0515756cf8d4e7accb981f158651b51fe52ad54b41d26a77e6aeef55bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff0ed156c33100fad1a3e37ee55c885c12daf086f4d2b920aa0a9e8b2b84c6e`

```dockerfile
```

-	Layers:
	-	`sha256:7e29c767ca041b689d7695c802aafbb39b1871b75b5d9eae57620a6351ff0421`  
		Last Modified: Fri, 14 Feb 2025 23:46:37 GMT  
		Size: 3.8 MB (3782512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8198dda60e91ffef7301805d9468a466cf0e8edfac661ddf0bc227445ca8f3`  
		Last Modified: Fri, 14 Feb 2025 23:46:37 GMT  
		Size: 24.0 KB (23954 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u442-b06-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:17fa6908dea760dd0f9c97c3390a19930ee542e921703b8492c7634964698527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170930906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff02ba741da86722b728d9527bab3c75731d07029ab25f63d6e39f870ef47d3`
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
ENV JAVA_VERSION=jdk8u442-b06_openj9-0.49.0
# Thu, 13 Feb 2025 04:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='619dca885ed8e86ea5ce0c64c4242c4fba3846117304b88c7aa54363c148d2e7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jdk_aarch64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='155ea4b99fedec6a38dfaf7825ecf7275f0a13f6a80f7169d6bff70ce72493b1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jdk_ppc64le_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='a6be6d9b7adf04d46448356e88128fe8c634215ff7816e023e7e94c98c35b763';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jdk_x64_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='f516bac072670a6bffb18ddf4cc6bfd4736dff830bfd545f27744409f3702dbc';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u442-b06_openj9-0.49.0/ibm-semeru-open-jdk_s390x_linux_8u442b06_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:617bf4af0c5351669394deb9fa554bfdb112c674acca1bafb86bce1e14da356c`  
		Last Modified: Sat, 15 Feb 2025 02:03:26 GMT  
		Size: 118.1 MB (118124470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08bc6c29a45ff77af23c9266e36801504aa04f57079fa9ac4df8237943bbfd`  
		Last Modified: Sat, 15 Feb 2025 02:03:22 GMT  
		Size: 3.5 MB (3482187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u442-b06-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:20ae976a376b14a344a67a6d82ff1d67ef2a2135d421e25a38b5298371acd095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cad6a7e2ffb12c5fde65474921775601bfc182e0b4c0bac52af9d36092e9880`

```dockerfile
```

-	Layers:
	-	`sha256:8fa4f1df7a26b1e22ce1ed84d9ac5f33f55f72894172dde0e27d64155084208d`  
		Last Modified: Sat, 15 Feb 2025 02:45:43 GMT  
		Size: 3.8 MB (3787120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f165e4da88cb1fbeb3e1c0c83bd3d66a614ccba838a5688994851a4b8406c8`  
		Last Modified: Sat, 15 Feb 2025 02:45:43 GMT  
		Size: 24.0 KB (23990 bytes)  
		MIME: application/vnd.in-toto+json
