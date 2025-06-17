## `ibm-semeru-runtimes:open-8-jdk-noble`

```console
$ docker pull ibm-semeru-runtimes@sha256:7f7dd51606856376019d97eb3a0b932dd1390061ff694e1903584d2b445c015f
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

### `ibm-semeru-runtimes:open-8-jdk-noble` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:9bf0e271d25909729b400544351f29c3a4145097863a46056223274755f2fe73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163562723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0bbb1ed7f835532f3e241baa6cc4536ada168670ea4d8b7af5a2bb03269f0c`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63440d5653d1f0918e4b4f6899330285ff039602665297c0e0720ac582f81864';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87fabcc61f08710c4e2f644b09632d29a48cb23e41c54a82bfd6e1d38b867229';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1049c6fc42d2d590981c4932a82e985b279c450eabc37bb13415b346a4ebad11';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='9392b88b4abc7843e903cbebd86854bebcefee262140c31f8b5ffd9e9443fe6d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:c93dd3f2b76daac4e73efa9837887606db87cae200aae7f92e1396a1c47dffd2`  
		Last Modified: Tue, 17 Jun 2025 17:12:21 GMT  
		Size: 12.8 MB (12796709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfac002e6855d3762444f1788315e689692d73cf0a6f830ef19d6f77a4eb3fb3`  
		Last Modified: Tue, 17 Jun 2025 19:53:19 GMT  
		Size: 116.7 MB (116749205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c564d91e322b378cc48156626b23875209a2aa262170e3bdf9ffc56836c66c11`  
		Last Modified: Tue, 17 Jun 2025 17:12:21 GMT  
		Size: 4.3 MB (4301472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:aa412a78c12e8ee188e0922e10effe4da20ac224d90fb203e2939fbec973bacc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b548cc67a31b0b8627d82010e40fdd00eedda561d77b5175881f016f50d4d56`

```dockerfile
```

-	Layers:
	-	`sha256:39486a7dd12bfc12c8dc7cdcc4be44232641315eebd278df186431787e872213`  
		Last Modified: Tue, 17 Jun 2025 19:47:28 GMT  
		Size: 3.4 MB (3363285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde8255f76a27cb0401a98360844e12b717ec37ca02871037fdb5c8f024d9b36`  
		Last Modified: Tue, 17 Jun 2025 19:47:29 GMT  
		Size: 25.9 KB (25929 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk-noble` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:402c0f262e775a37a49682bab186ee71b8d37527b4ecf177bf98cb9ea7d4104e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162364511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe66d760307d53aa0e07d75c46aea529d133d71b5eab7c4864428725d65045ec`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63440d5653d1f0918e4b4f6899330285ff039602665297c0e0720ac582f81864';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87fabcc61f08710c4e2f644b09632d29a48cb23e41c54a82bfd6e1d38b867229';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1049c6fc42d2d590981c4932a82e985b279c450eabc37bb13415b346a4ebad11';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='9392b88b4abc7843e903cbebd86854bebcefee262140c31f8b5ffd9e9443fe6d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:5dd455cb37d70d4300a6bb58081e5321b756aef06e41f913ecbf7e467a9b01bd`  
		Last Modified: Tue, 17 Jun 2025 17:41:16 GMT  
		Size: 116.6 MB (116631970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b068d9bef34a68d4bd1495525220cd2163f1d2ba100e37bd3b80bfffedfbe`  
		Last Modified: Tue, 17 Jun 2025 17:40:52 GMT  
		Size: 4.0 MB (4047684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:9b27d766bcf2ce7d07cbf3c33a595356fd92b57bd04ea0b2fc7d7e91d44d58a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09b4e2cb8c1a1964c55eaaa8bae12476ea11e141f9479d8749628e10f1d8b3`

```dockerfile
```

-	Layers:
	-	`sha256:bed356fc5a7f79bc7f76ad6bdec0682f31a66666436ad1fd8eef3918908a593b`  
		Last Modified: Tue, 17 Jun 2025 19:47:34 GMT  
		Size: 3.4 MB (3363908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915cc993bd200f06ee7d6b7d00248d88b631124181be05250035f9456cd2f91d`  
		Last Modified: Tue, 17 Jun 2025 19:47:35 GMT  
		Size: 26.1 KB (26063 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk-noble` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:d24474971af2dae53d34c2ce5d8939c5617fdcd19381f683d728ff0dbb48c294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169804165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196cf143083bfadc75525b260c61071723473b55297edbcfe8c0ca84e2bae458`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63440d5653d1f0918e4b4f6899330285ff039602665297c0e0720ac582f81864';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87fabcc61f08710c4e2f644b09632d29a48cb23e41c54a82bfd6e1d38b867229';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1049c6fc42d2d590981c4932a82e985b279c450eabc37bb13415b346a4ebad11';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='9392b88b4abc7843e903cbebd86854bebcefee262140c31f8b5ffd9e9443fe6d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb3d3a727bf52cc64383cf0903fe76de73b3a9f81931a96fc7774a425e1ddc1`  
		Last Modified: Tue, 17 Jun 2025 17:56:42 GMT  
		Size: 13.8 MB (13798845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ba7f23a063f31a02e1a9cb5a10a854bb87bf6956b5bfd9d150e6b98a0455c1`  
		Last Modified: Tue, 17 Jun 2025 17:56:45 GMT  
		Size: 118.2 MB (118222456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83e5ee12c0e5030315743b533cc3b2e51113257ec3a277421603fbab814277f`  
		Last Modified: Tue, 17 Jun 2025 18:15:12 GMT  
		Size: 3.5 MB (3457654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:8a98edbe57c7a429debf927cebfdbd490f5aad62e88cb192965ee38b2e5b5e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3394074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469bab1ddfc250893bc2478035d028f8f5e451bde317edc66b8ff6befa558139`

```dockerfile
```

-	Layers:
	-	`sha256:e04b669d808dee4c0bfacd74b088bb4fd4f8c45fb32736521b43c04da37944f5`  
		Last Modified: Tue, 17 Jun 2025 19:47:39 GMT  
		Size: 3.4 MB (3368097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21f44ed095ee1c156b7abeed9adc2c186c3ccc56db915b02668f9b48c964d019`  
		Last Modified: Tue, 17 Jun 2025 19:47:40 GMT  
		Size: 26.0 KB (25977 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jdk-noble` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:a336ab16086ec8ac8d2b8957d8fffb7196e3a0046e985c0c36b5b2af36a2d1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164021165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1760295debd853b27dcf71787d436baa1cd237b5b32a81c6a66e1ff757a56c18`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:29 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:29 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:31 GMT
ADD file:486993225aeae656f8d559f5c296f6c3164966e35f4b628d26e1da1b75592143 in / 
# Mon, 28 Apr 2025 09:45:32 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk8u452-b09_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63440d5653d1f0918e4b4f6899330285ff039602665297c0e0720ac582f81864';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='87fabcc61f08710c4e2f644b09632d29a48cb23e41c54a82bfd6e1d38b867229';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='1049c6fc42d2d590981c4932a82e985b279c450eabc37bb13415b346a4ebad11';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='9392b88b4abc7843e903cbebd86854bebcefee262140c31f8b5ffd9e9443fe6d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u452-b09_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_8u452b09_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:52a1750d5fddc355cdc90a83890b7d582c7f145aa5d114d9582cd010b8ead145`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 30.0 MB (29956186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c57a4cd6f9e08c6ca153a6d888f12e81ea6453fc88e81d3368fb7833166789`  
		Last Modified: Fri, 09 May 2025 03:23:20 GMT  
		Size: 13.1 MB (13120912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7ef2f651ad61112284c49560aec66caec6efd60d1df8dddab2a3de793d6c13`  
		Last Modified: Fri, 09 May 2025 16:47:20 GMT  
		Size: 116.6 MB (116564878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ffa5660fe22a594b8f06fca497b131b4ab0d85472d756fd66ce9a186e43a70`  
		Last Modified: Fri, 09 May 2025 16:47:18 GMT  
		Size: 4.4 MB (4379189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jdk-noble` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:9cf01cfa5448c24dbfe7583dbeb8b2b375d89e1af36e4af6b57a15b50b118aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952611c556c368cc8498b6f02e729b2e4537d0c4a6fcac1ebe86e0931359a242`

```dockerfile
```

-	Layers:
	-	`sha256:2af8ba7f69fca1dec59d7d19539e6eb3fa3bea63f5e838545191debbb61c4d81`  
		Last Modified: Tue, 17 Jun 2025 19:47:44 GMT  
		Size: 3.2 MB (3227402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:917bd809fa75045225bc17d470a2311a365a660d7cd3d93a9a3d9b7da5f01458`  
		Last Modified: Tue, 17 Jun 2025 19:47:45 GMT  
		Size: 24.6 KB (24634 bytes)  
		MIME: application/vnd.in-toto+json
