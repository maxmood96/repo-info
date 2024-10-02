## `maven:3-ibm-semeru-23-jammy`

```console
$ docker pull maven@sha256:a508cd0e82c5e8a9c86dafc47b179cf26516b14a15b8463748f87d472e037ab8
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

### `maven:3-ibm-semeru-23-jammy` - linux; amd64

```console
$ docker pull maven@sha256:dc0970abe2d24154b53acd11b13415a14ab3eb104ef228c218fb794300b73379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.4 MB (314397103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550c730fb899209363c433094b4aaa3434445f546675504d195e4877608105e8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ae78453c065c270e34634dcd46d95df82c3ed10f0117b8698b37b287372a5f`  
		Last Modified: Thu, 19 Sep 2024 20:01:57 GMT  
		Size: 12.2 MB (12156513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c2ab4976295f8e17787aa1212b346f2e6db74e89e19273aa3a2314adba44f9`  
		Last Modified: Thu, 19 Sep 2024 20:02:03 GMT  
		Size: 236.5 MB (236532682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f075cb1d2c92b9840c51b2083bff3ff61b4609bc7f020dcd8dea9bb32f061da0`  
		Last Modified: Thu, 19 Sep 2024 20:01:57 GMT  
		Size: 6.7 MB (6666597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d8fc419cb30952029961468d098886f4eb98d8ee65e9d30c26758394ccc925`  
		Last Modified: Fri, 27 Sep 2024 19:56:06 GMT  
		Size: 20.3 MB (20334150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9deae347c59ed971fc60b60651216a5a030ffba2627555b05a61a7e191eb2f`  
		Last Modified: Fri, 27 Sep 2024 19:56:06 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71cb797f03b09f735a1f7e503ee455714bb6fc926b5fc097b67b40f64a7e1a7`  
		Last Modified: Fri, 27 Sep 2024 19:56:05 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd3dc5cec2d3f55b3afba01782cd1976de0c08ec8c0ac222ff3a49bf5bb5846`  
		Last Modified: Fri, 27 Sep 2024 19:56:05 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-23-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:2c3f8d0b02ed2f651845b8293fe45c54f0698a12b1256c3358f5072a3008e4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01cef3e6dab6f51379ac1178e8565a3ded5095cfc33575a173cc18dd68b7d32`

```dockerfile
```

-	Layers:
	-	`sha256:0c0a841fd7e6380b5ca9280ba51fb020f476abe55b68d47fbf6b2f6a35ca6622`  
		Last Modified: Fri, 27 Sep 2024 19:56:05 GMT  
		Size: 5.1 MB (5133454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc4fc3308ac84011e6f8e8870d7ab0101e6e677b5469e4059c11cadc223be711`  
		Last Modified: Fri, 27 Sep 2024 19:56:05 GMT  
		Size: 19.1 KB (19050 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-23-jammy` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5d512026896baf838bc92d1d2590faa0be6dfd5ed8e9f2d034305450875bbfcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303622476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2706cb2fdddffb9a7eb7007c71ec1c5224a6b51a949145582712c95add02f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3831940244be8baa42f9d6629360ed0326dedeb7d18134cfa77184874d97bf6f`  
		Last Modified: Tue, 17 Sep 2024 02:06:03 GMT  
		Size: 12.1 MB (12114299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a318895f6d0c5640bdd7f24d63ec0ba4546bd1b7683df7c5cb9b6b0adfe260`  
		Last Modified: Thu, 19 Sep 2024 20:21:38 GMT  
		Size: 228.2 MB (228229378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1ade44129ca53089092585103f93bdba6d258fdd611adec07ac2aea354c57c`  
		Last Modified: Thu, 19 Sep 2024 20:21:33 GMT  
		Size: 6.4 MB (6448455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597908a782526cb534ca18cec2e14a21cb19b6f0fb7b3010a04c81358d9ba864`  
		Last Modified: Sat, 28 Sep 2024 03:34:39 GMT  
		Size: 20.3 MB (20300536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc31b1993ce24ceb92c878ecf7c31062c4be73d6cca6402cb816d42fb120c81`  
		Last Modified: Sat, 28 Sep 2024 03:34:38 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5490a6bb47d727141f0f7c2d012ed64bcd6f03703a78a687ddaf2841c6c44e`  
		Last Modified: Sat, 28 Sep 2024 03:34:38 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb741cbc353a6fe790eac9ab46a97f1b288687ee07acf5b71ed865422bfa367d`  
		Last Modified: Sat, 28 Sep 2024 03:34:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-23-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:99f45910b855e42b6b73b9a702dbfc9fa95d31a025ce2c46b1552e26e5efd164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac06333de7036a0534fa31fc7d295137077df53cf18c5c27428a3c140052320`

```dockerfile
```

-	Layers:
	-	`sha256:ee60215865f4d65de22cfe54107378441847c8d571ccf62fe3dcdcae4ee062f8`  
		Last Modified: Sat, 28 Sep 2024 03:34:38 GMT  
		Size: 5.1 MB (5132224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df58274a44e66dadf09480c1db6d47683d817a32d5ef68d41ac814880a418a7`  
		Last Modified: Sat, 28 Sep 2024 03:34:38 GMT  
		Size: 19.8 KB (19774 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-23-jammy` - linux; ppc64le

```console
$ docker pull maven@sha256:3bf6e89138c8c9289e8206c4314a290dc7c37c01cf6772f595aea203aee656e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325520003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3dfd312121b705fe90ad2b088af580bacd33247fa49fdf66757e6df8fafc18`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6230a31e14b4a918b32fc7a3b685fad8ecafe0901deee916736d3e6f4db6ad`  
		Last Modified: Tue, 17 Sep 2024 01:15:01 GMT  
		Size: 12.9 MB (12888132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f7f35d3f88abadb816461639ffa8662b06fa138ba9aa56a020610115280e50`  
		Last Modified: Thu, 19 Sep 2024 20:28:56 GMT  
		Size: 239.7 MB (239670430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b408ff56ee65fe594b40f408250bc5d4463a0b7f801f70b6582578db270e23d3`  
		Last Modified: Thu, 19 Sep 2024 20:28:50 GMT  
		Size: 5.5 MB (5453139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f04c1295d184af0439e29d6a4cc9554c6b367ea793c6292fa651070ac1d038`  
		Last Modified: Sat, 28 Sep 2024 06:07:55 GMT  
		Size: 23.9 MB (23888570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12acb35d8a4aed31986863f4352dcd10345a44edbf2ee5e472571dcc525d0aad`  
		Last Modified: Sat, 28 Sep 2024 06:07:53 GMT  
		Size: 9.2 MB (9170451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f15621ab6b493ce38b297ed9765dd332a4127ca608419b06380d2414aab8840`  
		Last Modified: Sat, 28 Sep 2024 06:07:52 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ccfdb26c78fbbbc4c58a11bc16d1fedbf8b36c424390756f69dc69aecb10aa`  
		Last Modified: Sat, 28 Sep 2024 06:07:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-23-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:ec1c87614552478b7afa4c20259a55caec7ee24b59b7e046470049771e21b2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02971503c6c7a1e67d502e85869617e4ab61860d390b01a863e3fdde4f657817`

```dockerfile
```

-	Layers:
	-	`sha256:7981eb567146f35063cff06093740fff9299369fb105dafa185eca31ff579d37`  
		Last Modified: Sat, 28 Sep 2024 06:07:53 GMT  
		Size: 5.1 MB (5140679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe80cb780d3726c5d65462759c39d4d0485d4ee652a451233a0162c0df64c252`  
		Last Modified: Sat, 28 Sep 2024 06:07:51 GMT  
		Size: 19.1 KB (19130 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibm-semeru-23-jammy` - linux; s390x

```console
$ docker pull maven@sha256:7973badd63b247798fb27991dd83914135452cf19c30e5e396517042f1c72d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311373978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f113a5a4b063b61c9d9818cfd5e6b62ac0103e2cd9d824c15d08d9c14f0f1d4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 17:39:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Sep 2024 17:39:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d5f711ef416afb5e83c1ebcb9aa0e232b984d23c3abee9dd3fc8edab2832a881';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='95e1116a38567fa5b1799045f05d95bd23f419ff5c0baa2100d88f113a2cb48b';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='07cf7e80101d9d63d9b896f590f5df561a5868c3de0264e7b11c8d2c79cf20d2';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='d3841ef50ee457b2e20476923f861414cd23b38735945ffe3611120bdec6f841';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jdk_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Sep 2024 17:39:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 19 Sep 2024 17:39:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b18103153169c7bf98da055f8ba0ac3e141d121c78869881d3be480e90fcbc3a178a8e71fa70a11aee7f2584727df72be15d30331faec65f4e57c7e67c85c1cf";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.95/bin/apache-tomcat-9.0.95.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN apt-get update   && apt-get install -y git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d7fcbb74a18dbda1a95a881c01c2cc4d8a0d6fe38b3b4f8b5899f281f9815e`  
		Last Modified: Tue, 17 Sep 2024 01:57:02 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712edb58fe67e469374fb2ce21c840db351ab8a5e49aa67d587d408321ca94e1`  
		Last Modified: Thu, 19 Sep 2024 20:32:27 GMT  
		Size: 234.6 MB (234626082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0704172dfea2a31d7d5c96b0140fb259ea69bc42109e705fbc93f6a64b053c`  
		Last Modified: Thu, 19 Sep 2024 20:32:24 GMT  
		Size: 6.9 MB (6868736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd34e2b21a6c707ae9a7d09fe75c5aa48c93034f094175bd84c754dccba11ea9`  
		Last Modified: Wed, 02 Oct 2024 03:15:21 GMT  
		Size: 20.5 MB (20502468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fadabc2dc8380dc9e5fc837feef417403a701b5b2e792b5ca9ea3c36a3a043`  
		Last Modified: Wed, 02 Oct 2024 03:15:21 GMT  
		Size: 9.2 MB (9170422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced511925399d1cb1f92edb67dd40996030099657e5596ebe81fceac5fb9b6bc`  
		Last Modified: Wed, 02 Oct 2024 03:15:20 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd537ea261e0fda00dbfe81fc278023b85eecad93a26d965c206254cbbbd0a8`  
		Last Modified: Wed, 02 Oct 2024 03:15:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibm-semeru-23-jammy` - unknown; unknown

```console
$ docker pull maven@sha256:fc05afe8d6934a69a0ff88484b998e56897e5dc2eb63af8b34b5e03e4d73cae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14896ba631bf1ac411b125faf34c3d4c9e5b48bbabe0963f8a34daa442f650f3`

```dockerfile
```

-	Layers:
	-	`sha256:8463f7d8facd8bf2c7395c771be911b4f6564e55baddcd39ef6fdb8c694436a2`  
		Last Modified: Wed, 02 Oct 2024 03:15:20 GMT  
		Size: 5.1 MB (5134461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b8cf2ef673f0db65bf5ec2e0476ac5f7e2127dffe1575056e9b8ba29958a97e`  
		Last Modified: Wed, 02 Oct 2024 03:15:20 GMT  
		Size: 19.1 KB (19085 bytes)  
		MIME: application/vnd.in-toto+json
