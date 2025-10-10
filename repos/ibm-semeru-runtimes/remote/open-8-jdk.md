## `ibm-semeru-runtimes:open-8-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:d7c4cd24127081d75a61228faccfa098cb554ba20e7a60c42cfa28ad29afb7d9
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

### `ibm-semeru-runtimes:open-8-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:2e737f2eaf51f71fa6696ac585ffd3937175c745ada8e32a97253b02a152bebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166701505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d54513866e63a6db32987792a87bb4f87bc799dc6d718116007db342098d78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk8u462-b08_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ffdfafe66c22b675393bdc78fff0e4260b677a049cb75c91d228e40a65fbb095';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cb72d241d6130158465bd8d57bed6c19dbd83fc3ecca200fa9c2373d1f2d9c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2acdebf2b8f016756bcd826b04fe04e40df81583a9cebc92b1beb6a85686ad59';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='ac8739f91dcd1b53811805a8070e548feba9054fc56e58ccad4d6f3384d7adb5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfa0560bae3df461afc1f6ca688481aae88ba0e112c1016a728c04fcc77eea`  
		Last Modified: Thu, 09 Oct 2025 21:14:30 GMT  
		Size: 12.8 MB (12796704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d584ec58937625c94b915fc010f9737301e2482e499c1841f8d34ef2cf8ab5a5`  
		Last Modified: Thu, 09 Oct 2025 21:14:41 GMT  
		Size: 119.9 MB (119941251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179650528ed77271540f6fb29be17cff08df22db7dd5e9f3aa319c9f5de5cfe0`  
		Last Modified: Thu, 09 Oct 2025 21:14:30 GMT  
		Size: 4.2 MB (4240403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:eecb3454ee7f9f41e8b4d45e7f07b000c55cbd975ab96abade508f7a5d6fe3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3390509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d0ecfaa9db811b112ad51675c23c217cbf9f2e27eff2108c2c0009e15da6c1`

```dockerfile
```

-	Layers:
	-	`sha256:28c3b7804ee3c9c0bf008123c3cb4553a2cc77d1f901a76d120771d50c2456b4`  
		Last Modified: Thu, 09 Oct 2025 22:48:35 GMT  
		Size: 3.4 MB (3364580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3ca42564f499fe111d45bdcde457c07ef80eeda6a594484b87d80b62174fb7`  
		Last Modified: Thu, 09 Oct 2025 22:48:37 GMT  
		Size: 25.9 KB (25929 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:62ada77fe991df9641dd6f522adaa017e68f5592ad320b12bb736c5ec7ccbb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165882968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b3fbeff9b43910f4db01d4a21ad53a8b67fe14d9e64d78fca98c01f6bf7a63`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk8u462-b08_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ffdfafe66c22b675393bdc78fff0e4260b677a049cb75c91d228e40a65fbb095';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cb72d241d6130158465bd8d57bed6c19dbd83fc3ecca200fa9c2373d1f2d9c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2acdebf2b8f016756bcd826b04fe04e40df81583a9cebc92b1beb6a85686ad59';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='ac8739f91dcd1b53811805a8070e548feba9054fc56e58ccad4d6f3384d7adb5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d6f42ce2665a1cfed2fc8663ddfa2f97ce63d2ef0d218bdf63bd9ea9166809`  
		Last Modified: Thu, 09 Oct 2025 21:18:15 GMT  
		Size: 12.8 MB (12832021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec297e600bd244e730394c9d4290e75be77756274b7ba6702532042873ae2b24`  
		Last Modified: Thu, 09 Oct 2025 21:18:20 GMT  
		Size: 120.1 MB (120099807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da7de90e60bf8f8bb900c9aebd4ff6520d82cfbac983eb8d55c4206ba71f170`  
		Last Modified: Thu, 09 Oct 2025 21:18:14 GMT  
		Size: 4.1 MB (4089428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a1f8759c76a6a4df51dbd3a84ad9b7b671196e066a2534bfcb7395338646a287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3391270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58e1b0b816e95611198b95c3e9f724f8e67b53925498e31e1b940a796f1da5d`

```dockerfile
```

-	Layers:
	-	`sha256:192a0d50b6fe788a3acd1c1723a3205fc38b3fd4f7af8969aae7ecc0a7b5ccfb`  
		Last Modified: Thu, 09 Oct 2025 22:48:43 GMT  
		Size: 3.4 MB (3365207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55ee6790af4ada6ebe999dd8023c8d047e7cffac9494786c0fd52786e58c053a`  
		Last Modified: Thu, 09 Oct 2025 22:48:45 GMT  
		Size: 26.1 KB (26063 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:26c2badaa915dc9456c5f360f6b62322eb9cb3a3b5fee0bcae89c2ea49510881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173257167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8c4884ae625851ee81452f677fc32b7d10bc5d96b3ddd3c097340d0d0879c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk8u462-b08_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ffdfafe66c22b675393bdc78fff0e4260b677a049cb75c91d228e40a65fbb095';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cb72d241d6130158465bd8d57bed6c19dbd83fc3ecca200fa9c2373d1f2d9c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2acdebf2b8f016756bcd826b04fe04e40df81583a9cebc92b1beb6a85686ad59';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='ac8739f91dcd1b53811805a8070e548feba9054fc56e58ccad4d6f3384d7adb5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90d60290856efe2971970dd841be418b3d4aef5c79e531fd5259b73b4161e6e`  
		Last Modified: Thu, 09 Oct 2025 21:24:01 GMT  
		Size: 13.8 MB (13795688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1922d82b8cd964244e7bb01023834463be4f3bbd2394d165c6c0c619ba39c1`  
		Last Modified: Thu, 09 Oct 2025 21:24:11 GMT  
		Size: 121.6 MB (121567534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e9db49c12b3cb3cb900de6ea3b38bf3d17d834a36d3ef0e1e6627143369e36`  
		Last Modified: Thu, 09 Oct 2025 21:24:00 GMT  
		Size: 3.6 MB (3590420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e7ca668b16c940873fb88753e37d31b35f05c96dd15ed7b935cad58278a7458c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3395373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773dcf0a8d032cde21e26c3e80059e8749d82d6fac847148038a49e675d72ca0`

```dockerfile
```

-	Layers:
	-	`sha256:543089ec48d4ca6b3ed465005e26077b7108b4385f73d34c6875b8c3be78d864`  
		Last Modified: Thu, 09 Oct 2025 22:48:50 GMT  
		Size: 3.4 MB (3369396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832ca8e598ff2c15ab5203887494f5d8ba2f346a4343c37078480c1f0bd588de`  
		Last Modified: Thu, 09 Oct 2025 22:48:51 GMT  
		Size: 26.0 KB (25977 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:4bc9d9eabdaf01ce19499319b1a6d230917406d58ce70edcd09b170ac81c7aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166797638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cf52c6654c8a103b9142b474a43b3477ee0fd07bb2970e7f62a4238906199b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk8u462-b08_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ffdfafe66c22b675393bdc78fff0e4260b677a049cb75c91d228e40a65fbb095';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cb72d241d6130158465bd8d57bed6c19dbd83fc3ecca200fa9c2373d1f2d9c1';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2acdebf2b8f016756bcd826b04fe04e40df81583a9cebc92b1beb6a85686ad59';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='ac8739f91dcd1b53811805a8070e548feba9054fc56e58ccad4d6f3384d7adb5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u462-b08_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_8u462b08_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abb1773fa607c3929aac3eb861ef6680d8e809e96bed56147de3baee3d0361f`  
		Last Modified: Thu, 09 Oct 2025 21:19:11 GMT  
		Size: 13.1 MB (13120820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c55e0e4a2942e2a4a868c070e414d6b80e664c76db754241320ec8cc63be87f`  
		Last Modified: Thu, 09 Oct 2025 21:19:12 GMT  
		Size: 119.4 MB (119384979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102235088ed869586b109356a4d4578a4a6b142c65e32e759034765ed0c448f3`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 4.4 MB (4385688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:34bf45620187f61fe460247c0fc14eeb1cbe743a76f48519b92cf03f608082f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3393333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11c21391ca1d3db5298f6ec71409c78bae62b638bda1d427bd62f4a41d6f8a`

```dockerfile
```

-	Layers:
	-	`sha256:d0a3a0de5faf8249b486eb1fc4a0893defe26a3f93b86855ab5e6460781b605e`  
		Last Modified: Thu, 09 Oct 2025 22:48:56 GMT  
		Size: 3.4 MB (3367404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaea5b5f16fb1776c4a1ef2510fbe085d642ab9bb61a3291ad168ab6f1931457`  
		Last Modified: Thu, 09 Oct 2025 22:48:57 GMT  
		Size: 25.9 KB (25929 bytes)  
		MIME: application/vnd.in-toto+json
