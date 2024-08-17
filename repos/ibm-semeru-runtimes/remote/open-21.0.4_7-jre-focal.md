## `ibm-semeru-runtimes:open-21.0.4_7-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:2d39d12234ec4e4da39d27c6f3124e4a7052d1bf791164765163cae56365710f
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

### `ibm-semeru-runtimes:open-21.0.4_7-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:b6d28089c5c2554e3a6982c590a602eb257a89d484c0f883ddcf35a7cd236402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104852104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2d5ac8121160c14a9358aec5d98c858742326104f76cd8a91fbc1d0f82cdd9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cda6391db96db77167829a775e72d90079fb78887140595648f2959dafc8360b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6db728e08b4cba2490e720cf4e11d13096f6ecfe9429a60a996128c4d629a26e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='f30cdddf90283b12fbf8ff8c9957fca82bd5f0cf2cc493e9a8bcf4646793b016';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='07f0b16876e7f54bcccc51d704db898812c72285fc72413a06517c3baacbf6b1';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bc66afda6dd973ae7308d0942a99e2330a31be7cfb6b274ebcf27ae4dae60d`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 16.1 MB (16061097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7442972f0095d415751b6f51756c4ce259c2a779504ad97359d0ffb5e94b6720`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 56.1 MB (56102311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36af490bd543df0b964c414f91b197be48bfaa0035a9f2be1eddfa8e33d6a8c7`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 5.2 MB (5176927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.4_7-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:1d9eac2984a2413ad209659253271f1370f5b99dd9f7c29813f495875557c271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e065b4efe9c74403b541c8f7fb2ee9805f281fcbfe7a1152563e9757ed0576b4`

```dockerfile
```

