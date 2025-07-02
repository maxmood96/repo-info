## `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:b2b16429bf6ba6ce97799981176c6e36c6c72ef362f0700aa3d81d1d52854338
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

### `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:08b310456115e5e124605585d4425f41b9428f64747fe378101e4350bed5eddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162731277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edce5eb24f91c75a00eccd26ddd8b05963a393e0bfa188cd4776766b5e1bfea`
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
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63440d5653d1f0918e4b4f6899330285ff039602665297c0e0720ac582f81864';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87fabcc61f08710c4e2f644b09632d29a48cb23e41c54a82bfd6e1d38b867229';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1049c6fc42d2d590981c4932a82e985b279c450eabc37bb13415b346a4ebad11';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='9392b88b4abc7843e903cbebd86854bebcefee262140c31f8b5ffd9e9443fe6d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:67fe2226de4ca37d749f8c4a546bab9536c23a8c184f109b7e2e66bda2c3c878`  
		Last Modified: Tue, 17 Jun 2025 17:12:32 GMT  
		Size: 12.2 MB (12172088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b9991051d784237285a3c7bca0371261c4560a1e6ec13aae26da639609e356`  
		Last Modified: Tue, 17 Jun 2025 22:31:43 GMT  
		Size: 116.7 MB (116749194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c888dc3ac369ad55bec5e441af8ecb4a99422e9d032ab1c4c338ee787eb1fb`  
		Last Modified: Tue, 17 Jun 2025 17:12:34 GMT  
		Size: 4.3 MB (4276992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ca95b447b62fd54d08b0a0f28c24451e824b900206fa1f078ff8d0181a395f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d19c61eaa17b7b8e47ccea1036a7098b775daecea9e6dede95fd3772aca0c43`

```dockerfile
```

-	Layers:
	-	`sha256:63d3cb5d7c1d9380efa36497aa1d1117022d865c67069a4957f26fe35693f44c`  
		Last Modified: Tue, 17 Jun 2025 19:47:42 GMT  
		Size: 3.9 MB (3922562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba79ad61b19949d5954d62674e80291fdc033efbe7e157b58fea9cc9e33334d0`  
		Last Modified: Tue, 17 Jun 2025 19:47:42 GMT  
		Size: 25.2 KB (25249 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:6171a1af560e6401e030e0c3420b3d81ff063aae3bf6c08ae33ad0716a6b1a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160159653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f487fd5080a3290b0544d1a8b22b51628e8d5882664e0df03b305dce9ee47c3`
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
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63440d5653d1f0918e4b4f6899330285ff039602665297c0e0720ac582f81864';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87fabcc61f08710c4e2f644b09632d29a48cb23e41c54a82bfd6e1d38b867229';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1049c6fc42d2d590981c4932a82e985b279c450eabc37bb13415b346a4ebad11';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='9392b88b4abc7843e903cbebd86854bebcefee262140c31f8b5ffd9e9443fe6d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:b04e58dffe948bbee7e0d61bf419b92b671604ec8bfe856114ea48d33a4b42d6`  
		Last Modified: Tue, 17 Jun 2025 22:32:23 GMT  
		Size: 116.6 MB (116631989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d7869a1a282cc50b456f5bd7a68b602e0b481b5d08425dfbe70e222dee3ea9`  
		Last Modified: Tue, 17 Jun 2025 17:39:16 GMT  
		Size: 4.0 MB (4042781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:0e1f6d14513867f1e9b72a8b981ff555e3f54f64a397811bfcfd9d6321af56df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fee42f349cb5f576393d7ad78c77ac8694411c251d78c0129b55b1274c78f04`

```dockerfile
```

-	Layers:
	-	`sha256:9faf52f5951286a6da79e570250d9ad8d4af35932f49df8a957d0f5653e074a8`  
		Last Modified: Tue, 17 Jun 2025 19:47:48 GMT  
		Size: 3.9 MB (3922368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0fd19a8054be797872e5800593c8d30d5530dbdb39c6bee834e43808259959`  
		Last Modified: Tue, 17 Jun 2025 19:47:49 GMT  
		Size: 25.4 KB (25359 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:fba37e89270cf4116fecd6b945f2d238fe677b7d54f9d03f16f4165523da489e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169081269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca8864141eb3e799effa79885d38b42f601bf28aa033eecaab3aa6ac5e62f71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Jun 2025 14:26:50 GMT
ARG RELEASE
# Tue, 17 Jun 2025 14:26:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 17 Jun 2025 14:26:50 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Tue, 17 Jun 2025 14:26:50 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63440d5653d1f0918e4b4f6899330285ff039602665297c0e0720ac582f81864';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87fabcc61f08710c4e2f644b09632d29a48cb23e41c54a82bfd6e1d38b867229';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1049c6fc42d2d590981c4932a82e985b279c450eabc37bb13415b346a4ebad11';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='9392b88b4abc7843e903cbebd86854bebcefee262140c31f8b5ffd9e9443fe6d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eadc2c3c98e81c215197904badede29a92518c461aab0c7b9d0848370fef917`  
		Last Modified: Wed, 02 Jul 2025 03:32:25 GMT  
		Size: 12.9 MB (12893371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3811409e6f2123ce046e601f8d88c8cc6828fe583eee3af495a3ff0b00a62`  
		Last Modified: Wed, 02 Jul 2025 03:32:40 GMT  
		Size: 118.2 MB (118222465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbde343e6f961a566cfb97c84b2bd8a6baef56304e80764a3a89d61edfe98f5`  
		Last Modified: Wed, 02 Jul 2025 03:32:25 GMT  
		Size: 3.5 MB (3522812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:fe1b38e299999a9f42e1406fc73f6e96d728b6214b4a4ec42f51d099ac091dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a188794d178492f9b1fdff2d4b38a101410541966c201669cc4a8c26990ac01`

```dockerfile
```

-	Layers:
	-	`sha256:0f0c0895563a79b482254c6ca52a3c238f7a91e58589c5b8f971dc19129767fc`  
		Last Modified: Wed, 02 Jul 2025 04:46:07 GMT  
		Size: 3.9 MB (3927361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b764a502b2e52592ef69198bfd2ce2e875bea5a7cda323322f9de781732e7fd1`  
		Last Modified: Wed, 02 Jul 2025 04:46:07 GMT  
		Size: 25.3 KB (25284 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:69d4b7f501d6182379bbd3686f3feef993d88e38a3fbd36cb2510f29269e3da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161105051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b1775c0933f6745a926c8a3d14ed9ff56be3ef97afc7be45f9243f5782576c`
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
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63440d5653d1f0918e4b4f6899330285ff039602665297c0e0720ac582f81864';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87fabcc61f08710c4e2f644b09632d29a48cb23e41c54a82bfd6e1d38b867229';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1049c6fc42d2d590981c4932a82e985b279c450eabc37bb13415b346a4ebad11';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='9392b88b4abc7843e903cbebd86854bebcefee262140c31f8b5ffd9e9443fe6d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
		Last Modified: Tue, 17 Jun 2025 21:00:33 GMT  
		Size: 12.2 MB (12219457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a48ab9df35823e7c63800cfcfa36f03fb02305a56360f24958403a7a1b13095`  
		Last Modified: Wed, 18 Jun 2025 12:37:07 GMT  
		Size: 116.6 MB (116564856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7965d59c19b74422232587a5346e190d44d994aa1e32de2e897902d3a42618fb`  
		Last Modified: Tue, 17 Jun 2025 18:19:08 GMT  
		Size: 4.3 MB (4320138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u452-b09-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:0fdebb96e7452ead56033085ac035f2fa5c325eb5c2b7c3f62b57802a3f985ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044145a812342c102d44dabec153c873505aff1a7ac1d24b27517eba0cb3e994`

```dockerfile
```

-	Layers:
	-	`sha256:26e0ba51a8ff95293f1e51a5558af0377440a1b59d1b226d7a4504389454d249`  
		Last Modified: Tue, 17 Jun 2025 19:47:59 GMT  
		Size: 3.9 MB (3924780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795931eb4c59dad308f885fe6e79417a11d7f9fc76cefd0a1bc50490ea81cabd`  
		Last Modified: Tue, 17 Jun 2025 19:48:00 GMT  
		Size: 25.2 KB (25249 bytes)  
		MIME: application/vnd.in-toto+json
