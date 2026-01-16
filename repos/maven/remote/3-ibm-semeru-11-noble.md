## `maven:3-ibm-semeru-11-noble`

```console
$ docker pull maven@sha256:60887eb9d285fcea4a5b2050afe7ee0525d5511f14b112cafed0709c604332ad
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

### `maven:3-ibm-semeru-11-noble` - linux; amd64

```console
$ docker pull maven@sha256:d201423f503214c63f73b4de3c10ce77fe6f90bd6fe4d4197aff51290315dab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300480302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df38ae534063a7e207ac190599f960f8aeea5c380f90e886218dccf5eaf3301`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:25:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:25:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:25:53 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 15 Jan 2026 22:25:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2c2d4bb11d96ff2e8c11dccd2012a34d62b635986b60fbfd22fe7e51ed889c8b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f17b7d34d108edff2b9da3a353378c972a1f5cf605cc2e08fce19e842e70d9d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='088a30c78efd377cf9d4d80c4f4288fa6538cf9cdccced79e4839171c9b3e151';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='00704dc2f0ca7aea13616fc5e1304248cb04f09170eb8eee728f5868476821f4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:25:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:25:58 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:26:30 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 15 Jan 2026 22:26:30 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 02:42:50 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:42:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:42:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:42:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:42:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:42:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:42:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:42:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:42:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:42:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:42:51 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:42:51 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:42:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:42:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:42:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e44054a64c49f2bc464e5a79b03f2fadc69ea9efbe3f836c393d439b23e84`  
		Last Modified: Thu, 15 Jan 2026 22:26:48 GMT  
		Size: 12.8 MB (12796317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1e2d7e4d691f320f85f6f3c065b176b2b4bbe8459e9eb4b10779d848576a8d`  
		Last Modified: Thu, 15 Jan 2026 22:27:12 GMT  
		Size: 220.6 MB (220596991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3291c7c761bd35a735c011c439724285f909ba8dea33ef829d8c6b6a4abc355`  
		Last Modified: Thu, 15 Jan 2026 22:26:59 GMT  
		Size: 5.5 MB (5481123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d562357dfa9fb059528a16a618993a9e4ae0327e309b8746cd3665b33fa455`  
		Last Modified: Fri, 16 Jan 2026 02:43:11 GMT  
		Size: 22.6 MB (22566576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd551fa315fd3de1b04cb53b3d64ee1a1b74cc84c25243e9147bce80e89c9882`  
		Last Modified: Fri, 16 Jan 2026 02:43:10 GMT  
		Size: 9.3 MB (9312245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10cf8d5aac2e6b8909514c7a54be2550d0b0748422fb3d6cba3333afc3c3887`  
		Last Modified: Fri, 16 Jan 2026 02:43:09 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d35239df4e5052844102c9b4fc1effc9f07db523a44dd221f49cf1f786ce24`  
		Last Modified: Fri, 16 Jan 2026 02:43:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:ad9a0adaa1d7a730a4191faba1414b889103e4acfb8a4b0d50766cee1e224f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4821470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754a6d5dc01734e423682263814448b12d80db27ef11d197cac5e7da885015c9`

```dockerfile
```

-	Layers:
	-	`sha256:4b37e45c9f234fe8d7ca121e014d0aa4e7beb24cc5f351207d1768ea87a4fa7c`  
		Last Modified: Fri, 16 Jan 2026 03:31:59 GMT  
		Size: 4.8 MB (4802415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be1149b8c2c2fa6d50a7bab568019ec86ebb84f359a313cd295179933678488`  
		Last Modified: Fri, 16 Jan 2026 03:32:00 GMT  
		Size: 19.1 KB (19055 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f969554921b052eacef87a9347e2c0f129123fb9cfc11bbc2396f25540048d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296293500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7943dc4ec157745e74f2868c51e92803718c53085b142ecd7f2273df07a948e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:54:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:54:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:54:53 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 21:54:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2c2d4bb11d96ff2e8c11dccd2012a34d62b635986b60fbfd22fe7e51ed889c8b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f17b7d34d108edff2b9da3a353378c972a1f5cf605cc2e08fce19e842e70d9d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='088a30c78efd377cf9d4d80c4f4288fa6538cf9cdccced79e4839171c9b3e151';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='00704dc2f0ca7aea13616fc5e1304248cb04f09170eb8eee728f5868476821f4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:54:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:54:58 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:55:30 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 01 Dec 2025 21:55:30 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:08:16 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:08:16 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:08:16 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:08:16 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:08:16 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:08:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:08:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:08:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:08:16 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:08:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:08:16 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:08:16 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:08:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:08:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:08:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f020d0ca72b864acd2e99df0d096bead0904bd21236a21f8fc8198ae784486f`  
		Last Modified: Mon, 01 Dec 2025 21:56:02 GMT  
		Size: 12.8 MB (12831459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b130b08aa41c03e69b9283cabec13509e25cd339b78bf29116a59cd3996f6e`  
		Last Modified: Mon, 01 Dec 2025 22:17:32 GMT  
		Size: 217.5 MB (217450636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1f661975b3ac63cf82aeea629a12540fc3bddc6794925dcada37d449f77201`  
		Last Modified: Mon, 01 Dec 2025 21:56:02 GMT  
		Size: 5.2 MB (5201000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6044ea19e30118b1d38f6777aeb2036e36b4b3877ce22f3374beee6b2da632f`  
		Last Modified: Wed, 17 Dec 2025 20:08:37 GMT  
		Size: 22.6 MB (22635170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56554281e1a0d3d881e444c5dbc9f476a954c781f88f6b17e024ed1abe597ffd`  
		Last Modified: Wed, 17 Dec 2025 20:08:34 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e6df96aeb0995fc8e6ed270925bf779bf6f3b56b9dd612592fb06980f92a4c`  
		Last Modified: Wed, 17 Dec 2025 20:08:36 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14e5e9ccf23704ae755b35a8119f7e96f4d4c0e6fbd65638ee3a7b1aea2d74`  
		Last Modified: Wed, 17 Dec 2025 20:08:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:39d2f9cd70cb4860383362498df7e214841d25f13784b205e39956cfeea9c924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb41b2a4e4761536dab94921414ae3718872fe273287e595c0dba05fc6cf612`

```dockerfile
```

-	Layers:
	-	`sha256:2b1d7eb71cbf09c75ee843db60c352987105aa54e280d5d2ad70bae6304514d8`  
		Last Modified: Wed, 17 Dec 2025 21:33:15 GMT  
		Size: 4.8 MB (4807632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bcb2c0588b67ef99a4942aec884e35ac2064a5f59a1e5ae69ca8b42417beee1`  
		Last Modified: Wed, 17 Dec 2025 21:33:16 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:4f7f5e0b8351e643702d265de178026fe8b32859abfd6447aaf823bb233c40e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312736458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeec3a90691f2df8a7f84789a54fd9f8e95dc2127975e817435a3cbf5c962ae1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:21 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 21:57:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2c2d4bb11d96ff2e8c11dccd2012a34d62b635986b60fbfd22fe7e51ed889c8b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f17b7d34d108edff2b9da3a353378c972a1f5cf605cc2e08fce19e842e70d9d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='088a30c78efd377cf9d4d80c4f4288fa6538cf9cdccced79e4839171c9b3e151';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='00704dc2f0ca7aea13616fc5e1304248cb04f09170eb8eee728f5868476821f4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:57:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:57:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:57:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 01 Dec 2025 21:57:53 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:18:49 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:18:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:18:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:18:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:18:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:18:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:18:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:18:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:18:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:18:52 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:18:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:18:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:18:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:18:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deeed061b7b811d5f2dacc798a5fa9f9027e6aadfe4d5cd0c08707f2ee04253a`  
		Last Modified: Mon, 01 Dec 2025 21:55:08 GMT  
		Size: 13.8 MB (13795823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1136b739291c39d8e95214240d91c857c0279f7a46b3d945ab7e8ba46cb58c`  
		Last Modified: Tue, 02 Dec 2025 00:27:14 GMT  
		Size: 224.2 MB (224242891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe9ffac31b82da4754229fa962e95e503a29a911c5b9e35f9538192a236d5f6`  
		Last Modified: Mon, 01 Dec 2025 21:59:00 GMT  
		Size: 4.5 MB (4468187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28d152e5bdca5692906517a7419451b28567297c6d486592e33f52efda1195`  
		Last Modified: Wed, 17 Dec 2025 20:19:46 GMT  
		Size: 26.6 MB (26611846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf1f3a9235c8acba7edf07258d6db3d523044a0ac2d88fc22793e46f7c342f1`  
		Last Modified: Wed, 17 Dec 2025 20:19:44 GMT  
		Size: 9.3 MB (9312249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3ef0957771bfabcdf9a8e495f9415678924d6bde502d4ae66f8848fa08b1bc`  
		Last Modified: Wed, 17 Dec 2025 20:19:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a4a99125ae030c62c665f2960268a817edc3259727ebb74b8ebf18075e767e`  
		Last Modified: Wed, 17 Dec 2025 20:19:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:2468b7710801167689ab5ba7711009060aeec962ef7877c4b624b92118280033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4828932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9b1261fb1e49ae76edb141c564bc5f5591f734c5704d6e98b6a9bb1b8b5164`

```dockerfile
```

-	Layers:
	-	`sha256:2ee8322835dac17ee8330e98373a2cde8293882ff023361dbb3481365e347462`  
		Last Modified: Wed, 17 Dec 2025 21:33:21 GMT  
		Size: 4.8 MB (4809826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fab885bae9cc436ed1056425a5392af4548ba11a44f70be9a7f6d82ebcb67c`  
		Last Modified: Wed, 17 Dec 2025 21:33:22 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; s390x

```console
$ docker pull maven@sha256:d67def35394b4f995646fab92bd2a1017d2af911218a143338c441e02fd29236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300295767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d835a74080db15ba07bbd48cc834d4678acd166b0fe898276e851dc3e0b98a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:12:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:12:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:12:15 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Thu, 15 Jan 2026 22:13:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2c2d4bb11d96ff2e8c11dccd2012a34d62b635986b60fbfd22fe7e51ed889c8b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f17b7d34d108edff2b9da3a353378c972a1f5cf605cc2e08fce19e842e70d9d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='088a30c78efd377cf9d4d80c4f4288fa6538cf9cdccced79e4839171c9b3e151';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='00704dc2f0ca7aea13616fc5e1304248cb04f09170eb8eee728f5868476821f4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:13:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:13:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:13:54 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 15 Jan 2026 22:13:54 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 00:47:44 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:47:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 00:47:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 00:47:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 00:47:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 00:47:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 00:47:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 00:47:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 00:47:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 00:47:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 00:47:44 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 00:47:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 00:47:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 00:47:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 00:47:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 07:12:17 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960e5a8a4758a7bb1786afff288a419a9926d43f49ae7f0b06153b15db8f8dbb`  
		Last Modified: Thu, 15 Jan 2026 22:13:12 GMT  
		Size: 13.1 MB (13119900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad1fc916db4307649b0db3f3ffeb9da537ce9449f3edbd1b5bdf354a67bb4e5`  
		Last Modified: Thu, 15 Jan 2026 22:14:37 GMT  
		Size: 218.6 MB (218628671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18172b40db7cf0784b526cbd43d24594325f8c632f89617eab2e1569338389b8`  
		Last Modified: Thu, 15 Jan 2026 22:14:31 GMT  
		Size: 5.6 MB (5628631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b15908812066f537dbab6dde77851a526360af70ead6129ddd0442dfa436e3`  
		Last Modified: Fri, 16 Jan 2026 00:48:18 GMT  
		Size: 23.7 MB (23696087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e90b79a0bd1f50a7fdda0b83264ff45f5cca0fd9e8f06ad3f7f4391a20fcbe`  
		Last Modified: Fri, 16 Jan 2026 00:48:13 GMT  
		Size: 9.3 MB (9312237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc6e038cac179424ce2c40c1ac4bfff5345ab47897d2f38be4207c56e5f90a`  
		Last Modified: Fri, 16 Jan 2026 00:48:12 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f58f7624fef57a90e516e7c0652e21176de641e681d623a6d4a05f13dd5c2a`  
		Last Modified: Fri, 16 Jan 2026 00:48:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:d9711b7f96f1aa7cb2c113b9fabf3221fdec3bffd693f44f746421e751d6f255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4823883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267f2b11f9a9c4abd1f0dc99b0f45be4366b3b9cf4695f17af1fa4e82b3045f9`

```dockerfile
```

-	Layers:
	-	`sha256:ab811e22d1a49767560c496311d92fba801f8e88d831c002e791fc2e3ea303b6`  
		Last Modified: Fri, 16 Jan 2026 03:32:12 GMT  
		Size: 4.8 MB (4804828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d86347c902fb8e4054338e765550a7e27b44ebf1862fcdf587137c07107aec`  
		Last Modified: Fri, 16 Jan 2026 03:32:13 GMT  
		Size: 19.1 KB (19055 bytes)  
		MIME: application/vnd.in-toto+json
