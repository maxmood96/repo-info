## `ibm-semeru-runtimes:open-24-jdk`

```console
$ docker pull ibm-semeru-runtimes@sha256:b5b2a82c50bf0309fedc43204252af6730768cc4c6d76d63fd139502f1730756
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

### `ibm-semeru-runtimes:open-24-jdk` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:177c77b222a6b57a8a9fb753212248eeb634940034a28457737b88b19bf523af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298704808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c44b501f0eaa6f6d250e193a3d81719870710f62e24d2c6a46f63dbd395567d`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a6cc2d6c240375bd2614b78bfd0361f9f4ff1303be9c1f71109e1c3764c28da';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='480845cb69ef0d7a33ff70e28bbdf882c27f764bd76bc905f5fa40934d5a0c06';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dbebbd5d4dd78260307ee3dcc3196c3803d46d9cd7d119ef4740272d6f534d98';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='ab97b68a71998516cb6ba334e54d121f70e15b2eda662404fddb198dcd396f39';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c96483013e28b9100e9480e3cfb07f820b85415c05fb4e3450d19bf63e95d88`  
		Last Modified: Thu, 02 Oct 2025 10:45:18 GMT  
		Size: 15.2 MB (15198516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2d543e949e6fc817825d95c9957fc0e9b0b0441ee57745b62d9eeeb4d7e405`  
		Last Modified: Thu, 02 Oct 2025 10:45:28 GMT  
		Size: 246.9 MB (246915510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f11eeaffc7d8807f16569c57e6ee54a3562f87af1ed4141943b8ec45d72304c`  
		Last Modified: Thu, 02 Oct 2025 10:45:20 GMT  
		Size: 6.9 MB (6867771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-24-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a834a4676cca68d17ffde1c8c4c5fbba1430fb4cc5da81c2035e7de00522e756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3275853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7547d3086d8fd5498b191d7160aeda72c65e59304962edd954db596a3fb116`

```dockerfile
```

-	Layers:
	-	`sha256:c4b68046581bb827394c7e8d3824bb5ac4f52bf251e20144600d8dc376c6f0eb`  
		Last Modified: Thu, 02 Oct 2025 07:46:22 GMT  
		Size: 3.2 MB (3249853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:344cfb1eccaa9a08eaf62096e1b930e55b153dae3f9864e5cb4987df821ab807`  
		Last Modified: Thu, 02 Oct 2025 07:46:23 GMT  
		Size: 26.0 KB (26000 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-24-jdk` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:5f77a11f1d654de8b80631a57b88cb7a169bcd29cad53bffd32ac76ec45378b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293500249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6cbcda180a5d9f1a74f48be87528f8d1fd488cd80bde039dc1e767f40a76b3`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a6cc2d6c240375bd2614b78bfd0361f9f4ff1303be9c1f71109e1c3764c28da';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='480845cb69ef0d7a33ff70e28bbdf882c27f764bd76bc905f5fa40934d5a0c06';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dbebbd5d4dd78260307ee3dcc3196c3803d46d9cd7d119ef4740272d6f534d98';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='ab97b68a71998516cb6ba334e54d121f70e15b2eda662404fddb198dcd396f39';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff886621ce6637347029af609b089f236ed317052dab19ab58835e21d9200dc6`  
		Last Modified: Thu, 02 Oct 2025 03:27:12 GMT  
		Size: 15.1 MB (15050037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d57eed7403e31061da5a1b13c06a6034d9eb0066233a5e2477b87336600f71`  
		Last Modified: Tue, 07 Oct 2025 07:39:43 GMT  
		Size: 243.1 MB (243114410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da03dadfc55deb7cc9db1b530517158c69dc314f0709e0925a8535d723eee4a`  
		Last Modified: Thu, 02 Oct 2025 01:24:02 GMT  
		Size: 6.5 MB (6474227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-24-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:21f3e1882bf81b5cd634b7b181bd57c9d4ba663983dc58e3b9342875a03554f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3275176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa4849b27de70fe04dce463750f090cc38b726eaa674d04a44a6b0ff826209e`

```dockerfile
```

-	Layers:
	-	`sha256:09fbd8d9a9fea11c943200f4412683c272935079244e905f105c9b4f56537e6f`  
		Last Modified: Thu, 02 Oct 2025 04:47:31 GMT  
		Size: 3.2 MB (3249042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b157889544aaacd30f6e970ba15f4a8954113e0886da7e481eb3b37f9262b72`  
		Last Modified: Thu, 02 Oct 2025 04:47:32 GMT  
		Size: 26.1 KB (26134 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-24-jdk` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:94174ee1028f760a553d092c7e72481351a55dea8ee0faded50754c05b9ae4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.9 MB (306917960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fa1b76225f7bf12ea6ec6c9faf9573e16208309b74095a759077151bbab646`
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
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a6cc2d6c240375bd2614b78bfd0361f9f4ff1303be9c1f71109e1c3764c28da';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='480845cb69ef0d7a33ff70e28bbdf882c27f764bd76bc905f5fa40934d5a0c06';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dbebbd5d4dd78260307ee3dcc3196c3803d46d9cd7d119ef4740272d6f534d98';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='ab97b68a71998516cb6ba334e54d121f70e15b2eda662404fddb198dcd396f39';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e2b114df3a23a209cae9e6a5f267a4fceeb504a0b0b36c576a0ba57888a77f`  
		Last Modified: Thu, 02 Oct 2025 01:51:58 GMT  
		Size: 16.4 MB (16413942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f356ac7c07b3014b60cf666b12d94c9aed890af3255d47c8b0f12e3a9e6ed0c`  
		Last Modified: Tue, 07 Oct 2025 15:02:21 GMT  
		Size: 250.7 MB (250749487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e30a589e7c3a0613be9abd859c3441b39a1b6a057b235ea51c91b1a8a633467`  
		Last Modified: Thu, 02 Oct 2025 02:22:56 GMT  
		Size: 5.5 MB (5450984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-24-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:37c048c567405103dd0a4a00084aacba1190171e6e806b56a2041f9b2bca3fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3280541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d3ee019671468f39e436d72bafdfd11931949a5114eee43d66aba96e9c9e35`

```dockerfile
```

-	Layers:
	-	`sha256:704cf0ea8faed99e25871c5d14376d7264b1bf654e214da192e9ac88fa0e3fb5`  
		Last Modified: Thu, 02 Oct 2025 04:47:36 GMT  
		Size: 3.3 MB (3254493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:785ea7ee3164d012c87ef1ea432cec6032900605fe64afcc41fb999d455a0fc1`  
		Last Modified: Thu, 02 Oct 2025 04:47:38 GMT  
		Size: 26.0 KB (26048 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-24-jdk` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:ff3b9feee1e6da26728daa23ceba3c6dfd5053f69897c2d8def85c1b9bebc653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296607004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633fc407508c1a6d47a6f73393f5695cc584e13c5ce12f5b669e41f09209fcb5`
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
ADD file:2df9e8bc7cd2e879b1bb1d4b43960e570cf8bf039e9c92e1b3599d2ec12b6674 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a6cc2d6c240375bd2614b78bfd0361f9f4ff1303be9c1f71109e1c3764c28da';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='480845cb69ef0d7a33ff70e28bbdf882c27f764bd76bc905f5fa40934d5a0c06';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dbebbd5d4dd78260307ee3dcc3196c3803d46d9cd7d119ef4740272d6f534d98';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='ab97b68a71998516cb6ba334e54d121f70e15b2eda662404fddb198dcd396f39';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jdk_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:e9a7df0c6e08fd0434347bd07ecdade7cc5d006c086084ec4347cd24546ee1a5`  
		Last Modified: Tue, 30 Sep 2025 17:14:38 GMT  
		Size: 29.9 MB (29906146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f94572172d1a2c27e960baa351452bb516c16e64f19bec4292973e4b8dd682e`  
		Last Modified: Thu, 02 Oct 2025 01:32:00 GMT  
		Size: 15.2 MB (15209100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee390a23e625ec97c3283e6ce830b51f92c6c3a08607ababc75d1c1245b08787`  
		Last Modified: Tue, 07 Oct 2025 15:01:25 GMT  
		Size: 244.6 MB (244610476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f65f157ce10e278122fc6cef1498f542763d189d7ea052d2f2b0cc8d53647a`  
		Last Modified: Fri, 03 Oct 2025 21:58:31 GMT  
		Size: 6.9 MB (6881282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-24-jdk` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:7fd21bdb756f42dd650bc307c7df626cdb9758493414040575f042ef4da50d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a661894a366bd4f8a7d19397226fc9394efc05509cb9d814eb927a6723a4a30`

```dockerfile
```

-	Layers:
	-	`sha256:b1b13a6da9a96c7ca35f7e98c991c3730339bd250c3e1d3714394d9d358597c9`  
		Last Modified: Thu, 02 Oct 2025 04:47:41 GMT  
		Size: 3.3 MB (3252677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9ffba67e5caa774c7c101bc3ed2c306de0026d7109c85d9250d55bb2865a4f`  
		Last Modified: Thu, 02 Oct 2025 04:47:42 GMT  
		Size: 26.0 KB (26000 bytes)  
		MIME: application/vnd.in-toto+json
