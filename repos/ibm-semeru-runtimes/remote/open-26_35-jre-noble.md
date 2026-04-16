## `ibm-semeru-runtimes:open-26_35-jre-noble`

```console
$ docker pull ibm-semeru-runtimes@sha256:d4051148134affb73386b885b67dd9cb1f43773a087f9aa6a6b9e7aad59bf146
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
$ docker pull ibm-semeru-runtimes@sha256:f9f0df3c0efe684337727a577208e72a2beae032edce53aeadde648b5a122bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109013294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ed70884981edd53efb5c84df5e675e2b25346e7db98e895095507447301b58`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:42:52 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:42:52 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Wed, 15 Apr 2026 20:42:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:42:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:42:54 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 20:44:08 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2714fbc0ae6d15f084ff3a63784272c883f5751a05bcddccc9d245d55bea687`  
		Last Modified: Wed, 15 Apr 2026 20:44:21 GMT  
		Size: 12.8 MB (12805392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f9ea0ee86f63b0c559df3b0a4a611b10d085738f5036f2549def385c65054a`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 61.1 MB (61061003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb38c3559983a6d6ca83e2dc48672abd51c05938c3af64198c16c096b125240`  
		Last Modified: Wed, 15 Apr 2026 20:44:21 GMT  
		Size: 5.4 MB (5413921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:bb2594a96d582b4c2d107683ed910a322d946282e07d98ca06ee20bebd6d6de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d831e5d38e930f906190fcd01599366fba24a5bb1f96799c6fb6134d92196b`

```dockerfile
```

-	Layers:
	-	`sha256:6f44b417200fd7389a6bf51ab434e93a2b3f7de1b0681d7cd16ddacaf51a4327`  
		Last Modified: Wed, 15 Apr 2026 20:44:20 GMT  
		Size: 3.2 MB (3177442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fbdd4e5250a8a0a9e98cac1493496252e49902f563a3ca11526738632692c85`  
		Last Modified: Wed, 15 Apr 2026 20:44:21 GMT  
		Size: 26.0 KB (26007 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-noble` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:e963c370375a65533e67fe5202bf1054eaf62ea6ebc008fa17b73e987d9e2145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106341751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82a6c1bafb747d39a370de121a8d77fb75279df110da6892fd8d6b932258baa`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:39:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:39:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:39:37 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Wed, 15 Apr 2026 20:43:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:43:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:43:00 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 20:44:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 20:44:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15301d7ca2755d5c36a4c577b1fd592ed5546d74b04bdb2e30079389ae9b114`  
		Last Modified: Wed, 15 Apr 2026 20:41:12 GMT  
		Size: 12.8 MB (12837752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c376016b33e91d886c0b9c3963aa99a9947be035ff1e1ca08c17dd9a1b5029d5`  
		Last Modified: Wed, 15 Apr 2026 20:44:21 GMT  
		Size: 59.3 MB (59303761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd4db613954a59bd874d910e1ff95945aefdaa9cc978d1515a735d1bca1b523`  
		Last Modified: Wed, 15 Apr 2026 20:44:19 GMT  
		Size: 5.3 MB (5324453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:fb5d82392cfd5e19518bc8ef0fa3ac58f967a222ed37cd79384f6864521646d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b898fc861656d0a469809d50e78851ba05b90e59bc76d7bb5297f0579b1c7f1b`

```dockerfile
```

-	Layers:
	-	`sha256:e9487e5813032a3a6943d3d271e5326cb1112934b0c9590a4eea8f1713d64716`  
		Last Modified: Wed, 15 Apr 2026 20:44:19 GMT  
		Size: 3.2 MB (3176008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9433e405913cc13a705585747c5c2b943d0b694f16c570700b957e838d15dffa`  
		Last Modified: Wed, 15 Apr 2026 20:44:19 GMT  
		Size: 26.1 KB (26141 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-noble` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:da4d37ca7e4bdc7a89aa80049da8a47b7ff0e62d062a4de1d6e41d24be1419c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115313101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944632fce446609b312ee6cfa43ad956d186a9b613b5ef208e85323a9e278648`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:39:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:39:02 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Thu, 16 Apr 2026 03:33:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 16 Apr 2026 03:33:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:33:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 16 Apr 2026 03:35:00 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 16 Apr 2026 03:35:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccf3833ba70e5f487e107c0fc757f71c24195588839e7b794b482f819b1bf2d`  
		Last Modified: Wed, 15 Apr 2026 21:40:36 GMT  
		Size: 13.8 MB (13788494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a519deb432d1c1ad9e35d42a726c6321b9c5b9d77ced040c15ed1e2454429a9c`  
		Last Modified: Thu, 16 Apr 2026 03:35:33 GMT  
		Size: 62.9 MB (62935285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d4bd7b22a5a92c6691cad1d81fea126319be2cf5248cb50275f0897f0bd555`  
		Last Modified: Thu, 16 Apr 2026 03:35:31 GMT  
		Size: 4.3 MB (4275144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7849aaa8d7714fa39a20819b3bae6167d403beb8efd19f2475f745dc22fd1eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3e217266b95ba88226ed030abd2d5caee32c8c6ff10a87ad22fcaf1d9a2637`

```dockerfile
```

-	Layers:
	-	`sha256:024db823ea2d302426a5f902cf68138eb0a154204ec16b7e02e140248ad8f697`  
		Last Modified: Thu, 16 Apr 2026 03:35:31 GMT  
		Size: 3.2 MB (3182082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6833f5c77ce8a8304cb95439871eae81e6ced1f932ee6e7b0fba8b13691d88f5`  
		Last Modified: Thu, 16 Apr 2026 03:35:30 GMT  
		Size: 26.1 KB (26055 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jre-noble` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:dee3ae504719b3458ac026181a8f04d7fff0040460aa3ae5805d00a69c033431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108810970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b320b48dd242e8c20cda4cbc5da39fea37e2c10b481b822e4dabd286bcf89eb5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:50:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:50:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:50:13 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Wed, 15 Apr 2026 20:59:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5a394cb0e8840aa53ae4c45597b3e871e7262625d522a6832cbce607d9960181';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b4ede963ede082d880a33da510c968174c1a9e435c7866680c06881c6f871290';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='857aee9de6e1ac7f6b2562d88287785852009b1055ad51db286321ca8baee536';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='45d1537513218e46e8d896302b789c72f4964f4147591d0d52cc7776f16b341e';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jre_s390x_linux_26.0.0.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:59:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 21:00:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 21:00:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a45433edaccf5d141e572facc743118ac3f34051bab72b31c6fffae6248562`  
		Last Modified: Wed, 15 Apr 2026 20:51:45 GMT  
		Size: 13.1 MB (13117615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3912ffa749d0cd018d87bcdc647433c9b7c3db901538929d9d5a82295bf417`  
		Last Modified: Wed, 15 Apr 2026 21:00:38 GMT  
		Size: 60.0 MB (60033676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa851a373f7a5d91cec511030c5160ee50f39f1dd878f0e032861881a10c3407`  
		Last Modified: Wed, 15 Apr 2026 21:00:36 GMT  
		Size: 5.7 MB (5747532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jre-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:2a147bc3e9b1c98977b5c409d72799dafcd6f3031d9a66fb5cbd5cc68cae7b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3205645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452bb9288ba4a631f93639c00f784d6d4f7459534e633feb3a37cbcfef3b1fc4`

```dockerfile
```

-	Layers:
	-	`sha256:cac29d3399a6cd470f8942de95cc5873818cadef49ceca0f96f7fdde8345ca6b`  
		Last Modified: Wed, 15 Apr 2026 21:00:35 GMT  
		Size: 3.2 MB (3179640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dc13a9afe91c069fbff7efe099d9dbd039f37ed35df1469963c3186fb71f4ce`  
		Last Modified: Wed, 15 Apr 2026 21:00:35 GMT  
		Size: 26.0 KB (26005 bytes)  
		MIME: application/vnd.in-toto+json
