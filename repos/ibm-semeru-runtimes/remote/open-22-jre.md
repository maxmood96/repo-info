## `ibm-semeru-runtimes:open-22-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:baafab3f332ddb061a7e42733343e211c5024f7f91c1406586905fcb163e7809
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

### `ibm-semeru-runtimes:open-22-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:272f5c418e20be1a801181787e0fa3908d7f3544af71098fa399bc6c9ab5b64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102033216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc1c77658ab9a078f6e24b4ac7da33e4de9c0d99d3841009b828a3288cb0c45`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Jun 2024 05:42:02 GMT
ARG RELEASE
# Tue, 04 Jun 2024 05:42:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 04 Jun 2024 05:42:02 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 04 Jun 2024 05:42:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-22.0.1+8_openj9-0.45.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a8f4d53b51eda84d76ba4ac6860ae300884f2d140fe7b756b3c4a6a5823eaea5';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_aarch64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8c02a6d2d78eff437dad98cb7fa0a27301bb1e6877bf6407ecb047c94a480452';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_x64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6a7a3f626d4672a17ad3b3b17f05ba29ecf37c479cd0434790a5566feffe92ef';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_ppc64le_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        s390x)          ESUM='6f652c2dc45f13bb24578e648207cc42c82d1732b70636a21d0dcbef9bc85e50';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_s390x_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1876b4b2ad10a485a0730642d2553cad73074629caa459ef1d4dce0d5f089c49`  
		Last Modified: Tue, 02 Jul 2024 03:04:00 GMT  
		Size: 12.2 MB (12156384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da8da7519b83374883a486c01fa887e97137228ba2c76efe53bcd197dfbe87`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 55.2 MB (55190191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a58964b13dc2ce007469200535b65c19695a9c268c2247c52825b3c1f1d12b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 5.2 MB (5152586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:f22207125a97ce4f464739ae86ad70bdb3fcf0a2f682570c5350af26236d9f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af425355201a9d49e9ee3e3044df53c16d5ba809ad3693d373a3a5cb76b610bb`

```dockerfile
```

-	Layers:
	-	`sha256:b104dec30c5d9bc6cb47062d09131d2e1e3232849ded5e6ccf0f6be7574aabad`  
		Last Modified: Tue, 02 Jul 2024 03:04:00 GMT  
		Size: 3.4 MB (3433979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:073dc90c3e204e2400210014deba8121f1aa7ef4d24af74dd3c98ef2bb0dde8b`  
		Last Modified: Tue, 02 Jul 2024 03:04:00 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:b5c4c9cab25facd85e43fc85dcfec4b4f57ccfc3c1945c30c4f860e143bbb740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95922947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a5eb6a6085e2964f654945178e82b99b6b1b3fd493d35c38bb622276ca4402`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Jun 2024 05:42:02 GMT
ARG RELEASE
# Tue, 04 Jun 2024 05:42:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 04 Jun 2024 05:42:02 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 04 Jun 2024 05:42:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-22.0.1+8_openj9-0.45.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a8f4d53b51eda84d76ba4ac6860ae300884f2d140fe7b756b3c4a6a5823eaea5';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_aarch64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8c02a6d2d78eff437dad98cb7fa0a27301bb1e6877bf6407ecb047c94a480452';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_x64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6a7a3f626d4672a17ad3b3b17f05ba29ecf37c479cd0434790a5566feffe92ef';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_ppc64le_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        s390x)          ESUM='6f652c2dc45f13bb24578e648207cc42c82d1732b70636a21d0dcbef9bc85e50';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_s390x_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692adf9a131a320c3ae4ce96d951bd52523484a08c2b71d83bd894fb57af1a9e`  
		Last Modified: Tue, 02 Jul 2024 15:05:06 GMT  
		Size: 12.1 MB (12114298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a0e6f3fc758d00f03ef386aad501c91b1b00636642ad4897d29048dac41e59`  
		Last Modified: Tue, 02 Jul 2024 15:15:15 GMT  
		Size: 51.6 MB (51576203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3da04b1bc4113ab30a47897ff95a3ecc81bccf4d0db2f6cd6b41e477191df8`  
		Last Modified: Tue, 02 Jul 2024 15:15:14 GMT  
		Size: 4.9 MB (4872421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ee376ab349084c680fc57879c5537fd601475c55514f85c315dd61370b789571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5814862dee48289587fab66e0ad3098d1678948a8bf7d80633b50bd318fd1ab8`

```dockerfile
```

-	Layers:
	-	`sha256:14274a6aa1f482cde690c4f89c4b298d78317f81afca2b9cf82aae41885ba81c`  
		Last Modified: Tue, 02 Jul 2024 15:15:14 GMT  
		Size: 3.4 MB (3434268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1ca9c5a04e9dae03836e972357c53219d18ba45032adf65abb61b9dd7a59560`  
		Last Modified: Tue, 02 Jul 2024 15:15:13 GMT  
		Size: 24.7 KB (24699 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:b3e00977d695077e30d808d51c7fa215ed3fca9acee2e252d2c1082dcbb02292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108188175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220284f8e9c84ebe716ab9baf09044c37a5b9f478f8ebf960a4e4168e33bbe99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Jun 2024 05:42:02 GMT
ARG RELEASE
# Tue, 04 Jun 2024 05:42:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 04 Jun 2024 05:42:02 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 04 Jun 2024 05:42:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-22.0.1+8_openj9-0.45.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a8f4d53b51eda84d76ba4ac6860ae300884f2d140fe7b756b3c4a6a5823eaea5';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_aarch64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8c02a6d2d78eff437dad98cb7fa0a27301bb1e6877bf6407ecb047c94a480452';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_x64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6a7a3f626d4672a17ad3b3b17f05ba29ecf37c479cd0434790a5566feffe92ef';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_ppc64le_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        s390x)          ESUM='6f652c2dc45f13bb24578e648207cc42c82d1732b70636a21d0dcbef9bc85e50';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_s390x_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba08511b677aee03243955ecffe2cf3bff11dcf9bbc6f35ad5e9deb073b144`  
		Last Modified: Tue, 02 Jul 2024 10:27:08 GMT  
		Size: 12.9 MB (12888223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7725f0c552e48d92b45caca7d9242e5ff68c2256f110710c0e31664e698d35f`  
		Last Modified: Tue, 02 Jul 2024 10:40:24 GMT  
		Size: 56.8 MB (56849587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933bddd554b15cb456059cdf68445a9e110f7a2ff3f2b6db05d4634f7c36484d`  
		Last Modified: Tue, 02 Jul 2024 10:40:22 GMT  
		Size: 4.0 MB (3989284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e137bdb9f9ac6f567aeaa3378b4ca2a5fd4b5c1534d9f9cf7f8fbbdd98ce7a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2e88fef2c5e9efad622f19e963099ede69c3a0a0d1bbd898f723c9721dd44e`

```dockerfile
```

-	Layers:
	-	`sha256:1a64b209e52094239fa1054256133e1c7ff28b40f62f9fc0ea072ddaf1a045f7`  
		Last Modified: Tue, 02 Jul 2024 10:40:22 GMT  
		Size: 3.4 MB (3438479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e341426d80ccee8ec203e020b4c663ee6aff81af8db15ee09259ce9cecf6b082`  
		Last Modified: Tue, 02 Jul 2024 10:40:22 GMT  
		Size: 24.4 KB (24440 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:db5eba02324f8138f1036a52c3d9d750279dcc1530de0732def3148a62570309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100059102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e07ffcef39c594da8bfcb4bc29dd195c21a42d4581de6d258383f7931233e5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 04 Jun 2024 05:42:02 GMT
ARG RELEASE
# Tue, 04 Jun 2024 05:42:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 04 Jun 2024 05:42:02 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 04 Jun 2024 05:42:02 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Tue, 04 Jun 2024 05:42:02 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-22.0.1+8_openj9-0.45.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a8f4d53b51eda84d76ba4ac6860ae300884f2d140fe7b756b3c4a6a5823eaea5';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_aarch64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8c02a6d2d78eff437dad98cb7fa0a27301bb1e6877bf6407ecb047c94a480452';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_x64_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='6a7a3f626d4672a17ad3b3b17f05ba29ecf37c479cd0434790a5566feffe92ef';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_ppc64le_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        s390x)          ESUM='6f652c2dc45f13bb24578e648207cc42c82d1732b70636a21d0dcbef9bc85e50';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.1%2B8_openj9-0.45.0/ibm-semeru-open-jre_s390x_linux_22.0.1_8_openj9-0.45.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac3110a5d1eebf9525a140f60c8dbde0133312ec7905bb4cff8ce58bfde450`  
		Last Modified: Tue, 02 Jul 2024 05:55:15 GMT  
		Size: 12.2 MB (12203618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe68c2b6908974aec7852a13d999b1034e468a7247ec83dbcab79d9237aa36a3`  
		Last Modified: Tue, 02 Jul 2024 06:07:04 GMT  
		Size: 54.6 MB (54559381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ca73d9bdcda962f4473b538d988d2bc121881ac4d501cd45b153be4397cbf1`  
		Last Modified: Tue, 02 Jul 2024 06:07:02 GMT  
		Size: 5.3 MB (5295563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:59b094fee0cfd6a04c6f3bb440ef5b56c030c81af9fb9a7ca662ef2bcdea4b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f5c54c06e506d42c04175029f53ac2be91ff996fee165fcea6a762a28426f1`

```dockerfile
```

-	Layers:
	-	`sha256:3efc59de8b07d839b1eb98e426271356a83c047b799b1e353d1b7e014322fc04`  
		Last Modified: Tue, 02 Jul 2024 06:07:02 GMT  
		Size: 3.4 MB (3435249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c96df165864580318c425bd04cf200f74eba055d5a297e5fe150d6780afe3c`  
		Last Modified: Tue, 02 Jul 2024 06:07:02 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json
