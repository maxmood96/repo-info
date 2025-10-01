## `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:b10822929ec2afa9f8c8363c9e3a098fc41117422bf8f2fa6c70d548075cada6
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

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:903129bac13eddc2b5b53dfcab7f47126ef5ab79eebc4e99713897b6e444bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106906001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c354ae6fe695bd7fa399afa10d320dc69e283a87688698b547b2edface452f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55ed4917f039ce5fa07ae7cb8f31d0f236abe0b9987fa1360dc7e7fa125a945`  
		Last Modified: Tue, 30 Sep 2025 18:07:06 GMT  
		Size: 12.2 MB (12171666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b0e9921756fac9e5ec0d71fc155ea85fd64cb93700840e4649871de90efaa`  
		Last Modified: Tue, 30 Sep 2025 18:07:10 GMT  
		Size: 59.6 MB (59565937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e500b87701bbb24ba10ffed7bd56d3856b09f3b35fddbacde2d51c82670cd31`  
		Last Modified: Tue, 30 Sep 2025 18:07:07 GMT  
		Size: 5.6 MB (5631463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:88d234716be1fbef4cae48e43d195e887f09e5442d9e507c5d9daee96ec78d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31619515613df813528d3f7b6d65b457c3cef50e9f889c0a646dda93213b90df`

```dockerfile
```

-	Layers:
	-	`sha256:64db1e1d1748e57064c4588ae4bcaaf2175a7c731040105b79f5fdafb0a55321`  
		Last Modified: Wed, 01 Oct 2025 13:45:55 GMT  
		Size: 3.7 MB (3740813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c27e5d28ed29e880a0310f6163c05ac756f7b7b294b6d6fd325ff5cf843442`  
		Last Modified: Wed, 01 Oct 2025 13:45:56 GMT  
		Size: 25.3 KB (25309 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:b3173f53942fd7d1f742e7830c07946ba07ad2c45cc550e536ac8882e2f0539b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102542377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e9ef31008bf9e9b07f0b22db39b569d4e1da66e2bf74cf9b999a8a5b552531`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e9498964721f75fba9d10ee8de633f6720871e2f2997d4e1074b086b6908f`  
		Last Modified: Tue, 30 Sep 2025 17:14:09 GMT  
		Size: 12.1 MB (12129392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dbf3638dac52dd1329cbc5c85e8189ed03159cb274f90365b550aab17500d0`  
		Last Modified: Tue, 30 Sep 2025 17:15:18 GMT  
		Size: 57.8 MB (57806345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2638e050db4ddf4e8ed11d4a37dec8660b00b83cb73afe18638502419e1e8fb9`  
		Last Modified: Tue, 30 Sep 2025 17:15:11 GMT  
		Size: 5.2 MB (5245171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a4a44b18d1ec292bf7dc4839368b6aa997c686fff224238664bab602fbc7fdb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc5f95c125dd4b4fec830a9675174c0a53b35b8ab003ef669fde470ac69ac91`

```dockerfile
```

-	Layers:
	-	`sha256:a6b5e12ad57676d9912274523e943965205dc30d0a1e1a9f64892c0875f2fade`  
		Last Modified: Wed, 01 Oct 2025 19:46:02 GMT  
		Size: 3.7 MB (3739185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b03025846a9b9b1821cf28f403a1bbd1fbb2d7b0a5e4ef8c13f38f0450f2a2`  
		Last Modified: Wed, 01 Oct 2025 19:46:03 GMT  
		Size: 25.4 KB (25419 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:f0f3270729736d744e283d462369755158ce8380d7975d760a47c88f56b7e223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112966948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a5e97299739a2139aa28b6a274f149b5eb662215d7e4bb0f10bcae7bb7a9aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc054adc41d4a1b555943ab3f79cf68266c04303fe6688bb6d414daaf232bbeb`  
		Last Modified: Tue, 30 Sep 2025 20:11:35 GMT  
		Size: 12.9 MB (12893821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbabf44a257bdbf4f0bc0e8597438ef83f5de351731ee3818206b24eab082b2`  
		Last Modified: Tue, 30 Sep 2025 20:40:14 GMT  
		Size: 61.4 MB (61417891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2d320729883e93829d96bfef474b5b599a57cc89a89b8b45b41fbdd83e6929`  
		Last Modified: Tue, 30 Sep 2025 20:40:05 GMT  
		Size: 4.2 MB (4212012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:255cfd045de3830edc1255bdb66f33890ddd3b1729e6179b22608dda912b2adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6465b1313b896f26e6c30fe41e02943711ca11e3266e6ccb10c7e861e5cc7f7f`

```dockerfile
```

-	Layers:
	-	`sha256:3332dc1b204409a2d879a0739374fdd2222da4dbe7f1b387466e9989a9506281`  
		Last Modified: Wed, 01 Oct 2025 19:47:38 GMT  
		Size: 3.7 MB (3745440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e7f62332561cedb1068a91fc7a851cf9a22b1d7d342c515390e7def2fd74be`  
		Last Modified: Wed, 01 Oct 2025 19:47:39 GMT  
		Size: 25.3 KB (25345 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:22362d873d7c669465a4317870553e7469d358402f3bd1543a20ac6ce97d5ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104506926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ecc7e3db0baef3bdc2e13322cbab39972b2cc759e5d406355c1cfd463317063`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-24.0.2+12_openj9-0.54.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8f4dbe68030a2ad641d6cc1dc03e47e9fe76af20ec4d640eb6b0232ae6ea1a`  
		Last Modified: Wed, 01 Oct 2025 00:11:15 GMT  
		Size: 12.2 MB (12219577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb96419ce29769f10c6e2373950a2d3d3a86aa42724cfb91758be217a4550fe`  
		Last Modified: Wed, 01 Oct 2025 00:37:14 GMT  
		Size: 58.6 MB (58576932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9d279426419f29cf3e96e4a80892548b2adf09455174f5f419543fd6849a7d`  
		Last Modified: Wed, 01 Oct 2025 00:37:07 GMT  
		Size: 5.7 MB (5706749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre-jammy` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:e2dba9ea9881a44c1d2178c80013e030a2c020c8c8146341cb6cd7287039c0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3768340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d8c761e6ab9bb96f5f70c561f46db11dfb4ee88f98f808e69f0486cf254ce7`

```dockerfile
```

-	Layers:
	-	`sha256:47054a2287e3faac69b7a4189eef22391f455f9f72226d5a382e10e1c9c4ce90`  
		Last Modified: Wed, 01 Oct 2025 19:47:43 GMT  
		Size: 3.7 MB (3743031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a0f7a69abaa744c9658f05bf8cbb84a445b7244da92bc94c17aa2c8b9e8780a`  
		Last Modified: Wed, 01 Oct 2025 19:47:44 GMT  
		Size: 25.3 KB (25309 bytes)  
		MIME: application/vnd.in-toto+json
