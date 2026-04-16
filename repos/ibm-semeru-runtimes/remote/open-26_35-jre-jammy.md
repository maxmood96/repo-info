## `ibm-semeru-runtimes:open-26_35-jre-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:888aa7b2e93c75b17ab75024390fc0b60eec84544182982a190c1991e5dcb577
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

### `ibm-semeru-runtimes:open-26_35-jre-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:19781e4a0531c0dd73a74b5ee9d9d5a5aa4bb67634c00a2f167de42da2bc1838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108394572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89efc500fd6a389ca947eff3b522e0e3a93c01dc81afe02558eca4ec80c030e0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:42:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:42:41 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:42:41 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Wed, 15 Apr 2026 20:42:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:42:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:42:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 20:43:51 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 20:43:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82622823262951ab4225c00207b231c080b1a570610ffb73737c9659a65c8928`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 12.2 MB (12172121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee5c558842464a50357c547909261e3d311014c387f4764171c8b6aaaca681f`  
		Last Modified: Wed, 15 Apr 2026 20:44:06 GMT  
		Size: 61.1 MB (61061018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda380164fb54472e90409552f43ad72a8b2d4f1c2b9026f2b2d380a37ef305`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 5.4 MB (5424935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:936175a05727d91c97a3249830f6769b1e67a5cd0a9a589786fb83baa0341156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3762010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa87e041fb08ec2c0a87e8acbade46e13ba2443c732ffb88a692372be4b049ba`

```dockerfile
```

-	Layers:
	-	`sha256:862cc1b407e945854714caa01850fee27232ee2c83810b8d2aeeaa9a66300880`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 3.7 MB (3736679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fc15555bf900267969fb88a6a2409dc924e2b8465f02e9e758629027c562dc1`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 25.3 KB (25331 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:373642e093c8f285232ecbd5e91bb98e2ec1eaa6cf2aca050b477a611835ca28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104240979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622ca7b100a4a5433ca2e4683db604fc1aa4ae28e0cc2bd4c529520a910827e5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:15:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:15:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:15:35 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Wed, 15 Apr 2026 20:42:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:42:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:42:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 20:43:49 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 20:43:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8592f0a39cc33678ea3ae68a5c207b9a33d8e7f61752a8b14426f77361009`  
		Last Modified: Wed, 15 Apr 2026 20:16:59 GMT  
		Size: 12.1 MB (12142653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3caf5856fddde202447953c09b6a0539e69b83c59144143a9e1f6dd523b5b75`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 59.3 MB (59303754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe17f72b13d418dcd362107d9941f8a4b0ca664eebd228ac28e4208fbd091f80`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 5.2 MB (5188029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d1994c7c422e09b2fd31b62ec51f732738bc02a69f5a6697bda4586045fb30eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd76a513b711a939785bd7099ce0c214752904e7f688b8ef36e71c5b9c8bc8a8`

```dockerfile
```

-	Layers:
	-	`sha256:e11c08d92d30e56ec05d2a276b0f1664ae3854f491c675941597fb3b178e969f`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 3.7 MB (3734428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d477ccbce3744847ff09e800519cefdf87402fbdcb1b91e153c7b70d494d16`  
		Last Modified: Wed, 15 Apr 2026 20:44:01 GMT  
		Size: 25.4 KB (25443 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:8aad46e8b3e6d09ddb778b70185fbd232acfe8a6f34e395271a7306ee87cdde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114738542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e145554e45379a088ed89f660236298012096d9d3180b176a00602d45edb407`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:36:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:36:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:36:31 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Wed, 15 Apr 2026 21:54:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 21:54:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:54:12 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 21:55:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 21:55:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49442ce9b5aa160801b510939c1cf8c4083fa3673d806c1ae754d2342a161a0`  
		Last Modified: Wed, 15 Apr 2026 21:38:21 GMT  
		Size: 12.9 MB (12898247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1341e4655ab0d593685b017ec07f8070b7498d011470a11269132e584239c7`  
		Last Modified: Wed, 15 Apr 2026 21:55:59 GMT  
		Size: 62.9 MB (62935267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a287d40adc1f963fa48c423b396b8f241e0a82c30145731993dbb8e8b48aa84c`  
		Last Modified: Wed, 15 Apr 2026 21:55:57 GMT  
		Size: 4.3 MB (4256630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7d0cb2d4b522d56d2585adfe1eea455dbf751fc6685179b31dd76ed11c4aef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4aee31d52b9b44381eb756c8dfa6925080eac7c4c968598f651cefeaf63938`

```dockerfile
```

-	Layers:
	-	`sha256:cadbed62173d9234312e7878fbb6c5adc410754564737442d12e2a88f9f086cb`  
		Last Modified: Wed, 15 Apr 2026 21:55:57 GMT  
		Size: 3.7 MB (3741306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5945f8b9f31cd3cd658d0e272afa4e4c7d810b0fc5320021a595e1e40b711013`  
		Last Modified: Wed, 15 Apr 2026 21:55:56 GMT  
		Size: 25.4 KB (25369 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:e7824e533e781c3abf985ff10ba05f2e6e6b9b487467adbd4d19e9891c35db40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106093900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534968dd988eca4c717547b19caec5ad27e66364e1c5f3005bd1ff15f6871061`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:50:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:50:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:50:11 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Wed, 15 Apr 2026 20:58:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:58:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:58:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 21:00:05 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 21:00:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0badf736d5dc588ee1611bcc905fc1b6be06b130293cdb7383b80f11cd7f549b`  
		Last Modified: Wed, 15 Apr 2026 20:51:44 GMT  
		Size: 12.2 MB (12224849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a87b4ba026eacfe15dd98f418ff9057cf41ecf6e7db9817d66e0a33b703049`  
		Last Modified: Wed, 15 Apr 2026 21:00:36 GMT  
		Size: 60.0 MB (60033682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243a01d6ac19ca24c5e6a92b56fa84260235d243bf4ed98312a494d47e58ce1`  
		Last Modified: Wed, 15 Apr 2026 21:00:35 GMT  
		Size: 5.6 MB (5633070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d96e99f502f4f633da2eb09116cc80a30e83de8c4009cdfbb0180811ae4d2c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3763604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41abedef1732e6066dd68dc14f7d743d9f729f3660db690a0bbd50a1af1cc059`

```dockerfile
```

-	Layers:
	-	`sha256:953c3a5fc171982dc17c1362c4b33dd6cb8928f136865503b7b3c35e87545c1f`  
		Last Modified: Wed, 15 Apr 2026 21:00:35 GMT  
		Size: 3.7 MB (3738271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9915dca2a1f10e90e716cac6b585428530b318e07e07130f8c60204610ab6c71`  
		Last Modified: Wed, 15 Apr 2026 21:00:35 GMT  
		Size: 25.3 KB (25333 bytes)  
		MIME: application/vnd.in-toto+json
