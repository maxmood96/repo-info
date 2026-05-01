## `ibm-semeru-runtimes:open-26.0.1.0-jdk-noble`

```console
$ docker pull ibm-semeru-runtimes@sha256:8cdf0669e20781fc988b31506b8b41677ec0773548dbc4ed8d01fa0478f8728c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-noble` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:29af80fd202b3f40b6f602914b123eabb5d27f8962a9d69b36493907a62b2277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303162827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728ec84893463b68c79a3479996f9fdb7a5435be5f182cbf4064190aa72e92d9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:46:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:46:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:46:10 GMT
ENV JAVA_VERSION=26.0.1.0
# Thu, 30 Apr 2026 23:47:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='98fe02a30ee4aa709c9bdf8d358205e76b87194e737accf83dc94499973acfc6';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_aarch64_linux_26.0.1.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3dff964af21b38cf968568832e48a6b4053f3680c685644b7336864570f201f1';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_x64_linux_26.0.1.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5ec6fb11341c7508e8b9d7ccf44f6126039b2ae6be9d713506cd2bdbeb92e1ca';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.1.0.tar.gz';          ;;        s390x)          ESUM='08f5164d2cab42eb7ca8c4130fc1e27da9df6508399eb5d0615d0932b8ddae72';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_s390x_linux_26.0.1.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:47:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:47:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:48:49 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Apr 2026 23:48:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cd737a8b9091e9a2bcd6d0afc1e4c62a0f2c266c8566bc302804b9c46de824`  
		Last Modified: Thu, 30 Apr 2026 23:47:27 GMT  
		Size: 12.8 MB (12805392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2777d54ebdedc2c1bf76ee286fdfbe0038a3183042d4630cd0e7e81b8e312bf`  
		Last Modified: Thu, 30 Apr 2026 23:49:15 GMT  
		Size: 253.9 MB (253916025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ea8173903eb7f473de6cade8a43066a7e3a4083575b83b640b70a2ce24b4b0`  
		Last Modified: Thu, 30 Apr 2026 23:49:08 GMT  
		Size: 6.7 MB (6708432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:9888353434ca7791a452e79de9dea967062ca338d8a53bca5ca1e552e85ecce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3287561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09efbc20520ccc5f9d2797a672b8a1f61b15543485d1e4ae606aa73076dec065`

```dockerfile
```

-	Layers:
	-	`sha256:84fde3e2f926b1e731150c5673e8c180d862c3d2bf3f11e783cf0c2c70e48756`  
		Last Modified: Thu, 30 Apr 2026 23:49:08 GMT  
		Size: 3.3 MB (3261695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53cc62845227b7cedd04c971047960159c0bc772ce19203371e1e1aa8e9696d`  
		Last Modified: Thu, 30 Apr 2026 23:49:07 GMT  
		Size: 25.9 KB (25866 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-noble` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:85b94ff5de1f132c0289957e36275803e7d47737193fbdb75d58aeb5c63f0b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297541652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3eb74b7a4f5ecbace5676ce6cfadfc1e27682316f388af05ef76c3aa4e30e5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:44:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:44:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:44:47 GMT
ENV JAVA_VERSION=26.0.1.0
# Thu, 30 Apr 2026 23:47:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='98fe02a30ee4aa709c9bdf8d358205e76b87194e737accf83dc94499973acfc6';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_aarch64_linux_26.0.1.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3dff964af21b38cf968568832e48a6b4053f3680c685644b7336864570f201f1';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_x64_linux_26.0.1.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5ec6fb11341c7508e8b9d7ccf44f6126039b2ae6be9d713506cd2bdbeb92e1ca';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.1.0.tar.gz';          ;;        s390x)          ESUM='08f5164d2cab42eb7ca8c4130fc1e27da9df6508399eb5d0615d0932b8ddae72';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_s390x_linux_26.0.1.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:47:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:47:52 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:48:56 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Apr 2026 23:48:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc4c9b689ae1dc862c993ab2e648a6c8bb6f88c5194c547d934ac67358471f0`  
		Last Modified: Thu, 30 Apr 2026 23:46:10 GMT  
		Size: 12.8 MB (12837720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0cdd78442ad78c961ac481ec13a34df76474fbfd44701619559e3d15636b1a`  
		Last Modified: Thu, 30 Apr 2026 23:49:24 GMT  
		Size: 249.2 MB (249209293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee4e55d0c7dd0d4ecb65152f79d030c255e4f8d917ce44b30b228a0b613cbc`  
		Last Modified: Thu, 30 Apr 2026 23:49:18 GMT  
		Size: 6.6 MB (6618854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:51367204a5a95480670150bb6720a9178f6b7f38886429bb75ca3026ed9ffe3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3286260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e490009791bd120414eaf8582a1b303fc62489ba30f780b446c1ae830d4c87c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a2a5771e97cfda9ab92c8c11b94a5399f57615421483fdc16de781f4277a`  
		Last Modified: Thu, 30 Apr 2026 23:49:18 GMT  
		Size: 3.3 MB (3260261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47261b8077b5bacee4242626e795457c77dbf648a7bb5218e0c7fdc347d90679`  
		Last Modified: Thu, 30 Apr 2026 23:49:17 GMT  
		Size: 26.0 KB (25999 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-noble` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:cb91934604d02c0f52436c75a788062677fdfcd7efd934425a582e690c61957f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300382730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318032126533dc6672c138ada8960f46870d391cd015b159849d58970295792`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:55:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:55:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:19 GMT
ENV JAVA_VERSION=26.0.1.0
# Thu, 30 Apr 2026 23:45:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='98fe02a30ee4aa709c9bdf8d358205e76b87194e737accf83dc94499973acfc6';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_aarch64_linux_26.0.1.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3dff964af21b38cf968568832e48a6b4053f3680c685644b7336864570f201f1';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_x64_linux_26.0.1.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5ec6fb11341c7508e8b9d7ccf44f6126039b2ae6be9d713506cd2bdbeb92e1ca';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.1.0.tar.gz';          ;;        s390x)          ESUM='08f5164d2cab42eb7ca8c4130fc1e27da9df6508399eb5d0615d0932b8ddae72';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_s390x_linux_26.0.1.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:45:49 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:45:49 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:46:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Apr 2026 23:46:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1dca01c7f8a5c02c033ddd80e1849e4d2dce0090b72e585925cee97f083f26`  
		Last Modified: Wed, 15 Apr 2026 20:56:59 GMT  
		Size: 13.1 MB (13117391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15662db92a1ded7801579923aa51b644287d9bf5aeb6acec3469bd9764b02`  
		Last Modified: Thu, 30 Apr 2026 23:47:28 GMT  
		Size: 250.4 MB (250404020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d284867b183a036b0fc541e7f7a65007b2957b73ababdf252fd8bad8d72eb10`  
		Last Modified: Thu, 30 Apr 2026 23:47:24 GMT  
		Size: 6.9 MB (6949172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:61f027c87465fb1cc8e5b570ee6fca63f509d29bcbb35a4ebeee1b2cceac141f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3277347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7743517a7a06067ee80a6afc8cd528ea9973fe9867cab0e79c28c964b22f6215`

```dockerfile
```

-	Layers:
	-	`sha256:5fc53a498893f9ffd99930e7d9c0ce4f60371f1a5248bd784465d598b9ef9dc8`  
		Last Modified: Thu, 30 Apr 2026 23:47:24 GMT  
		Size: 3.3 MB (3251481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a486c304cfb9d7f90ffe81673478c9cd33d128cf397f12cbec20d149b4d2813d`  
		Last Modified: Thu, 30 Apr 2026 23:47:24 GMT  
		Size: 25.9 KB (25866 bytes)  
		MIME: application/vnd.in-toto+json
