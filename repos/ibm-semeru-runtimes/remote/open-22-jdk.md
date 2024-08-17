## `ibm-semeru-runtimes:open-22-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:81801db1fa4b7b4fef67b18e06984e7bb8356db4c1741defd868c584b21edfcf
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

### `ibm-semeru-runtimes:open-22-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:649bb2e96cf30676d2c075bd7adc495222bb2d1f5209feb5fabaf1955cdfb550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276238730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffbe40cff3bb0c44703ac196bbbd058ec7f28d490c8e1d87526c9013579a471`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f9936b8374e5a0fb8fca8a4d11339eb63678e08db389852fd149fec27896df69';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b644d099fdacf660c627c6fda09ee5d680611f3195f8cebc1588b410e85cc9f0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='21c630eba973418d266c3cf1d96fdd3983537283c7529ee2ad304ac232fc745e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='4a1cd1d4e775453593d285daf2167c49c765b696c84083b57cc9148443025fdd';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679d4879f6556412f0258d7fff57ea135b17b48926579e8ca8273824e2527212`  
		Last Modified: Sat, 17 Aug 2024 02:05:13 GMT  
		Size: 12.2 MB (12156482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c99ca2bec02402db8ce7ad4f871808115a2be4fab6b0481895ead51811b009`  
		Last Modified: Sat, 17 Aug 2024 02:05:16 GMT  
		Size: 228.2 MB (228165704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3679da09f22c1f0ba162a71a96ab452dd359da72ff4356ceae836e0272ea7c7`  
		Last Modified: Sat, 17 Aug 2024 02:05:13 GMT  
		Size: 6.4 MB (6380519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:76255b8027e84c76a4f3e0e88f9ddc781794eb36df42f105ce5a4c717b302a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6600fe1aaa3ba4b882325c766079bad49480ec06eadfafa6b1150ace79e306cc`

```dockerfile
```

-	Layers:
	-	`sha256:09a1414050b2ccaf7de44ce4ef77bb18ea24b50e9beffcc3a200b5b6a786dfef`  
		Last Modified: Sat, 17 Aug 2024 02:05:13 GMT  
		Size: 3.5 MB (3460616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e87622a9f0b8e04e790705cc037ac98d57203e09aa782423e471f93c5d0aa66`  
		Last Modified: Sat, 17 Aug 2024 02:05:13 GMT  
		Size: 24.4 KB (24395 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:3744a579857d78f8d9e9f440634f1709b0e02b63fd3c097af801bf72760f1c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.7 MB (265696954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd6eb1ca6607f261cb5830f4d21286e180e621f4a70f5dc2f6ca9d19f595a0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f9936b8374e5a0fb8fca8a4d11339eb63678e08db389852fd149fec27896df69';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b644d099fdacf660c627c6fda09ee5d680611f3195f8cebc1588b410e85cc9f0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='21c630eba973418d266c3cf1d96fdd3983537283c7529ee2ad304ac232fc745e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='4a1cd1d4e775453593d285daf2167c49c765b696c84083b57cc9148443025fdd';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796176255eb9eadf7741e60b3298ab78bb156acff4ff0b231c1728a3fab9c654`  
		Last Modified: Sat, 17 Aug 2024 02:29:05 GMT  
		Size: 12.1 MB (12114317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf28f29f72295fa6a61058bad3e2bdfbb944aa6282d1cb1036be5cf0b5bb2eab`  
		Last Modified: Sat, 17 Aug 2024 02:48:16 GMT  
		Size: 220.1 MB (220053227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241fa38442f67da1caefcf757126397625c61240706723c99959784ba77986b`  
		Last Modified: Sat, 17 Aug 2024 02:48:11 GMT  
		Size: 6.2 MB (6170727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8d7ad60df1d2f76d6967c944296a88f663a4bfd7eca380104dfbfdef71b308f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7afde78491275de847e801adb1f4a62df1b222f0ce2570dff6b69c957600047`

```dockerfile
```

-	Layers:
	-	`sha256:cfe86e6013e849623c250d9e425188741ac10e9a59456b2c1677472dae4f323b`  
		Last Modified: Sat, 17 Aug 2024 02:48:11 GMT  
		Size: 3.5 MB (3460905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda6c0d54d1e1693318021735f3549039a2c164e21e3338a1d4a86cca685d853`  
		Last Modified: Sat, 17 Aug 2024 02:48:11 GMT  
		Size: 24.7 KB (24695 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:9b05f5aa60943e657ac4fe406f5d85f94e7e3f1960a98e2ed0558bf42ee60f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284060101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af62e297542fffa2f4fa6850043773372aef0aaf3b404d745b378eb6e4590b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f9936b8374e5a0fb8fca8a4d11339eb63678e08db389852fd149fec27896df69';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b644d099fdacf660c627c6fda09ee5d680611f3195f8cebc1588b410e85cc9f0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='21c630eba973418d266c3cf1d96fdd3983537283c7529ee2ad304ac232fc745e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='4a1cd1d4e775453593d285daf2167c49c765b696c84083b57cc9148443025fdd';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8034c9a8e8a92761eab1079b6deff5f91278bcf3719ef203182c3fda1ab19c29`  
		Last Modified: Sat, 17 Aug 2024 01:11:07 GMT  
		Size: 12.9 MB (12888375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0f370074891c1de3f205bf1c38c5b90ea0d60412b2d172e4eada924badeff8`  
		Last Modified: Sat, 17 Aug 2024 01:34:51 GMT  
		Size: 231.5 MB (231505326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9a05066903a29e40912a9efb21a0a40079d28afd68f22c636adc1d691fe409`  
		Last Modified: Sat, 17 Aug 2024 01:34:46 GMT  
		Size: 5.2 MB (5202222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a405c23f35ef3c38f6d91b0183d2dfd2181a450be5c5326e6c0670dbd1dd627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3489552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324380297b36d8628e82d13aa222cdb26c54645b82f5abecbde4a6a926ba65a3`

```dockerfile
```

-	Layers:
	-	`sha256:c4e493ebdfe8ca44414e5ecf8a0486d3b98fd9eef583ab2f34c2ac8f5422471e`  
		Last Modified: Sat, 17 Aug 2024 01:34:46 GMT  
		Size: 3.5 MB (3465116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c04ade2dbed46e0f2ac3d021e300b985895d7b96bc6fc6f1f85a6ec038af41`  
		Last Modified: Sat, 17 Aug 2024 01:34:45 GMT  
		Size: 24.4 KB (24436 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:0b9993e4c747163bf063ce83a7b523eb789b1e8fab047a1dd8c0c0a23d66453b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273198960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ce97a32c6a44a1b4d5b22cbb22904d05802f563dd1a5cab79e3d83350164fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:560440017e541c07ad2788f24ed9fd81ef2e2966bd15d8bdd9726934a79c5242 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f9936b8374e5a0fb8fca8a4d11339eb63678e08db389852fd149fec27896df69';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_aarch64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b644d099fdacf660c627c6fda09ee5d680611f3195f8cebc1588b410e85cc9f0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_x64_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='21c630eba973418d266c3cf1d96fdd3983537283c7529ee2ad304ac232fc745e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_ppc64le_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='4a1cd1d4e775453593d285daf2167c49c765b696c84083b57cc9148443025fdd';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.0/ibm-semeru-open-jdk_s390x_linux_22.0.2_9_openj9-0.46.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:e280dadf5b2aeff3eee5ef7e055d95037f9fdf834a26d90fa2a2127a91d7cf49`  
		Last Modified: Tue, 13 Aug 2024 10:45:20 GMT  
		Size: 28.0 MB (28001322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a83917f7a3690422ed69c46b3c3cc9974d2c6923abc79136b0058ca106546`  
		Last Modified: Sat, 17 Aug 2024 02:04:16 GMT  
		Size: 12.2 MB (12203845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289534473702fc5afe43f61f93e5705f04c3e1360ec1d6dd84abe528f6c3aece`  
		Last Modified: Sat, 17 Aug 2024 02:26:24 GMT  
		Size: 226.4 MB (226428073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e91416a5ba8ae6298cacbdb83499a4595e11f595f97315bf65f6618efd8d693`  
		Last Modified: Sat, 17 Aug 2024 02:26:21 GMT  
		Size: 6.6 MB (6565720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ff780d750588ae36b935aa0b6587477c7f01ab4d1fbbc2ffb865cbecf9d050f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a9bdc4530b97165e2a6413bf67273d91a696a05ce614ac746a5a9087780897`

```dockerfile
```

-	Layers:
	-	`sha256:13952f08909c265fd56efd4b63b74a04c5c30f765c850cbe32c8ac6f1d382de4`  
		Last Modified: Sat, 17 Aug 2024 02:26:21 GMT  
		Size: 3.5 MB (3461743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a3a23d0df6be0c6457ff2f2dd1d15ed40d09c913d661165ef21dba5d987eb6`  
		Last Modified: Sat, 17 Aug 2024 02:26:21 GMT  
		Size: 24.4 KB (24394 bytes)  
		MIME: application/vnd.in-toto+json
