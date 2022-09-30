## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:613109ae64f2936fa7ca536e9b969bc9809864d27b62308ed1712a8dda5941e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:5a8be49f90cb95de3794cb65f157f201cd80cb68881a172f67b7ad6414e561c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.6 MB (410559559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1608aadb16b52c278c5924249adfb01e56954c811ecd3a24055509d3aeea6fcf`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:17:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 03:17:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:23:49 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1_openj9-0.33.1
# Fri, 02 Sep 2022 03:24:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0114aada7edc773346a6729c992bdd2f5ff8aedec756547f42839bb37c12e3bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_aarch64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='35955d6ce7b9e262abfd2b2dff585b3be71fa7e320ea23b5d604aa45fac2d251';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_ppc64le_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='338ea5fe72f5a1a075c02953882a985dee437f0b60e432eacb02ba8ca15b3e0b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_x64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='cf8b58da8d98f0a01d228ed3fe7177ed6ba783b8134113073977cc3ebf9eec33';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_s390x_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 02 Sep 2022 03:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 03:24:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 02 Sep 2022 03:25:30 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 02 Sep 2022 08:46:23 GMT
ARG VERBOSE=false
# Fri, 02 Sep 2022 08:46:23 GMT
ARG OPENJ9_SCC=true
# Fri, 30 Sep 2022 01:31:30 GMT
ARG EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb
# Fri, 30 Sep 2022 01:31:30 GMT
ARG NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34
# Fri, 30 Sep 2022 01:31:30 GMT
ARG NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725
# Fri, 30 Sep 2022 01:31:30 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.10 org.opencontainers.image.revision=cl221020220912-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 30 Sep 2022 01:31:30 GMT
ENV LIBERTY_VERSION=22.0.0_10
# Fri, 30 Sep 2022 01:31:30 GMT
ARG LIBERTY_URL
# Fri, 30 Sep 2022 01:31:30 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 30 Sep 2022 01:31:42 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Sep 2022 01:31:42 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Sep 2022 01:31:42 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.10 BuildLabel=cl221020220912-1100
# Fri, 30 Sep 2022 01:31:42 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 30 Sep 2022 01:31:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 30 Sep 2022 01:31:43 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Fri, 30 Sep 2022 01:31:43 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 30 Sep 2022 01:31:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 30 Sep 2022 01:31:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 30 Sep 2022 01:31:51 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 30 Sep 2022 01:31:51 GMT
USER 1001
# Fri, 30 Sep 2022 01:31:51 GMT
EXPOSE 9080 9443
# Fri, 30 Sep 2022 01:31:51 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 30 Sep 2022 01:31:52 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 30 Sep 2022 01:46:59 GMT
ARG VERBOSE=false
# Fri, 30 Sep 2022 01:46:59 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 30 Sep 2022 01:54:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 30 Sep 2022 01:54:17 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 30 Sep 2022 01:54:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d642f39b1087c24de3648cfa4a5a57017b2065655f2534de49f99c9c47642de`  
		Last Modified: Fri, 02 Sep 2022 03:28:57 GMT  
		Size: 16.0 MB (16014639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47403ad8a20a031a647a68e5bbe870d936043afd5242bb4bf4e6fa981a203a96`  
		Last Modified: Fri, 02 Sep 2022 03:31:31 GMT  
		Size: 47.9 MB (47889162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6509e2964560336c310cbd0fbb1489ab3cac5ccae1198f0140e6060010501893`  
		Last Modified: Fri, 02 Sep 2022 03:31:25 GMT  
		Size: 4.8 MB (4771841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4922ad6f67870c26070a76a425879b75b9dcda14a0cd9b5743179a548d94cf`  
		Last Modified: Fri, 30 Sep 2022 01:56:18 GMT  
		Size: 14.3 MB (14277309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7be09a28cd633bd1066118ccfa50138f632a14acf5d264f40f1e97393a7bebb`  
		Last Modified: Fri, 30 Sep 2022 01:56:14 GMT  
		Size: 679.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353c2537853d3cf0ab974616888d371d8d08e16bd96e2020528165f9312e0853`  
		Last Modified: Fri, 30 Sep 2022 01:56:14 GMT  
		Size: 9.8 KB (9754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9008fc5f761f3c0f65ab5d21da55956a263bca0b44ac3e78e850b821f0a3dd0`  
		Last Modified: Fri, 30 Sep 2022 01:56:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ef6c50a302abe47f84eea15f4e302adafc0a5e53e15ef100928a43ca8aa1fa`  
		Last Modified: Fri, 30 Sep 2022 01:56:14 GMT  
		Size: 10.7 KB (10731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa3bdcf0568027466504e7dda14539e1f6a8d7ced38eeb9bbd2fa796748105b`  
		Last Modified: Fri, 30 Sep 2022 01:56:15 GMT  
		Size: 2.6 MB (2598710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c578ed7906339ac5c23060fb1a8b70d0d4f75aab7b44661d105ddc31247aad`  
		Last Modified: Fri, 30 Sep 2022 01:57:26 GMT  
		Size: 281.6 MB (281599689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7a947294013d28f43ed68973d88613ce086ce0b7457b6f3a5018c6ac68bee7`  
		Last Modified: Fri, 30 Sep 2022 01:57:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56338deb32e98ac491438b6f185f5fe7006581e1f696ad6118cf27c9531d2b6`  
		Last Modified: Fri, 30 Sep 2022 01:57:14 GMT  
		Size: 14.8 MB (14813148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:82317d9a6c407a9eaadc1bb5095ed17c0d8074e7f0b735e59279c001489159eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.4 MB (414428080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa32e4bb760b444da8133c9147c1870f10898b23c9a9c04d5fee071b7e81ce3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:54 GMT
ADD file:eb82827919ea73f9595d7b0b70fe9aa5ff23e16ea6a87f7f9ef4e1905857b789 in / 
# Thu, 01 Sep 2022 23:49:56 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:31:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 04:31:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:38:50 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1_openj9-0.33.1
# Fri, 02 Sep 2022 04:40:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0114aada7edc773346a6729c992bdd2f5ff8aedec756547f42839bb37c12e3bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_aarch64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='35955d6ce7b9e262abfd2b2dff585b3be71fa7e320ea23b5d604aa45fac2d251';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_ppc64le_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='338ea5fe72f5a1a075c02953882a985dee437f0b60e432eacb02ba8ca15b3e0b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_x64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='cf8b58da8d98f0a01d228ed3fe7177ed6ba783b8134113073977cc3ebf9eec33';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_s390x_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 02 Sep 2022 04:40:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 04:40:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 02 Sep 2022 04:41:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 02 Sep 2022 08:07:02 GMT
ARG VERBOSE=false
# Fri, 02 Sep 2022 08:07:02 GMT
ARG OPENJ9_SCC=true
# Fri, 30 Sep 2022 06:42:32 GMT
ARG EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb
# Fri, 30 Sep 2022 06:42:32 GMT
ARG NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34
# Fri, 30 Sep 2022 06:42:33 GMT
ARG NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725
# Fri, 30 Sep 2022 06:42:33 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.10 org.opencontainers.image.revision=cl221020220912-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 30 Sep 2022 06:42:34 GMT
ENV LIBERTY_VERSION=22.0.0_10
# Fri, 30 Sep 2022 06:42:34 GMT
ARG LIBERTY_URL
# Fri, 30 Sep 2022 06:42:35 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 30 Sep 2022 06:43:08 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Sep 2022 06:43:09 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Sep 2022 06:43:09 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.10 BuildLabel=cl221020220912-1100
# Fri, 30 Sep 2022 06:43:09 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 30 Sep 2022 06:43:11 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 30 Sep 2022 06:43:12 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Fri, 30 Sep 2022 06:43:12 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 30 Sep 2022 06:43:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 30 Sep 2022 06:43:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 30 Sep 2022 06:43:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 30 Sep 2022 06:43:28 GMT
USER 1001
# Fri, 30 Sep 2022 06:43:28 GMT
EXPOSE 9080 9443
# Fri, 30 Sep 2022 06:43:28 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 30 Sep 2022 06:43:29 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 30 Sep 2022 07:14:15 GMT
ARG VERBOSE=false
# Fri, 30 Sep 2022 07:14:15 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 30 Sep 2022 07:28:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 30 Sep 2022 07:28:54 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 30 Sep 2022 07:29:41 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:891f6400ce611ee5975f04ad6d2c68305c76a8628b846df1b1f9ac7c45b1311c`  
		Last Modified: Thu, 01 Sep 2022 23:52:11 GMT  
		Size: 33.3 MB (33295624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27973b7f1fd40002c606c38a9008bc69ce1434ac2f21f853be42bc2ce78370a4`  
		Last Modified: Fri, 02 Sep 2022 04:46:47 GMT  
		Size: 17.2 MB (17186881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4fb788431a6f38f365e6cd1688c8ea92a5e96e5456a223f1fcf1a3256d5545`  
		Last Modified: Fri, 02 Sep 2022 04:50:38 GMT  
		Size: 49.0 MB (48957670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e602d3c496736215f4d92c0a85d58cd175ab1a9175aa6b53aef0c5e97b4e590`  
		Last Modified: Fri, 02 Sep 2022 04:50:27 GMT  
		Size: 3.8 MB (3752388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07b61e9bebf8ee9568e6e39b24c604ff9f30382a9175fcdd1d156f0733ced9c`  
		Last Modified: Fri, 30 Sep 2022 07:32:36 GMT  
		Size: 14.3 MB (14277783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5363408c4524740dcd60b3c1e2084129c46411adb20ed63506a373cef2bc8ac4`  
		Last Modified: Fri, 30 Sep 2022 07:32:32 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce476597d08c938b99ee9b355441b3c4986b0ae38f448f21bb5a10d6ef1847f`  
		Last Modified: Fri, 30 Sep 2022 07:32:32 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43652ed2feae0b52a26ea3c628bc72b463e24035544fa3ad850077e33b72a838`  
		Last Modified: Fri, 30 Sep 2022 07:32:32 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c56cc698fe54e019b11d09725d9c88f89e58398811590e93bcc339fc6bef7eb`  
		Last Modified: Fri, 30 Sep 2022 07:32:32 GMT  
		Size: 10.7 KB (10740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95daa9fc2c775cc87df5c704c4c07f859062c82337d4c0453907a1b66f37eb07`  
		Last Modified: Fri, 30 Sep 2022 07:32:33 GMT  
		Size: 2.5 MB (2549965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2473b924d241154988d08c8798f39d4a950e16b224fcf77a7c3d320db3eb3639`  
		Last Modified: Fri, 30 Sep 2022 07:34:28 GMT  
		Size: 281.6 MB (281600862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c01026eee1d5e737471c0885289dd5230a824bfcc47d42f1918b8f48fedacbf`  
		Last Modified: Fri, 30 Sep 2022 07:33:56 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3361ca35278b27df40621d72fa0438ef17caab4a26a6d55ad72387050eb3dfd0`  
		Last Modified: Fri, 30 Sep 2022 07:33:59 GMT  
		Size: 12.8 MB (12784511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:820fc1bf458180a330f132c29bb6d4f0defbd700802277ad389db34dd973e47f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.9 MB (407920208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300a1b803cd3e70ea9f9523e91c3b1191c9d1a98dd13da041331f7b94ed97525`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 02 Sep 2022 01:03:13 GMT
ADD file:75a78d9ec31ac5486bdde3e48ebfc534089c5f38f14850243c2ab2e632f0bbe5 in / 
# Fri, 02 Sep 2022 01:03:16 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 01:36:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 01:36:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 01:42:22 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1_openj9-0.33.1
# Fri, 02 Sep 2022 01:43:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0114aada7edc773346a6729c992bdd2f5ff8aedec756547f42839bb37c12e3bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_aarch64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='35955d6ce7b9e262abfd2b2dff585b3be71fa7e320ea23b5d604aa45fac2d251';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_ppc64le_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='338ea5fe72f5a1a075c02953882a985dee437f0b60e432eacb02ba8ca15b3e0b';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_x64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='cf8b58da8d98f0a01d228ed3fe7177ed6ba783b8134113073977cc3ebf9eec33';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jre_s390x_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 02 Sep 2022 01:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 01:43:26 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 02 Sep 2022 01:43:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 02 Sep 2022 03:32:46 GMT
ARG VERBOSE=false
# Fri, 02 Sep 2022 03:32:46 GMT
ARG OPENJ9_SCC=true
# Fri, 30 Sep 2022 01:15:30 GMT
ARG EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb
# Fri, 30 Sep 2022 01:15:30 GMT
ARG NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34
# Fri, 30 Sep 2022 01:15:31 GMT
ARG NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725
# Fri, 30 Sep 2022 01:15:31 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.10 org.opencontainers.image.revision=cl221020220912-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 30 Sep 2022 01:15:31 GMT
ENV LIBERTY_VERSION=22.0.0_10
# Fri, 30 Sep 2022 01:15:31 GMT
ARG LIBERTY_URL
# Fri, 30 Sep 2022 01:15:32 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 30 Sep 2022 01:15:47 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Sep 2022 01:15:48 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Sep 2022 01:15:49 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.10 BuildLabel=cl221020220912-1100
# Fri, 30 Sep 2022 01:15:49 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 30 Sep 2022 01:15:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 30 Sep 2022 01:15:51 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Fri, 30 Sep 2022 01:15:51 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 30 Sep 2022 01:15:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 30 Sep 2022 01:16:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=44a2cb9704f0ed8e871e9d1a8faa55563d093d0c34af3c248492dd1790a794eb NON_IBM_SHA=9e1ddbc876eb5fd3182799b2ccf6619f23acfe6d4b0b8ee82c72e3944ad15b34 NOTICES_SHA=1f852693234e6b9fabccb4218a21a88b485300dccd76ee089fb007aaf3180725 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 30 Sep 2022 01:16:02 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 30 Sep 2022 01:16:03 GMT
USER 1001
# Fri, 30 Sep 2022 01:16:03 GMT
EXPOSE 9080 9443
# Fri, 30 Sep 2022 01:16:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 30 Sep 2022 01:16:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 30 Sep 2022 01:32:24 GMT
ARG VERBOSE=false
# Fri, 30 Sep 2022 01:32:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 30 Sep 2022 01:39:50 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 30 Sep 2022 01:40:04 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 30 Sep 2022 01:40:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:b87ab7b8bb5c2a1f34d9a2e9887fde669c33cea7428fdb048362dfa81eccaa75`  
		Last Modified: Fri, 02 Sep 2022 01:04:49 GMT  
		Size: 27.0 MB (27045282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd01eb1d3fd7f360311787e7b3dc9a7432fb610c419ed60b3af169f5a016d2dc`  
		Last Modified: Fri, 02 Sep 2022 01:47:23 GMT  
		Size: 15.7 MB (15712131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0d3be90ba55b6080aff8d2288b1e65386db4b9a62d83bfdd3802b7f46f0457`  
		Last Modified: Fri, 02 Sep 2022 01:49:27 GMT  
		Size: 47.0 MB (47029683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca5666e52dd5e420fb0341efbb7575d32ab69cf24dc30cd5aa79013c6d49bd7`  
		Last Modified: Fri, 02 Sep 2022 01:49:21 GMT  
		Size: 4.9 MB (4885621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75d3bfb29940587ce7309509d4598338bafa8213453c2707164a6ba7d4dfc72`  
		Last Modified: Fri, 30 Sep 2022 01:44:44 GMT  
		Size: 14.3 MB (14277529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d985cdc64acc3863bc93c0b92083a41b96245fb239ff73f6230e9d7b9246963b`  
		Last Modified: Fri, 30 Sep 2022 01:44:42 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5492339535564888929e849ef6f87be4de149004e6fa0492eae51728d3852fa5`  
		Last Modified: Fri, 30 Sep 2022 01:44:42 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305a86dd4b191bbe357d20a529e123c2cc4e20da675e275223c8c0ff9987057f`  
		Last Modified: Fri, 30 Sep 2022 01:44:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed47ba57f0a2f5941f21e1fee03fc5dc01f843a6943f972f11d16c0e9297cbe`  
		Last Modified: Fri, 30 Sep 2022 01:44:41 GMT  
		Size: 10.7 KB (10739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86558b5cf2bca370738f77602bf604e779069726fd05ccc84fa3321cdd996058`  
		Last Modified: Fri, 30 Sep 2022 01:44:42 GMT  
		Size: 2.6 MB (2620669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d63bbe39e8e69c8beb7a5b3aaad57776dee9181dc5db2f1b3412993338e366`  
		Last Modified: Fri, 30 Sep 2022 01:45:45 GMT  
		Size: 281.6 MB (281600027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eca1087468ef1a0a2232523c774aec9e8f98a8205d7e6641c4b21bb785bfd4b`  
		Last Modified: Fri, 30 Sep 2022 01:45:32 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1d34b9795b34fcf10f4c57b49415943285fb9d61d0724867f6a511f53387ed`  
		Last Modified: Fri, 30 Sep 2022 01:45:34 GMT  
		Size: 14.7 MB (14726880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
