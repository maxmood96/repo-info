## `maven:3-ibm-semeru-21-noble`

```console
$ docker pull maven@sha256:63b453701d8e0a4c14dc138efa7d46d3235a156fb80fd16342bb554b00b456db
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
$ docker pull maven@sha256:fc106e21088744ba8cdd90405ce407b94cc0716111f7215205bd7e041304f891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329130119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5293685a0a427113a222e102267ff2e0094a5200873c202376bcba91870aea10`
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
# Mon, 09 Feb 2026 20:07:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:07:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:07:39 GMT
ENV JAVA_VERSION=jdk-21.0.10+7_openj9-0.57.0
# Mon, 09 Feb 2026 20:07:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='35baeac85832c46fe9bd93cdf8a9b1b2dbaa08eb7eb74fa9ad3fba0e1ce05560';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f7f971225362cac4170f601795da97371746ccddc9fa6ea937b83f08bb901b03';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='851215d482bcfb4c71ff576810fd086bf6e7359cee252d93d82c4929ad53c6eb';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='5dcf896cb3ef72623e6e190d3fe72521a46dcab358984179e8c4addd0f7d11ff';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:07:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:07:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:08:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 21:16:43 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 21:16:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Feb 2026 21:16:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 21:16:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 21:16:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Feb 2026 21:16:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Feb 2026 21:16:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Feb 2026 21:16:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Feb 2026 21:16:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Feb 2026 21:16:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Feb 2026 21:16:43 GMT
ARG MAVEN_VERSION=3.9.12
# Mon, 09 Feb 2026 21:16:43 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Feb 2026 21:16:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Feb 2026 21:16:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Feb 2026 21:16:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91190a3dc5d85ae41d8c130d4094a79347b8671e0fe8a5ddc1356ad7852def`  
		Last Modified: Mon, 09 Feb 2026 20:09:08 GMT  
		Size: 21.3 MB (21297022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8319bf3d0b06944374241b30308cb20f94262bf45a8b40bae85e792dbc836408`  
		Last Modified: Mon, 09 Feb 2026 20:09:13 GMT  
		Size: 239.8 MB (239824872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bf7108fecb87f97db9f667778fdbc68cfc213217c6ffdc9cba9aa85a30c871`  
		Last Modified: Mon, 09 Feb 2026 20:09:07 GMT  
		Size: 6.4 MB (6401924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4018264e97f761f7412ecc4a014eb5260f428ce8b75f010f987007dfc290693c`  
		Last Modified: Mon, 09 Feb 2026 21:16:58 GMT  
		Size: 22.6 MB (22566997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085c711f4bcdcff87012d71ca4a188c45686a747f2d173cc8c44a39e44cd1284`  
		Last Modified: Mon, 09 Feb 2026 21:16:57 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fa5959c66941781fab1412f408d6268aabd229b085c49b0829aad9d1231855`  
		Last Modified: Mon, 09 Feb 2026 21:16:57 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513fefc16c8c78908d23f05e58909dfc5c878d67557e731ba319e53f83e8e13f`  
		Last Modified: Mon, 09 Feb 2026 21:16:57 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:77938e561a26eed741c651394b8864c4f2cd3c6a026e6a0ff798fc55155e4982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4809497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd284b84a394e4b245ffee5a31fed9f4229f0b31faf9b1553c967e819f306bed`

```dockerfile
```

-	Layers:
	-	`sha256:8fafdcbf742c34bf3eafcf4e87f52d81a90cad9d2d008f52b22400ab7db3dfe4`  
		Last Modified: Mon, 09 Feb 2026 21:16:57 GMT  
		Size: 4.8 MB (4790441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d4e4c3e5a147b6ee36670799606b8c7511c22e8cf50b5d8bbf47be66f889df8`  
		Last Modified: Mon, 09 Feb 2026 21:16:57 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-21-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5ba87b03854374b70bab39f7af9148b20079e555fb9fcd97651c5b4ba995df45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323881317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4126ccacdaf41a24ce193d967db6ecd7476a6b2c1dc6f0ac2ed5bbca7dc10a45`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:06:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:06:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:06:12 GMT
ENV JAVA_VERSION=jdk-21.0.10+7_openj9-0.57.0
# Mon, 09 Feb 2026 20:07:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='35baeac85832c46fe9bd93cdf8a9b1b2dbaa08eb7eb74fa9ad3fba0e1ce05560';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f7f971225362cac4170f601795da97371746ccddc9fa6ea937b83f08bb901b03';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='851215d482bcfb4c71ff576810fd086bf6e7359cee252d93d82c4929ad53c6eb';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='5dcf896cb3ef72623e6e190d3fe72521a46dcab358984179e8c4addd0f7d11ff';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:07:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:07:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:08:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 21:16:16 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 21:16:16 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Feb 2026 21:16:16 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 21:16:16 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 21:16:16 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Feb 2026 21:16:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Feb 2026 21:16:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Feb 2026 21:16:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Feb 2026 21:16:16 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Feb 2026 21:16:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Feb 2026 21:16:16 GMT
ARG MAVEN_VERSION=3.9.12
# Mon, 09 Feb 2026 21:16:16 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Feb 2026 21:16:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Feb 2026 21:16:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Feb 2026 21:16:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e796ea7c8223bf8e5ff125e7b109a1ef6dcf359ecf05ecb7d04c6ac11f1dd8d2`  
		Last Modified: Mon, 09 Feb 2026 20:07:29 GMT  
		Size: 20.9 MB (20913345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3578dd3855eece19a2558a4b6c2b3905d95dca2b315844eebd69e367ccd0f94`  
		Last Modified: Mon, 09 Feb 2026 20:09:18 GMT  
		Size: 236.0 MB (236048127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e840413ce8f8c4a77d3b20235fe4ac32f1d1aeaa392c9cf7cad94ce5c2c0c584`  
		Last Modified: Mon, 09 Feb 2026 20:09:13 GMT  
		Size: 6.1 MB (6107380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0714fae1bb400f07afd6703a4bd750f57233e64c4b39b4a2913fac815d801a`  
		Last Modified: Mon, 09 Feb 2026 21:16:30 GMT  
		Size: 22.6 MB (22635360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43280ef18ef95de0533cdbedabf78e6cec19e1d313472b128b9fdd30d3eaabf5`  
		Last Modified: Mon, 09 Feb 2026 21:16:30 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddef27f1260510dca1cd93aa9608e3c93b4c655a2aaf8e99aa8004f4eeeb87b`  
		Last Modified: Mon, 09 Feb 2026 21:16:29 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b90621aa43c17e7a2a26b2dd7183f5b41fc50927a985d80c8a883bbf6b5b3f`  
		Last Modified: Mon, 09 Feb 2026 21:16:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:202be05ca02c3edc338f5379d04cac2d79e61adce541f43bc93ed73084dd8b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4814236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6ececd909572e10609fd23daa32c312a42769b8272bb605d6bebd0a4aa303f`

```dockerfile
```

-	Layers:
	-	`sha256:c8f7c3cd46ef0eaccd04247bf3ce5035b4d495f739fd1efe225e8cf7a0731170`  
		Last Modified: Mon, 09 Feb 2026 21:16:29 GMT  
		Size: 4.8 MB (4795047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:889205683886d2946e34e6ffa3a9b38f1efd9bc91b8b84d64f1696ef0d9c3007`  
		Last Modified: Mon, 09 Feb 2026 21:16:29 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-21-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:de2fe3e7ca04b5e09b4e4c4c1cd195c6da3904d2d07182af6e69fc2f8c1d80cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342507722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1796e9ce6f9938a58a7020c7b474dd6742c7a1722995d580d9aeb095697b47`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:34:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:34:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:34:09 GMT
ENV JAVA_VERSION=jdk-21.0.10+7_openj9-0.57.0
# Mon, 09 Feb 2026 20:44:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='35baeac85832c46fe9bd93cdf8a9b1b2dbaa08eb7eb74fa9ad3fba0e1ce05560';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f7f971225362cac4170f601795da97371746ccddc9fa6ea937b83f08bb901b03';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='851215d482bcfb4c71ff576810fd086bf6e7359cee252d93d82c4929ad53c6eb';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='5dcf896cb3ef72623e6e190d3fe72521a46dcab358984179e8c4addd0f7d11ff';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:44:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:45:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 21:39:35 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 21:39:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Feb 2026 21:39:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 21:39:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 21:39:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Feb 2026 21:39:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Feb 2026 21:39:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Feb 2026 21:39:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Feb 2026 21:39:36 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Feb 2026 21:39:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Feb 2026 21:39:37 GMT
ARG MAVEN_VERSION=3.9.12
# Mon, 09 Feb 2026 21:39:37 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Feb 2026 21:39:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Feb 2026 21:39:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Feb 2026 21:39:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca127b638f72ed7f9e1f454f0122c3723c277c84c84220dabb2fe7b41220d548`  
		Last Modified: Mon, 09 Feb 2026 20:36:03 GMT  
		Size: 23.3 MB (23280007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a032a5b06cc2073c1c98c51fd51473ff459c970a977c2959149b23dc4789d`  
		Last Modified: Mon, 09 Feb 2026 20:46:12 GMT  
		Size: 243.8 MB (243763456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e8b76b664309c8de013c0721d15826cb9f69fc7ca9840df55f1fc81b3f9485`  
		Last Modified: Mon, 09 Feb 2026 20:46:06 GMT  
		Size: 5.2 MB (5232527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2db40adb295c4df6168a551598da85c47daf49b2115363c1bd052dd7e79b695`  
		Last Modified: Mon, 09 Feb 2026 21:40:11 GMT  
		Size: 26.6 MB (26612286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10953d726575a0a531f6aa39339103b322d88d2c2de54e64cb72e4bdea4bb79`  
		Last Modified: Mon, 09 Feb 2026 21:40:10 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8676baf54c31e594c7c7e7fd323d026021d2963695674418364ae38ad9b9db`  
		Last Modified: Mon, 09 Feb 2026 21:40:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408cef418b703e0018cc22751de083f29789c6ec212d7246e10213ae8caaa122`  
		Last Modified: Mon, 09 Feb 2026 21:40:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:5f701faae35a8643a82e617b59c730f6cbd4bbe66646911bd841b1e1f694ca4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4816970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4994ffe9393329c1ef812fae546d9048edcb8e7fa68c1b24c17ef3f218110e4`

```dockerfile
```

-	Layers:
	-	`sha256:25e361c1e788d9352ab46ffceb090db4f7dd1e1bb5f3bf8c3aed2e3391566048`  
		Last Modified: Mon, 09 Feb 2026 21:40:10 GMT  
		Size: 4.8 MB (4797864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f1aea8b21fb28833d0a3f5d3eb66d362fb988fd8a033eb5e80b15cafbe9bf7`  
		Last Modified: Mon, 09 Feb 2026 21:40:10 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-21-noble` - linux; s390x

```console
$ docker pull maven@sha256:56f67dfe4fa167e3c445fa6d7f3184df27231f8e601009c9a4ee70eb03b3cd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327235681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcef3ac2a2cff8349124eb9b9c2f0375b9aef8c35eea69ade4f99388a5854aa`
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
# Mon, 09 Feb 2026 20:11:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Feb 2026 20:11:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:11:01 GMT
ENV JAVA_VERSION=jdk-21.0.10+7_openj9-0.57.0
# Mon, 09 Feb 2026 20:11:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='35baeac85832c46fe9bd93cdf8a9b1b2dbaa08eb7eb74fa9ad3fba0e1ce05560';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_aarch64_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f7f971225362cac4170f601795da97371746ccddc9fa6ea937b83f08bb901b03';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_x64_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='851215d482bcfb4c71ff576810fd086bf6e7359cee252d93d82c4929ad53c6eb';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='5dcf896cb3ef72623e6e190d3fe72521a46dcab358984179e8c4addd0f7d11ff';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.10%2B7_openj9-0.57.0/ibm-semeru-open-jdk_s390x_linux_21.0.10_7_openj9-0.57.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 09 Feb 2026 20:11:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:11:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 09 Feb 2026 20:12:08 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 09 Feb 2026 21:18:09 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 21:18:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Feb 2026 21:18:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 21:18:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Feb 2026 21:18:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Feb 2026 21:18:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Feb 2026 21:18:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Feb 2026 21:18:10 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Feb 2026 21:18:10 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Feb 2026 21:18:10 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Feb 2026 21:18:10 GMT
ARG MAVEN_VERSION=3.9.12
# Mon, 09 Feb 2026 21:18:10 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Feb 2026 21:18:10 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Feb 2026 21:18:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Feb 2026 21:18:10 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7c7cad99caef52ede636ac1355f65db6d1c6c6122f538f2519f19091e57987`  
		Last Modified: Mon, 09 Feb 2026 20:12:37 GMT  
		Size: 20.5 MB (20450262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf8a6e21772f2c7aa34d42e7ebb5d43a86f8f1aab89d5e87bf9899884155deb`  
		Last Modified: Mon, 09 Feb 2026 20:12:42 GMT  
		Size: 237.3 MB (237316016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078ba730ecdca801c5efc36f1c94f82f16e5e4cb8c0414daa249852d15f19f7`  
		Last Modified: Mon, 09 Feb 2026 20:12:37 GMT  
		Size: 6.6 MB (6551115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bf02a14a6ea7dfbeb5add2bcc34995219e723ada038619c83a0053a305f051`  
		Last Modified: Mon, 09 Feb 2026 21:18:33 GMT  
		Size: 23.7 MB (23695806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbec69ff4ec04c99ff248052e0b035bbac32ffb8de3d5656d8594e99d3ad546`  
		Last Modified: Mon, 09 Feb 2026 21:18:33 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251773b8851624eed9fd88d8248c01465261397b968da806ec8abd58d7a25af5`  
		Last Modified: Mon, 09 Feb 2026 21:18:33 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1fae8380ab40c0e203c887d810d7302bd645f8b830c9201000dc1eaaf6f359`  
		Last Modified: Mon, 09 Feb 2026 21:18:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-21-noble` - unknown; unknown

```console
$ docker pull maven@sha256:ed74b34d61a19bc2e408493535022025e8bfab86c2e85b17dc1f1881e2a6ba9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4811284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebee8716e92ec97292f299ab51d295ff7bcee24151febf71b556e29409b37eff`

```dockerfile
```

-	Layers:
	-	`sha256:b298fa5de3bb890ec273738758d6cc2e7ea8f0c588d9c637ae9fb502268a44d3`  
		Last Modified: Mon, 09 Feb 2026 21:18:33 GMT  
		Size: 4.8 MB (4792228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede9e55c9e56a0464302c2d795c638622f3565aa6daf49b5faedce881542b5f3`  
		Last Modified: Mon, 09 Feb 2026 21:18:33 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json
