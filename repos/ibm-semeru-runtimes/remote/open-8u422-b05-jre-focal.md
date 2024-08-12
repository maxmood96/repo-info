## `ibm-semeru-runtimes:open-8u422-b05-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:b2f99503382e8f9a1aff0a6e981e2d882067b1f71aec1ad3fe70f242673595d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibm-semeru-runtimes:open-8u422-b05-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:6d30165e03a3bd30d24d0ba675d1eb405b89dd92b4e83b60815450e054a9649d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98166808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c91a9a8906d0c11bfdaac8d299428b032bc84f96ae101504d43ddcb9a594dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='5b89c3f2d330edf6d338f25b5f42ca19a86e4a47bd05e2ab71588f7bf12e2a37';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87abc1becdf3217ac22bd8cd82283da4dd05feb2e1d20a3e2fe54b29629c331a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='bc8d17fa5435a72ccd22348b3374ce725b7e9fcdffdb65f1d3245ec84c0cc114';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='6f6330081657d3d87d9d822124c143fa1a89cc329e02303e2cd9b254a0a86ff9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2879252b1df64eb9a46a4feb7941f845d18e534f4e50ce1d0a712901cd7982`  
		Last Modified: Mon, 12 Aug 2024 17:59:19 GMT  
		Size: 16.1 MB (16061133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60c5c8d99f90af5ea91fd74791782753fc52679b0c46e32da69e8e32067a03`  
		Last Modified: Mon, 12 Aug 2024 17:59:19 GMT  
		Size: 50.3 MB (50315836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7919fc1f865214f77f8479e02559a2e27e26a2a0514444ea1c6cc30d1f254577`  
		Last Modified: Mon, 12 Aug 2024 17:59:19 GMT  
		Size: 4.3 MB (4278070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:0f921cd3d71c370aed42b3e5d15cb72954a64f4cdf0de9f953db7f86a1e0aefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3510051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b109414ac17f2d4bc6a707668d0ba7e24b5c24bb6c3704b3e4a7c6431defea5`

```dockerfile
```

-	Layers:
	-	`sha256:d4f6d83c7b1fd88af64d96bbf3e85641ae5c728f5239862ddcb7579058f08eb1`  
		Last Modified: Mon, 12 Aug 2024 17:59:19 GMT  
		Size: 3.5 MB (3486361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0ae9c986ce37f61308b10b61a5e38920a1787dee4aa7453cbf7bc489d3ddd2`  
		Last Modified: Mon, 12 Aug 2024 17:59:19 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u422-b05-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:290a084fe572a003e481685220d59b89e3820ccdf8b3b20f63bfe9db0d5d3372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95717819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c75e6c89df2fd036dc7532ecd8aa8fbcc55cc57167a0b2c0f9478b84435c9b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='5b89c3f2d330edf6d338f25b5f42ca19a86e4a47bd05e2ab71588f7bf12e2a37';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87abc1becdf3217ac22bd8cd82283da4dd05feb2e1d20a3e2fe54b29629c331a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='bc8d17fa5435a72ccd22348b3374ce725b7e9fcdffdb65f1d3245ec84c0cc114';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='6f6330081657d3d87d9d822124c143fa1a89cc329e02303e2cd9b254a0a86ff9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32447b8d1d57938895b10ad9b2309236208473c6fb3255b4549476e77fb29e2`  
		Last Modified: Mon, 12 Aug 2024 17:59:36 GMT  
		Size: 15.9 MB (15924034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b54cb08b9af7851db43b70d850865a8827f389006ae6f2763f13b6d6f9e0f0`  
		Last Modified: Mon, 12 Aug 2024 18:02:23 GMT  
		Size: 49.8 MB (49752552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2ce29d3f2690b1726da17dde6205d10f8499acfd39fbc4a32c6e769e2223b`  
		Last Modified: Mon, 12 Aug 2024 18:02:22 GMT  
		Size: 4.1 MB (4067016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:35b73f7e59309bd2f01472e881700d50a00f7f798b329f943e62a036279e267e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3510575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7654bfc0a535f1ccaa2d117b49ed2f229b642b3c65b498d898ff7ef515df86a`

```dockerfile
```

-	Layers:
	-	`sha256:51cf480d9c50ab51d3973cc9d9ec7027a368ac247a91ca08f95782c01efc01a3`  
		Last Modified: Mon, 12 Aug 2024 18:02:21 GMT  
		Size: 3.5 MB (3486607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a98bf29e2fb2cbfb4473dcbde8af298a1a7872a8b40becdbbbebbc263dff0f`  
		Last Modified: Mon, 12 Aug 2024 18:02:21 GMT  
		Size: 24.0 KB (23968 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8u422-b05-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:c572a7a03246d0fb66a4b5d81ce4c16a07ff3a937f319580bf09b5b189eeef09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96822776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67e43334be8176444d9bc24ca1c6c9e5577ff90a555af34ff91cbd82e3b71d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk8u422-b05_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='5b89c3f2d330edf6d338f25b5f42ca19a86e4a47bd05e2ab71588f7bf12e2a37';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87abc1becdf3217ac22bd8cd82283da4dd05feb2e1d20a3e2fe54b29629c331a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='bc8d17fa5435a72ccd22348b3374ce725b7e9fcdffdb65f1d3245ec84c0cc114';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='6f6330081657d3d87d9d822124c143fa1a89cc329e02303e2cd9b254a0a86ff9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u422-b05_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_8u422b05_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d9bfbbbf60157e2169295f7cd4bd25fa2a1795efc1e7ae7dbbde5a31ba28b7`  
		Last Modified: Mon, 12 Aug 2024 18:00:43 GMT  
		Size: 15.8 MB (15753637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96103776a9d9bf8a29ac16e5c8e55a2cb720e65b3d132fc2f7db0a6e2e42947`  
		Last Modified: Mon, 12 Aug 2024 18:04:07 GMT  
		Size: 50.3 MB (50287026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dbb2cd7322ff176b79e82a1554a35b1c6357eff22da7a052da12a1fd79a53d`  
		Last Modified: Mon, 12 Aug 2024 18:04:07 GMT  
		Size: 4.4 MB (4414919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8u422-b05-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c84ebd0ebca95123e555a18551b7a8e445f77317a54da766c011cf6edb56a0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3510370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a8ad2351c28b4c6a5f2494b709c849dd73ac5c11b0b646e32ce82277bf6345`

```dockerfile
```

-	Layers:
	-	`sha256:bf68081caea62fd7d73ec1dbc00947760532ac9c4f58b6042fcc1335d76f321f`  
		Last Modified: Mon, 12 Aug 2024 18:04:06 GMT  
		Size: 3.5 MB (3486679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1fe8a24531e69b92eee462a5ea976197f4d388c9f042bec3b5923318d6c54d`  
		Last Modified: Mon, 12 Aug 2024 18:04:06 GMT  
		Size: 23.7 KB (23691 bytes)  
		MIME: application/vnd.in-toto+json
