## `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:35509ef07407cf6282310b8f64b94fe4c3cca2704e942cd4c096926720359657
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

### `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:c22c4d63a5ca25d8b28649db9543761c221dba490a0a38649e30966e9fca9201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278216771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcd2c3cbe098cd53ee6bd74e392c2055191e5ad1f259fa4f0fc9b8398afc0f2`
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef9e7ddf951c4ab6a4a32d35bf8e56de2a607ce0375ac9f8e96a329077b5585`  
		Last Modified: Sat, 17 Aug 2024 02:05:16 GMT  
		Size: 16.1 MB (16061153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b2852532a64123f2cc7383e63937118d63d80df2f3b4b86e26229412455590`  
		Last Modified: Sat, 17 Aug 2024 02:05:19 GMT  
		Size: 228.2 MB (228165655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cfd70aa30032fadfccf9e7655b3222d326d94c4d4649c9861b7bd7fe2bf43e`  
		Last Modified: Sat, 17 Aug 2024 02:05:16 GMT  
		Size: 6.5 MB (6478194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:59bdf23b86833a2c20342217a468a9ec12a7a0465a21b4eb95bdacefd875d40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6db688669cb1c26d6d25b28b84b2db8cc14330e8b94ab42c45952d7ad48403`

```dockerfile
```

-	Layers:
	-	`sha256:ef1d89126b4e3c811a98c5949628e7cb72ab5d22029b4cc763de096fb0a7baa1`  
		Last Modified: Sat, 17 Aug 2024 02:05:16 GMT  
		Size: 3.5 MB (3464787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08559182e5d69ee01e1ed4a8fa82379192dbbb7d956fe08ac4671f8452535b3a`  
		Last Modified: Sat, 17 Aug 2024 02:05:16 GMT  
		Size: 23.7 KB (23715 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:b8b272b168d566b4afe5d481123fd4416c8b864759f3e3b3f178eacfa02afb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268076698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc629bbf26ffcad64fb54cac9a5cf8352e4c0035bafea907ec674e39e0c1f65`
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
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32447b8d1d57938895b10ad9b2309236208473c6fb3255b4549476e77fb29e2`  
		Last Modified: Mon, 12 Aug 2024 17:59:36 GMT  
		Size: 15.9 MB (15924034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1542a59159f72fea488e9bdbc5c479dd1b6f3de870c3e3fc1bdd28789f8089`  
		Last Modified: Sat, 17 Aug 2024 02:47:02 GMT  
		Size: 220.1 MB (220053244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e37f6f3db96a617b86910c735173cd84683229cfb9f93ad90a62cfa086c8a5`  
		Last Modified: Sat, 17 Aug 2024 02:46:57 GMT  
		Size: 6.1 MB (6125203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:752d184be0eae8226979c5dc2ac898773a941cf362c3266593157b3007e2fd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3489025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9956907605a5ddcf0a645e239e67768dd758511539a608feb363601dfca7193`

```dockerfile
```

-	Layers:
	-	`sha256:ce2765fd2274ff19ffba61318b10b9d3cdd7d554a50fdc717a6f38317baa0464`  
		Last Modified: Sat, 17 Aug 2024 02:46:57 GMT  
		Size: 3.5 MB (3465033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:422ddafb626c23c1f31ef0fd41dda8f12be970d15bd049560391ed57cf725fad`  
		Last Modified: Sat, 17 Aug 2024 02:46:57 GMT  
		Size: 24.0 KB (23992 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:0c8db51cbd91482a31e2240b122d56e0254c26567db0152195ff1e17ad4204d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286004978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584cb113b1af9511acab29886957c6380cfe04682ae686240c40b5534e2a79aa`
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
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695549a4136bb16b902bceb966443542642f9c9131abb21acd5bd8417bdb51c7`  
		Last Modified: Mon, 12 Aug 2024 18:01:30 GMT  
		Size: 17.2 MB (17242215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676e77c68c9145eae0e58fb9bdc2f91930cc226e61e024bc3e3e8f93782a0bbf`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 231.5 MB (231505360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aeae5e97c40fe54ec2857a7b8b1e96da8f60ac6330f383c16574cbe0270e9d5`  
		Last Modified: Sat, 17 Aug 2024 01:33:06 GMT  
		Size: 5.2 MB (5180263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:09b45416dee5baf9ed3ec9c809de4123b0598542a348681e7a3625f35b7e7d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3492967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85f2fcd94bbfd41c293b646386fdc951c2537d8af4560611203d0851232883b`

```dockerfile
```

-	Layers:
	-	`sha256:e47120ee551a4fc380052a5bf73bed14970f2afc91ae295841e14e6bb39464d1`  
		Last Modified: Sat, 17 Aug 2024 01:33:06 GMT  
		Size: 3.5 MB (3469222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af172356a722ff2a45f3f3c6fbba5600eef8e7541ba3d1c578ec1b9354f631f8`  
		Last Modified: Sat, 17 Aug 2024 01:33:06 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:236d4c7a05a16de40a065a9b66022c1d2baf3d409fb698b850e7779448c9f1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275085358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ce425782eaedabd8ac466c9b744efaadc56d80d08f302be4ab7b6dac17ce55`
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
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b93975e5d2fc73ed41c077a1d77fbf02d2aa8bdc632d27ffbfa396e568a20ab`  
		Last Modified: Sat, 17 Aug 2024 02:02:42 GMT  
		Size: 15.8 MB (15753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8882692631031ce91991b2fb90675888486692f1d945e98a654a793fffdf8`  
		Last Modified: Sat, 17 Aug 2024 02:24:53 GMT  
		Size: 226.4 MB (226428072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f96538e53b04e463d437b27cac693948e7b32227b3af49eeb4207610d756ed`  
		Last Modified: Sat, 17 Aug 2024 02:24:48 GMT  
		Size: 6.5 MB (6536429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2_9-jdk-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:4963ade9f0832bf2bc6c5e593960f2e3b916847ee0a5b5a67e62d565124a0dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79af7a1f0bb0571a4b01cfcbdfa07541aa9a5e08bafbbfe51c6e477c26de25de`

```dockerfile
```

-	Layers:
	-	`sha256:2ad52803cc81c18f1c1368df5c69f0b17983a1662822b6e892bfab53f51f996e`  
		Last Modified: Sat, 17 Aug 2024 02:24:48 GMT  
		Size: 3.5 MB (3465113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0120e079047245958f5fb724563cdcf861045deebc8e1f98d3dfcd5536fa4b37`  
		Last Modified: Sat, 17 Aug 2024 02:24:48 GMT  
		Size: 23.7 KB (23715 bytes)  
		MIME: application/vnd.in-toto+json
