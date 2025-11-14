## `ibm-semeru-runtimes:open-8u472-b08-jdk-noble`

```console
$ docker pull ibm-semeru-runtimes@sha256:63bb8aad02000edbc5f90222a018862f546a0ac21ec01d6b31af6202083297e8
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

### `ibm-semeru-runtimes:open-8u472-b08-jdk-noble` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:703be684f41b13d04d2000aceba36e562692325c8763a9714903dd05556eb2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166775636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136d347163d25042b7e4921bf419a77f5750fadb698b1af0a1bdb77f3b528a24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:24:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:24:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:24:55 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 13 Nov 2025 23:25:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f7b39daad8690ab08a2e73d8b7b3d8768c5771e0d83e1082fc89ae640f3e4b2';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3df1f0b003ea7abfebdb5f6311f1f9bbac970897dabfb21a6d4d380df15d38b4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e6c7faea4fc0bcf43b252621f8ec9b1bfcc4986f5fb914266e80f135d3139940';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='6fb5c76486bace90781a8133ab2619d073244ad2b8692bb3c9afefffd8f131b8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:25:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:25:01 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:25:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400c7eb21b38c4c344156f5a8481b6a1ad7b30cbb91634961211d4da67729e90`  
		Last Modified: Thu, 13 Nov 2025 23:25:56 GMT  
		Size: 12.8 MB (12796461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc15b15473f814269d94f391aaf65d570cb09b827083fc083bb6e83c1b5aa57e`  
		Last Modified: Thu, 13 Nov 2025 23:26:05 GMT  
		Size: 120.0 MB (120001255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72296b802f72b440fef69234a84922c1c81b8715c5f49f3322871663c175c07a`  
		Last Modified: Thu, 13 Nov 2025 23:25:56 GMT  
		Size: 4.3 MB (4253232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u472-b08-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:99eda6d9036ba62f5964575998991ffc7bd5025e6ad78e73a9bd060a052405be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3390465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97febc99bc04d2093b3f850691e1050c1e07d77c80859ffb342485f1a511faec`

```dockerfile
```

-	Layers:
	-	`sha256:d999e886a5b86ff52c87f08ff90e6504a85a25eeace9366e2b4fc7a258e5a014`  
		Last Modified: Fri, 14 Nov 2025 02:49:09 GMT  
		Size: 3.4 MB (3364580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a3f2652acafb9635409e2a3fefc33541775b7535408af745edbab8c41c29dc`  
		Last Modified: Fri, 14 Nov 2025 02:49:10 GMT  
		Size: 25.9 KB (25885 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u472-b08-jdk-noble` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:b6bd254bec91c92712bbcbcc2e0eab7173510bf2c8a2ed8294eff2b32c487a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165998290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a255883e0455d580157be0ddab758aad64540bf2355bd3e74d97b65c8736768d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:24:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:24:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:24:49 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 13 Nov 2025 23:24:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f7b39daad8690ab08a2e73d8b7b3d8768c5771e0d83e1082fc89ae640f3e4b2';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3df1f0b003ea7abfebdb5f6311f1f9bbac970897dabfb21a6d4d380df15d38b4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e6c7faea4fc0bcf43b252621f8ec9b1bfcc4986f5fb914266e80f135d3139940';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='6fb5c76486bace90781a8133ab2619d073244ad2b8692bb3c9afefffd8f131b8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:24:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:24:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:25:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e773fbeac4b45a8f3c14aa233b7c9c15c9307082455ad52125e468aff2e4b58a`  
		Last Modified: Thu, 13 Nov 2025 23:25:49 GMT  
		Size: 12.8 MB (12831418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad4a9b45a320fedcc501478b4688cf96725a60008c3e742bd7ee64fb960db77`  
		Last Modified: Thu, 13 Nov 2025 23:25:59 GMT  
		Size: 120.2 MB (120153822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9800a8970ba9cd89d520bb8eb05829759c93ca2953528d16828491dbc0250`  
		Last Modified: Thu, 13 Nov 2025 23:25:49 GMT  
		Size: 4.2 MB (4151093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u472-b08-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:eb52271fd2ae466443d4551ec74e20ad53efcf1c5d0f93df797ca606d7f815f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3391227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062e116e1f303b36285aedc3b9daa8c554736e169eb8b35bbd1bebd59c8d3791`

```dockerfile
```

-	Layers:
	-	`sha256:17805b2caa8a791433b97033c7586824f7114ef0b6002cfb800f808109ea8a0f`  
		Last Modified: Fri, 14 Nov 2025 02:49:15 GMT  
		Size: 3.4 MB (3365207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89d62733efdcdb94843d674e891d7705d5009a5abb4255211cc4ada7dd3ccb96`  
		Last Modified: Fri, 14 Nov 2025 02:49:16 GMT  
		Size: 26.0 KB (26020 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u472-b08-jdk-noble` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:f457cfa6d33f86fd6eccbaf4214e17764db8e9022ad1d5867b6372160cce258c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173234157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f939e39552e8bac5d41fb206a7a1a9f37771641978e03d500867ea67973f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:39:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:21 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 13 Nov 2025 23:39:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f7b39daad8690ab08a2e73d8b7b3d8768c5771e0d83e1082fc89ae640f3e4b2';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3df1f0b003ea7abfebdb5f6311f1f9bbac970897dabfb21a6d4d380df15d38b4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e6c7faea4fc0bcf43b252621f8ec9b1bfcc4986f5fb914266e80f135d3139940';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='6fb5c76486bace90781a8133ab2619d073244ad2b8692bb3c9afefffd8f131b8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:39:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:39:29 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:40:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a76c425c79bf766b59c998d5db4eb2aa18eff8ad07eb7fc0177fa2aa73a414`  
		Last Modified: Thu, 13 Nov 2025 23:40:42 GMT  
		Size: 13.8 MB (13795716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa3e8bb3182d04386c65e06ecdc22ffe29bc707c6eeb36e5d38059f33b8aad5`  
		Last Modified: Thu, 13 Nov 2025 23:40:53 GMT  
		Size: 121.6 MB (121606691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6b57709ad4a887b9cb0e3f34d7a25b3844740d0099976ca28ce4cc4166a6a4`  
		Last Modified: Thu, 13 Nov 2025 23:40:42 GMT  
		Size: 3.5 MB (3527326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u472-b08-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:729db080fac32a18a84d786c788cd0865a0b9da07221d5ab221daa0de469299b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3395330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b0f9f981d2f615215fadaac7fadc89f778a88ab2e4dff193e4e39884ae0a0d`

```dockerfile
```

-	Layers:
	-	`sha256:452f6002a9fcd576f5a590da0f8ac5485fd4c0129707c2f023e21ffdb9335eac`  
		Last Modified: Fri, 14 Nov 2025 02:49:20 GMT  
		Size: 3.4 MB (3369396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039e7c496327d76446fe86b735cac64dfe3198ece50201ba95564ba274afa3e4`  
		Last Modified: Fri, 14 Nov 2025 02:49:21 GMT  
		Size: 25.9 KB (25934 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u472-b08-jdk-noble` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:00e28be9c39e48153a3e0732081944d2d5957e3736ad43684356af922e89f656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166855676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98baef65f923e5e00176c6dc861be4d3cd29215673fce9072b5214287ddbe0be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:14:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:14:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:14:02 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 13 Nov 2025 23:14:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f7b39daad8690ab08a2e73d8b7b3d8768c5771e0d83e1082fc89ae640f3e4b2';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3df1f0b003ea7abfebdb5f6311f1f9bbac970897dabfb21a6d4d380df15d38b4';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e6c7faea4fc0bcf43b252621f8ec9b1bfcc4986f5fb914266e80f135d3139940';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='6fb5c76486bace90781a8133ab2619d073244ad2b8692bb3c9afefffd8f131b8';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jdk_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:14:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:14:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:14:36 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39d3eb489052c74f699c599a5ba4c87e284b8313fbd505aa262212a6dcd6cc7`  
		Last Modified: Thu, 13 Nov 2025 23:15:06 GMT  
		Size: 13.1 MB (13120834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9459f68f0531ea90529b2572d3e8c770bc6473030f562745a45dd10bef09e15b`  
		Last Modified: Thu, 13 Nov 2025 23:15:17 GMT  
		Size: 119.4 MB (119427096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1911a6de353c9e0e691bfee5f72547aac5d39631651675d2a10ea8fa2595b8f1`  
		Last Modified: Thu, 13 Nov 2025 23:15:04 GMT  
		Size: 4.4 MB (4400149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u472-b08-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:2c2ae521f7067fb561d4b1842a62c9c468df6283aced64821d98fce4a7503674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3393290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba9c0c6f45f491f8ec97874161d67657fea56151b74ae360f35083dcb9fddcb`

```dockerfile
```

-	Layers:
	-	`sha256:6c4e82e02e27deee67b86817a2324edc293aeca3cb9ac16e061423cb12a7fade`  
		Last Modified: Fri, 14 Nov 2025 02:49:26 GMT  
		Size: 3.4 MB (3367404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afd7a8a51167252425aaccafd3b58e8447895e97e733eba1c4e48736cb9ed175`  
		Last Modified: Fri, 14 Nov 2025 02:49:27 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json
