## `ibm-semeru-runtimes:open-26.0.1.0-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:b2fedfb507b62520bd576e9de09cd41d265217e66a94e125d6f0234eefe7dc59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:20be7ab6d2d5b8c5aa42ae6dc2f0429936ec4fdf5100d64be72116d1d9fe7a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302618404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e353eb0ededab045bd923ab38be0cd771961aed9c060c7eab2dd391f27d2309`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:46:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:46:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:46:06 GMT
ENV JAVA_VERSION=26.0.1.0
# Thu, 30 Apr 2026 23:47:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='98fe02a30ee4aa709c9bdf8d358205e76b87194e737accf83dc94499973acfc6';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_aarch64_linux_26.0.1.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3dff964af21b38cf968568832e48a6b4053f3680c685644b7336864570f201f1';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_x64_linux_26.0.1.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5ec6fb11341c7508e8b9d7ccf44f6126039b2ae6be9d713506cd2bdbeb92e1ca';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.1.0.tar.gz';          ;;        s390x)          ESUM='08f5164d2cab42eb7ca8c4130fc1e27da9df6508399eb5d0615d0932b8ddae72';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_s390x_linux_26.0.1.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:47:47 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:47:47 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:48:51 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Apr 2026 23:48:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73deabe49f5a3366034b61ee0a801655f1999c54861478351017b1b26b6f8186`  
		Last Modified: Thu, 30 Apr 2026 23:47:27 GMT  
		Size: 12.2 MB (12172077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1724259f9a91fcca8442c4fc8a655dffcb633a7f43a22ad16befa4809cfafb5`  
		Last Modified: Thu, 30 Apr 2026 23:49:16 GMT  
		Size: 253.9 MB (253916016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e317ddad0eb7b5546bfb9e24c6f6438c252bb7d14c4f5863ec11bf2712db9648`  
		Last Modified: Thu, 30 Apr 2026 23:49:11 GMT  
		Size: 6.8 MB (6793813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d5a7693a554afb1296ad13140ee43cd52f53c68f2e4cff4dd1d9ec382fe679f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3bfde9648018cc1cc2df865b3b74b8adac84996d8faf19695e24a799030ba6`

```dockerfile
```

-	Layers:
	-	`sha256:eae16470fd8659b53a2e58174dff23366112b7198104379f5898133035bc422d`  
		Last Modified: Thu, 30 Apr 2026 23:49:11 GMT  
		Size: 3.8 MB (3820926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a041da71d97ce7eee0937d9d11e4389edc7dd86c7a135ea3793c86d90e3049`  
		Last Modified: Thu, 30 Apr 2026 23:49:11 GMT  
		Size: 25.2 KB (25186 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:672f62c9da2e6155a5e2ecadf9b688691debee7a8a57d21a9a25662888bfdf4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295493912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e1ebf16643219e0f0ed7bc22c46ca31cd5e110b671eb49f5755181d62d148c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:46:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:46:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:46:01 GMT
ENV JAVA_VERSION=26.0.1.0
# Thu, 30 Apr 2026 23:47:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='98fe02a30ee4aa709c9bdf8d358205e76b87194e737accf83dc94499973acfc6';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_aarch64_linux_26.0.1.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3dff964af21b38cf968568832e48a6b4053f3680c685644b7336864570f201f1';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_x64_linux_26.0.1.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5ec6fb11341c7508e8b9d7ccf44f6126039b2ae6be9d713506cd2bdbeb92e1ca';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.1.0.tar.gz';          ;;        s390x)          ESUM='08f5164d2cab42eb7ca8c4130fc1e27da9df6508399eb5d0615d0932b8ddae72';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_s390x_linux_26.0.1.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:47:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:47:43 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:48:47 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Apr 2026 23:48:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c01f9b946f616afade4a2702a5b15ea782588d477982815baf0fb6456beeb1`  
		Last Modified: Thu, 30 Apr 2026 23:47:21 GMT  
		Size: 12.1 MB (12142757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c93b4e7a2a8b051e0dd4358c21a5230c6c92632a924af0af98306e08681c0a`  
		Last Modified: Thu, 30 Apr 2026 23:49:14 GMT  
		Size: 249.2 MB (249209293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd511234922f0099825a2c59365c9444dc554b069f3bc4f55020062ded4b342`  
		Last Modified: Thu, 30 Apr 2026 23:49:08 GMT  
		Size: 6.5 MB (6535319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:dda8ca64548254570b124c269aacbae0d36a5564e088eafef5b39ecebd61b9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19cd9d61d9b858663c1f87d61c2400dac6e2a465a969dfe73789b8e00cde080`

```dockerfile
```

-	Layers:
	-	`sha256:63c63e45df61e7048c3865176004ab371122d823c73ee9fb913515b54d9849fb`  
		Last Modified: Thu, 30 Apr 2026 23:49:08 GMT  
		Size: 3.8 MB (3818675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c637890c437448230c4a3515c7bf3b55d897aa570e404b09a88bd26338a94cab`  
		Last Modified: Thu, 30 Apr 2026 23:49:08 GMT  
		Size: 25.3 KB (25296 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:e5d3ba279005b2d310d43f3ca3172cf7f000bf6859bc230a8426c979d1099c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297839003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cca30fedadc7404159e03d443fed6b62fbafd422f394c0fb61d6730f597afed`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:50:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:50:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:50:11 GMT
ENV JAVA_VERSION=26.0.1.0
# Thu, 30 Apr 2026 23:57:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='98fe02a30ee4aa709c9bdf8d358205e76b87194e737accf83dc94499973acfc6';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_aarch64_linux_26.0.1.0.tar.gz';          ;;        amd64|x86_64)          ESUM='3dff964af21b38cf968568832e48a6b4053f3680c685644b7336864570f201f1';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_x64_linux_26.0.1.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5ec6fb11341c7508e8b9d7ccf44f6126039b2ae6be9d713506cd2bdbeb92e1ca';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_ppc64le_linux_26.0.1.0.tar.gz';          ;;        s390x)          ESUM='08f5164d2cab42eb7ca8c4130fc1e27da9df6508399eb5d0615d0932b8ddae72';          BINARY_URL='https://github.com/ibmruntimes/semeru26-binaries/releases/download/jdk-26.0.1.0/ibm-semeru-open-jdk_s390x_linux_26.0.1.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:57:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:57:25 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:58:29 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Apr 2026 23:58:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0badf736d5dc588ee1611bcc905fc1b6be06b130293cdb7383b80f11cd7f549b`  
		Last Modified: Wed, 15 Apr 2026 20:51:44 GMT  
		Size: 12.2 MB (12224849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b35da972d9326db81039eaa0fcf0e80025c90cda3a4bda8f48dbd002e55ed22`  
		Last Modified: Thu, 30 Apr 2026 23:59:02 GMT  
		Size: 250.4 MB (250403967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f96704090e28185583b0d60feeb101cc9eaa57e765ee9102e77e54a25e1da63`  
		Last Modified: Thu, 30 Apr 2026 23:58:58 GMT  
		Size: 7.0 MB (7007888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-26.0.1.0-jdk-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:37b7c5cce78d2168d34fa4c98da2374e272b7fb2ae81c0446a064ad796cc9d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5515b2faa8ca9487d119b013369818ed3e6439314233af901e28564da2800b1a`

```dockerfile
```

-	Layers:
	-	`sha256:e27b8c27ca897f55409c57c965c22b9fe79dccea0c6c789625afc439b235f5ae`  
		Last Modified: Thu, 30 Apr 2026 23:58:58 GMT  
		Size: 3.8 MB (3810106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea10faa992b4d431d413f5ec48fb470048469e280ebc709ac3579c8a49d50e09`  
		Last Modified: Thu, 30 Apr 2026 23:58:58 GMT  
		Size: 25.2 KB (25185 bytes)  
		MIME: application/vnd.in-toto+json
