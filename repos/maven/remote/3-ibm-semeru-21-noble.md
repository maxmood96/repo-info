## `maven:3-ibm-semeru-21-noble`

```console
$ docker pull maven@sha256:be6a2dec1f3cc6981d85793890fedacba4d5b4e2f06251a0ab1fe9b6d771dbca
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

### `maven:3-ibm-semeru-21-noble` - linux; amd64

```console
$ docker pull maven@sha256:ccee104e801d77479bf0fadbb94578eacaf7a82146aae8d06c1cdb1606b2dd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320586305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a808ffa79d21354e6f266590c7dbb55b50c26fd25314332d09f7c825c1752438`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:56:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:56:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:56:47 GMT
ENV JAVA_VERSION=jdk-21.0.10+7.1_openj9-0.57.0
# Tue, 07 Apr 2026 01:56:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fbd5af08d6abb7ac8a9707982f6759d33245e0b8b05d7ddd593cd45c0cb98e90';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_21.0.10.1.tar.gz';          ;;        amd64|x86_64)          ESUM='df501befcb3f6b7f47c3557d9887197d78f013beb57b0d56494176b54ad80c19';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_21.0.10.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c60264d4b7dbd0ad94207ed85f4c71a5263ecb7c5bb6329da120194847d44611';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.10.1.tar.gz';          ;;        s390x)          ESUM='50d3a0a8d251a1826af4532a7b97874b58231b749bc44a29a61736ae1df47e69';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_21.0.10.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 01:56:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:56:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 01:58:05 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 05:06:55 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:06:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:06:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:06:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:06:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:06:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:06:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:06:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:06:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:06:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:06:55 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:06:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:06:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:06:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:06:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd90ba65b026a56b727d38f53b8a77bb62a26b3f13cafa1b1a521e6b49bfc20a`  
		Last Modified: Tue, 07 Apr 2026 01:58:26 GMT  
		Size: 12.8 MB (12805572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258760ceea33575f64310328ab311093174779632e2fab53e1c254eb7011a1f8`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 239.8 MB (239832214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba27e9dbf82b0f495839a877114aafe8ebf389d7e31989d12c32f68a92de5cf`  
		Last Modified: Tue, 07 Apr 2026 01:58:27 GMT  
		Size: 6.3 MB (6333543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5753d67d1c8d147d2296f6181937f09b406b012cdc64c42064bbe113381faf46`  
		Last Modified: Tue, 07 Apr 2026 05:07:11 GMT  
		Size: 22.6 MB (22569292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2adf30197ce99bf91a25ae19da515f066b7365f08d1d43311c42c8dfc1aee39`  
		Last Modified: Tue, 07 Apr 2026 05:07:11 GMT  
		Size: 9.3 MB (9311190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581579dd0a9544b056e36fc831359f83ce8fd89978b284e5d452ff75b5d1a1f9`  
		Last Modified: Tue, 07 Apr 2026 05:07:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ba166932b4c95483ad33ba56610ce6602bbb440338b852c453fb85a675fc56`  
		Last Modified: Tue, 07 Apr 2026 05:07:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:eb597a19df0f24be06bcef263ba275ffeb728af9bccf4df7113d8f6e529a3ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4809517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea03df24d445cc639d477e44d6464d4b18b54415fd70e78289738eaab7e39e84`

```dockerfile
```

-	Layers:
	-	`sha256:d30374414d50dc3c381b3e8eba899f85a7e93046b489eb6f8d783178b2d737d3`  
		Last Modified: Tue, 07 Apr 2026 05:07:10 GMT  
		Size: 4.8 MB (4790457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835361a636ff789a102148788e3bceb83b1c46950c9bd7f6fb1b54011b6fad14`  
		Last Modified: Tue, 07 Apr 2026 05:07:10 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-21-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c62de2d30c2423bc4f1373bf7578f10182238a5f5b1e21b2f2d7764f6254defc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.8 MB (315801232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb1be6d034abfbffc6fd8ddc7b1fe5437b7ce55bbcee4328c7a5c63bab8cdbc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:00:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:00:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:01 GMT
ENV JAVA_VERSION=jdk-21.0.10+7.1_openj9-0.57.0
# Tue, 07 Apr 2026 02:00:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fbd5af08d6abb7ac8a9707982f6759d33245e0b8b05d7ddd593cd45c0cb98e90';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_21.0.10.1.tar.gz';          ;;        amd64|x86_64)          ESUM='df501befcb3f6b7f47c3557d9887197d78f013beb57b0d56494176b54ad80c19';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_21.0.10.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c60264d4b7dbd0ad94207ed85f4c71a5263ecb7c5bb6329da120194847d44611';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.10.1.tar.gz';          ;;        s390x)          ESUM='50d3a0a8d251a1826af4532a7b97874b58231b749bc44a29a61736ae1df47e69';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_21.0.10.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 02:00:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:00:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 02:01:19 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 05:13:01 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:13:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:13:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:13:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:13:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:13:01 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:13:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:13:02 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:13:02 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:13:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:13:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3fc540bb5bfa9f0cd9aa5424b05cbddd7b5a10b93e12b0c18ccb76945161ad`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 12.8 MB (12837848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63837a93efd091b3c087f366c8938bf1a899e3eddaa2d4f7c296d72a62061f4f`  
		Last Modified: Tue, 07 Apr 2026 02:01:45 GMT  
		Size: 236.1 MB (236057840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993a7ee64b240cc0a02d3d4b7a11f125642d66d22c5e0fc672bed8a02a02f4f6`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 6.1 MB (6082296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0dc695a029c946ec2c550f8c747ad3726c1e892868cf23391f60312ae6bf2c`  
		Last Modified: Tue, 07 Apr 2026 05:13:17 GMT  
		Size: 22.6 MB (22636964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31b54ada39a6c3720b3cdd2dd8ea64714fc95d2f89a7d35de0ff85f568efd6`  
		Last Modified: Tue, 07 Apr 2026 05:13:17 GMT  
		Size: 9.3 MB (9311173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873dedd04321586c7de93a2c37c4353f6466ceb970749ac189ea58d509d8e9c8`  
		Last Modified: Tue, 07 Apr 2026 05:13:17 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b8baa726af69d9c2f7aaf2816c1c24b8c5cf2a2abc4aba4384fbbcde954155`  
		Last Modified: Tue, 07 Apr 2026 05:13:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:b7d367aba83d68c6d887a00063eeaa4e540d53c3a1eaccabf4ad130272fdeaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4814256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d92188a901e39ac2cebe8763d57d9eb8382a4d8b6149c73c941f42119ebdfa`

```dockerfile
```

-	Layers:
	-	`sha256:da088f875bdc2dd2077fab8549fe1b90b3fea6e89405d51681ec44a45ed59a02`  
		Last Modified: Tue, 07 Apr 2026 05:13:17 GMT  
		Size: 4.8 MB (4795063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbaed9a4b6c46b22421b86c7c9f8c7b37d5600288fc7862a38dfd945dc16d39`  
		Last Modified: Tue, 07 Apr 2026 05:13:16 GMT  
		Size: 19.2 KB (19193 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-21-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:c833fcee22318e22737a197f139e864638599067bef43b9266ed67c940f5bf7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (332984775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a4228e3395cc6e6bd7faa63477944375bf9ef3b91edbebd65839ce5d63b41b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:45:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:45:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:45:44 GMT
ENV JAVA_VERSION=jdk-21.0.10+7.1_openj9-0.57.0
# Wed, 18 Mar 2026 00:55:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fbd5af08d6abb7ac8a9707982f6759d33245e0b8b05d7ddd593cd45c0cb98e90';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_21.0.10.1.tar.gz';          ;;        amd64|x86_64)          ESUM='df501befcb3f6b7f47c3557d9887197d78f013beb57b0d56494176b54ad80c19';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_21.0.10.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c60264d4b7dbd0ad94207ed85f4c71a5263ecb7c5bb6329da120194847d44611';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.10.1.tar.gz';          ;;        s390x)          ESUM='50d3a0a8d251a1826af4532a7b97874b58231b749bc44a29a61736ae1df47e69';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_21.0.10.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 18 Mar 2026 00:55:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Mar 2026 00:55:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 18 Mar 2026 05:10:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 18 Mar 2026 06:09:43 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 06:09:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 18 Mar 2026 06:09:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 18 Mar 2026 06:09:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 18 Mar 2026 06:09:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 18 Mar 2026 06:09:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 Mar 2026 06:09:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 18 Mar 2026 06:09:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 18 Mar 2026 06:09:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 18 Mar 2026 06:09:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 18 Mar 2026 06:09:47 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 18 Mar 2026 06:09:47 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 Mar 2026 06:09:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 Mar 2026 06:09:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 Mar 2026 06:09:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fe6dcb8fff5ef43c62b8992539a79449cf84c229ea4dd2a5c95e478fed5d02`  
		Last Modified: Tue, 17 Mar 2026 08:47:39 GMT  
		Size: 13.8 MB (13787899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81442d3fd3562e03530f145f0acf25eae4359ac7738ae5a003eaf3c61145f34b`  
		Last Modified: Wed, 18 Mar 2026 00:57:27 GMT  
		Size: 243.8 MB (243775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19719aeb5aa66479879c3b1dfc9f8ce6d9a16820c923386e70af4e3c0665d075`  
		Last Modified: Wed, 18 Mar 2026 05:10:51 GMT  
		Size: 5.2 MB (5188125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e3c884e0242a55e0f2818e811ccea99eb9da39a3b354badfe97c48d688ec92`  
		Last Modified: Wed, 18 Mar 2026 06:10:17 GMT  
		Size: 26.6 MB (26611047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2227f6558410f4b42fdc22f2037e5ffa7965967841aa5ea28c7a56618b417f3d`  
		Last Modified: Wed, 18 Mar 2026 06:10:16 GMT  
		Size: 9.3 MB (9311176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251816ccb0494954eb6625aae36e032c36b22cdb637b7c2698b432343390f491`  
		Last Modified: Wed, 18 Mar 2026 06:10:16 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da73ca1112677d6f6a548ed22b4cdfaeba1e7b79d6a38d076e003b6aa46f80f`  
		Last Modified: Wed, 18 Mar 2026 06:10:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:d23c41f2e314f909d810be201bb2766344b0ac42b0fbddcf0fe90e1528303bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4816990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441799f34676b7dd5c4d3e862123b0745f47fd95aeb4a50e1769aba323692c5c`

```dockerfile
```

-	Layers:
	-	`sha256:59ffcc0ff2a524b011e26a59ba4b36c3ae91218cba843971131b8c4c22a43498`  
		Last Modified: Wed, 18 Mar 2026 06:10:16 GMT  
		Size: 4.8 MB (4797880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7480d74e2d115e6801a223a248cb3b151646730090295cf2efc695302adb51ba`  
		Last Modified: Wed, 18 Mar 2026 06:10:15 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-21-noble` - linux; s390x

```console
$ docker pull maven@sha256:e34f831407350586f805734102bb5325b476480bfc45fa9bf2a2979520400f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319901027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb3a40a8fcb45979ee910343ce8c32b122653b354fdb81484afc44425f542ad`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:14:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:14:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:14:10 GMT
ENV JAVA_VERSION=jdk-21.0.10+7.1_openj9-0.57.0
# Tue, 07 Apr 2026 05:55:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='fbd5af08d6abb7ac8a9707982f6759d33245e0b8b05d7ddd593cd45c0cb98e90';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_21.0.10.1.tar.gz';          ;;        amd64|x86_64)          ESUM='df501befcb3f6b7f47c3557d9887197d78f013beb57b0d56494176b54ad80c19';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_21.0.10.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='c60264d4b7dbd0ad94207ed85f4c71a5263ecb7c5bb6329da120194847d44611';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.10.1.tar.gz';          ;;        s390x)          ESUM='50d3a0a8d251a1826af4532a7b97874b58231b749bc44a29a61736ae1df47e69';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_21.0.10.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 05:55:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:55:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 05:57:11 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 09:47:39 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:47:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 09:47:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 09:47:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 09:47:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 09:47:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 09:47:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 09:47:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 09:47:40 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 09:47:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 09:47:40 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 09:47:40 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 09:47:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 09:47:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 09:47:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29f401ac367125349aab30446b6585fe53cab8476142395c42e2c8bcde2f000`  
		Last Modified: Tue, 07 Apr 2026 03:16:01 GMT  
		Size: 13.1 MB (13117397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865b71cba56d65a22bd2b64a78b5120141209e6da294557e66a4462dc5be6f71`  
		Last Modified: Tue, 07 Apr 2026 05:57:42 GMT  
		Size: 237.3 MB (237326247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bea4f47dcd31da21abe9d7aaeaf27b0b5c1e636a001f6024f2b3dafc583b17`  
		Last Modified: Tue, 07 Apr 2026 05:57:38 GMT  
		Size: 6.5 MB (6534443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f38f7acf7630d53bd2978d30efc5cc2857a50af17884093f53b838b202f6c`  
		Last Modified: Tue, 07 Apr 2026 09:48:04 GMT  
		Size: 23.7 MB (23698872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cb8bdda5fe62683b6924b48b83331d76cdd1768b5a1f5b9d231ba679631af4`  
		Last Modified: Tue, 07 Apr 2026 09:48:02 GMT  
		Size: 9.3 MB (9311188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47be13838b94321917f94798406ee68d5ddb3b2fb5399e97708797c80aa8db8a`  
		Last Modified: Tue, 07 Apr 2026 09:48:02 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b151dbd98b665cb62e548dffc68ebbb8937ff0c8b897719b2b765aa589104c1f`  
		Last Modified: Tue, 07 Apr 2026 09:48:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:906851a08bd44d60eb0979ef6dc8b332dbb16e3fb4845377a9f2d3c2f948909c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4811304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94169b554b90f0dd30c3596a391c7c6f3d689ffe2e8af7c7d468d72bfa8128e0`

```dockerfile
```

-	Layers:
	-	`sha256:2160692e08f20e17e5737487a3b1262716a62b10894ff248f7dc4bbcd1c36af5`  
		Last Modified: Tue, 07 Apr 2026 09:48:02 GMT  
		Size: 4.8 MB (4792244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53f4b24ccee5bcf80d8990db688cd31ef22863e51a0544ee699b42a31b7bb58`  
		Last Modified: Tue, 07 Apr 2026 09:48:02 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json
