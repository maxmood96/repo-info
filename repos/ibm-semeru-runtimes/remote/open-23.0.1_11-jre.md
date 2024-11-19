## `ibm-semeru-runtimes:open-23.0.1_11-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:83fc7d642df46cfa877804876beb626e5497b501656c739747656f551e06175e
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

### `ibm-semeru-runtimes:open-23.0.1_11-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:7cbab1a8870e24b18e26973a7f01f2d1eefebed9a4cc22441b70720b05456343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102856763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f10c7ff12e1cb9ff96372e894f57951fed95b8494b57440a5011935923b4aaf`
-	Default Command: `["\/bin\/bash"]`

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
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-23.0.1+11_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='99a087ff6ad4b6ab5da8acc8003b7977188ab8fbeebb45d7a3e8f68963ad74e3';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76d25ba5887695011fce8d23418e86371aea43b9f5d326c140060ea89c4c9e99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a324b158e0478a584207d436578f3d088ad14add28d433897234ebcba8729ba0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='7d0fdd1b68b86788394ddfdf391eefb4d384b1bcba0784dd25d1f3c517a7f330';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423c6e679662b9a4a85180753b4f9e5d0f1a8692d9464863f29caa54d5d99533`  
		Last Modified: Mon, 18 Nov 2024 19:06:23 GMT  
		Size: 12.2 MB (12175057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc339e0c1ca47ce150373472198291e13b73d993a31dc9fbed3161b9214740b`  
		Last Modified: Mon, 18 Nov 2024 19:06:25 GMT  
		Size: 55.7 MB (55676347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00acc7b7c82411da99dadd071ca9a5a06104af9ae3554e7154129c1ef4755e1`  
		Last Modified: Mon, 18 Nov 2024 19:06:23 GMT  
		Size: 5.5 MB (5469671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23.0.1_11-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:b8da34ab601049d5a1905e808ccd530732e130eceb9871f15847a5e6b626ae05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3613944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2809814dffef4729193db622bcf5ac3e244b32580ed2cf0c04c05cfea87b1c39`

```dockerfile
```

-	Layers:
	-	`sha256:5b6ab7a33ab57b306334b6ab4850196e0c4f2b0e88ddab2ae23c7144926474f6`  
		Last Modified: Mon, 18 Nov 2024 19:06:23 GMT  
		Size: 3.6 MB (3589130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50566e80e80c0faccd2946c20dc1a2b13b8c8a3476889e64175b3f28c5dae18a`  
		Last Modified: Mon, 18 Nov 2024 19:06:23 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23.0.1_11-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:b2fcc4efbd9173d89f597baafd2b453183b0347186349206432cb02825f11475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96182117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2c683768776825bf42bcd7992069086ecf874239af5037bcce2e168904a0f9`
-	Default Command: `["\/bin\/bash"]`

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
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-23.0.1+11_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='99a087ff6ad4b6ab5da8acc8003b7977188ab8fbeebb45d7a3e8f68963ad74e3';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76d25ba5887695011fce8d23418e86371aea43b9f5d326c140060ea89c4c9e99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a324b158e0478a584207d436578f3d088ad14add28d433897234ebcba8729ba0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='7d0fdd1b68b86788394ddfdf391eefb4d384b1bcba0784dd25d1f3c517a7f330';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e2579fa9ed432452dd8563d1dc040de22c49fcfc4a3cd906b5e75b095c2926`  
		Last Modified: Mon, 18 Nov 2024 19:12:40 GMT  
		Size: 12.1 MB (12128239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40434bfa8fdc51417a4d0a556396f8b25b9a185fd3b778ae8e647a82a50e419f`  
		Last Modified: Mon, 18 Nov 2024 19:35:04 GMT  
		Size: 51.5 MB (51498087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5544896c5a7971fdb4482bd5b42873a5d9723301e804b55e6fc08225418eb`  
		Last Modified: Mon, 18 Nov 2024 19:35:03 GMT  
		Size: 5.2 MB (5197462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23.0.1_11-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d891e8578b646cc87198b4ec2aeac9b018f87dda14c51743c828e0eb2edf9b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ad0c5f328de74ae1b0c2ca5483ef8d30ab50237082385cb78030d4e0df74e1`

```dockerfile
```

-	Layers:
	-	`sha256:5ebf6c24e3fb228ce5acd52fad924c3cbda6ead8bf2f829a3a4e0ed1a8e6222b`  
		Last Modified: Mon, 18 Nov 2024 19:35:03 GMT  
		Size: 3.6 MB (3580631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccb0496c81e28b7603964b4c333c2660ac71d8ebb6d6d726165f7ab4a99a6170`  
		Last Modified: Mon, 18 Nov 2024 19:35:03 GMT  
		Size: 24.9 KB (24948 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23.0.1_11-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:d79af29c4a82b81bfd5725bdc7937213cb1e4f55812b25746c5d2e911e9ef4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108290255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4569e55dfa6f48c59f85f45aaacad2930bdbc31f3997d7dc2d9b271449c548b0`
-	Default Command: `["\/bin\/bash"]`

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
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-23.0.1+11_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='99a087ff6ad4b6ab5da8acc8003b7977188ab8fbeebb45d7a3e8f68963ad74e3';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76d25ba5887695011fce8d23418e86371aea43b9f5d326c140060ea89c4c9e99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a324b158e0478a584207d436578f3d088ad14add28d433897234ebcba8729ba0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='7d0fdd1b68b86788394ddfdf391eefb4d384b1bcba0784dd25d1f3c517a7f330';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:42ccfbd8d4b28c1f0d558eca058d7749230169faa0d3fd9a771e44b5e5a07111`  
		Last Modified: Mon, 18 Nov 2024 22:45:44 GMT  
		Size: 56.7 MB (56734561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72740dd06dfef131c3d829aba52d33d0a09d9aee315d5518efb3d5374caa94c`  
		Last Modified: Mon, 18 Nov 2024 22:45:42 GMT  
		Size: 4.2 MB (4219320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23.0.1_11-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8c05b403f335a1a4e160a1fa4a14e183e1280054903e7d22f27ea48de1ce9d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3610745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffa6cde3cdd1a32f5d31dd5a8433cd478e6d2a626523d348b1390216e236527`

```dockerfile
```

-	Layers:
	-	`sha256:dad0565f455522c54c1b6f0a832657e02fa8f3d02bf29614864171009a450fce`  
		Last Modified: Mon, 18 Nov 2024 22:45:42 GMT  
		Size: 3.6 MB (3585883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:346b3a2b1d16f383a10169b3ff6035d6980e73bb4d2e00d9e9b7625e3decf102`  
		Last Modified: Mon, 18 Nov 2024 22:45:42 GMT  
		Size: 24.9 KB (24862 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23.0.1_11-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:4dd5bde64530bfc42837c25514a6b0597f73af7d784b6563276437f4e3f130ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100275827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc28252231fe3e4225b8d21ffe416a2a3d3cdf63a759d4146ee77547d45b1c0`
-	Default Command: `["\/bin\/bash"]`

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
# Thu, 14 Nov 2024 10:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Nov 2024 10:27:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_VERSION=jdk-23.0.1+11_openj9-0.48.0
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='99a087ff6ad4b6ab5da8acc8003b7977188ab8fbeebb45d7a3e8f68963ad74e3';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='76d25ba5887695011fce8d23418e86371aea43b9f5d326c140060ea89c4c9e99';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a324b158e0478a584207d436578f3d088ad14add28d433897234ebcba8729ba0';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='7d0fdd1b68b86788394ddfdf391eefb4d384b1bcba0784dd25d1f3c517a7f330';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23.0.1%2B11_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_23.0.1_11_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Nov 2024 10:27:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 14 Nov 2024 10:27:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:e4612829333cff87d45a052f7a4ca734483082d99ebcd07d24f516a22174137a`  
		Last Modified: Mon, 18 Nov 2024 19:58:05 GMT  
		Size: 54.4 MB (54434434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47c7afeb84532d550c76d7e0c3e34d247515254c81b7af1c11ca063bc793c6`  
		Last Modified: Mon, 18 Nov 2024 19:58:04 GMT  
		Size: 5.6 MB (5636159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23.0.1_11-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:63795c1d4d5b21abf192bf47dc6fe07688b87d7d12de645edde08cca1f30af32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688c04b336aa4048732ae081451bd315c11c37b898287bdf81b5bb44f0016973`

```dockerfile
```

-	Layers:
	-	`sha256:544115037827080c6c43767dd53dfe68e129b7341fc9bb76d59dca7ac961ca01`  
		Last Modified: Mon, 18 Nov 2024 19:58:04 GMT  
		Size: 3.6 MB (3583605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00bf57eb9c26661dc730d57505d1d32c795d8b0a9727a98927bfd65390fa6b84`  
		Last Modified: Mon, 18 Nov 2024 19:58:04 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json
