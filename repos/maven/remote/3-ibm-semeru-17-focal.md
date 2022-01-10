## `maven:3-ibm-semeru-17-focal`

```console
$ docker pull maven@sha256:37ba8d9879ae2ff5c670f4b70cf3eee36991d1787321f7b4d830b1e586908ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

### `maven:3-ibm-semeru-17-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:99843f7f8960649a5f58050611e175fd8835d775545dc9e0bd431bd5e6d17339
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292088064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543c234f5c6c06244493b403918d6e65aab748a0a4e04f334f189b736e62536d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:32:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 02:41:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 19:40:28 GMT
ENV JAVA_VERSION=jdk-17.0.1+12_openj9-0.29.1
# Fri, 07 Jan 2022 19:40:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e0f80052ac4613d2d689904b20ff8b6e2bbd1edd87271db0659a646a24dfeb6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_aarch64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        amd64|x86_64)          ESUM='154f6411742ee1f8cbf004d72e7e71053b9ad4e89090cb930b6f16951e56503e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_x64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='80b6389dbed9b7de9c63b1cb423e719aa5e6fbab42387fdb1f68d9d199bf5196';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.1_12_openj9-0.29.1.tar.gz';         ;;       s390x)          ESUM='56e01c97f98bfb2cf9959b09b5d0cfae9993f82f1f54f77ef1199425c0b64bc2';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_s390x_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 19:40:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 19:40:47 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 07 Jan 2022 19:41:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 07 Jan 2022 19:41:24 GMT
CMD ["jshell"]
# Mon, 10 Jan 2022 21:42:41 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 10 Jan 2022 21:42:41 GMT
ARG USER_HOME_DIR=/root
# Mon, 10 Jan 2022 21:42:42 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 10 Jan 2022 21:42:43 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 10 Jan 2022 21:42:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Jan 2022 21:43:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 10 Jan 2022 21:43:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 10 Jan 2022 21:43:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 10 Jan 2022 21:43:14 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 10 Jan 2022 21:43:15 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 10 Jan 2022 21:43:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 10 Jan 2022 21:43:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d29c227106c1dba2893356b67a809c01fd77c745e8543df25145dfe5e7ef84`  
		Last Modified: Fri, 07 Jan 2022 02:46:50 GMT  
		Size: 15.9 MB (15894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcd324088ba527ea466905250d0bfb3ffe191a8c868e6624f8f1c738b1b02e9`  
		Last Modified: Fri, 07 Jan 2022 19:46:04 GMT  
		Size: 203.3 MB (203293772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ab9bb7d9e3efd7836528a4a8aa5879ffcc69cfeb389ab16b7b7183ee348238`  
		Last Modified: Fri, 07 Jan 2022 19:45:47 GMT  
		Size: 5.7 MB (5653210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ec9a1c4ca37d826815c3a0bea8e794be7f282ee956ccea9c349323f641b18b`  
		Last Modified: Mon, 10 Jan 2022 21:46:37 GMT  
		Size: 31.0 MB (30964728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e1e173ec62f495cccca89509b15a9092021f20d1ada1eb3e29010a4f8edb7f`  
		Last Modified: Mon, 10 Jan 2022 21:46:34 GMT  
		Size: 9.1 MB (9109762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa22e29d02f63dfb97204d1cb8431268136e4bd13eaf249cc85c9fdf82a23145`  
		Last Modified: Mon, 10 Jan 2022 21:46:32 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520bd40410dc9ac2a2c7506ede19290cfa905f642b846f78a73f56a626237ccd`  
		Last Modified: Mon, 10 Jan 2022 21:46:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-17-focal` - linux; s390x

```console
$ docker pull maven@sha256:922c27866e73b45844be512c33f5d937d8f4864ecf5aef857c6fdbe53369ad37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293084366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444f9ba066c3f678119e1cf10975bea5630a7adf0548c318f3556ef5001f0857`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:15:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 02:24:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:29:51 GMT
ENV JAVA_VERSION=jdk-17.0.1+12_openj9-0.29.1
# Fri, 07 Jan 2022 02:30:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e0f80052ac4613d2d689904b20ff8b6e2bbd1edd87271db0659a646a24dfeb6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_aarch64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        amd64|x86_64)          ESUM='154f6411742ee1f8cbf004d72e7e71053b9ad4e89090cb930b6f16951e56503e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_x64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='80b6389dbed9b7de9c63b1cb423e719aa5e6fbab42387fdb1f68d9d199bf5196';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.1_12_openj9-0.29.1.tar.gz';         ;;       s390x)          ESUM='56e01c97f98bfb2cf9959b09b5d0cfae9993f82f1f54f77ef1199425c0b64bc2';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_s390x_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 02:30:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 02:30:07 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 07 Jan 2022 02:30:42 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 07 Jan 2022 02:30:42 GMT
CMD ["jshell"]
# Mon, 10 Jan 2022 21:43:30 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 10 Jan 2022 21:43:30 GMT
ARG USER_HOME_DIR=/root
# Mon, 10 Jan 2022 21:43:31 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 10 Jan 2022 21:43:31 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 10 Jan 2022 21:43:40 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Mon, 10 Jan 2022 21:43:44 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 10 Jan 2022 21:43:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 10 Jan 2022 21:43:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 10 Jan 2022 21:43:44 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 10 Jan 2022 21:43:44 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 10 Jan 2022 21:43:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 10 Jan 2022 21:43:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2ea75c80fa68be6367734322b7c053932a41106663b880c832691c5c615f18`  
		Last Modified: Fri, 07 Jan 2022 02:32:46 GMT  
		Size: 15.7 MB (15739670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26895d5767c9b753c5f78a81886caebd33d5dc75ae1c108da768dab052f7e42d`  
		Last Modified: Fri, 07 Jan 2022 02:34:47 GMT  
		Size: 204.4 MB (204443746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716b6fe4c57feab18f1fe61c43efb16bb68330997bb2330444e4614e523ece2`  
		Last Modified: Fri, 07 Jan 2022 02:34:33 GMT  
		Size: 6.0 MB (5980788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffacfd4c9dee817820f95547ff8e34570c797218730b6944561a1d70a066aab`  
		Last Modified: Mon, 10 Jan 2022 21:45:16 GMT  
		Size: 30.7 MB (30688134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b369c45cf7f977b8920f9b959d87bdd8768266fd99501d8895c9fb78c9cf43`  
		Last Modified: Mon, 10 Jan 2022 21:45:12 GMT  
		Size: 9.1 MB (9109817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3ababa5f451b5f683c44d1c48765997427af0738d4b5ff3ac1b8c3dc0585ee`  
		Last Modified: Mon, 10 Jan 2022 21:45:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e7b141d00eacec8911ca28e081ff22e553435c483e12fd2dcacaf07d08b3f1`  
		Last Modified: Mon, 10 Jan 2022 21:45:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
