## `ibm-semeru-runtimes:open-26_35-jre-noble`

```console
$ docker pull ibm-semeru-runtimes@sha256:7bddb6a18b93067f2c974165ecd1f9af0d252bd17e702e7febd08f11ece52939
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

### `ibm-semeru-runtimes:open-26_35-jre-noble` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:a43b3b66c5a38b93acb9ef5aa5cef61a4aa038d97180ae64c52c25125b07d4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (108987984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c46a0a5fabfe60419008204d1d93eb333147ee770c140436e970689b08ff18`
-	Default Command: `["jshell"]`

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
# Tue, 07 Apr 2026 01:55:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:55:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:55:58 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Tue, 07 Apr 2026 01:57:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 01:57:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:57:39 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 01:58:44 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 01:58:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b4de73744723c75dd24888cf645c6ed66cd0be4c91a26f51c8d0a1ef6cb74`  
		Last Modified: Tue, 07 Apr 2026 01:57:20 GMT  
		Size: 12.8 MB (12805622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fd325666a1da7dce3061ec16757f79c1c85e3562a5f32f167249641dc44124`  
		Last Modified: Tue, 07 Apr 2026 01:59:00 GMT  
		Size: 61.1 MB (61061015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d65fa9a1896cb1e4ab4b3a72c0c91eda39fe85e89398b1cdc99dda71dcd20d7`  
		Last Modified: Tue, 07 Apr 2026 01:58:58 GMT  
		Size: 5.4 MB (5387888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:30c3f11a55b516c171a82d1c3baf592ac8445dbd6d3211d3f0575c2eb2ed2d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe64f665aa1ea5637e85622a6386fa75c0a3754d14e8897fa0ced2f9ef45b112`

```dockerfile
```

-	Layers:
	-	`sha256:0dead91f81a8f6b14e2a2742d34e89f021a6f0218ee90b412d4a2f77b711be5d`  
		Last Modified: Tue, 07 Apr 2026 01:58:58 GMT  
		Size: 3.2 MB (3177442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc59d81bf0782615a55d769b670b3f68077764cd7dcb49d60a6097a94ee0a3d`  
		Last Modified: Tue, 07 Apr 2026 01:58:58 GMT  
		Size: 26.0 KB (26007 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-noble` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:538552aa165f5bea8c668773a03934cc6632258ddd16da1e0d40022dc9cd6d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c30971dd75a0386a7f8e8a9c7013348db0db1399146ba4dff838078247ad7c6`
-	Default Command: `["jshell"]`

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
# Tue, 07 Apr 2026 01:58:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:58:24 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:24 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Tue, 07 Apr 2026 02:00:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 02:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:00:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 02:01:56 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 02:01:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72b02eb213f54cd02795387bf27cd1ad7e7dc2238137a5a55cd522434928b90`  
		Last Modified: Tue, 07 Apr 2026 02:00:08 GMT  
		Size: 12.8 MB (12837871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02840e9b7bf8ac79280e4225068fd84bdccc5a5277299d0ee1b22fb0a73646b5`  
		Last Modified: Tue, 07 Apr 2026 02:02:12 GMT  
		Size: 59.3 MB (59303770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b62ed71ce143818364fec61aaaa764c3059f4fa57172400f180254e9eb8c41`  
		Last Modified: Tue, 07 Apr 2026 02:02:10 GMT  
		Size: 5.3 MB (5314718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:92e98d79632c6ce0d58aa2607e11a60545dc6348d81d77196a9bdb568acdd5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e1845bc2cb756aba1bbf22c77e6699ae1f444531c6ecb353ce83b317c4e9b6`

```dockerfile
```

-	Layers:
	-	`sha256:36a57e5a970899d58acedfca85d2a40f2d4a01a6bc0877d86e7f2443c19d79c8`  
		Last Modified: Tue, 07 Apr 2026 02:02:10 GMT  
		Size: 3.2 MB (3176008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cddb6df78406abc73aaec19edf2e66338a7f5e62703d83cbaea42c41b891e0c`  
		Last Modified: Tue, 07 Apr 2026 02:02:10 GMT  
		Size: 26.1 KB (26141 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-noble` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:7d993671288332554aa7b20f62c2b31ba8f62b14c4c5de79b941d2ec00f76f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115292311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203e36d04916ca548c5ae5e6394955a219f79ad23c7c797fc913e20258257cf6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:44:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 04:44:05 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:44:05 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Tue, 07 Apr 2026 16:30:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 16:30:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 16:30:58 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 16:32:44 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 16:32:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148ce2142119bc6023086d2508635e22f653b242afa8c35372a4604dda8783d0`  
		Last Modified: Tue, 07 Apr 2026 04:46:14 GMT  
		Size: 13.8 MB (13788147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f35b62443d6c4965d9d04e1350cea6a2039d420ee6f8a53173fd769bd3d4a`  
		Last Modified: Tue, 07 Apr 2026 16:33:11 GMT  
		Size: 62.9 MB (62935351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd03a90ace51b08470640cff48fe5f92b5d1473d96b7b4f68040b9edadd6ff4`  
		Last Modified: Tue, 07 Apr 2026 16:33:09 GMT  
		Size: 4.3 MB (4255479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:da9df374f17109d54d0722cfa11e79ca867eb5f235b60638ca72a9f815830670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00af69796573dfeda8366b91185746cfd840ebcf7294c898fd70e51648c4a9d5`

```dockerfile
```

-	Layers:
	-	`sha256:4d31d7cef7d86708b60f5853b922abe9740a3650a6ebe3eef088190ad9389c0f`  
		Last Modified: Tue, 07 Apr 2026 16:33:09 GMT  
		Size: 3.2 MB (3182082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c244a87a42cdc82d75182daf9531936d1f7c10d140bef3980817e84d8fb0358f`  
		Last Modified: Tue, 07 Apr 2026 16:33:09 GMT  
		Size: 26.1 KB (26055 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-noble` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:3327e000f1720ede7d99009bace869e77322130d358e8c79710f004bfe0bfe17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108723232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f434bacd549a11e2233fa308b1901ec63d9b75d3ac2ef822dc79fb3d9736a13b`
-	Default Command: `["jshell"]`

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
# Tue, 07 Apr 2026 03:14:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:14:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:14:17 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Tue, 07 Apr 2026 05:56:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 05:56:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:56:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 05:58:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 05:58:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eac572405261a6d50ac103757aa272403cfd1f9ac6696ef2960d76d1fbec0b7`  
		Last Modified: Tue, 07 Apr 2026 03:15:58 GMT  
		Size: 13.1 MB (13117469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8d2648081e352c3ef2226b7ecb3f086432acc14a077d51f54828433632c282`  
		Last Modified: Tue, 07 Apr 2026 05:58:25 GMT  
		Size: 60.0 MB (60033652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4b123bf388216878f0e3f47a97754806110d48fdb6ef28bc5400ea19e6f895`  
		Last Modified: Tue, 07 Apr 2026 05:58:24 GMT  
		Size: 5.7 MB (5660268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e221bcf155210f7c7305a9342dde9e8d11d75f740a93de77d64739f8ef8b5f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3205646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5791ca6911d0d2002a2710dd9e6bc01e64eab173cc86c4b211636a909f5bacb6`

```dockerfile
```

-	Layers:
	-	`sha256:972f581d198edf53b8b231a8ccdfc61a1489deedc53fa054535ca310f9c5a655`  
		Last Modified: Tue, 07 Apr 2026 05:58:24 GMT  
		Size: 3.2 MB (3179640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4663ab2681b99b17ea6b62dfd237765376bf409d5123bcc136f197eebe82852`  
		Last Modified: Tue, 07 Apr 2026 05:58:23 GMT  
		Size: 26.0 KB (26006 bytes)  
		MIME: application/vnd.in-toto+json
