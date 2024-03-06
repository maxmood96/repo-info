## `ibm-semeru-runtimes:open-8-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:010810d7423c763655ad51e22e6717a25c04caa8b0b082bc7f481e0a1c815a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ibm-semeru-runtimes:open-8-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:694113b4878663f559655109ff1e50626780107ca32f4e0f8458d528c59041d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99306113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fe363dcae8989176bed316eb97c3c7a832aae21ac8fb8557258e058b90b0fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:43:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 02:43:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 02:43:54 GMT
ENV JAVA_VERSION=jdk8u402-b06_openj9-0.43.0
# Wed, 06 Mar 2024 02:46:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='4921671d26754483f096007cfb537922f1b190ca471aaebda6eccdefe91f7fb0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d0efc1cee9a57bdb623e4f976aaa2ca96b7b724631521d9e387e543b2c57288b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6f2e0e977f833ad9b2d85e97e568aa57c658eea3f096a1544d72e70f94e55f73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='2c4cf63ea82f8d1fc84394b83c6c1e93fb30c6a83c8635ee648885f81b5d8d31';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Mar 2024 02:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 02:46:08 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Mar 2024 02:46:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e07ca78125fe890e216f5f8c44c168dda4825b7ec514a33d5262ddd919f315`  
		Last Modified: Wed, 06 Mar 2024 02:57:25 GMT  
		Size: 16.1 MB (16061454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b69ce13b3669f0334859c8ca3789e4295a09f65aa2025cc08faacb701c9e64`  
		Last Modified: Wed, 06 Mar 2024 02:58:05 GMT  
		Size: 50.4 MB (50386599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e43489ba6b97585079c7ab67b1ee524c4c038f86fec04753e710b7bb93d2237`  
		Last Modified: Wed, 06 Mar 2024 02:58:00 GMT  
		Size: 4.3 MB (4273743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:ae050b1f9dd217fc76ddb2ea2baa9775f5bcaf9b51c650c5e1d6ca97c91361e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96831453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c6a083da714eaef3b6f1612d137c5872ccc7438d65dcceae08341f9bd7cd33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:05:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 03:06:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:06:33 GMT
ENV JAVA_VERSION=jdk8u402-b06_openj9-0.43.0
# Wed, 06 Mar 2024 03:08:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='4921671d26754483f096007cfb537922f1b190ca471aaebda6eccdefe91f7fb0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d0efc1cee9a57bdb623e4f976aaa2ca96b7b724631521d9e387e543b2c57288b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6f2e0e977f833ad9b2d85e97e568aa57c658eea3f096a1544d72e70f94e55f73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='2c4cf63ea82f8d1fc84394b83c6c1e93fb30c6a83c8635ee648885f81b5d8d31';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Mar 2024 03:08:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 03:08:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Mar 2024 03:09:04 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2e4aa27158cc6973e8b7dccccbc360c797656a9911deb258ca2438872fa81d`  
		Last Modified: Wed, 06 Mar 2024 03:19:28 GMT  
		Size: 15.9 MB (15924449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39b12048992bcde01961952221783589f2bc77551b3e564055891dd919b9450`  
		Last Modified: Wed, 06 Mar 2024 03:20:04 GMT  
		Size: 49.7 MB (49661893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85943de84b301f52ff7415c508ed41d4f91d265e9255a393923422c5ffa9ad4b`  
		Last Modified: Wed, 06 Mar 2024 03:20:01 GMT  
		Size: 4.0 MB (4040824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:f3bb1847a4ddbbe561d0fc6d8956c7e9b7d434e69fe63a1df96862a0b4e4e6e0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105701242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd70c8d78c2e3772ea2e5dc417f65968d07eed48618fc5eb8f79a72d387f0f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:37 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:37 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:40 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Fri, 16 Feb 2024 19:14:40 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 01:52:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 01:53:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 01:53:13 GMT
ENV JAVA_VERSION=jdk8u402-b06_openj9-0.43.0
# Wed, 06 Mar 2024 01:55:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='4921671d26754483f096007cfb537922f1b190ca471aaebda6eccdefe91f7fb0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d0efc1cee9a57bdb623e4f976aaa2ca96b7b724631521d9e387e543b2c57288b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6f2e0e977f833ad9b2d85e97e568aa57c658eea3f096a1544d72e70f94e55f73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='2c4cf63ea82f8d1fc84394b83c6c1e93fb30c6a83c8635ee648885f81b5d8d31';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Mar 2024 01:55:41 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 01:55:42 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Mar 2024 01:56:17 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14837d4b18b532d33348e805f5b595b49a636d1a48af52704db4a0a9d63c7e38`  
		Last Modified: Wed, 06 Mar 2024 02:09:42 GMT  
		Size: 17.2 MB (17242680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be92a2462c8a291daff61507ef93f483e148223932863ab72ef86766f823b932`  
		Last Modified: Wed, 06 Mar 2024 02:10:32 GMT  
		Size: 51.6 MB (51641959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a5ae690319939644ed4b07d48559c2df95f72a82bb29b397087b6c7095ce1`  
		Last Modified: Wed, 06 Mar 2024 02:10:24 GMT  
		Size: 3.5 MB (3500994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:532e85add1735856e06cc8d7e0e3d7920a94bff6779d68ac6fcd40cf99556c75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97271152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef434d7181288a46a5bbe814c50ba73ce7fa1be0dbbba19cfcbd0fad6512f8a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Feb 2024 19:14:03 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:14:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:14:03 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:14:06 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Fri, 16 Feb 2024 19:14:07 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:01:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 05:02:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 05:02:09 GMT
ENV JAVA_VERSION=jdk8u402-b06_openj9-0.43.0
# Wed, 06 Mar 2024 05:06:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='4921671d26754483f096007cfb537922f1b190ca471aaebda6eccdefe91f7fb0';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d0efc1cee9a57bdb623e4f976aaa2ca96b7b724631521d9e387e543b2c57288b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6f2e0e977f833ad9b2d85e97e568aa57c658eea3f096a1544d72e70f94e55f73';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='2c4cf63ea82f8d1fc84394b83c6c1e93fb30c6a83c8635ee648885f81b5d8d31';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u402-b06_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_8u402b06_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Mar 2024 05:06:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 05:06:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Mar 2024 05:06:38 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8270f7dae6e45588c3d7d64e868d0c0a92a79c2d1416e7c4f4e6d8e072a804c5`  
		Last Modified: Wed, 06 Mar 2024 05:33:50 GMT  
		Size: 15.8 MB (15754442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aeb01ca9a7d321b237ff51bb2b32c0b0adf096d5ddbf9e83f6c0560cb6b956f`  
		Last Modified: Wed, 06 Mar 2024 05:34:24 GMT  
		Size: 50.2 MB (50163392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273b54aad2f81c1596d823fe4e6b257f75813f3ab2369ff2dc7949f5f020cca4`  
		Last Modified: Wed, 06 Mar 2024 05:34:19 GMT  
		Size: 4.3 MB (4337253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