-	Layers:
	-	`sha256:5c0c18c620d65fc75e10cd056552634f542687f9012ab495bb9d740064fd80e0`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 3.5 MB (3463701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347a682338cfaec3eca7eb8b4754164ebd6bf5ae7affcff1ff6bd47d2769837`  
		Last Modified: Sat, 17 Aug 2024 02:04:57 GMT  
		Size: 23.7 KB (23717 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.4_7-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:547b59ef7fc267c155c64a3593fa3847223eddd7f5d2ec7d420a94435cdf0994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99309401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f08f0d29228cb8c41a389f2eea19e89fbc965c332f31aa9c518fef793e8d5e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cda6391db96db77167829a775e72d90079fb78887140595648f2959dafc8360b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6db728e08b4cba2490e720cf4e11d13096f6ecfe9429a60a996128c4d629a26e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='f30cdddf90283b12fbf8ff8c9957fca82bd5f0cf2cc493e9a8bcf4646793b016';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='07f0b16876e7f54bcccc51d704db898812c72285fc72413a06517c3baacbf6b1';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:d1dbbb1c5d31b6b82888e676a7c77ea51fa5bce4c28d968fa65d86ee9fc619d8`  
		Last Modified: Sat, 17 Aug 2024 02:44:41 GMT  
		Size: 52.5 MB (52489470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797c4b4b979412ac71e40b2d894fe583422874cb73635b79ce8bf3e5a9511733`  
		Last Modified: Sat, 17 Aug 2024 02:44:40 GMT  
		Size: 4.9 MB (4921680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.4_7-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:901f01db04159055b1bc8c8bf33fe7df9b876427be8ae9107d5f8c1b7495a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ed59b3a120085eed6f77c58153babd09433375b4e5de3c33a02793f9b1d343`

```dockerfile
```

-	Layers:
	-	`sha256:af6b4a36b9175e935d7525bea27780aed913bf763fdf1b32960ce26b351e7b31`  
		Last Modified: Sat, 17 Aug 2024 02:44:40 GMT  
		Size: 3.5 MB (3463947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f32f2ba8e74c830527696aac884171e50dc588278b8515e7bc0b3186b50f33`  
		Last Modified: Sat, 17 Aug 2024 02:44:39 GMT  
		Size: 24.0 KB (23995 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.4_7-jre-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:1d2cca4c8e454abe148ed58782d0610e344785d90edfe64146ce014e81c3e0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111067038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55938f5bf5a0b1cf23aad6f7b1d9c0a62bcb547ec9de7ccc0f8ca37be0f13bc0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cda6391db96db77167829a775e72d90079fb78887140595648f2959dafc8360b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6db728e08b4cba2490e720cf4e11d13096f6ecfe9429a60a996128c4d629a26e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='f30cdddf90283b12fbf8ff8c9957fca82bd5f0cf2cc493e9a8bcf4646793b016';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='07f0b16876e7f54bcccc51d704db898812c72285fc72413a06517c3baacbf6b1';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695549a4136bb16b902bceb966443542642f9c9131abb21acd5bd8417bdb51c7`  
		Last Modified: Mon, 12 Aug 2024 18:01:30 GMT  
		Size: 17.2 MB (17242215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85072fbf2815f5628bdaf5f5200293e94121cad3880167f6acdd17eab56c6ac8`  
		Last Modified: Sat, 17 Aug 2024 01:30:12 GMT  
		Size: 57.8 MB (57774602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a95d38fd7a829368b7e36c4cf0d8ce6ee4e930106c63f607bbf7eaaa6795da`  
		Last Modified: Sat, 17 Aug 2024 01:30:10 GMT  
		Size: 4.0 MB (3973081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.4_7-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8f97c8a0264d6233019426f872f49c9b99c7d3424b4cabab30ecbdb6f7b98cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c960fb6c2a23a284a2a419704d58355c322953ec5db5dd3606734a6d46729f`

```dockerfile
```

-	Layers:
	-	`sha256:cfd35fa7047440e1bf04afa73100f5c26aae71085b9abcbbadda71575bfacf42`  
		Last Modified: Sat, 17 Aug 2024 01:30:10 GMT  
		Size: 3.5 MB (3468136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ab13081f3838db227c169b25b729728c296acb119e8992cda0b8c601c61c521`  
		Last Modified: Sat, 17 Aug 2024 01:30:10 GMT  
		Size: 23.7 KB (23748 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.4_7-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:4144ae62411aa56bfd3a5366f91a2d00935eb2bcc1dc87b84891a07b0174e8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102508477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a4a079e219c9c4c3e80353a884c8e8e0f3c8b661e3c7296c7ced4b477badd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 12 Aug 2024 02:58:45 GMT
ARG RELEASE
# Mon, 12 Aug 2024 02:58:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 12 Aug 2024 02:58:45 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 12 Aug 2024 02:58:45 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 12 Aug 2024 02:58:45 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-21.0.4+7_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cda6391db96db77167829a775e72d90079fb78887140595648f2959dafc8360b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6db728e08b4cba2490e720cf4e11d13096f6ecfe9429a60a996128c4d629a26e';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='f30cdddf90283b12fbf8ff8c9957fca82bd5f0cf2cc493e9a8bcf4646793b016';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='07f0b16876e7f54bcccc51d704db898812c72285fc72413a06517c3baacbf6b1';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.4%2B7_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_21.0.4_7_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:3b93975e5d2fc73ed41c077a1d77fbf02d2aa8bdc632d27ffbfa396e568a20ab`  
		Last Modified: Sat, 17 Aug 2024 02:02:42 GMT  
		Size: 15.8 MB (15753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba57d702238d6242b2890ef9a1916add7aad44372f504f87ab1a5d3938b3f89`  
		Last Modified: Sat, 17 Aug 2024 02:21:58 GMT  
		Size: 55.0 MB (55046493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4b4d3b614f5debaeafe0635915f78ff6325407e8ed92f2300e22312871edc6`  
		Last Modified: Sat, 17 Aug 2024 02:21:57 GMT  
		Size: 5.3 MB (5341127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.4_7-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e9405d453c3b226ded8c092c4539bf023788bcd9fd140a84c441c9a454c19218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cd80ab694f806c2010d74b06d071499318f7206de2b655f993447b8caec2e9`

```dockerfile
```

-	Layers:
	-	`sha256:ecef7951d2ad64974eaf02cc7625dc410bb5598337562dae2673a30216ef48ba`  
		Last Modified: Sat, 17 Aug 2024 02:21:57 GMT  
		Size: 3.5 MB (3464019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cadeab07b0fb957bb42911bb86aa0fb1d5ab5473763818b904e3f7e9f3f1fea`  
		Last Modified: Sat, 17 Aug 2024 02:21:57 GMT  
		Size: 23.7 KB (23717 bytes)  
		MIME: application/vnd.in-toto+json
