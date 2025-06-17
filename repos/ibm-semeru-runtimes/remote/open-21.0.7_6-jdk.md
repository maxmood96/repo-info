## `ibm-semeru-runtimes:open-21.0.7_6-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:3406bb4a8f2a491f4603b48a43384a4a3d6f9cd8cc643bad45099a2dcb5285ef
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

### `ibm-semeru-runtimes:open-21.0.7_6-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:50c38fd9f953d192914d63306b5e03149532e1c468d4b14df293246325112729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281279332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2243b41e37bf9d7d7de08cd4b94092345a83758930abb210f9d6517f9825478`
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
ENV JAVA_VERSION=jdk-21.0.7+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a2bd932fc2737f7605172dbfc4f6a1dfa262cbf9606a21cb83ba1ea94c5898e0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='70228be801934a3a51761cc6ec5531b4ab52a8942efd2f0f5033ae6b24ae1423';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7e094e5a25b46452ef2067be50a8b5137a1a00d9fddf47993b0a1f56e70c1632';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='946269e578033f52b2cfa01b04a3e7223f157f5bd99129b7728126a4d7866a59';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:d4653c0c6a74e27657d2da621a65a3a55dcea8d0761ca3232ef20565049e553d`  
		Last Modified: Tue, 17 Jun 2025 17:12:40 GMT  
		Size: 12.8 MB (12796665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410d2318aab1f690d86e1ba95b3e16f7952a2814f0c8db1d95f5990ed1eb6b07`  
		Last Modified: Tue, 17 Jun 2025 17:22:40 GMT  
		Size: 232.4 MB (232388155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07c449de607e74d68cf276d8b47e58ca77702c42ceef2efa357aa30220539bb`  
		Last Modified: Tue, 17 Jun 2025 17:12:40 GMT  
		Size: 6.4 MB (6379175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.7_6-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:9d0a886ed66a3fd7337593831c87f48c22c1c80a482d6232fd0b3149902f790b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3280586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbc2ee7285de7e06e09782cd6f8dc02baa11168a54445a3bebdf7900e94618b`

```dockerfile
```

-	Layers:
	-	`sha256:4651f5ee012979032b915a8906a58155ff100770d64a2f62924cfe71b39c1f8d`  
		Last Modified: Tue, 17 Jun 2025 19:46:29 GMT  
		Size: 3.3 MB (3254628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d90078a21642c38863f9466d6187b4b9301089fd856d050c24605a5cb76cfd9`  
		Last Modified: Tue, 17 Jun 2025 19:46:30 GMT  
		Size: 26.0 KB (25958 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.7_6-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:65a01669f3ad56f2d88142d550acc539eb0a5f04c5cc98bf75a3e7538e251612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcd74a4b35d7e5beaba9878e768f3a127b69631eb6a635d1e92e1342ef08365`
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
ENV JAVA_VERSION=jdk-21.0.7+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a2bd932fc2737f7605172dbfc4f6a1dfa262cbf9606a21cb83ba1ea94c5898e0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='70228be801934a3a51761cc6ec5531b4ab52a8942efd2f0f5033ae6b24ae1423';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7e094e5a25b46452ef2067be50a8b5137a1a00d9fddf47993b0a1f56e70c1632';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='946269e578033f52b2cfa01b04a3e7223f157f5bd99129b7728126a4d7866a59';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:08b5a7e48a30bbea9a6410d93fd12d059a95c478593f67b76156a8a1cb3bf6b8`  
		Last Modified: Tue, 17 Jun 2025 17:53:54 GMT  
		Size: 224.4 MB (224383804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd11cb5fb804e78038c15dcd8b18b557d87aef296d01d2870c829bfd3d4222b`  
		Last Modified: Tue, 17 Jun 2025 17:54:19 GMT  
		Size: 6.1 MB (6128551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.7_6-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:d2bd7312c3f3a08788a7a05207e7c46d6f8a4bca29fe2ac3f661444e44a730ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3274258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c427463bff7e5bd64440f57f99faafae7354ab48f574b6250d71657a41b12e`

```dockerfile
```

-	Layers:
	-	`sha256:2fcd913fd0c7372da6a518e37101026027672b3382443c29293ec52833047666`  
		Last Modified: Tue, 17 Jun 2025 19:46:34 GMT  
		Size: 3.2 MB (3248166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0423c22042aa828e3fbcae2d263549a8b770029eb5ce84285808057b91f37ac8`  
		Last Modified: Tue, 17 Jun 2025 19:46:35 GMT  
		Size: 26.1 KB (26092 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.7_6-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:db5e2ad42eef7988b3ee3a56fa55109611a28766e8be855241740168b7330f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289190992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d28b20a006bd977c59f02522c05e86452dbc0fbeed2965a88b998187db5d88`
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
ENV JAVA_VERSION=jdk-21.0.7+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a2bd932fc2737f7605172dbfc4f6a1dfa262cbf9606a21cb83ba1ea94c5898e0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='70228be801934a3a51761cc6ec5531b4ab52a8942efd2f0f5033ae6b24ae1423';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7e094e5a25b46452ef2067be50a8b5137a1a00d9fddf47993b0a1f56e70c1632';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='946269e578033f52b2cfa01b04a3e7223f157f5bd99129b7728126a4d7866a59';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:c6a309dfa1f0ba6d307d9cc298256b39c0769b28c0b1eb68becbffb5492a949a`  
		Last Modified: Tue, 17 Jun 2025 18:13:32 GMT  
		Size: 235.9 MB (235900096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39c83f8b91c589363acce86e0cb8b2267846775237379207c43cff4768040fc`  
		Last Modified: Tue, 17 Jun 2025 18:13:26 GMT  
		Size: 5.2 MB (5166841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.7_6-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7d97e74ddd0e3fac7b88e70c23ab5fc5fd55e014c35c024074f5c29b5693c4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3285274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e08997c3a38d03b06a5bc837525d598fd6bf59053cc19a971f9808bed7f52a4`

```dockerfile
```

-	Layers:
	-	`sha256:cad54fcd668afedf2f011bf1c776bfd80dca0ae06d2a41620e441f86f039601d`  
		Last Modified: Tue, 17 Jun 2025 19:46:39 GMT  
		Size: 3.3 MB (3259268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f26683de8ae5d90ac1743c1e2dacf124bc2aff3d08e10ada8447c83a5f6f90`  
		Last Modified: Tue, 17 Jun 2025 19:46:40 GMT  
		Size: 26.0 KB (26006 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.7_6-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:9f10c5b148f50d90b35c0edc142dca983962e4e3aad8f72a2519ce293be7d96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280267026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12205053011cb2341b1ac19d09bdcef50a5eb251b641674a9d58c17ed74101`
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
ENV JAVA_VERSION=jdk-21.0.7+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a2bd932fc2737f7605172dbfc4f6a1dfa262cbf9606a21cb83ba1ea94c5898e0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_aarch64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='70228be801934a3a51761cc6ec5531b4ab52a8942efd2f0f5033ae6b24ae1423';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_x64_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7e094e5a25b46452ef2067be50a8b5137a1a00d9fddf47993b0a1f56e70c1632';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_ppc64le_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='946269e578033f52b2cfa01b04a3e7223f157f5bd99129b7728126a4d7866a59';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.7%2B6_openj9-0.51.0/ibm-semeru-open-jdk_s390x_linux_21.0.7_6_openj9-0.51.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:0657dc8c7ea3e26900f40ce5495a424cb4d11d0857f401ede2dea967959dba6f`  
		Last Modified: Tue, 17 Jun 2025 18:27:21 GMT  
		Size: 230.7 MB (230688521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a832e52e12ff77a3f1093e5a3b2459e127c4d4cca7297f1de472103d867a2466`  
		Last Modified: Tue, 17 Jun 2025 18:27:44 GMT  
		Size: 6.5 MB (6528229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.7_6-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:dec4008f73dbfdbffc70e0c3838dedd800a61d8f65d70f82040de7e4079cfed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3283410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d329ad4cd025bcf1c555961b9a611d807f081a503b8eead4f3a6e2753d3b27`

```dockerfile
```

-	Layers:
	-	`sha256:76084d9c80c1bd6911f9a614595db9571176b6c89d29bbb3ba1179f9ca03f85e`  
		Last Modified: Tue, 17 Jun 2025 19:46:45 GMT  
		Size: 3.3 MB (3257452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd9fe9ff4324403d78b9cd33858d9d6d017030d8f58de76b759ca24adbfb68f`  
		Last Modified: Tue, 17 Jun 2025 19:46:46 GMT  
		Size: 26.0 KB (25958 bytes)  
		MIME: application/vnd.in-toto+json
