## `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:8c7d1960a6f16b77ae07594b2bd90487a3d07a9c293d53ed1af99a88981be3af
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

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:0f179723f67c8a34bdd63ebae72a3a49de4f10e9b29775cafc248d69f87a2348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116188929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9732e3bf2669b165423df31a81c2b4a7e95eafdb3835af3395201dd6e2ae28f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d8354f63b4b73db451eb426d4f819e3e491305d2aa42a7924fc51c3ea4a1ed`  
		Last Modified: Tue, 30 Sep 2025 18:06:08 GMT  
		Size: 21.3 MB (21299651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664ac4ce5ced188252d0779336b6a0164e5094c887bfab97260723b13af3f9b`  
		Last Modified: Wed, 01 Oct 2025 16:04:41 GMT  
		Size: 59.6 MB (59565989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d2cbf4844d7d8eee406749d64c95e4173d63f28779e956b7c43f9ec123146c`  
		Last Modified: Wed, 01 Oct 2025 05:07:37 GMT  
		Size: 5.6 MB (5599839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:291811e1975029881625013ff9aa88b2c78c7770e5baebe8a8a5bc842ec0c679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3204046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dee631798c9a971dbf8b307d05d0fe2c188b21f384dca8029224f2b497e193`

```dockerfile
```

-	Layers:
	-	`sha256:347ae502007adb49657154b4be0fab70b3cb84f9db097d544f812f8c61bddb56`  
		Last Modified: Wed, 01 Oct 2025 13:46:42 GMT  
		Size: 3.2 MB (3178047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f1972f7e089a6ecaa2b233c04f65ab984dd832cc90657afbf39fc933a64d67`  
		Last Modified: Wed, 01 Oct 2025 13:46:43 GMT  
		Size: 26.0 KB (25999 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:62db9f9d70f1c9195b4af8881add8d0d1b888de1ce0273179d511be3a59915f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106928116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee3e65e19c3a6f2520f75afcee99d1339582502c9df093def33171dcb0267fb`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:1c248ee5625226e9234ff9d26b218c3873bfb9ee5bcad2ced2bfb42de6062eb0`  
		Last Modified: Thu, 02 Oct 2025 01:21:19 GMT  
		Size: 15.0 MB (15049924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1cba190d5d66c66a635f057357a5d2b112d871e49093a766ffe2f1f6b45fe5`  
		Last Modified: Thu, 02 Oct 2025 01:23:28 GMT  
		Size: 57.8 MB (57806343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a26325bf89c0e14fb8cc3706758f3d6831c3f01992b2343f447e46301a0bf2d`  
		Last Modified: Thu, 02 Oct 2025 01:23:27 GMT  
		Size: 5.2 MB (5210274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:c3720845be658f4a26f1d6675ff570c124ead110cab342804d6c8011a1e4c571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58801b6af5dade542a265a22c8f2ade905c032ee8e9c5e4a3fca976a7bc87620`

```dockerfile
```

-	Layers:
	-	`sha256:5f8f9484e878093610817c1ae90f3c15fb3f311c2bc000f3e20bef6241cc9c7e`  
		Last Modified: Thu, 02 Oct 2025 04:47:53 GMT  
		Size: 3.2 MB (3177236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee60791821f65a7c5b9a115896e91021d8ed9f672d5cab351d1b34bdc6a06f5e`  
		Last Modified: Thu, 02 Oct 2025 04:47:54 GMT  
		Size: 26.1 KB (26133 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:fd5b74e830fd25930e9dae329f83dd697d547dddd1276b0ca8dc58bad20f3e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116354752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b961f8dbd2a8e35568acd4cb01c1fc07df760c4f53c38f71bc170550ff43e7`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:dcfbd0d7d96dd3a7c6b8175964f7dc422073fce567783bf1bb2468e058183d17`  
		Last Modified: Thu, 02 Oct 2025 02:26:22 GMT  
		Size: 61.4 MB (61417865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b678b4e3a85429778a26309acfd025be2f2dc6d39e16abdeb3ddb66a46926ff3`  
		Last Modified: Thu, 02 Oct 2025 02:26:19 GMT  
		Size: 4.2 MB (4219398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:f96456c690a92e0f23459441169069211ad08e802b2906af537950db034b1951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3208734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9441e3c492a268cf6789ba36521e0891411db1b63575500a5263f9c42768680`

```dockerfile
```

-	Layers:
	-	`sha256:62b4db227f33d5126788a8fa738c8c6d0d146dc4fff55bc004d245dc364f2e8d`  
		Last Modified: Thu, 02 Oct 2025 04:47:58 GMT  
		Size: 3.2 MB (3182687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb87db348e9cc51cb1fa9ec8df64c9f6ef52e622c6c13030f50a0b60e7764c4`  
		Last Modified: Thu, 02 Oct 2025 04:47:59 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:7d94716e36b477e847fa93efac2238d367cf0434e741e9680f7c82e416109dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109372337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e62410ecc60bdf88f2e00040b445379427ea6c94dda5ab4e3fcc217cec9013`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='590d70bcd1d7a029a78ddcad3a36ee5ca2277fa2bdaf9b1585caef627b45e4ed';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_aarch64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ef433a588d348f14ea9bb29a4bc3042db8dabf6f8bf7f46ff2d9dfd48d89a0ca';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_x64_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='94bc64417befbf28a5d60593c3a3d101272d956f3e87e7fcaa62c10417ef4d9f';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_ppc64le_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        s390x)          ESUM='2b5d3e51eb1b9273df6c1142a6a52e31540a1da31cd87c82661340d7cc023808';          BINARY_URL='https://github.com/ibmruntimes/semeru24-binaries/releases/download/jdk-24.0.2%2B12_openj9-0.54.0/ibm-semeru-open-jre_s390x_linux_24.0.2_12_openj9-0.54.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:bee8f2c06404bbbe5e79f04890978aa2825dc61efdd27942b637fc4956ea9a44`  
		Last Modified: Thu, 02 Oct 2025 01:57:11 GMT  
		Size: 58.6 MB (58576903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a312a8482a265e231965d2be2982b73ef514f8592146cb4916ca3fa5079ff4f`  
		Last Modified: Thu, 02 Oct 2025 01:57:04 GMT  
		Size: 5.7 MB (5680188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-jdk-24.0.2_12-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:5ef95548e42ea2fec9508acf75e29093ed8ada71975dd333e24aeb2c3cd0ad53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3206870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3b875c55eb2afa76525f7cad40c54c7e5fb61b11c4aca49deb6c288111f2c4`

```dockerfile
```

-	Layers:
	-	`sha256:f55049f18bd7282ae876fb70f84db0aef7f7659825feb0c2bde3626067e4173d`  
		Last Modified: Thu, 02 Oct 2025 04:48:03 GMT  
		Size: 3.2 MB (3180871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe2a0ece60f1fdd0f757c12d205963a33c048e0da00ae4edf67e387e8b9b692`  
		Last Modified: Thu, 02 Oct 2025 04:48:04 GMT  
		Size: 26.0 KB (25999 bytes)  
		MIME: application/vnd.in-toto+json
