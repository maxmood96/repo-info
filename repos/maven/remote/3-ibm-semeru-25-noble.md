## `maven:3-ibm-semeru-25-noble`

```console
$ docker pull maven@sha256:1586ce80f65129b84fbb2034c524523559500b7d18472993a62cc397502f85c2
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

### `maven:3-ibm-semeru-25-noble` - linux; amd64

```console
$ docker pull maven@sha256:b96c03157f9bdfcd770a44b663437873f5578c7432648164231510bdfc2a1bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.2 MB (329158074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a408fc2aa0acd0f69e6a094e616dd5503b3900dabc45763ca173d462bbcbe74f`
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
# Tue, 07 Apr 2026 01:56:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:56:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:56:49 GMT
ENV JAVA_VERSION=jdk-25.0.2+10.1_openj9-0.57.0
# Tue, 07 Apr 2026 01:57:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='08fe20fbcb5c5ad8d9f32ce4c9aaa42388aeea30b2f16dcb4d28acd50df99375';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_25.0.2.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eda3cce037d291e78ea4228e50b1a6b79e9e95cf6cfabc939305c1b25042509e';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_25.0.2.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de8401f40bfc667174ecc02fbcb51dbf85e476d4542684210659f51231dbaa4b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_25.0.2.1.tar.gz';          ;;        s390x)          ESUM='45333a107e8364b10cf1b924ae8efd5ff202ad7a376417fb2cb33bbdecb606b5';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_25.0.2.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 01:57:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:57:00 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 01:58:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 01:58:06 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:07:10 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:07:10 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:07:10 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:07:10 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:07:10 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:07:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:07:10 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:07:10 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:07:10 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:07:10 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:07:10 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:07:10 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:07:10 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:07:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:07:10 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c01a03597da9cad21f448e97a18e20a5c88b4db9864256812cc973259b09d15`  
		Last Modified: Tue, 07 Apr 2026 01:58:28 GMT  
		Size: 12.8 MB (12805566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bf4873a602f7e609eec6c27058e669346c3cba838f74c7c03d8ca333a6aa59`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 248.1 MB (248103601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35262cec0594bf9d62e37d53a183b7041311c733c742aa0e1777ef8fdb5e5db`  
		Last Modified: Tue, 07 Apr 2026 01:58:27 GMT  
		Size: 6.6 MB (6633990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00db906d116ec9475e08c57ad6741ea959aef19228cb8f8d5f736155ada7ed53`  
		Last Modified: Tue, 07 Apr 2026 05:07:23 GMT  
		Size: 22.6 MB (22569230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b40a170f7262a501206297b94d65b8b81e426e76550fc751abedea5bf9447`  
		Last Modified: Tue, 07 Apr 2026 05:07:23 GMT  
		Size: 9.3 MB (9311190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fb5e9be07607013ec7360a1b2f85e58f2c47dccf9bf95f64df4b426feab9fc`  
		Last Modified: Tue, 07 Apr 2026 05:07:23 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9cef306fd5a468dc70ed144d808364b2a85b473a61370fcb2abbdbbcbfa92c`  
		Last Modified: Tue, 07 Apr 2026 05:07:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:ad4a5fbd5b76133bbf360c2cc87c457a4ed483e96d603db50482bff2bf4a6638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4816497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4e9fa474541a32ed5793d774054f1ee75563e5a8d91c2a237ef43f2008f5ec`

```dockerfile
```

-	Layers:
	-	`sha256:91f802ae31a0bd141b577dc40204262681a17d976917ac53219176e1df17cdb5`  
		Last Modified: Tue, 07 Apr 2026 05:07:23 GMT  
		Size: 4.8 MB (4797437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b108a4508338a064c9a7d25ee9d96dc6be88257a3b534ae83513a07388e52b5f`  
		Last Modified: Tue, 07 Apr 2026 05:07:22 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-25-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a59b4c972a0e2686b17221bf18fa3d1bb94ee94f13e8d93ba4202b94d7097b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324509263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5c29ef9c5e26159ca6a3f7831bc81f9185e52bc695b84af01cf39f4e043ff3`
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
# Tue, 07 Apr 2026 02:00:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:00:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:16 GMT
ENV JAVA_VERSION=jdk-25.0.2+10.1_openj9-0.57.0
# Tue, 07 Apr 2026 02:00:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='08fe20fbcb5c5ad8d9f32ce4c9aaa42388aeea30b2f16dcb4d28acd50df99375';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_25.0.2.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eda3cce037d291e78ea4228e50b1a6b79e9e95cf6cfabc939305c1b25042509e';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_25.0.2.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de8401f40bfc667174ecc02fbcb51dbf85e476d4542684210659f51231dbaa4b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_25.0.2.1.tar.gz';          ;;        s390x)          ESUM='45333a107e8364b10cf1b924ae8efd5ff202ad7a376417fb2cb33bbdecb606b5';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_25.0.2.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 02:00:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:00:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 02:01:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 02:01:37 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:13:07 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:13:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:13:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:13:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:13:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:13:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:13:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:13:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:13:08 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:13:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:13:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:13:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43344d02966b3ba60e2370d0e1b467c9e94f68fd5a6d2fd767ac39828aafb5d9`  
		Last Modified: Tue, 07 Apr 2026 02:02:00 GMT  
		Size: 12.8 MB (12837714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6589278a4820ce67138b8cc8e206ce69853de118477dcc8ab75462e1ba2869a2`  
		Last Modified: Tue, 07 Apr 2026 02:02:09 GMT  
		Size: 244.3 MB (244309291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5838181f5f6fe689fb5d00a4e4b9280a10bf066da730192e881074236822151`  
		Last Modified: Tue, 07 Apr 2026 02:01:59 GMT  
		Size: 6.5 MB (6539017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f05bdcdd7d501c9112f25a621cff3bfd95c28bde849c77d73f6b61e18b33b17`  
		Last Modified: Tue, 07 Apr 2026 05:13:21 GMT  
		Size: 22.6 MB (22636957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6830c15ad1270b3e8ebac36278af5481e04b139ebfaee842efc0d71d9e35ad58`  
		Last Modified: Tue, 07 Apr 2026 05:13:21 GMT  
		Size: 9.3 MB (9311173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26642658c47126069525a2edd4958b12c8d9c663682ee419d048ac430dc9a8f6`  
		Last Modified: Tue, 07 Apr 2026 05:13:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce2092da7e5eadae48a63d3d7c42bad288d4460a36415e6959025cb93a3a9d9`  
		Last Modified: Tue, 07 Apr 2026 05:13:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:959d398e07b91dff6ecabf5116b44792ef4c6c5e0d1ccff8ad2f8c99c5310ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4821236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5739754d224b2831c2580f95d270acd5e3384f0e8f9841e8a37b33199e0f1c5`

```dockerfile
```

-	Layers:
	-	`sha256:1f44952954fb1af5e9b83529cef9dadfaab2f1529f9fb133bbb5d0ecddeae40a`  
		Last Modified: Tue, 07 Apr 2026 05:13:21 GMT  
		Size: 4.8 MB (4802043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66219310453294e3f7430746544b77210ed19f5804246574d1dc437265a6a360`  
		Last Modified: Tue, 07 Apr 2026 05:13:20 GMT  
		Size: 19.2 KB (19193 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-25-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:c4d69595e60e7d6b6b1055de1565bbeacf59e1ee1b38154ce708021a2ee3f6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341184613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d446da7fe433b8b440a65de74e7da22bca8300a932b0215b4e1fc418d28a0b89`
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
ENV JAVA_VERSION=jdk-25.0.2+10.1_openj9-0.57.0
# Tue, 17 Mar 2026 08:57:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='08fe20fbcb5c5ad8d9f32ce4c9aaa42388aeea30b2f16dcb4d28acd50df99375';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_25.0.2.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eda3cce037d291e78ea4228e50b1a6b79e9e95cf6cfabc939305c1b25042509e';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_25.0.2.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de8401f40bfc667174ecc02fbcb51dbf85e476d4542684210659f51231dbaa4b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_25.0.2.1.tar.gz';          ;;        s390x)          ESUM='45333a107e8364b10cf1b924ae8efd5ff202ad7a376417fb2cb33bbdecb606b5';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_25.0.2.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 08:57:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:57:20 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 08:58:27 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 08:58:27 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 22:07:11 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 22:07:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 22:07:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:07:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:07:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 22:07:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 22:07:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 22:07:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 22:07:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 22:07:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 22:07:18 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 22:07:18 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 22:07:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 22:07:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 22:07:18 GMT
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
	-	`sha256:9ff4e8e994c38243368198baca8be1f54fc542de6faac48c97ec80f1c82f1f86`  
		Last Modified: Tue, 17 Mar 2026 08:59:16 GMT  
		Size: 251.7 MB (251690508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f785530d45172f525167056f54e13ff75871c34bc572c4ccf23471d509405e9f`  
		Last Modified: Tue, 17 Mar 2026 08:59:11 GMT  
		Size: 5.5 MB (5473066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9893b95b602ebf94f1e1fd3cba9f8103932f9d15c6015858c3539f6bf1dba2de`  
		Last Modified: Tue, 17 Mar 2026 22:07:47 GMT  
		Size: 26.6 MB (26610869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119d61d3fbb74033146dedbd33d5ec63286f6f81716ecb0bff6b7a1d96e46dbc`  
		Last Modified: Tue, 17 Mar 2026 22:07:47 GMT  
		Size: 9.3 MB (9311181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0112d53bac95871edacd8994d9e08ef61c30e9323a14afe1ff9c1bd06c9b99`  
		Last Modified: Tue, 17 Mar 2026 22:07:46 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dba512622a0b3b697bb7dc744142c7c2b2a30a8fe1fffe4768d17fde3a454e0`  
		Last Modified: Tue, 17 Mar 2026 22:07:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:1e5205e28ee0f116774934a670f7e76421e228e69bffaaeafc32aaef70fa6915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4810934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c39fc51ea537cada1bea68f5c437a08559de40b4ad2f0b699ae1fbdb7de468`

```dockerfile
```

-	Layers:
	-	`sha256:fc53d1afeed22f721a635c988bec595f5d73a4413e45621cedea06a38b0631fb`  
		Last Modified: Tue, 17 Mar 2026 22:07:46 GMT  
		Size: 4.8 MB (4791824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:804dcdf2d3870e3b5d18bef5486eaa624c641e5fd15f2b609b01a98f01ce94b5`  
		Last Modified: Tue, 17 Mar 2026 22:07:46 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-25-noble` - linux; s390x

```console
$ docker pull maven@sha256:837f4df323aeb7aec1c31c90db1c9bd29162b84bf7cebc7454c363491e5216b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328234530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d1e33dcaf8f662586197a339f3e3fb8aac70818c02c51b2cedec225054086`
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
ENV JAVA_VERSION=jdk-25.0.2+10.1_openj9-0.57.0
# Tue, 07 Apr 2026 03:18:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='08fe20fbcb5c5ad8d9f32ce4c9aaa42388aeea30b2f16dcb4d28acd50df99375';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_25.0.2.1.tar.gz';          ;;        amd64|x86_64)          ESUM='eda3cce037d291e78ea4228e50b1a6b79e9e95cf6cfabc939305c1b25042509e';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_25.0.2.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='de8401f40bfc667174ecc02fbcb51dbf85e476d4542684210659f51231dbaa4b';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_25.0.2.1.tar.gz';          ;;        s390x)          ESUM='45333a107e8364b10cf1b924ae8efd5ff202ad7a376417fb2cb33bbdecb606b5';          BINARY_URL='https://github.com/ibmruntimes/semeru25-binaries/releases/download/jdk-25.0.2+10.1_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_25.0.2.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 03:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:18:05 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 03:19:25 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 03:19:25 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 09:48:41 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:48:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 09:48:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 09:48:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 09:48:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 09:48:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 09:48:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 09:48:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 09:48:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 09:48:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 09:48:41 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 09:48:41 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 09:48:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 09:48:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 09:48:41 GMT
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
	-	`sha256:465a032fc4ffc3184cd878adb7b8804c12dcc4402264fac9ec1f2d870756c16f`  
		Last Modified: Tue, 07 Apr 2026 03:19:58 GMT  
		Size: 245.2 MB (245234527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecec7c47c2fcb0d1eec31b28508a83cbd23669e190029b0c76124285af28d5b`  
		Last Modified: Tue, 07 Apr 2026 03:19:53 GMT  
		Size: 7.0 MB (6960031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f66c15fd919da34ad8483a2b9412b15627bf88ccc47a6d6112cc5d8d15dfea`  
		Last Modified: Tue, 07 Apr 2026 09:49:03 GMT  
		Size: 23.7 MB (23698506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c86d31c44b8dc4dc4c3b4517faf97ed8e7e4d8f79df4eb0de52b8428313a9c9`  
		Last Modified: Tue, 07 Apr 2026 09:49:02 GMT  
		Size: 9.3 MB (9311188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e5b04174aae63912c4111c3be2e41e7bf6cb965bb984830a5341fc59498b9e`  
		Last Modified: Tue, 07 Apr 2026 09:49:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b9b1ba817c8d1e70defd2e41031bc58896d75a6c037d7d8a40bb8ee7ae9ad2`  
		Last Modified: Tue, 07 Apr 2026 09:49:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-25-noble` - unknown; unknown

```console
$ docker pull maven@sha256:759f571c01eb72e2f46e8438f19aad565bf0fa270c4d28c73f9be256599df746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4805248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f38c49ee90691bea85a05a39ddce8987a38888234c80956239e0774775dc4a`

```dockerfile
```

-	Layers:
	-	`sha256:28d85a6fb2e6279e8db46ec24a191f16046d9a0876c3e780a32a777aa287a4a0`  
		Last Modified: Tue, 07 Apr 2026 09:49:02 GMT  
		Size: 4.8 MB (4786188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8043ad1bd371c8a62843658bfc6ee57d5cb24f9191cce56639b29b3cad011d5`  
		Last Modified: Tue, 07 Apr 2026 09:49:02 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json
