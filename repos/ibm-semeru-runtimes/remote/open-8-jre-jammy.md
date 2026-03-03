## `ibm-semeru-runtimes:open-8-jre-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:5f908739232278330540df7bfb65f805aa64cd0a6b81031eb76911c4da10df0a
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

### `ibm-semeru-runtimes:open-8-jre-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:c706ac39b1ccb9a3302cbc0423256da4635a8c9941bccce23f2a1a9e951c5360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99945033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec18e7bf362b4af1ee164ccb260b1f9c6afd615b83da65ebab6cdee45c7a776`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 03 Mar 2026 20:13:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Mar 2026 20:13:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 20:13:42 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 03 Mar 2026 20:13:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 20:13:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:13:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 20:14:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7ab00954e0b6a8eaf58c6dd519b5388e9ba4c857f845e107232607110184`  
		Last Modified: Tue, 03 Mar 2026 20:15:00 GMT  
		Size: 12.2 MB (12171320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835c20d76c5af408c2bfe49a5e080b713cc002e55ab7531e2a6a9d11f5580b49`  
		Last Modified: Tue, 03 Mar 2026 20:15:02 GMT  
		Size: 54.0 MB (53997216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e0736a80cca9f1134b2b0656fe6c435108f591c353bbfacc09754491791ff0`  
		Last Modified: Tue, 03 Mar 2026 20:15:00 GMT  
		Size: 4.2 MB (4239131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:80dde0d78c9a33e88e1267742a101093d487e413288b166e832b10dd26649ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbb1906dd5c56eeb8d253b4b6ed3d4c50ea8748f135f14d6f3497a75632e732`

```dockerfile
```

-	Layers:
	-	`sha256:3eea913341173a9d5e8ae622797fb335437f31f3d061b3fd0a9017227f3785b3`  
		Last Modified: Tue, 03 Mar 2026 20:15:00 GMT  
		Size: 3.8 MB (3758663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c84cfaa3e6bec3407291e85ea5e44230ff6ac1d154e50842ead4ec93e97c7ce`  
		Last Modified: Tue, 03 Mar 2026 20:15:00 GMT  
		Size: 25.4 KB (25381 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:056759fe66ce81099fa75520d4a3c19f9f616303bc68c8cd58e62187479fd342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97357860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c7d90318f4ae425c7697263c5799bff2208a9a427f20646c86d879313bc5db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 03 Mar 2026 20:13:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Mar 2026 20:13:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 20:13:17 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 03 Mar 2026 20:13:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 20:13:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:13:20 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 20:14:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4fd341e7816cd22c1372a1cd79022f12e83376cd233e836b48a8f903dfadef`  
		Last Modified: Tue, 03 Mar 2026 20:14:36 GMT  
		Size: 12.1 MB (12140532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42304facd27989e4551e249ed0d396441486074d679f5dadb9554c5aedd91ee`  
		Last Modified: Tue, 03 Mar 2026 20:14:37 GMT  
		Size: 53.7 MB (53702902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0647bdee5ad8f46836a295459c91aa5e7fef57d02af158094fc7c4ad5d6e7f33`  
		Last Modified: Tue, 03 Mar 2026 20:14:36 GMT  
		Size: 4.1 MB (4129482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6c89f8a3b6a599fcb50422ac838c2f761b179764a961e15d35300b61c41259d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d3deb609edcab65d570793871ffa508b504a47274eeb63373b3edf3adb61e8`

```dockerfile
```

-	Layers:
	-	`sha256:4e99e1ef974348d1fde9a484b85c58d80e7510150c7b9263f6713cb757c5e4b9`  
		Last Modified: Tue, 03 Mar 2026 20:14:36 GMT  
		Size: 3.8 MB (3758471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9722e8afd66f5098f5e7a4e1b580f45f572f102493564187ba6334d18af527`  
		Last Modified: Tue, 03 Mar 2026 20:14:36 GMT  
		Size: 25.5 KB (25491 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jre-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:2dd7ea74b386178c5d7438c549c73b6e3bdca1c6c1ca16647ccb9132cc84fa1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106495628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dd821484c70f53968343c0ba57c1ab26b650454b834ea150a8af50a13a5fed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:26:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:26:21 GMT
ENV JAVA_VERSION=jdk8u482-b08_openj9-0.57.0
# Tue, 17 Feb 2026 20:27:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='9ca01471228baa5a57f2cc3a044358ab36adedecef72b07c700df40d8a0f855a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8u482b08_openj9-0.57.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='da6a204f2d3f84e6a15830524d4296aca5326895a3e32e3cb2e87b456f3bf345';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8u482b08_openj9-0.57.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9f13f8c5107a4743255b7fc5c557753050d9b6f52f46e19f303878478944502b';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8u482b08_openj9-0.57.0.tar.gz';          ;;        s390x)          ESUM='2aa11016501e63beb5638242bcb8d824ba3df84166130c53b1110e32973e3d2f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8u482b08_openj9-0.57.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Feb 2026 20:27:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:27:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Feb 2026 20:28:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77dff1debf7d6c358e50aecf65d3cd5582b3f49c3695e48ad2c62ad09db6ebb`  
		Last Modified: Tue, 17 Feb 2026 20:28:16 GMT  
		Size: 12.9 MB (12893709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84036da8237055591bcd9724d487b1b55f54ec8ba4eb94c6038cbc1ad9fea34`  
		Last Modified: Tue, 17 Feb 2026 20:29:27 GMT  
		Size: 55.6 MB (55591024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337d63734cdb4fa3fa705ba63da733bf3954b65ecf9523957db1d03383723279`  
		Last Modified: Tue, 17 Feb 2026 20:29:26 GMT  
		Size: 3.6 MB (3564793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d480229d4aef969fcfe260ae1b052822692e375670860611657a01ee9471b507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3788966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c497a14e4900f28111b4ecddeb4f42610a5719e29674345f2018821cb77771`

```dockerfile
```

-	Layers:
	-	`sha256:5c06ddcee3a7a00d8a3ee9c8b631591f89f017f9edb53381af7d9e2323aa0265`  
		Last Modified: Tue, 17 Feb 2026 20:29:26 GMT  
		Size: 3.8 MB (3763456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655da0b43dba92aaa78f4ec067bc4642eab79dafc1d05e1cc9ac3fbd738e0e21`  
		Last Modified: Tue, 17 Feb 2026 20:29:26 GMT  
		Size: 25.5 KB (25510 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-8-jre-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:ad0c7b3ed0908705bc5072baa0d89726651fb80c0afcf72bed4bb618dcfb14a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98095942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d71d9f90ded74ce859422159cc8cda85693fd597ab4c4f0fce2d6ed4d7cb2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:31 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:33 GMT
ADD file:682bbddd1f3d784d0c4ab5eef9460f0b47a94f3c62f629b59163a7f6543a159f in / 
# Tue, 10 Feb 2026 17:41:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:17:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:17:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:17:19 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 03 Mar 2026 20:12:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 20:12:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:12:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 20:13:24 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:4e2905dbd81d6a42c24ec5f7ce51f2d8f24a616b4fe2e90d0be791922a8d3b5f`  
		Last Modified: Tue, 10 Feb 2026 18:14:06 GMT  
		Size: 28.0 MB (28004382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ce45d51ae3f82df624a77668b4566c33a40c6ed0b6d7eb4ddc11addbb3a2d`  
		Last Modified: Tue, 17 Feb 2026 20:22:47 GMT  
		Size: 12.2 MB (12220382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cb2d2d28e5df65f623f9ba852a3544206ff0a64d95a57e2b6fcaeaef68a1c8`  
		Last Modified: Tue, 03 Mar 2026 20:13:52 GMT  
		Size: 53.4 MB (53424186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0a373e544b0f357a3733f03e7c9f23bb4fa2279ec485727590c0f1f1a0d4a`  
		Last Modified: Tue, 03 Mar 2026 20:13:51 GMT  
		Size: 4.4 MB (4446992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-8-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:98b5ea69749f662ae41e7e0f351206bed934c1347ae5a2653d82e235483fe19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd0f4ff4231783f6faba73e136d856425e2d834cebe743351a09d61ebce2388`

```dockerfile
```

-	Layers:
	-	`sha256:446c0b94c337ce9aade7dd13ec69f98d1f40e29a674479a3ccc27984ec504e53`  
		Last Modified: Tue, 03 Mar 2026 20:13:51 GMT  
		Size: 3.8 MB (3760881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da17d5f07513ca683348e71720502b1a559270af60860936b6e8a51e5c13c71b`  
		Last Modified: Tue, 03 Mar 2026 20:13:51 GMT  
		Size: 25.4 KB (25382 bytes)  
		MIME: application/vnd.in-toto+json
