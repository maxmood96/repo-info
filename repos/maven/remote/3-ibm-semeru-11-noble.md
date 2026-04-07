## `maven:3-ibm-semeru-11-noble`

```console
$ docker pull maven@sha256:5d7a9819136b2058e94f795ee4bc0e8a21ce7f3efb8f04f1b18749b9eb747fa2
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
$ docker pull maven@sha256:9edaedb766bec1b73754e42d730b56a480c8ded012ab5aa3d71e52ac021954c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (301011552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b3018de9f9204c77c08f8b6795f8cbce2f6afa6877903b4021aca791b21a49`
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
# Tue, 07 Apr 2026 01:56:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:56:15 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:56:15 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Tue, 07 Apr 2026 01:56:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9fb6a2524378d7f49913406eded71013d9de853009a3e6df58fb27fa6fb727b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='89a4d7d40cdd82bbbc9bbf4e24c23062eb137cadc9a1958a890282e158696691';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='477c31aabf2862ef40c1210384ad4643d0d52bf381aa9399ca872e46dcdde9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='bba879725fa70ab38b021a984f6617477c18ad1fe1a153b0b230474e09dd0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 01:56:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:56:25 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 01:57:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 01:57:32 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:06:49 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:06:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:06:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:06:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:06:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:06:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:06:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:06:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:06:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:06:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:06:49 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:06:49 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:06:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:06:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:06:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57cf003f0a75ddd0eb75191324634130f9941f5440d14c46ab2939c09d08c34`  
		Last Modified: Tue, 07 Apr 2026 01:57:51 GMT  
		Size: 12.8 MB (12805533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d3d40013a10a77be10851f213f0eb0cec8ca6731d820c21dd6ae4bf48913c0`  
		Last Modified: Tue, 07 Apr 2026 01:57:55 GMT  
		Size: 221.3 MB (221273515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f057461cbd16939a09789eb4e7f17ab03f43aea23115edfa78a527e32d36d4`  
		Last Modified: Tue, 07 Apr 2026 01:57:51 GMT  
		Size: 5.3 MB (5317697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1ad18c41e4b9266709c59904ea12ebea05da295044b91622683fed7d6689f1`  
		Last Modified: Tue, 07 Apr 2026 05:07:04 GMT  
		Size: 22.6 MB (22569123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f3d729e1c11932e84026c423154226610bcb0aad20b7399f93420e1ef407d1`  
		Last Modified: Tue, 07 Apr 2026 05:07:03 GMT  
		Size: 9.3 MB (9311188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4a6b40810cb9b4017f04a513d4e091ebab5dd03d89d41d12d803b994d22982`  
		Last Modified: Tue, 07 Apr 2026 05:07:03 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2ae2cd196b06652f0026d0abfe45408652fce68c0ed55a8f76ed964b04a180`  
		Last Modified: Tue, 07 Apr 2026 05:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:01c60f3776bb1160c3bc17f40cda9fae4a797beb7befff05d3760b9cf1046208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4822765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5f7a0afd25785edc65ed6bffb450ea9f121dd9dc594cdf54596edca4defe5e`

```dockerfile
```

-	Layers:
	-	`sha256:b80492c0e0bc6193352d2b44cb2923e01c14d238f26e5e60ed5ed337315b81d3`  
		Last Modified: Tue, 07 Apr 2026 05:07:03 GMT  
		Size: 4.8 MB (4803705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc916138fa91e91da5bed59f58d19cbda902f8e3658ef8628c61e2e3f2957ec`  
		Last Modified: Tue, 07 Apr 2026 05:07:03 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:40e57100995525b604a16de0a79b55e2fc9cc8b9bd5b147b267a1ca49f0f6957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297070132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf49be4fb7e1a02ee65166998561d1fde52001d87a4a7c6220072801f814ed82`
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
# Tue, 07 Apr 2026 01:59:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:59:52 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:52 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Tue, 07 Apr 2026 02:00:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9fb6a2524378d7f49913406eded71013d9de853009a3e6df58fb27fa6fb727b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='89a4d7d40cdd82bbbc9bbf4e24c23062eb137cadc9a1958a890282e158696691';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='477c31aabf2862ef40c1210384ad4643d0d52bf381aa9399ca872e46dcdde9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='bba879725fa70ab38b021a984f6617477c18ad1fe1a153b0b230474e09dd0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 02:00:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:00:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 02:01:09 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 02:01:09 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:12:24 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:12:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:12:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:12:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:12:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:12:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:12:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:12:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:12:24 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:12:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:12:24 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:12:24 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:12:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:12:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:12:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22183b54f1bdaf5704f2675b9282d317fe0c0ec78fc925f29ec4c23aee07d7e`  
		Last Modified: Tue, 07 Apr 2026 02:01:47 GMT  
		Size: 12.8 MB (12837787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1275646bc32282caac98cd9e98bbf61406ca049f047a3ff1c1e3a4e794699811`  
		Last Modified: Tue, 07 Apr 2026 02:01:52 GMT  
		Size: 218.1 MB (218134523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4c9c6a378b440d162efaaf6d32cb41f604fe4f497ee92d671c3be5631c140`  
		Last Modified: Tue, 07 Apr 2026 02:01:47 GMT  
		Size: 5.3 MB (5274625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662209190a210cf65536b1e8da702b0a3c612b74ce357eae65087713d1cfdb11`  
		Last Modified: Tue, 07 Apr 2026 05:12:37 GMT  
		Size: 22.6 MB (22636902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8553e80730b7fbb5287e2a3c043bda4493bcb481ddff2ed957a45ef86df2de8`  
		Last Modified: Tue, 07 Apr 2026 05:12:37 GMT  
		Size: 9.3 MB (9311185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d84e3fc049758c56e270d2a5b3f76a05e170daec3d9b18fe26995ee8d570c6`  
		Last Modified: Tue, 07 Apr 2026 05:12:36 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463829709a8224c94130124177fcfeb9420b24747886270b0f945d352a019aa`  
		Last Modified: Tue, 07 Apr 2026 05:12:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:a527e58c52e4edb20dd8ff870edea14f37a1a5c45ef5de66763615af9c3b576f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4827503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1b5d7683dc57ec5b02e58ce0c71fa0fd7cc14188e42b8c1ffb907bcd50677a`

```dockerfile
```

-	Layers:
	-	`sha256:0de537ef96a0a2a6e2a64f4a1444b4d462c4a57a3942570b851218432d698ee1`  
		Last Modified: Tue, 07 Apr 2026 05:12:37 GMT  
		Size: 4.8 MB (4808311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd5c90437ae2c2a6b20fb66b4a81c44621b321750870c9b5e89bdf0e584689d`  
		Last Modified: Tue, 07 Apr 2026 05:12:36 GMT  
		Size: 19.2 KB (19192 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:597ae93376eba4876e6a44697bbdf2a60bba3486018c4ca14d1ea60cc589731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313489128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3917079af06bda68da795698f39a032342532757791d85f3a7d4a44b413b72d1`
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
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Tue, 17 Mar 2026 18:54:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9fb6a2524378d7f49913406eded71013d9de853009a3e6df58fb27fa6fb727b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='89a4d7d40cdd82bbbc9bbf4e24c23062eb137cadc9a1958a890282e158696691';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='477c31aabf2862ef40c1210384ad4643d0d52bf381aa9399ca872e46dcdde9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='bba879725fa70ab38b021a984f6617477c18ad1fe1a153b0b230474e09dd0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 18:54:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:54:12 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 18:55:17 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 18:55:17 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 22:06:06 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 22:06:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 22:06:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:06:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:06:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 22:06:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 22:06:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 22:06:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 22:06:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 22:06:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 22:06:08 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 22:06:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 22:06:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 22:06:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 22:06:08 GMT
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
	-	`sha256:beeca431673d7c48aeb4ef30416b1dcd4ef5199b1bb0ab748fc410e0f6a21489`  
		Last Modified: Tue, 17 Mar 2026 18:56:02 GMT  
		Size: 225.0 MB (224996748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683027ac801baa081640349b34d3b5af8909178b592f1372610d2d8a517cea5e`  
		Last Modified: Tue, 17 Mar 2026 18:55:57 GMT  
		Size: 4.5 MB (4471752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97ea5d963abed45b4d8e1ae585d04d2ca2f2fbb1995837fca6dbb709d8875b6`  
		Last Modified: Tue, 17 Mar 2026 22:06:39 GMT  
		Size: 26.6 MB (26610459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b10d9ff77fab1b697d916c4b9227c8827c5853b2fdcb37f126f0c8fb7cc124d`  
		Last Modified: Tue, 17 Mar 2026 22:06:38 GMT  
		Size: 9.3 MB (9311181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fca69f263646dd165b0859dc28c7b45c99dadcb70aab9ab9414aa3c63d9f51`  
		Last Modified: Tue, 17 Mar 2026 22:06:37 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bd0c3b3e97a042b7cb73cceb6e9c937909c73a1bbf81056c5bfb1ca261ed2a`  
		Last Modified: Tue, 17 Mar 2026 22:06:38 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:3b35d43bf442465dd17e5f0f6d0711abc038ee59c7fdc6d952f9f68e99702cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4830238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c3c95084809c98323de722738a31323f069a7eb0baab6282cc944c28a5007e`

```dockerfile
```

-	Layers:
	-	`sha256:70ef2a92e8ea67bcf8cee5498f07c8f2224f192b2b34020a1f2c73f1ea54c656`  
		Last Modified: Tue, 17 Mar 2026 22:06:38 GMT  
		Size: 4.8 MB (4811128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444532f69164dd088ef7f32d747846156271d49303a68f3318ae4dcd1983ed23`  
		Last Modified: Tue, 17 Mar 2026 22:06:37 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; s390x

```console
$ docker pull maven@sha256:607a4aabbda1f3ae143368ff1ab12690437762f9ed21e82f6eebb48615470d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300682426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2740061117831cc9a95ddfe3a285815bfbc65dc5a38c075e96bdc1d0809081`
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
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Tue, 07 Apr 2026 03:14:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9fb6a2524378d7f49913406eded71013d9de853009a3e6df58fb27fa6fb727b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='89a4d7d40cdd82bbbc9bbf4e24c23062eb137cadc9a1958a890282e158696691';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='477c31aabf2862ef40c1210384ad4643d0d52bf381aa9399ca872e46dcdde9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='bba879725fa70ab38b021a984f6617477c18ad1fe1a153b0b230474e09dd0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 03:14:22 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 03:15:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 03:15:33 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 09:46:00 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:46:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 09:46:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 09:46:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 09:46:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 09:46:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 09:46:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 09:46:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 09:46:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 09:46:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 09:46:00 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 09:46:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 09:46:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 09:46:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 09:46:00 GMT
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
	-	`sha256:b8441f6844a8bcbf778e63d97f57df9edbdfd473dca1a7634f3dbb5a59c09c6e`  
		Last Modified: Tue, 07 Apr 2026 03:16:04 GMT  
		Size: 219.0 MB (219005655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37352d8f61250711e8fceb36efe44303bb0052f431d9dca340821fe2d041f305`  
		Last Modified: Tue, 07 Apr 2026 03:16:01 GMT  
		Size: 5.6 MB (5636339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9395c33cfabb19e2b4d4b0e9001e1b4453dc44cab59391f1d24a89a4ef0533`  
		Last Modified: Tue, 07 Apr 2026 09:46:20 GMT  
		Size: 23.7 MB (23698968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940987911879e841a741bbebfa393272315b3e75dbc65a6d8090736565386d15`  
		Last Modified: Tue, 07 Apr 2026 09:46:20 GMT  
		Size: 9.3 MB (9311186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04714e25b955e44587869cefd29e7fbe772f431028001053e3a7231557f25080`  
		Last Modified: Tue, 07 Apr 2026 09:46:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87c6c888a0b315605acceef999215a575e54a4ac02f50faddae0b9066012c4`  
		Last Modified: Tue, 07 Apr 2026 09:46:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:cf3ce2ec63444405a528f08aae0f4daab8d562fd2cf715934b0265b619dc133b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4824552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf28f0c82ce2af00fc16b32a853907e49a6a686d154ad7237089f7e5dd51fe2`

```dockerfile
```

-	Layers:
	-	`sha256:0b31d43a07dbf7de019b927a66c4c831806b7fcd2929b3e7912f2cb600c2bc11`  
		Last Modified: Tue, 07 Apr 2026 09:46:20 GMT  
		Size: 4.8 MB (4805492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1922378b65b8d110d6ccf90e23390fbf60093878ff1d771727a25ea9318e66`  
		Last Modified: Tue, 07 Apr 2026 09:46:19 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json
