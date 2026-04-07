## `ibm-semeru-runtimes:open-26_35-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:13e47958f490c3d70d6e64673df281c50bc0431c907c68770e5b0bff95628cca
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

### `ibm-semeru-runtimes:open-26_35-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:0b3742a186c3b2dc5cce180c5ecb438440c3b7eddd733b7145c6f795ae33894a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302010164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d0d45a94ce1b7cddf2ba51c4d399b55130a281643e7094b08d6c6f3366d2e5`
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
# Tue, 07 Apr 2026 01:55:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:55:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:55:45 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Tue, 07 Apr 2026 01:57:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='01fab55d3c3006c753134a2563c6b66cddcbdbc47f2db548ce42a9d39e793288';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c11f26e93266666d32f010562d50b977984fd554801a54c99012bafc9d588ab4';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='196f9e25dc0e7875a8aa09a597f88ef1fac7d32dd06dc99dfa0374fd5d653739';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='f7a5a07445a0f22d31c65a62fe03adb16ebae0c1f9a518e8be437a392462e92f';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_s390x_linux_26.0.0.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 01:57:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:57:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 01:58:51 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 01:58:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2acd8d576f7893b6738c8ee27423ab0251ca2e9ee14950702f1c3dbf5ee0d5d`  
		Last Modified: Tue, 07 Apr 2026 01:57:12 GMT  
		Size: 12.8 MB (12805585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb6d06b9d9f3523f0380ca4255e276ec9fef64de3b3f2f43c4028491fec77c8`  
		Last Modified: Tue, 07 Apr 2026 01:59:18 GMT  
		Size: 252.8 MB (252801375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6581030658a6b3827662e3050e9dec1117f8b8b7f320663b2276049d3226bf`  
		Last Modified: Tue, 07 Apr 2026 01:59:13 GMT  
		Size: 6.7 MB (6669745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ffb1e64c428990f55af4000087e673c3afbeeb998175e31e34672b2278a271ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3287677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc6b3f249a60e10b6ec4f224a0beca5488fb6848e99079a39c5a0a1a03249ff`

```dockerfile
```

-	Layers:
	-	`sha256:411b26dd25c4178e0672ee21064a73c398059057106f478ba0dea93d16c111f3`  
		Last Modified: Tue, 07 Apr 2026 01:59:12 GMT  
		Size: 3.3 MB (3261669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb8105b25e5a7b87d67f30085850ed7ac3508a2a798053ca63aa4ced2230753b`  
		Last Modified: Tue, 07 Apr 2026 01:59:12 GMT  
		Size: 26.0 KB (26008 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:c726355822bc2baa2ba4e89db471d306e46918e0fa087c75634b2c93b346a951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297278804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3bf88724289cf4e0ac731af217866f4b76cd8e2b73997c2ad19bbbc4bd683a`
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
# Tue, 07 Apr 2026 01:58:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:58:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:32 GMT
ENV JAVA_VERSION=jdk-26+35_openj9-0.58.0
# Tue, 07 Apr 2026 02:00:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='01fab55d3c3006c753134a2563c6b66cddcbdbc47f2db548ce42a9d39e793288';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c11f26e93266666d32f010562d50b977984fd554801a54c99012bafc9d588ab4';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='196f9e25dc0e7875a8aa09a597f88ef1fac7d32dd06dc99dfa0374fd5d653739';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='f7a5a07445a0f22d31c65a62fe03adb16ebae0c1f9a518e8be437a392462e92f';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_s390x_linux_26.0.0.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 02:00:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:00:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 02:01:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7995e8752ac062cef851186db99cf4e29664b6cd236182a857eca30223dc6ec6`  
		Last Modified: Tue, 07 Apr 2026 02:00:00 GMT  
		Size: 12.8 MB (12837861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b80bedc65603db71ec2a9ef42ce7502b32210e81681b86ef8ef48a5c87ce8a4`  
		Last Modified: Tue, 07 Apr 2026 02:02:20 GMT  
		Size: 249.0 MB (248992369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c148073729c149f08de4326e4270990e20d00888a1c29671b6a42e2c3d034ca4`  
		Last Modified: Tue, 07 Apr 2026 02:02:15 GMT  
		Size: 6.6 MB (6574499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d730fed4cd7791a0589e737aeb95cc00458dd9b8ae16b61672f1e85f9b863ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2bc685065f64e0a6b2980bdab70ee0242134b94832d7763efafa3a3519bf76`

```dockerfile
```

-	Layers:
	-	`sha256:d897a56cdcbce30526d9504e3c9d430dcb369160e18815c94faed712b02342c8`  
		Last Modified: Tue, 07 Apr 2026 02:02:15 GMT  
		Size: 3.3 MB (3260235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2670ceec431e7ab88c35b615512edbef0d32da9446604b65fde52e05b21d7449`  
		Last Modified: Tue, 07 Apr 2026 02:02:14 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:f83da9e573c50f7c2ae33251029285de9f8cd4d496c308bd2ffa4710644fe106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (310036104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c2efe3ca725b54cd86754abd7c3b8a98d8d4d8bdb1f4072346a8ea3194c230`
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
# Tue, 07 Apr 2026 04:57:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='01fab55d3c3006c753134a2563c6b66cddcbdbc47f2db548ce42a9d39e793288';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c11f26e93266666d32f010562d50b977984fd554801a54c99012bafc9d588ab4';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='196f9e25dc0e7875a8aa09a597f88ef1fac7d32dd06dc99dfa0374fd5d653739';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='f7a5a07445a0f22d31c65a62fe03adb16ebae0c1f9a518e8be437a392462e92f';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_s390x_linux_26.0.0.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 04:57:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:57:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 04:58:49 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 04:58:49 GMT
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
	-	`sha256:b19afad45f852b6bdb696faa1e3be787e843ef7923cd0cb73864a04a084db9bc`  
		Last Modified: Tue, 07 Apr 2026 04:59:40 GMT  
		Size: 256.4 MB (256350700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727d7f36c06e89e48a8fd52dbb3521a22931d1e62161bbb3beb1092b6a1b4ca1`  
		Last Modified: Tue, 07 Apr 2026 04:59:34 GMT  
		Size: 5.6 MB (5583923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:4f1a18694066acdba63d7f5c3a6070d1f1a96150cc08f743fb5c6ff483de1dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3279953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8ebc6b8bf65a6006aab84e882d671a7207c24120011158582a0cd10f0ecdcb`

```dockerfile
```

-	Layers:
	-	`sha256:669fbb323127fe27b1734d75849a5e69bc458a6fda62db06468161fc6f35888e`  
		Last Modified: Tue, 07 Apr 2026 04:59:34 GMT  
		Size: 3.3 MB (3253897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb35c265ad8ad82216512baeef218f23b70a35cd55478756bab9f23f32b7ff4e`  
		Last Modified: Tue, 07 Apr 2026 04:59:34 GMT  
		Size: 26.1 KB (26056 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26_35-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:0b0c19ef022edf94b1da37cf0b207d0c198a7ff4884f03b31f7dc187fd9b3124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.0 MB (300032436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99074927652872d47f0426de7b5c5ca7362f1b730c0d421dd0b14f98cc2cbb38`
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
# Tue, 07 Apr 2026 03:18:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='01fab55d3c3006c753134a2563c6b66cddcbdbc47f2db548ce42a9d39e793288';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_aarch64_linux_26.0.0.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c11f26e93266666d32f010562d50b977984fd554801a54c99012bafc9d588ab4';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_x64_linux_26.0.0.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='196f9e25dc0e7875a8aa09a597f88ef1fac7d32dd06dc99dfa0374fd5d653739';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.0.0.tar.gz';          ;;        s390x)          ESUM='f7a5a07445a0f22d31c65a62fe03adb16ebae0c1f9a518e8be437a392462e92f';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26+35_openj9-0.58.0/ibm-semeru-open-jdk_s390x_linux_26.0.0.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 07 Apr 2026 03:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:18:36 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Apr 2026 03:19:54 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 07 Apr 2026 03:19:54 GMT
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
	-	`sha256:b6d3910a88598451073df16daa3c3ee85071c81075b6d0a7948da233b0b07a87`  
		Last Modified: Tue, 07 Apr 2026 03:20:28 GMT  
		Size: 250.1 MB (250073946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1f30af33f4ec3b4751734235714375169629730c4bf505af12bbcd3170358a`  
		Last Modified: Tue, 07 Apr 2026 03:20:25 GMT  
		Size: 6.9 MB (6929178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26_35-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d54cecb09578351f009d592c977d7861f9aa591414f4aff087a8d2a9bb64d320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3277463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707ec9dff7b65ac0f0bfe891d86d6d5ef5799e7f322e0065e8539b087cd2c405`

```dockerfile
```

-	Layers:
	-	`sha256:c782d79147dcbbdcd8a49ec3c9ca6df833e82545b6237d7ffb25da968b1ee53b`  
		Last Modified: Tue, 07 Apr 2026 03:20:24 GMT  
		Size: 3.3 MB (3251455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7347c19e91ff793b0b129df2077a94110b37a95a83fd887045fc5ff084dfe412`  
		Last Modified: Tue, 07 Apr 2026 03:20:24 GMT  
		Size: 26.0 KB (26008 bytes)  
		MIME: application/vnd.in-toto+json
