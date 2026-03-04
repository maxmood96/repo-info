## `maven:3-ibm-semeru-11-noble`

```console
$ docker pull maven@sha256:2440d538ad6328fd4c559dabae59c60d0ee68e30015dd580e40b1d7bacb88e4e
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
$ docker pull maven@sha256:3f667f0e757bf5a9b8e20f1f349bcffe7118b2a21053481aa7d41503664ded50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301061287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7038175de4bda4e3f3af519651ae1d43b1ce881e73df9607b74698676f87a6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 03 Mar 2026 20:13:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Mar 2026 20:13:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 20:13:22 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Tue, 03 Mar 2026 20:13:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9fb6a2524378d7f49913406eded71013d9de853009a3e6df58fb27fa6fb727b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='89a4d7d40cdd82bbbc9bbf4e24c23062eb137cadc9a1958a890282e158696691';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='477c31aabf2862ef40c1210384ad4643d0d52bf381aa9399ca872e46dcdde9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='bba879725fa70ab38b021a984f6617477c18ad1fe1a153b0b230474e09dd0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 20:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:13:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 20:14:34 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Mar 2026 20:14:34 GMT
CMD ["jshell"]
# Tue, 03 Mar 2026 21:07:58 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 21:07:58 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 21:07:58 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 21:07:58 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 21:07:58 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 21:07:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 21:07:58 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 21:07:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 21:07:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 21:07:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 21:07:59 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 21:07:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 21:07:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 21:07:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 21:07:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd69884ee026f0e52bf5f176b86bb2ba6cbbe0e7e819fbb90732e928a51c883`  
		Last Modified: Tue, 03 Mar 2026 20:14:53 GMT  
		Size: 12.8 MB (12804508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2079e7722695e044767a6311639fdbc2baba418a6934948c87e74ad7cbae337f`  
		Last Modified: Tue, 03 Mar 2026 20:14:57 GMT  
		Size: 221.3 MB (221273503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42db7c8e275e25bb17bf8135428ea4555c0876501a75346580392481fdadd3ea`  
		Last Modified: Tue, 03 Mar 2026 20:14:53 GMT  
		Size: 5.4 MB (5375142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b569757a234c41fad0712537af9d18fd2c2419a294a97cf9e6f5d1d5f2feeb33`  
		Last Modified: Tue, 03 Mar 2026 21:08:11 GMT  
		Size: 22.6 MB (22567250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d578ffd5b6fad62c874b295a94bb0f0480e7629be55b341e594c4696d8855980`  
		Last Modified: Tue, 03 Mar 2026 21:08:11 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438567c1d894b47e33972fcc55648c456360828505b85fc533083eff89b6e23`  
		Last Modified: Tue, 03 Mar 2026 21:08:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6721d30da4d74fdd455f24e79417dad8333e3ae7c26d4ef732ee1a4cffa52d1`  
		Last Modified: Tue, 03 Mar 2026 21:08:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:58bd95c87091cdad87f74428c61c000b9b95da0f4ceb3927026fe900cc4a5b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4822749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7459a633d0043d29bcac12289bebf88fe080d34aa3010891cc86e63e099261d`

```dockerfile
```

-	Layers:
	-	`sha256:34ce094ce602555def214d79d775c7de12278f368fd41de801f310a491c44df2`  
		Last Modified: Tue, 03 Mar 2026 21:08:11 GMT  
		Size: 4.8 MB (4803689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3247382d9a925d3562595df9b44050f31064e0c08ebe5ac18156d2975423e6d`  
		Last Modified: Tue, 03 Mar 2026 21:08:10 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6aa83a5d0ee8fbdbbc1534b7635297d448aeef649a003411117015dddb074c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297017173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb3272214968dfb7a25a9e9e3610dba8432adeb26eb63d074189d6cada2776`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 03 Mar 2026 20:13:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Mar 2026 20:13:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 20:13:19 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Tue, 03 Mar 2026 20:13:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9fb6a2524378d7f49913406eded71013d9de853009a3e6df58fb27fa6fb727b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='89a4d7d40cdd82bbbc9bbf4e24c23062eb137cadc9a1958a890282e158696691';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='477c31aabf2862ef40c1210384ad4643d0d52bf381aa9399ca872e46dcdde9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='bba879725fa70ab38b021a984f6617477c18ad1fe1a153b0b230474e09dd0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 20:13:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:13:27 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 20:14:30 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Mar 2026 20:14:30 GMT
CMD ["jshell"]
# Tue, 03 Mar 2026 21:05:50 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 21:05:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 21:05:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 21:05:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 21:05:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 21:05:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 21:05:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 21:05:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 21:05:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 21:05:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 21:05:50 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 21:05:50 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 21:05:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 21:05:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 21:05:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228d19e5a0245577db8166f056db685c09a06436fb2bc74658780a691a60e8a`  
		Last Modified: Tue, 03 Mar 2026 20:14:50 GMT  
		Size: 12.8 MB (12836351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82a6d6c0bfd629070843d146a3ef63a3de5c2e1058f161146206454049f69db`  
		Last Modified: Tue, 03 Mar 2026 20:14:55 GMT  
		Size: 218.1 MB (218134513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fe6fef1e0a2519e87155fa6f246591b5a3ae282a1ae98e7751c6b820c8c126`  
		Last Modified: Tue, 03 Mar 2026 20:14:50 GMT  
		Size: 5.2 MB (5231401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c7addf72f428e6e34b16259c7ca5bf04e9375927166f34280868e05e64e138`  
		Last Modified: Tue, 03 Mar 2026 21:06:03 GMT  
		Size: 22.6 MB (22636492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b54e355f136ce92f2d09c91403e5b0d97ea396eca4ebdf73abb146364b7c4f`  
		Last Modified: Tue, 03 Mar 2026 21:06:03 GMT  
		Size: 9.3 MB (9312255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d587256cd3a6f2345a5946045dc5a912032aa00c7a5c7554f101c2ea14fdcb`  
		Last Modified: Tue, 03 Mar 2026 21:06:02 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff63d8768aa3e517757523acaf32e4328d860b280c188b5d0ead10ccf7eac0d4`  
		Last Modified: Tue, 03 Mar 2026 21:06:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:b25c420d6b640f269ac13407fcf30a2dab42eb2599b8d47fb26d121e0a74c943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4827488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da81c506cc1ef34fdee18c92f7d7640a66bb998d4cd0c40b2824633de9721059`

```dockerfile
```

-	Layers:
	-	`sha256:adde84c8d2d76b923628becb466454da8b9d83a01d6ba79aec8673b25071adfe`  
		Last Modified: Tue, 03 Mar 2026 21:06:03 GMT  
		Size: 4.8 MB (4808295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9f84f79bc5a1dd364407784c90c9ea6aa885036c6d4d8324eb2fbc4e01d379`  
		Last Modified: Tue, 03 Mar 2026 21:06:03 GMT  
		Size: 19.2 KB (19193 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:f4a054dde3b2138d515ada9467e62ce7a52da71ae05aabf8f1ffbf81179eaac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314186682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5601898a2e1c5fcc6768a3ea2b9ca335aed8ae5a989ca0cffb41214f143a24e9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:28:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:56 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Wed, 04 Mar 2026 00:48:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9fb6a2524378d7f49913406eded71013d9de853009a3e6df58fb27fa6fb727b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='89a4d7d40cdd82bbbc9bbf4e24c23062eb137cadc9a1958a890282e158696691';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='477c31aabf2862ef40c1210384ad4643d0d52bf381aa9399ca872e46dcdde9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='bba879725fa70ab38b021a984f6617477c18ad1fe1a153b0b230474e09dd0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 04 Mar 2026 00:48:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 00:48:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 04 Mar 2026 07:56:27 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 04 Mar 2026 07:56:27 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 08:09:20 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Mar 2026 08:09:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 04 Mar 2026 08:09:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 04 Mar 2026 08:09:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 04 Mar 2026 08:09:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 04 Mar 2026 08:09:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 04 Mar 2026 08:09:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 04 Mar 2026 08:09:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 04 Mar 2026 08:09:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 04 Mar 2026 08:09:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 04 Mar 2026 08:09:22 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 04 Mar 2026 08:09:22 GMT
ARG USER_HOME_DIR=/root
# Wed, 04 Mar 2026 08:09:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 04 Mar 2026 08:09:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 04 Mar 2026 08:09:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc74705b5205a118b6fdfc67d17a8b658c02f7792610bbbab1a9a9579b5bc8`  
		Last Modified: Tue, 17 Feb 2026 20:30:36 GMT  
		Size: 13.8 MB (13799621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd684dbabc3e65069e0d389054b4f2c6b49b2a038dbc488e741ed738b8a57ecd`  
		Last Modified: Wed, 04 Mar 2026 07:57:06 GMT  
		Size: 225.0 MB (224996747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c673ef401564b30958dd065e104d4509269106c2c10e5990c7570d5e3bbbd4de`  
		Last Modified: Wed, 04 Mar 2026 07:57:01 GMT  
		Size: 4.5 MB (4479992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d8626f1b638326a8b8cce2be9106b6023652c993e04abdae0e5d082a2ac4de`  
		Last Modified: Wed, 04 Mar 2026 08:09:46 GMT  
		Size: 27.3 MB (27290124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916b4f8cb3c07b7196dc763a5973bc6fcb41a9623b1c437273f7f39bafaae7ff`  
		Last Modified: Wed, 04 Mar 2026 08:09:45 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e09fd59afc129f508fd15ddca8f9b88970fe74dec50700b4fe42be338ea9275`  
		Last Modified: Wed, 04 Mar 2026 08:09:45 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37342045c5c43a184a37ae810535144a3ea13b8c767dbf77332e2ba0726d743`  
		Last Modified: Wed, 04 Mar 2026 08:09:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:3a84874fe447e73d50191844b16d1c0c024f91d9f12216a84f0ef420c57a37b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4830222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73d8112fb97263ea1a65bb9088d549fec5f73e970843ebb82a9afec4d8cf32b`

```dockerfile
```

-	Layers:
	-	`sha256:131fe52af99a7c9ceb306f0b8b242d4f9f5911eeca79f9582322d53de6297fed`  
		Last Modified: Wed, 04 Mar 2026 08:09:45 GMT  
		Size: 4.8 MB (4811112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e942cae501bba504f494cc981c6e031491d28c3bd9d611d6dfbf9af935d528ee`  
		Last Modified: Wed, 04 Mar 2026 08:09:45 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-11-noble` - linux; s390x

```console
$ docker pull maven@sha256:0cb37e92d20cfdfaae417193054e541519b34755f60ed42d5e9bd8f097920b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301346248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866a259ed6655f8f42b1f4f14dacb5a4e7b20052baaf80da54be6a9672b8e6a3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:17:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:17:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:17:22 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Tue, 03 Mar 2026 21:24:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a9fb6a2524378d7f49913406eded71013d9de853009a3e6df58fb27fa6fb727b';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='89a4d7d40cdd82bbbc9bbf4e24c23062eb137cadc9a1958a890282e158696691';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='477c31aabf2862ef40c1210384ad4643d0d52bf381aa9399ca872e46dcdde9ee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='bba879725fa70ab38b021a984f6617477c18ad1fe1a153b0b230474e09dd0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 21:24:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 21:24:05 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 21:25:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Mar 2026 21:25:10 GMT
CMD ["jshell"]
# Tue, 03 Mar 2026 22:24:37 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 22:24:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 22:24:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 22:24:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 22:24:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 22:24:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 22:24:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 22:24:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 22:24:37 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 22:24:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 22:24:37 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 22:24:37 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 22:24:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 22:24:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 22:24:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2ce3b2a70015000a5b0ceaa4885f1aceec67cb23d3ef542311e0f5506c39b0`  
		Last Modified: Tue, 17 Feb 2026 20:19:02 GMT  
		Size: 13.1 MB (13118433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66435f803c4529252175de4527cef86dd749f49fd080d7c4aacf8b48fd3267e9`  
		Last Modified: Tue, 03 Mar 2026 21:25:43 GMT  
		Size: 219.0 MB (219005647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b528345800a9e9861fc3ac674e8df53ef8a667acc88c5560e68672e79526d7`  
		Last Modified: Tue, 03 Mar 2026 21:25:39 GMT  
		Size: 5.7 MB (5710223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb6d5d960619d2e23517c7a54f4891fb1fe38dd2f99a09367c0b340959d8ac4`  
		Last Modified: Tue, 03 Mar 2026 22:24:54 GMT  
		Size: 24.3 MB (24288880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4645836b9467cd57f9787c5dee5764e0310764d971234561695d8c7ca60cf4e`  
		Last Modified: Tue, 03 Mar 2026 22:24:54 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34e6f9470f0b11181c585825502c6ba232b75d0ff500fdf33923b6ab98e5ae2`  
		Last Modified: Tue, 03 Mar 2026 22:24:54 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa68c6f174e2a3912f312f0db6530498dca59e148eacf6f49a1fadd161b5647`  
		Last Modified: Tue, 03 Mar 2026 22:24:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-11-noble` - unknown; unknown

```console
$ docker pull maven@sha256:0aa6540b008a0c80c5f5421df6952b25349fad80cc0a66d0a7563b555a294783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4824536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681e00e30bbc8b60380fc667b05791d42b554c943130f2879c4d6fe1a5b2d9a0`

```dockerfile
```

-	Layers:
	-	`sha256:8df4f05d49ddd1feb373315038ee148bfacbce316384ec06b1fceb66f09919b4`  
		Last Modified: Tue, 03 Mar 2026 22:24:54 GMT  
		Size: 4.8 MB (4805476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f6913e261cca6efc4563f5c065611527b7c4efa4baa633e56c5f2e90de097f`  
		Last Modified: Tue, 03 Mar 2026 22:24:54 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json
