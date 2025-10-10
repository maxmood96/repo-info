## `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble`

```console
$ docker pull ibm-semeru-runtimes@sha256:629d8dab4d7e90883170d12715ecae14aff3c0af42daf32eecf6efb0cc03fd67
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

### `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:5a051de37dc7fa33657552f19955b47e4cf28437be88bf51f9718990430547c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274206789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45f8bbb995e4e337b3ea86b74f8608fa0ba8fb08bcb61ea3bea6d5f4c4ce21c`
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
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e8e03fdc309b3de4508516d0a5a06aa967a6fc2174cb52fb0201ac721c07d4e0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1d0ece62635ec04e23876139346aee778abd223d9f9fa65a3179405574de655d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30fa6751199feb88a866a01a24aea5845e445f0d49535920246db4436e48e6ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='756c3e8b504a3a7ea7483c16b313965ba665b3b6f39009f2aa420740c4642cc5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:5875f16cfbdc91b886191b0daa18cbb6f24ad6dd276e420d061123629793b1d8`  
		Last Modified: Thu, 09 Oct 2025 21:18:05 GMT  
		Size: 12.8 MB (12796721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15bb50cb3b141be0dafb7796350db804cc4ab334ce0174bb571f90ef09730a2`  
		Last Modified: Thu, 09 Oct 2025 22:50:26 GMT  
		Size: 225.3 MB (225320051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c833390573c801b05d0c23b9759d577e521e179c6d14e2098a094da8a6efc6`  
		Last Modified: Thu, 09 Oct 2025 21:18:01 GMT  
		Size: 6.4 MB (6366870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:09ca4948cc071e5a7dbbdf96579a98f8e4a81bdf24b17af7dd47688d7e8cb7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3279404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7196d154227192de23446293199af1e12133c6f3d638d9bf10bd63c1440adc`

```dockerfile
```

-	Layers:
	-	`sha256:c7e66672af92e679536c52fde993e9eae501e617bfd21ed137e57fbbcd73a86e`  
		Last Modified: Thu, 09 Oct 2025 22:45:09 GMT  
		Size: 3.3 MB (3253420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:131b1fee0c74f3910d53099d5fb91330f50d06395ecf1d0d914ef132d398caa8`  
		Last Modified: Thu, 09 Oct 2025 22:45:11 GMT  
		Size: 26.0 KB (25984 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:7b6f7b037aad8ea7375a15681b7842af7b6c02d59b222127c1960db8e10ed412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269225093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41b76b9cda87fae7121e8cfec26d89d6fb9425083bba4a7bf6769572a4b092b`
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
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e8e03fdc309b3de4508516d0a5a06aa967a6fc2174cb52fb0201ac721c07d4e0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1d0ece62635ec04e23876139346aee778abd223d9f9fa65a3179405574de655d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30fa6751199feb88a866a01a24aea5845e445f0d49535920246db4436e48e6ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='756c3e8b504a3a7ea7483c16b313965ba665b3b6f39009f2aa420740c4642cc5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:1a9dc6f8714f5e9dfd080d008db06e991e9d3b8911bb093e155f73919ef11832`  
		Last Modified: Thu, 09 Oct 2025 21:19:20 GMT  
		Size: 12.8 MB (12832062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a05365086b3cdd415519b8425a5f80fdb9d80a538431689a0bef2dd7650f73a`  
		Last Modified: Thu, 09 Oct 2025 22:54:28 GMT  
		Size: 221.6 MB (221561515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e69aea4dd5c9fcb7656370f82a27186a332111bcf73ea59f0326cea48bac908`  
		Last Modified: Thu, 09 Oct 2025 21:19:20 GMT  
		Size: 6.0 MB (5969804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c8054bb85c94078dad121435671ef92bf724c7625b34ff87a3c81dec857680c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d67a5c9655889d8e8718fa178e6f8b5ae7dbb72e16f4c442a6f945f00e7537`

```dockerfile
```

-	Layers:
	-	`sha256:c8b9927d2d60662016fd4e0af095c4fdea5d296f93d16b00068d29d91d4fb382`  
		Last Modified: Thu, 09 Oct 2025 22:45:16 GMT  
		Size: 3.3 MB (3252609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b1b3fa1023518f20e6f9e8a804d55a0a88f03443f36d8a3074ff2f136d4355`  
		Last Modified: Thu, 09 Oct 2025 22:45:17 GMT  
		Size: 26.1 KB (26118 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:9618c6e7cb664db92842b4641b9bcf6ad04a6b596f938fb33d1a372207d283f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282243383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9c939ab89de8644aa11881c96d748e269a0fa816e6f00fcdff3022b0b7f3f7`
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
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e8e03fdc309b3de4508516d0a5a06aa967a6fc2174cb52fb0201ac721c07d4e0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1d0ece62635ec04e23876139346aee778abd223d9f9fa65a3179405574de655d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30fa6751199feb88a866a01a24aea5845e445f0d49535920246db4436e48e6ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='756c3e8b504a3a7ea7483c16b313965ba665b3b6f39009f2aa420740c4642cc5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:76c4858b5b4b6be8c3c3114f549c0b29538be2a24819514674113a285a75b16d`  
		Last Modified: Thu, 09 Oct 2025 22:16:30 GMT  
		Size: 229.1 MB (229090464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6a1f38756a1779e3ced15286bdaa778154da4a3d4a6fd286f93bc138047a1`  
		Last Modified: Thu, 09 Oct 2025 21:32:26 GMT  
		Size: 5.1 MB (5053706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6de9cb20b32a0d9c7a9abcb4e9e1ba5a23783b4160616a786b4380e6a42f2620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3284092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f4aaa854dd45cc2c5765cea3a5c5a48335db9794c9d1c318faf53b17175eae`

```dockerfile
```

-	Layers:
	-	`sha256:86108f5b49798aabbcbd3b02bc701e3b272de7bff176b99cd99d6b9a9498c0bc`  
		Last Modified: Thu, 09 Oct 2025 22:45:21 GMT  
		Size: 3.3 MB (3258060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:157087079f5162bb09b8875f191dce6ebbd90f7658697477adcf857bc22d0848`  
		Last Modified: Thu, 09 Oct 2025 22:45:22 GMT  
		Size: 26.0 KB (26032 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:979ea8a80c7b0afdfe2aae9310cf0c861cceef6417982d05de732248a6b8a7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272410130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba059d9b1b93f26181d6b746a5f62e51929bbec6187271b32c26a71f865e9ce`
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
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e8e03fdc309b3de4508516d0a5a06aa967a6fc2174cb52fb0201ac721c07d4e0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1d0ece62635ec04e23876139346aee778abd223d9f9fa65a3179405574de655d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='30fa6751199feb88a866a01a24aea5845e445f0d49535920246db4436e48e6ee';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='756c3e8b504a3a7ea7483c16b313965ba665b3b6f39009f2aa420740c4642cc5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jdk_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:c10cf2b12567388a619bd04538b42e85ddb38fb92732eec842c56ab66d1341f1`  
		Last Modified: Thu, 09 Oct 2025 21:25:24 GMT  
		Size: 223.0 MB (223034680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcb3c778eb2d571cc3c9028ed55638b92c6d520638855765d12bcd51eea8ad1`  
		Last Modified: Thu, 09 Oct 2025 21:25:31 GMT  
		Size: 6.3 MB (6348479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-17.0.16_8-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c26c2032b65c15f13dd47987625aadb084291fb73e42245a6d392148b89ff190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3282228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faeb41fa7cff9d1db8c6bf1c506be63f65bcf9fac757554559c4568ef56febe`

```dockerfile
```

-	Layers:
	-	`sha256:b453472f337407601c97f7c2aa353786c1becbb667d40b0285652f17db7c8f82`  
		Last Modified: Thu, 09 Oct 2025 22:45:27 GMT  
		Size: 3.3 MB (3256244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe0558c7ffe7208d9b5fe015149a185d907f34a30b3e12a587cfb366ee5a0b8`  
		Last Modified: Thu, 09 Oct 2025 22:45:29 GMT  
		Size: 26.0 KB (25984 bytes)  
		MIME: application/vnd.in-toto+json
