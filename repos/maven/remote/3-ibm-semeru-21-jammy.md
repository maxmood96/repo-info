## `maven:3-ibm-semeru-21-jammy`

```console
$ docker pull maven@sha256:18e8a0aea6732540a41bb5cb67b65bd93f9491d169cf875249944f04cc3c6249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-ibm-semeru-21-jammy` - linux; amd64

```console
$ docker pull maven@sha256:422a8318d1bf55728c9b32bd853d63cfe92963728734d89bbbf15fd4cd7c20e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301751002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dffaf90fe80cc262ee905a73316906d9c961392ee65bfc0fc83875127efe5dd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:44:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:45:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:54:28 GMT
ENV JAVA_VERSION=jdk-21.0.2+13_openj9-0.43.0
# Wed, 06 Mar 2024 02:54:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6404c5fe4a71049d4f80429720b7d3f3e3b0ebea8067b823a6bfb24b9fe69797';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_aarch64_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7a7a186a7a48537519917331ec91d9180b961dcc7ea0f627a23fa369edab6f16';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_x64_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='43d53cc8fbec42b1f47069178838e65ee5119ec992b511973db7badc51742674';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='15fa4c41c15fda8365d868621f75d8599cb8ea92537494c1a6d2fccb5b46c19f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_s390x_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Mar 2024 02:54:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:54:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Mar 2024 02:55:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
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
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6765038b5c8932c53e512c7ea92effec12ce3ed25e8ca9579cf3390b86bee564`  
		Last Modified: Wed, 06 Mar 2024 02:57:43 GMT  
		Size: 12.2 MB (12155916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf71eea64670b71a056987df363796922ab4845c60c378ceae2968e6db4ef4a`  
		Last Modified: Wed, 06 Mar 2024 03:01:48 GMT  
		Size: 224.3 MB (224295632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98eaa3b38c932865c4aff52fd67e5a992d11461d1c5e7b39e4934e745018f3e`  
		Last Modified: Wed, 06 Mar 2024 03:01:33 GMT  
		Size: 6.4 MB (6378359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32a5ff50600909039fc7256b65ed5cf6de8dac0ec4346a33aa7207b266e98b5`  
		Last Modified: Wed, 06 Mar 2024 06:22:28 GMT  
		Size: 19.0 MB (18988486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffab74d919c8722ad7a29b28df6e39657f165418a6918257e375488d1c2484b`  
		Last Modified: Wed, 06 Mar 2024 06:22:26 GMT  
		Size: 9.5 MB (9479939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7a325fa6c98aa5a741720ce2a035b569664d4c79e5e024b68268b987bd5651`  
		Last Modified: Wed, 06 Mar 2024 06:22:25 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bccd9e0ee562b67caa47d22d83433306f5b19956ec211e479f4536984e2a1f`  
		Last Modified: Wed, 06 Mar 2024 06:22:25 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ac9a525ccd0a807eb9f5f4ffcb9d0bfff91e0d883bb9302117c7ed1c54053e`  
		Last Modified: Wed, 06 Mar 2024 06:22:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-21-jammy` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e2477f90f33149af50c890a287659d33090aac9df9782ee375ee7aa4437dc6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296645205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf29c5b9dff5b4e4e6441693fe1dda83877129daab0c956cd710d64487ac8f0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:07:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:07:38 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:16:39 GMT
ENV JAVA_VERSION=jdk-21.0.2+13_openj9-0.43.0
# Wed, 06 Mar 2024 03:16:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6404c5fe4a71049d4f80429720b7d3f3e3b0ebea8067b823a6bfb24b9fe69797';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_aarch64_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7a7a186a7a48537519917331ec91d9180b961dcc7ea0f627a23fa369edab6f16';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_x64_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='43d53cc8fbec42b1f47069178838e65ee5119ec992b511973db7badc51742674';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='15fa4c41c15fda8365d868621f75d8599cb8ea92537494c1a6d2fccb5b46c19f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_s390x_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Mar 2024 03:16:49 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:16:49 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Mar 2024 03:17:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
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
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f31d30ecaf4575ccc11fabf7803ae6ebc387548c21b0d1546fafb5f25e260d`  
		Last Modified: Wed, 06 Mar 2024 03:19:44 GMT  
		Size: 12.1 MB (12114547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0405fb8e8e8a2ddcc800c3f67431c51d19a6b851a3ecfa2a6377e26784a7a22`  
		Last Modified: Wed, 06 Mar 2024 03:23:20 GMT  
		Size: 221.6 MB (221649535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2325bc360dc435602bab84899f5cffc5de893ecbe8b81680e3e9e0b4b97c39e3`  
		Last Modified: Wed, 06 Mar 2024 03:23:08 GMT  
		Size: 6.0 MB (6001372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f70830217dd3c3cff9e09ab77bb728086e715017ce9a4dec8170a8eb1c4ee6`  
		Last Modified: Wed, 06 Mar 2024 06:01:01 GMT  
		Size: 19.0 MB (18997821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503720ef7bd17d818dfc8c024122e6adeaf6a538d2f7888495c045b31e72d33d`  
		Last Modified: Wed, 06 Mar 2024 06:00:59 GMT  
		Size: 9.5 MB (9479925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a1dbe75fb58e42bceea2ca69ff440b92e04a4364d9a09b7e75756acedd9989`  
		Last Modified: Wed, 06 Mar 2024 06:00:58 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ee1417417ba954474d949af7fc25508065247e581044a3062b981d69137681`  
		Last Modified: Wed, 06 Mar 2024 06:00:58 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d867b9924ecc61c7aee75be084edb1ae1f73f1d41302014b47905846d838876`  
		Last Modified: Wed, 06 Mar 2024 06:00:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-21-jammy` - linux; ppc64le

```console
$ docker pull maven@sha256:3da214bd6455eae8ca84a196e06118d2ec2f42f262d0147f9b0ee057b6b18ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312108702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eace809e57b8c3adde4689374709ba510560c43ef4da2c92a02ed0ddc28f10d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:54:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:54:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:06:00 GMT
ENV JAVA_VERSION=jdk-21.0.2+13_openj9-0.43.0
# Wed, 06 Mar 2024 02:06:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6404c5fe4a71049d4f80429720b7d3f3e3b0ebea8067b823a6bfb24b9fe69797';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_aarch64_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7a7a186a7a48537519917331ec91d9180b961dcc7ea0f627a23fa369edab6f16';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_x64_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='43d53cc8fbec42b1f47069178838e65ee5119ec992b511973db7badc51742674';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='15fa4c41c15fda8365d868621f75d8599cb8ea92537494c1a6d2fccb5b46c19f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_s390x_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Mar 2024 02:06:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:06:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Mar 2024 02:06:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
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
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a37eb799955ef7832c2ba60acf9d2cdb59c5dc58c47e206f53ffa1a642c746`  
		Last Modified: Wed, 06 Mar 2024 02:10:03 GMT  
		Size: 12.9 MB (12891323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc21e5a1220e3c5c5acadfde0b16e746957303dcb546e6df9ce0e43d6e377385`  
		Last Modified: Wed, 06 Mar 2024 02:14:56 GMT  
		Size: 226.9 MB (226918612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50176ceb6932e632b739a8ff4a96eec983dbb13ab6541178100010e4124cf423`  
		Last Modified: Wed, 06 Mar 2024 02:14:36 GMT  
		Size: 5.1 MB (5111991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc70079378858868a3d34ca8f9332e581664a4a0b16658373b53938b7a0a4a9`  
		Last Modified: Wed, 06 Mar 2024 05:45:00 GMT  
		Size: 22.1 MB (22082730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b07f584ea02ca1f053da259469572903e8eb73e6451bb8b5c7c28a1a4928ae`  
		Last Modified: Wed, 06 Mar 2024 05:44:55 GMT  
		Size: 9.5 MB (9479935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd0c1ba5ef595d0e1c854929d9c46f716070054b19b4c70d721ebe17eb10365`  
		Last Modified: Wed, 06 Mar 2024 05:44:54 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fbc766802bb8c7befd9c9dd690707ee5eb474013fc12c83f37b42395c7057c`  
		Last Modified: Wed, 06 Mar 2024 05:44:54 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d5914a436a2123144eedfd5c16c966121ff0401562dbad53aab7a5803aa85b`  
		Last Modified: Wed, 06 Mar 2024 05:44:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-21-jammy` - linux; s390x

```console
$ docker pull maven@sha256:9e3a3910873df13de70e14105aa8a636573c9613ff1e045761ccddf12f250af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297659078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cd339119facab3aa0f40347baae176ce22f5634edd76ed61e282054f312c53`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:00 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Tue, 27 Feb 2024 18:53:00 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:03:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 05:04:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:27:22 GMT
ENV JAVA_VERSION=jdk-21.0.2+13_openj9-0.43.0
# Wed, 06 Mar 2024 05:27:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6404c5fe4a71049d4f80429720b7d3f3e3b0ebea8067b823a6bfb24b9fe69797';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_aarch64_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7a7a186a7a48537519917331ec91d9180b961dcc7ea0f627a23fa369edab6f16';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_x64_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='43d53cc8fbec42b1f47069178838e65ee5119ec992b511973db7badc51742674';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='15fa4c41c15fda8365d868621f75d8599cb8ea92537494c1a6d2fccb5b46c19f';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.2%2B13_openj9-0.43.0/ibm-semeru-open-jdk_s390x_linux_21.0.2_13_openj9-0.43.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Mar 2024 05:27:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 05:27:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Mar 2024 05:28:08 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
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
	-	`sha256:34c2c4dff60b52886f8ffe75945626cde03551a775fc6e99a1aaee265e75df5f`  
		Last Modified: Wed, 06 Mar 2024 03:56:35 GMT  
		Size: 28.6 MB (28636756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed79df339db8929e0c36ab7bdb51988e4302caec3ad4ff82daa9b39dd2542420`  
		Last Modified: Wed, 06 Mar 2024 05:34:05 GMT  
		Size: 12.2 MB (12203414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b901189dd0d9f1bcbbbf78415dd03e1925d7db17cf9199d6565db21fb7ce2c`  
		Last Modified: Wed, 06 Mar 2024 05:37:22 GMT  
		Size: 221.7 MB (221704163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b04c1e7d89c5f488f02e31c8b6b6e56a46357af0e7589611f29b4fe6099985d`  
		Last Modified: Wed, 06 Mar 2024 05:37:09 GMT  
		Size: 6.4 MB (6416141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f77735a462cc99a83d8686a3c8c92db0b1decf9ff05b563afe2b09ab64867a`  
		Last Modified: Wed, 06 Mar 2024 08:12:27 GMT  
		Size: 19.2 MB (19217293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f091c474aff53414d98ab2f0532edcff9dd2cd4480350a15e2152e03927ed8cd`  
		Last Modified: Wed, 06 Mar 2024 08:12:24 GMT  
		Size: 9.5 MB (9479942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f16749bc725fbb57598bb6300468def33f64c10cd01fe85f5ef94909cdc4466`  
		Last Modified: Wed, 06 Mar 2024 08:12:24 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c93ce2fc19df657f9afddac644cd9a0575447f1f02836ed1c99ab40044df7`  
		Last Modified: Wed, 06 Mar 2024 08:12:24 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0909aa892c0cc6ade4d55dfc8effef98d34223787b52f86200721b573a829a`  
		Last Modified: Wed, 06 Mar 2024 08:12:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
