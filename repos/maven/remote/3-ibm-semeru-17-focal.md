## `maven:3-ibm-semeru-17-focal`

```console
$ docker pull maven@sha256:d3457daae4d1461c6aa4d035eed2e26927aff0844ca3ff0d342b96b5877f3942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-ibm-semeru-17-focal` - linux; amd64

```console
$ docker pull maven@sha256:9a63fddee8df274ac0f669e3bb6d0745096fc7bc0c8e91448c57ea7f3786a57c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 MB (298918169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5423a711234b17ba213329fb000c6bda59de051997a46ec13c7f91457f3a65ef`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 13:19:55 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:19:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:19:57 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Thu, 26 Jan 2023 13:19:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:20:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:20:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:27:14 GMT
ENV JAVA_VERSION=jdk-17.0.5+8_openj9-0.35.0
# Tue, 31 Jan 2023 18:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='693604e48eef24c20d785f3a7e81e538a30e436ed36b7539a5e23e0008b2c405';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_aarch64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b46de9cd00af8a0223f4b50deb2627ab91fe515a69383a96fd2c12757cef24fe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_x64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3158c8e46be057ddacab25a52c2ded470102f994719025ccfa77c23d1106daa9';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        s390x)          ESUM='d16e4d6187cb0911489da46201ab0a0f2bac4ba3b558fc849d1a0eb8c457505b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_s390x_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Jan 2023 18:27:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 18:27:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 31 Jan 2023 18:28:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 31 Jan 2023 18:28:13 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 23:18:21 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 23:18:22 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 23:18:22 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 23:18:22 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 23:18:22 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 23:18:24 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 23:18:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 23:18:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 23:18:24 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 23:18:24 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 23:18:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 23:18:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae357c533a478b944881de975cc4193cce5335354cc192363e4a18c421e51c2`  
		Last Modified: Tue, 31 Jan 2023 18:36:11 GMT  
		Size: 16.0 MB (15995992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927620b583ee9298040022a159588077d1253d75fe3b2034a84551c7ea96e33c`  
		Last Modified: Tue, 31 Jan 2023 18:38:49 GMT  
		Size: 208.8 MB (208803722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57eb911a490eea946197556bae6bd9447af0ca2f859a6d5d0e2518651224ec5c`  
		Last Modified: Tue, 31 Jan 2023 18:38:35 GMT  
		Size: 6.0 MB (5990299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb8ffc5d81546911a36f79e0ecfdd6d44bed4c1c2f0c26873d2bf9857a756c6`  
		Last Modified: Tue, 31 Jan 2023 23:23:36 GMT  
		Size: 31.2 MB (31197910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a83d04b49f28543ab2ae83cd724222bc55550e9fa6935402be149cfae108123`  
		Last Modified: Tue, 31 Jan 2023 23:23:32 GMT  
		Size: 8.4 MB (8351151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928ab2da3f9233cd4e36031d8ed8fb3dc2dff19f772cf9acb3659e0bb32ed8f`  
		Last Modified: Tue, 31 Jan 2023 23:23:31 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8245229d568ccf2c3fe0588ec24d0dbce2b09126642ba83eb8e69408d9fba339`  
		Last Modified: Tue, 31 Jan 2023 23:23:32 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-17-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d1d34e491839411b1984771c0301fed6a0a7b0306bd3dc89a36bd15bea0e6b96
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293301957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dca051a70fc48dff35d4a9f34bed0dcc7a96d99c6f5f9d657c26a8eedf8a467`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 13:50:26 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:50:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:50:26 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:50:33 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Thu, 26 Jan 2023 13:50:33 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:37:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:37:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:36 GMT
ENV JAVA_VERSION=jdk-17.0.5+8_openj9-0.35.0
# Tue, 31 Jan 2023 18:44:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='693604e48eef24c20d785f3a7e81e538a30e436ed36b7539a5e23e0008b2c405';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_aarch64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b46de9cd00af8a0223f4b50deb2627ab91fe515a69383a96fd2c12757cef24fe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_x64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3158c8e46be057ddacab25a52c2ded470102f994719025ccfa77c23d1106daa9';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        s390x)          ESUM='d16e4d6187cb0911489da46201ab0a0f2bac4ba3b558fc849d1a0eb8c457505b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_s390x_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Jan 2023 18:44:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 18:44:56 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 31 Jan 2023 18:45:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 31 Jan 2023 18:45:31 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 22:07:15 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 22:07:15 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 22:07:15 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 22:07:16 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 22:07:16 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 22:07:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 22:07:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 22:07:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 22:07:17 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 22:07:17 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 22:07:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 22:07:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdbed22b0a8a0e7be353c90eedf03945efc6451043f2f84c4b81d21cdf90ff8`  
		Last Modified: Tue, 31 Jan 2023 18:53:46 GMT  
		Size: 15.9 MB (15860320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1753ceb68baaf464d5259cdca4db2e53e3d08176edc50a0dc9a5e500baa2311e`  
		Last Modified: Tue, 31 Jan 2023 18:56:03 GMT  
		Size: 205.0 MB (204994897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f37d930d4c6baef66e5a205b7b257df2e6d60a1b60957ddcc32547c3d85a629`  
		Last Modified: Tue, 31 Jan 2023 18:55:52 GMT  
		Size: 5.7 MB (5669269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76fd407a97cdf90ceb99f2b1511036fff89982379f139995c699059d5b76021`  
		Last Modified: Tue, 31 Jan 2023 22:10:54 GMT  
		Size: 31.2 MB (31231375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9f18c37577e9865f722b87273fee7ac3cdc84b8193871591b00e7254dff91c`  
		Last Modified: Tue, 31 Jan 2023 22:10:51 GMT  
		Size: 8.4 MB (8351152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b43291e25903d65bf875b63c7b6687d12fce00f293701966bc7de605a261b3`  
		Last Modified: Tue, 31 Jan 2023 22:10:50 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba558a82dad70629db896e34b2e6cf9e82ce2021002003ee6e5934ab158eb42`  
		Last Modified: Tue, 31 Jan 2023 22:10:50 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-17-focal` - linux; ppc64le

```console
$ docker pull maven@sha256:c9885c6af942d855ecb0e2aba3b7cd6075c61a1bf20e4e58466836bdbca09bda
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.3 MB (313308701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5277177b08f91dc04fa815ca2771e98aae98b359ab5cc3b8e862df140119359`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 13:47:16 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:47:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:47:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:47:17 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:47:20 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Thu, 26 Jan 2023 13:47:20 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:53:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Jan 2023 18:54:20 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:59:05 GMT
ENV JAVA_VERSION=jdk-17.0.5+8_openj9-0.35.0
# Tue, 31 Jan 2023 18:59:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='693604e48eef24c20d785f3a7e81e538a30e436ed36b7539a5e23e0008b2c405';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_aarch64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b46de9cd00af8a0223f4b50deb2627ab91fe515a69383a96fd2c12757cef24fe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_x64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3158c8e46be057ddacab25a52c2ded470102f994719025ccfa77c23d1106daa9';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        s390x)          ESUM='d16e4d6187cb0911489da46201ab0a0f2bac4ba3b558fc849d1a0eb8c457505b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_s390x_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Jan 2023 18:59:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Jan 2023 18:59:39 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 31 Jan 2023 19:00:17 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 31 Jan 2023 19:00:17 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 21:57:39 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 21:57:41 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 21:57:41 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 21:57:42 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 21:57:42 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 21:57:44 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 21:57:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 21:57:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 21:57:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 21:57:46 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 21:57:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 21:57:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df25ba8fe9a5a6fef5f902c8e3443c2a1529b9200c6d57a9a4f2e0283cf5422`  
		Last Modified: Tue, 31 Jan 2023 19:05:38 GMT  
		Size: 17.2 MB (17168712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a5e0c274a3f08ddd9a5b1f9ddb41954e7c897c87223e81c36163da3ac2a468`  
		Last Modified: Tue, 31 Jan 2023 19:07:54 GMT  
		Size: 211.2 MB (211198912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1522fa7d764d72791a8654cc385db7cad624c0073bc3dcba42d1caa3f3f4005e`  
		Last Modified: Tue, 31 Jan 2023 19:07:29 GMT  
		Size: 4.9 MB (4865443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53075e89dd23c5ff68440ec2d96838299e6169c284628bc64975f70969b83666`  
		Last Modified: Tue, 31 Jan 2023 22:04:09 GMT  
		Size: 38.4 MB (38422924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7e262cac7ae30c61ea998f575dedc12eb55262f31db1d89a6899a1720abe06`  
		Last Modified: Tue, 31 Jan 2023 22:04:00 GMT  
		Size: 8.4 MB (8351156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544a391b051bbdc423dddfe9da4aa91b287ebea0211f966496c66134da9dfe98`  
		Last Modified: Tue, 31 Jan 2023 22:03:59 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7ba3a7bdd5336221ceddcdd50b9a7ebd319f421cdc71467100530443645560`  
		Last Modified: Tue, 31 Jan 2023 22:03:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-17-focal` - linux; s390x

```console
$ docker pull maven@sha256:33446a5b6a245e643c717911bde2353fb89714862b4580f3326e38fa58ca0c77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294387074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0c52435255f87122e05be7d3642463eb231b06a8935c6d18a0358f2523f2aa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Feb 2023 12:00:21 GMT
ARG RELEASE
# Wed, 01 Feb 2023 12:00:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 12:00:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 12:00:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 12:00:23 GMT
ADD file:4d5fa9b68af51e9c8cd7b25fb55ddd47256efb0b2eda9432507b72b7c1a17053 in / 
# Wed, 01 Feb 2023 12:00:24 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 18:23:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Feb 2023 18:23:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 18:27:49 GMT
ENV JAVA_VERSION=jdk-17.0.5+8_openj9-0.35.0
# Wed, 01 Feb 2023 18:27:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='693604e48eef24c20d785f3a7e81e538a30e436ed36b7539a5e23e0008b2c405';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_aarch64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b46de9cd00af8a0223f4b50deb2627ab91fe515a69383a96fd2c12757cef24fe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_x64_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3158c8e46be057ddacab25a52c2ded470102f994719025ccfa77c23d1106daa9';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;        s390x)          ESUM='d16e4d6187cb0911489da46201ab0a0f2bac4ba3b558fc849d1a0eb8c457505b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.5%2B8_openj9-0.35.0/ibm-semeru-open-jdk_s390x_linux_17.0.5_8_openj9-0.35.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 01 Feb 2023 18:28:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Feb 2023 18:28:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 01 Feb 2023 18:28:36 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 01 Feb 2023 18:28:36 GMT
CMD ["jshell"]
# Wed, 01 Feb 2023 19:10:38 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:10:40 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 01 Feb 2023 19:10:40 GMT
ARG USER_HOME_DIR=/root
# Wed, 01 Feb 2023 19:10:40 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 01 Feb 2023 19:10:40 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 01 Feb 2023 19:10:47 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 01 Feb 2023 19:10:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 01 Feb 2023 19:10:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 01 Feb 2023 19:10:47 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 01 Feb 2023 19:10:47 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 01 Feb 2023 19:10:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 01 Feb 2023 19:10:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cbc0e1117f61ba365a9a02263b82c04f704d5d162aa31b25a9326797dd1c7084`  
		Last Modified: Tue, 31 Jan 2023 17:54:46 GMT  
		Size: 27.0 MB (27016130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32329c78fa891c29ef5b9df096b2cffaba8738e3e5a77aa5d7cb00958cf46491`  
		Last Modified: Wed, 01 Feb 2023 18:33:24 GMT  
		Size: 15.7 MB (15686940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec32adadbc6232b4aa3b2890f01dc49507542288b800fccfa09c8e9187882b58`  
		Last Modified: Wed, 01 Feb 2023 18:34:45 GMT  
		Size: 206.6 MB (206582604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df8d3bdb42d36f098f02b06b045ab6af0b805d9c1bb50c08eecbe20792abf4e`  
		Last Modified: Wed, 01 Feb 2023 18:34:32 GMT  
		Size: 6.0 MB (6033372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e37bca5820b8c0c493289adb3e80842da0a97f27db2d0395dd774fd5d3fb8f`  
		Last Modified: Wed, 01 Feb 2023 19:13:24 GMT  
		Size: 30.7 MB (30715673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0fa788a04a5f871cb691f769f9f1276d4b3f1118e60d0b2d89482378f68343`  
		Last Modified: Wed, 01 Feb 2023 19:13:20 GMT  
		Size: 8.4 MB (8351145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e89b5d244dc5fbf4a1d490ade3f491ffd9c0ea948203fe6f61dfc2d4e68341`  
		Last Modified: Wed, 01 Feb 2023 19:13:20 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc348642fe01188e59668989b34641d5680c11391c050d044884bee541093de`  
		Last Modified: Wed, 01 Feb 2023 19:13:20 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
