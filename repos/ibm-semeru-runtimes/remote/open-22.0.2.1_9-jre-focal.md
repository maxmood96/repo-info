## `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:99167f51fa6831c9530df6a7daf68ff95ae8a2205e53e7d2f660ef1e843d7ecf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:73cc20ed8d6df1374a37dfb1d981fd68573773fe259bf0f4abc05fe3ac8359fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104155913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60eaaa8faf1209732b6d7dbe5c842182eee8108d9841ca71809b98a2b6fef6a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cbb8426ba078d2f7c8cf1096e63d1878a10ba8b34faf082a9bb0cd2a2746c6`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 16.1 MB (16061118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2882489699fd63ee1348f6e9c7bf832be835b1b9f90f8f7b96893aac9c88e00a`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 55.3 MB (55324815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec555fb0762de888f250a8900c93656af6f1f8ac0524bd65806948253defcc9`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 5.3 MB (5258211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:6c7ea98c2f4848de8eac29cc48886f8a12173324fc1317520898273ce6fc9a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ae2af59a6b2436f9d01f1466ca0330cd1211c5f511b61ae323bc84dfc9e058`

```dockerfile
```

-	Layers:
	-	`sha256:f4cee8325f744409044fdbe66e0c9e541b2730e83b49fd0468eb8d18a2d3ca41`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 3.5 MB (3463697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baba335b5b17933eed8da5c11b88a9ce4ac8566e4f4101d6c60e2710cc024f76`  
		Last Modified: Thu, 12 Sep 2024 22:02:25 GMT  
		Size: 23.7 KB (23721 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:a21bac9d4a79355f44077da7a258a4468082eb2d37d1496ac003f25fdeff8772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98539780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a87576ed93f206f8bcfb298d8a27449f9ef971f36682019f629db340bd49ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2bfb687179cbe19551365186a120e8f0cd6d43a6cb5b4ed94041823a689f08`  
		Last Modified: Fri, 13 Sep 2024 01:54:18 GMT  
		Size: 15.9 MB (15924339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd89750f57492e0ef340b8df0aa01dab4a1ebfbb45faaf7bb5a006e99781377`  
		Last Modified: Fri, 13 Sep 2024 02:15:16 GMT  
		Size: 51.7 MB (51691306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b128cbe17c2d00e74d968c336392411d20f6d612e472599051b3ab8ff1efac5`  
		Last Modified: Fri, 13 Sep 2024 02:15:14 GMT  
		Size: 4.9 MB (4949918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:783c6863553f53fd893eee2bc5f9042a5ba1df4737a4f6d0eb829b6bf6988569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b29b035c147834969c1996e4c827049286978d5bd02ed680ea10c9d70e9d46`

```dockerfile
```

-	Layers:
	-	`sha256:9d3d6f25e9a926ebc8c39a4a96dc5dfa31143c1839ee028e062fde444bfc51da`  
		Last Modified: Fri, 13 Sep 2024 02:15:14 GMT  
		Size: 3.5 MB (3463943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046b5420b17009d1c539a3b312fcc19ad4815377b3d6a9ba449a19215f2df212`  
		Last Modified: Fri, 13 Sep 2024 02:15:14 GMT  
		Size: 24.0 KB (23999 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:29fee9a3179a4678c008042be95a8fcaf7d1a41a3cad52ba64b57876887e92f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102144070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d126fe8723b89098ad98671d0312c7faf9d4ca249bef2a585afad0c3e9f6826d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 07:55:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 12 Sep 2024 07:55:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_VERSION=jdk-22.0.2+9_openj9-0.46.1
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='033d4d3dd15dd7191fe232e2d117187788268685963b5b7e63709f06a462da4e';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b757ae8028136ec0bace63c9f5b698a31d1b3b6f7a07ada6d5da3879859fabc7';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='bb4a5c07cd7997b160be4b087140c3698be5cf46eb3fee43751674c29b995523';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='5e4f3cf3a5e91d288d663004e566cd34807f269e932e8fa4f83bfb4eb874bfa0';          BINARY_URL='https://github.com/ibmruntimes/semeru22-binaries/releases/download/jdk-22.0.2%2B9_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_22.0.2_9_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Sep 2024 07:55:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 12 Sep 2024 07:55:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:43a275ddff09c9f4397e978092ab9952ebd3393a5572a06df70e3545dccb0c4d`  
		Last Modified: Tue, 13 Aug 2024 10:24:18 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d59eaa0200787a041bd8220cb7f34aced7071473572370459f90d9eefe6da68`  
		Last Modified: Fri, 13 Sep 2024 02:22:47 GMT  
		Size: 15.8 MB (15753804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37552af196101051d5019b51f9917469f00f9b1b53ab4c809ba5bb741afa9c9`  
		Last Modified: Fri, 13 Sep 2024 02:50:05 GMT  
		Size: 54.7 MB (54656461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c3338da89d2a8704ceb370a0171712ed40298cd8b7f002a597874b58028adb`  
		Last Modified: Fri, 13 Sep 2024 02:50:04 GMT  
		Size: 5.4 MB (5366611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-22.0.2.1_9-jre-focal` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:3ceef86dc71a2c174e65a594866cfa77d30df7f265d30dc8cd52bbcb10bb8abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b813f1dfd1fa613d4f5870c47f790bd39e99fe601a8b40bf5d3a16197fd8282`

```dockerfile
```

-	Layers:
	-	`sha256:79de24393ed8b4dae841c46dbed91309885cf6ef3e6a21a57ad0c1f5da51b1fe`  
		Last Modified: Fri, 13 Sep 2024 02:50:04 GMT  
		Size: 3.5 MB (3464023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f2bfcefe94beeafe6d6905ec3d273a1421395fb7bd198607068ed1906ac0d62`  
		Last Modified: Fri, 13 Sep 2024 02:50:04 GMT  
		Size: 23.7 KB (23722 bytes)  
		MIME: application/vnd.in-toto+json
