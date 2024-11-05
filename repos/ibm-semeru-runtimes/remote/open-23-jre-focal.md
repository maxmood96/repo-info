## `ibm-semeru-runtimes:open-23-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:cf26d7c068984247ee21e326876b08f37f64d7728d121e124ef2881cb2645c5a
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

### `ibm-semeru-runtimes:open-23-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:a3a5147bacedb163ae321fde00a413008314b8bb97e53db5dc8cb5139717f125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104264500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979dfa7798c1bc19e3889073db19d81cf1492060b6e17a8ec33e6ecfc56aa1a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='df011058dbfbe58ed7cbd96ce9123ca13cedec3d3ffd106f4051fd8b6dbcf489';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='07fbd261313f5121953936cdee0a02ed70f62e4dcc18b06b1072a26fdf37ddc7';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='19418381d4deb34bff8aaceb9d951f967ba42a33a764a0e096d5282ad6566edc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='3cbaeccbbe6ab1d14639a781264341e95abd16a813551bbd38c03f824e1cdffc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6655bb9c1f80bde32086fd96fa6e920739f0605ad3c75b75d852ef8bf2910a`  
		Last Modified: Mon, 04 Nov 2024 22:05:02 GMT  
		Size: 16.1 MB (16082599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b774a5c81835a9494510e1c072e60f03fad98b6b1869a55ca5017c81bd3569`  
		Last Modified: Mon, 04 Nov 2024 22:05:03 GMT  
		Size: 55.2 MB (55212121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812e0a5d63dfc9057f26bd1e6164200e7f9d955de323a0cdfa554be9726f9d19`  
		Last Modified: Mon, 04 Nov 2024 22:05:02 GMT  
		Size: 5.5 MB (5458720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d6e590db7e38df9618785f7418bd1293727d684abcd6ad96ec2792ae380283ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a628400a344bc1788f11f2e15e2e6fe977812789ee881ef758af5f28e63f508f`

```dockerfile
```

-	Layers:
	-	`sha256:2c4cc59176095240d74612813322f8b25c6f15d8a9ad2e960c67f944123a089a`  
		Last Modified: Mon, 04 Nov 2024 22:05:02 GMT  
		Size: 3.6 MB (3592266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e2c0a31912e426be01c4e1e85efd1f876e8deef6ccd14af12c1778b5c5dbf44`  
		Last Modified: Mon, 04 Nov 2024 22:05:02 GMT  
		Size: 24.0 KB (24047 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:8107ebe9959e7dda8c4d2604a55c7cc204f9e760f43c06fc41bfbf7e3d2ce101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98626450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5db950b73ef7af2c72fb73545dd2535d66d3212f71553e42329d276e47e02d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='df011058dbfbe58ed7cbd96ce9123ca13cedec3d3ffd106f4051fd8b6dbcf489';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='07fbd261313f5121953936cdee0a02ed70f62e4dcc18b06b1072a26fdf37ddc7';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='19418381d4deb34bff8aaceb9d951f967ba42a33a764a0e096d5282ad6566edc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='3cbaeccbbe6ab1d14639a781264341e95abd16a813551bbd38c03f824e1cdffc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c87aac1d4ce7ba28204a4f8c7ccbc4da254cdd092097b48a1bbda757f24ae4c`  
		Last Modified: Mon, 04 Nov 2024 22:06:02 GMT  
		Size: 15.9 MB (15945006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2098c2060c77932c7485882615b3d80caa824bcac18932bf4716130b9ead65a0`  
		Last Modified: Mon, 04 Nov 2024 22:36:53 GMT  
		Size: 51.5 MB (51547834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2103801b078573e81af59e022fbd69a1193056d5270dc452bd2a816cddab53`  
		Last Modified: Mon, 04 Nov 2024 22:36:52 GMT  
		Size: 5.2 MB (5159782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:9df61e31f2bdb02522fce637952147687eeaded4f96b05b75a08e3edd06ecba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac00be4ae7275f42f711b8c5a9b0d23a02d4c89f15f460a0ebce39dfce7fe487`

```dockerfile
```

-	Layers:
	-	`sha256:292072b1bd402b6268085418d17675fd58b04510a6c151632726690cd3f234b2`  
		Last Modified: Mon, 04 Nov 2024 22:36:52 GMT  
		Size: 3.6 MB (3585581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bdaa57c2cfdecdca113a66b70014f9b098005c587008e8a642fe3987849d591`  
		Last Modified: Mon, 04 Nov 2024 22:36:51 GMT  
		Size: 24.2 KB (24158 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:a84fd198f424938ae48cc3c2bee0ff6fa9b5620206ec257476c6b2c1b7cd7dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110362062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10c3e204836f6c064e1f71b1e46c14a45dfa574d2da72309529759a8ac04d46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='df011058dbfbe58ed7cbd96ce9123ca13cedec3d3ffd106f4051fd8b6dbcf489';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='07fbd261313f5121953936cdee0a02ed70f62e4dcc18b06b1072a26fdf37ddc7';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='19418381d4deb34bff8aaceb9d951f967ba42a33a764a0e096d5282ad6566edc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='3cbaeccbbe6ab1d14639a781264341e95abd16a813551bbd38c03f824e1cdffc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c03062ba6cc89d48fbed8c001c307b5b41e0a5f776a5ecb43457bcbf48b0c0d`  
		Last Modified: Mon, 04 Nov 2024 22:05:24 GMT  
		Size: 17.3 MB (17256542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c955afbfec6358842ca2e74636574acfb2ebdd68df980223fde969836847205`  
		Last Modified: Mon, 04 Nov 2024 22:51:35 GMT  
		Size: 56.8 MB (56806286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639f67422a818106deb6544ad28d326d7fbb1d044cd80fae27793b5995173dcb`  
		Last Modified: Mon, 04 Nov 2024 22:51:34 GMT  
		Size: 4.2 MB (4222728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6871849d658def9fe9501fbcdc21d85176da0820fbd391910516e529e5dab1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0216bd823b895adf540275e5ebfb6d9c25bd69cad86cf82afb737627f5633eb`

```dockerfile
```

-	Layers:
	-	`sha256:c1591d1b3eafb593799a39392593b12d7d70885f4d8f322b6e5257db23b42f1e`  
		Last Modified: Mon, 04 Nov 2024 22:51:34 GMT  
		Size: 3.6 MB (3596701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9474f1ed3f2870a998aeaaa5ba5bc7fc74560f5fea33541f532d314e4cc1c6dd`  
		Last Modified: Mon, 04 Nov 2024 22:51:33 GMT  
		Size: 24.1 KB (24084 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-23-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:48968817570c55bfa229bd7f2c3dd97d3cd54581013ff6be472e2dd09ca82b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102270388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b67c5436baf912695f200e71dd5c7ff670f5cee8ee119e9ffc1ec184edb51c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:23 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:23 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:24 GMT
ADD file:e3e9bad1c3576edf8ddea2dd7af2ed8ecac1ad0b15d714dd9c51f679d44d13b6 in / 
# Fri, 11 Oct 2024 03:38:24 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-23+37_openj9-0.47.0
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='df011058dbfbe58ed7cbd96ce9123ca13cedec3d3ffd106f4051fd8b6dbcf489';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_aarch64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        amd64|x86_64)          ESUM='07fbd261313f5121953936cdee0a02ed70f62e4dcc18b06b1072a26fdf37ddc7';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_x64_linux_23_37_openj9-0.47.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='19418381d4deb34bff8aaceb9d951f967ba42a33a764a0e096d5282ad6566edc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_ppc64le_linux_23_37_openj9-0.47.0.tar.gz';          ;;        s390x)          ESUM='3cbaeccbbe6ab1d14639a781264341e95abd16a813551bbd38c03f824e1cdffc';          BINARY_URL='https://github.com/ibmruntimes/semeru23-binaries/releases/download/jdk-23%2B37_openj9-0.47.0/ibm-semeru-open-jre_s390x_linux_23_37_openj9-0.47.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f6b14778eb4fed5cbb0bd80eea19d48526571f3b2dfa0196faf63f42fdb8c6c2`  
		Last Modified: Fri, 11 Oct 2024 04:41:53 GMT  
		Size: 26.4 MB (26365979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae76440d6755e318199681b6d987a4b8660d5945e0ea29db0a034c2ad4c00548`  
		Last Modified: Mon, 04 Nov 2024 22:07:59 GMT  
		Size: 15.8 MB (15773072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab15f22ae1e7fc381987a74a88a10641dd3a4f63c38ccfc480d70beb7ed2cb5`  
		Last Modified: Mon, 04 Nov 2024 22:47:58 GMT  
		Size: 54.5 MB (54522262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a41b6d0e7e76dfcad265e4e95a463e0cf588c3264854b5410b1ca7284b9e5f`  
		Last Modified: Mon, 04 Nov 2024 22:47:57 GMT  
		Size: 5.6 MB (5609075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-23-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:5d57b420752a25e04fce3e2c3ce02c7c1193ff45b388620da6f6d5f8718b0ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f8bff54fcbb3c8d6ce5082bf6319be52a14c9661d51beeb0adad719f7dc8a1`

```dockerfile
```

-	Layers:
	-	`sha256:0f4510e0642b7fd643d829b096202e7118e3a996598433af543e01e4d03357a2`  
		Last Modified: Mon, 04 Nov 2024 22:47:57 GMT  
		Size: 3.6 MB (3593687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563238849dfc72e0368d975fbd8d41077beed06cba1e36e67bd99c9b2d660e1f`  
		Last Modified: Mon, 04 Nov 2024 22:47:57 GMT  
		Size: 24.0 KB (24047 bytes)  
		MIME: application/vnd.in-toto+json
