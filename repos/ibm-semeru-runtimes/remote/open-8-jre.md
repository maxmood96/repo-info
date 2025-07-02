## `ibm-semeru-runtimes:open-8-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:138aaa3656d0d6258b9e7dd1c5769702b0fb5e55f2087b7566cac80e24407971
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

### `ibm-semeru-runtimes:open-8-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:6143c3fb8db1e62d323c828d09b0ccfbe80b64bb27a8c56341af700a6067a50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97295188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fd838aaeb5ffe7c28090b7a5e8b086443e5e844b66c77024065d5b0c7934b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='89cf44e225cb1daa274e805a615f59bb0140dbd4bddcfbe4cecc12dd8c3a9fed';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='59b6b66a14f4c264e81aca7a35339fc2eb907211a1953d61c44c9882fa79153c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0ac75bf18399ece85749ebf63f1fd6210daa63f6df595205edcc7a45400ba13c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='512b7127dce034ee0e0430e11ddcf25c91bbe4356d66c5e4ede311be7fbca16d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b61ecbfe14e73f3ffccab37e142358f2a8d97e0a6e2374c19ced000c7fd429`  
		Last Modified: Tue, 17 Jun 2025 17:12:21 GMT  
		Size: 12.8 MB (12796588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3777d173cea45ff8bb19827f460761a17904faf6f2c8ef65e2b7baeccb68221b`  
		Last Modified: Tue, 17 Jun 2025 17:12:31 GMT  
		Size: 50.5 MB (50498638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa12946670711557864a6d96e097cea3a22dcf26099010d9751d808d2984e8`  
		Last Modified: Tue, 17 Jun 2025 17:12:24 GMT  
		Size: 4.3 MB (4284625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:05c62f2e54dc06c15d63af705882c59f3686709e3ed65dbe7bd51af5c183ebd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3224019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8294aff9463057964a25cf0611877d1a396831fbc324744d91ef21a05c8f610f`

```dockerfile
```

-	Layers:
	-	`sha256:40e7ecfea741ae14fbfb1d2e185042b994281aa240f6ef36d55696454211cf62`  
		Last Modified: Tue, 17 Jun 2025 19:47:58 GMT  
		Size: 3.2 MB (3198093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d571c5c07f8577792060fb00ec80e5decb18eaf8c66b9ce90d0add7bf2ab6de`  
		Last Modified: Tue, 17 Jun 2025 19:47:59 GMT  
		Size: 25.9 KB (25926 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:3d44dcdbe675436ab5b33df12f084b6c855f3c63772c56fd6183e82b8c9e5455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95680128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b439650329b4478bb59fee6f2ed0f979dd80bcea972f0e385dad0039aefdb405`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='89cf44e225cb1daa274e805a615f59bb0140dbd4bddcfbe4cecc12dd8c3a9fed';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='59b6b66a14f4c264e81aca7a35339fc2eb907211a1953d61c44c9882fa79153c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0ac75bf18399ece85749ebf63f1fd6210daa63f6df595205edcc7a45400ba13c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='512b7127dce034ee0e0430e11ddcf25c91bbe4356d66c5e4ede311be7fbca16d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955e26dc56bf1ae03f975ad08a85374b58c57b02658a31e012ab92e88b350f74`  
		Last Modified: Tue, 17 Jun 2025 17:40:52 GMT  
		Size: 12.8 MB (12832958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a97558551ea4d13c45e1c22af32aac23b06e9ee68058fc5844ca174bda62b4`  
		Last Modified: Tue, 17 Jun 2025 17:43:12 GMT  
		Size: 49.9 MB (49934823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60df17a95ca8e051a62f491b3739101413a63c5885aaa102b091765b75225633`  
		Last Modified: Tue, 17 Jun 2025 17:43:04 GMT  
		Size: 4.1 MB (4060448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3472f39773c81400266af138f89159ce97376bbcb9a61f14d9ae88a559cbe1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3224774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c59bab6fed5cd906d77cdf7ab9ec4c1ce0aff923e2cb1b45cd669b76f9676`

```dockerfile
```

-	Layers:
	-	`sha256:1a893d5d1ddaf8f289229e59ef55478dfa388c30b9f43a87086b2e8ea15808a2`  
		Last Modified: Tue, 17 Jun 2025 19:48:04 GMT  
		Size: 3.2 MB (3198714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f2aa851ce271a40489dd83c723aff2454f7c5ade4516017c6cb250a7325f39`  
		Last Modified: Tue, 17 Jun 2025 19:48:05 GMT  
		Size: 26.1 KB (26060 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:da13c9c32b56d696bd92029995540e9fb722281175481aaf26d1f5df7f8416c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103500226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ad6f93fee676f53450a694d935d945d060598c293747bc995d9e49429b3087`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 17 Jun 2025 14:26:50 GMT
ARG RELEASE
# Tue, 17 Jun 2025 14:26:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Jun 2025 14:26:50 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 17 Jun 2025 14:26:50 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Tue, 17 Jun 2025 14:26:50 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='89cf44e225cb1daa274e805a615f59bb0140dbd4bddcfbe4cecc12dd8c3a9fed';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='59b6b66a14f4c264e81aca7a35339fc2eb907211a1953d61c44c9882fa79153c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0ac75bf18399ece85749ebf63f1fd6210daa63f6df595205edcc7a45400ba13c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='512b7127dce034ee0e0430e11ddcf25c91bbe4356d66c5e4ede311be7fbca16d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd26c3c59cb80b8708ba86b5eccadbcdb584bbcce61b0bbb1ba8d99090fd48d`  
		Last Modified: Wed, 02 Jul 2025 03:34:12 GMT  
		Size: 13.8 MB (13798752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d300c3d7c8317d7dd45a7465e0da79ca30d334e7f33d9d2221d28b2bf206c33`  
		Last Modified: Wed, 02 Jul 2025 03:36:29 GMT  
		Size: 51.9 MB (51920025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339feae8bfd43274be5b453f0d4379292f6509e888f682b49a327b6e8ffe9380`  
		Last Modified: Wed, 02 Jul 2025 03:36:27 GMT  
		Size: 3.5 MB (3459943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d6ae8074ec85e0ea3bdc60e8fce79ac8516ac00905688dc9c60a3bf9814a44f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3228873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a0b78f1d5f65633507786f85dcff86a4b6d371187634b6e0466da1a379785e`

```dockerfile
```

-	Layers:
	-	`sha256:9bba0464d4178becfb6dbad758d3f38db9146714a099913e13c7fc6518b41420`  
		Last Modified: Wed, 02 Jul 2025 04:46:13 GMT  
		Size: 3.2 MB (3202899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258d7860c92ee9ab4b86588266bcadd25ca086a4eae2dfcb956b27c6a84ba062`  
		Last Modified: Wed, 02 Jul 2025 04:46:14 GMT  
		Size: 26.0 KB (25974 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:0cab9a95f971573a6125c8a78d7b82a3ddd8de1f1387cb45ea5d8194cf8da148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97859363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8550ca081fd5601a48cdc9c3c9d11facba616b08ecb879815897cce73bacf68d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 May 2025 04:29:46 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:46 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:29:47 GMT
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
# Thu, 29 May 2025 04:29:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='89cf44e225cb1daa274e805a615f59bb0140dbd4bddcfbe4cecc12dd8c3a9fed';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='59b6b66a14f4c264e81aca7a35339fc2eb907211a1953d61c44c9882fa79153c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='0ac75bf18399ece85749ebf63f1fd6210daa63f6df595205edcc7a45400ba13c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='512b7127dce034ee0e0430e11ddcf25c91bbe4356d66c5e4ede311be7fbca16d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3d9804ea46173500d61b748d47fd014ac4a121d697f8b77915d0922d08f34`  
		Last Modified: Tue, 17 Jun 2025 18:05:15 GMT  
		Size: 13.1 MB (13120220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdf504ecd563e55e7b3f0da558727a7540c9e769953f8cb9b97f678d5f2190c`  
		Last Modified: Tue, 17 Jun 2025 18:05:20 GMT  
		Size: 50.4 MB (50447209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e298cea7ca0bc8d1d3445fff27c2e7dd20eafc7e4915d530bc1df7a7aea075`  
		Last Modified: Tue, 17 Jun 2025 18:05:15 GMT  
		Size: 4.4 MB (4361878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6472c04197c171efac60e6fa63e19a6df361df421a9429bd70c037a11ee0aa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3226843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23851621992a480aaf9500ed71a7383cb29071b7d37b8d7e30bbcff235b00001`

```dockerfile
```

-	Layers:
	-	`sha256:4106c29e6d1a61a927374a69643fcf69af4aa2b8625f8fba07e598b78bdde9c7`  
		Last Modified: Tue, 17 Jun 2025 19:48:14 GMT  
		Size: 3.2 MB (3200917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994ea8324dd17ae5d28672c6e65bbdaa709b32d7c256bab14b33dfc3e4229730`  
		Last Modified: Tue, 17 Jun 2025 19:48:15 GMT  
		Size: 25.9 KB (25926 bytes)  
		MIME: application/vnd.in-toto+json
