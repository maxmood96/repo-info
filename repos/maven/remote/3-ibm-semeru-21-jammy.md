## `maven:3-ibm-semeru-21-jammy`

```console
$ docker pull maven@sha256:3df5b02bc3d6d50c984ae24ffb265727e12c7639625819f8a16d8cfb0bb9a4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-ibm-semeru-21-jammy` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1dea7e30e0147eff36bcc21903348bd3b02e1a6577c20920903d308fee227c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296494172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9854496ddbc7f8c25ab6e427102f1f929051b4dedf8b0fbe9e7913092aed9c16`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:04:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:04:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:08:58 GMT
ENV JAVA_VERSION=jdk-21.0.1+12_openj9-0.42.0
# Wed, 17 Jan 2024 07:09:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1a08663fe3dbf572d47fa9fbb068c43629982e30a0b21aaef8dceb306b6538c1';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.1%2B12_openj9-0.42.0/ibm-semeru-open-jdk_aarch64_linux_21.0.1_12_openj9-0.42.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ad575bc4b1fa9e9fa56661444b6153abfa147ec155845afa054472fa6357f026';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.1%2B12_openj9-0.42.0/ibm-semeru-open-jdk_x64_linux_21.0.1_12_openj9-0.42.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1da4674141be2deaa4effbe5cd7f5f935087f487c4cb1df26aff2ada1623073';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.1%2B12_openj9-0.42.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.1_12_openj9-0.42.0.tar.gz';          ;;        s390x)          ESUM='75324ae031427e18ecafc8139c250e4a59c4bc453f36eacc8df4222201f91af0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.1%2B12_openj9-0.42.0/ibm-semeru-open-jdk_s390x_linux_21.0.1_12_openj9-0.42.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jan 2024 07:09:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:09:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jan 2024 07:09:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 18 Jan 2024 13:37:30 GMT
RUN apt-get update   && apt-get install -y git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Jan 2024 13:37:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 18 Jan 2024 13:37:30 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Jan 2024 13:37:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Jan 2024 13:37:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Jan 2024 13:37:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d5742c9c31cbb7424e60c563307d1f6430ce374e15e840b77696a22c5a6727`  
		Last Modified: Wed, 17 Jan 2024 07:11:10 GMT  
		Size: 12.1 MB (12116817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639c19834ef445b05bedb4b0c2862ed0aa171c547bc1bbe469eed2de17c96254`  
		Last Modified: Wed, 17 Jan 2024 07:13:06 GMT  
		Size: 221.5 MB (221476769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bf77ff79cd74bde1ff360b4aa9a5e0c09da30a8ca71464689b7b057be6c626`  
		Last Modified: Wed, 17 Jan 2024 07:12:54 GMT  
		Size: 6.0 MB (6021945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0a1561a00b7352e9505ef26a01b7e55a505c608cf970dab39d152bbd48a6df`  
		Last Modified: Thu, 18 Jan 2024 19:14:56 GMT  
		Size: 19.0 MB (18997711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e737b521bb00ec360ef7e63cad1eaca61d10d3641f6db38378f427947a1c8ce8`  
		Last Modified: Thu, 18 Jan 2024 19:14:55 GMT  
		Size: 9.5 MB (9479944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd6c1d6a47d26e98ebf550bf3c3f4ec2c1d682263905f131c0443bdb8d5c89f`  
		Last Modified: Thu, 18 Jan 2024 19:14:54 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a949d2ea00392190c76543bc6c286cb345fac1a05fe1488d5ef6867ed5bb7405`  
		Last Modified: Thu, 18 Jan 2024 19:14:54 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1ee56445e68a882d5725a7c27b48c2679da184a50b4951cd3fd2169697c3e4`  
		Last Modified: Thu, 18 Jan 2024 19:14:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-21-jammy` - linux; ppc64le

```console
$ docker pull maven@sha256:586c6ce72dbd075105f30dfe8a6baa420cc61c54316837cf09351a13fe6810e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312003805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addebdfe722282f8d2c4f51ad4af6557519d97012e0bf93e55b9e086f2612c84`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 08:11:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 08:12:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 08:18:35 GMT
ENV JAVA_VERSION=jdk-21.0.1+12_openj9-0.42.0
# Wed, 17 Jan 2024 08:18:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='1a08663fe3dbf572d47fa9fbb068c43629982e30a0b21aaef8dceb306b6538c1';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.1%2B12_openj9-0.42.0/ibm-semeru-open-jdk_aarch64_linux_21.0.1_12_openj9-0.42.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ad575bc4b1fa9e9fa56661444b6153abfa147ec155845afa054472fa6357f026';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.1%2B12_openj9-0.42.0/ibm-semeru-open-jdk_x64_linux_21.0.1_12_openj9-0.42.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e1da4674141be2deaa4effbe5cd7f5f935087f487c4cb1df26aff2ada1623073';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.1%2B12_openj9-0.42.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.1_12_openj9-0.42.0.tar.gz';          ;;        s390x)          ESUM='75324ae031427e18ecafc8139c250e4a59c4bc453f36eacc8df4222201f91af0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.1%2B12_openj9-0.42.0/ibm-semeru-open-jdk_s390x_linux_21.0.1_12_openj9-0.42.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 17 Jan 2024 08:18:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 08:18:54 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 17 Jan 2024 08:19:28 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3f022ec8552bce1b72eb85d0778c93052ccb00226de3302544ec844ab93a9991e19c2db56ed06c18f03e5d75f34a46cedac46ae83bdd225518a55c62fc69ea04";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.83/bin/apache-tomcat-9.0.83.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 18 Jan 2024 13:37:30 GMT
RUN apt-get update   && apt-get install -y git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Jan 2024 13:37:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Jan 2024 13:37:30 GMT
ARG MAVEN_VERSION=3.9.6
# Thu, 18 Jan 2024 13:37:30 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Jan 2024 13:37:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Jan 2024 13:37:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Jan 2024 13:37:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65667c00b5fcfd11e7e44a89f1b0e57aad8c84c14d66d24807227d6ff9bf00da`  
		Last Modified: Wed, 17 Jan 2024 08:21:10 GMT  
		Size: 12.9 MB (12893691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae104270c3e6ebea8959d2e3bb389414e7c2acc492f619385ca94d1d92910e9`  
		Last Modified: Wed, 17 Jan 2024 08:23:35 GMT  
		Size: 226.8 MB (226768913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1227f7b405cf35f13b9ae9a2bfdad301408f8e2ce4f8edea31aec3b9bbf3df8`  
		Last Modified: Wed, 17 Jan 2024 08:23:19 GMT  
		Size: 5.1 MB (5119810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461fc17ed83124bf1b78b12fdabb6ba9b4c138bfd4269c5ba52c1ab32c356c8d`  
		Last Modified: Thu, 18 Jan 2024 19:00:15 GMT  
		Size: 22.1 MB (22082932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c021da0b7018e092f02b4f5c94cbef9d99187a35be06290384c78578e1ab2448`  
		Last Modified: Thu, 18 Jan 2024 19:00:12 GMT  
		Size: 9.5 MB (9479933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05170685859125cd945d62cc8f84386e8e183ef2eb0343d03edef19d33147b48`  
		Last Modified: Thu, 18 Jan 2024 19:00:11 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019d8ce7456151932bdb4a05aeec9b3d1a61a8425db48ff2026eafbdebfd5001`  
		Last Modified: Thu, 18 Jan 2024 19:00:11 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438c65d36730a763bddce847592d50e8a46878532016bae6d8345d3463d6e374`  
		Last Modified: Thu, 18 Jan 2024 19:00:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
