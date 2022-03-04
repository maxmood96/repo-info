## `websphere-liberty:kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:29deb4bfd1cb683231b91b9c06f3037dd80c17216e0386fd5995ca850a22303e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:e8e495fb78050100285d96d7f5fdb6d7598b66a47c075de850dd27a31259cf9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113202377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9027e41478470df16d4ef4cfdb30b59d0304505317a932a26f75ae26d9d2443`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:23:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 23:58:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 00:00:36 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1_openj9-0.30.1
# Fri, 04 Mar 2022 00:01:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7c639ec9fff1e9d401b9e616bd63bf5cf046bbe6381ba89fdc1b2a2aa31c22bd';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_aarch64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f2ac9794343a450d0fcf5be392ce4d6abd5f13a6a1c9beb9e69b0d29abc0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_ppc64le_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f8debbd4326883a47c8afe8bbaabb5ed63d1cd2d82ef42b0fea2c6e2e54f74f1';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_x64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        s390x)          ESUM='c0707d8389945f144f8910314ae8eed1d99dd7a653ae3d8e2f58ce656e3c7349';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_s390x_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 04 Mar 2022 00:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:01:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 04 Mar 2022 00:02:17 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 04 Mar 2022 03:36:01 GMT
ARG VERBOSE=false
# Fri, 04 Mar 2022 03:36:01 GMT
ARG OPENJ9_SCC=true
# Fri, 04 Mar 2022 03:36:01 GMT
ARG EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171
# Fri, 04 Mar 2022 03:36:01 GMT
ARG NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87
# Fri, 04 Mar 2022 03:36:01 GMT
ARG NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659
# Fri, 04 Mar 2022 03:36:02 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.2 org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 04 Mar 2022 03:36:02 GMT
ENV LIBERTY_VERSION=22.0.0_02
# Fri, 04 Mar 2022 03:36:02 GMT
ARG LIBERTY_URL
# Fri, 04 Mar 2022 03:36:02 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 04 Mar 2022 03:36:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:36:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 03:36:14 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.2 BuildLabel=cl220220220201-1901
# Fri, 04 Mar 2022 03:36:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 04 Mar 2022 03:36:15 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 04 Mar 2022 03:36:15 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Fri, 04 Mar 2022 03:36:15 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 04 Mar 2022 03:36:15 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 04 Mar 2022 03:36:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 04 Mar 2022 03:36:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 04 Mar 2022 03:36:23 GMT
USER 1001
# Fri, 04 Mar 2022 03:36:23 GMT
EXPOSE 9080 9443
# Fri, 04 Mar 2022 03:36:23 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 04 Mar 2022 03:36:23 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d66994d054da0091fad11fb497b2a23c0cfd350d897d78d57f78b3200b90fd6`  
		Last Modified: Fri, 04 Mar 2022 00:06:51 GMT  
		Size: 16.0 MB (16030868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567b8f8eb8089aa72d03cfbac6276b00568320b44f8548f5c65bd83bd5fe2358`  
		Last Modified: Fri, 04 Mar 2022 00:07:59 GMT  
		Size: 47.7 MB (47658340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c934f4d5f4297067be69f40f99b06c810790e6ecf5d54e30bba34a2dfa4b7684`  
		Last Modified: Fri, 04 Mar 2022 00:07:53 GMT  
		Size: 4.2 MB (4171320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4c26195d1b04d56785b7103515dbd0f85cbc2f57f1407ecaea6305f5401423`  
		Last Modified: Fri, 04 Mar 2022 04:13:53 GMT  
		Size: 14.2 MB (14186231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6c383100ab6c11a8cc96bd686a23448acc271d8bc87dc3c69840a3ba87a5d6`  
		Last Modified: Fri, 04 Mar 2022 04:13:49 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c55672a7c856123edf5aa01d4bc300446fde23ba2a3e7feb2e028dea6859dc`  
		Last Modified: Fri, 04 Mar 2022 04:13:49 GMT  
		Size: 9.7 KB (9678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44fbd00f0fb8b295b673461ec87ec834dcb0b90d958ff4432121c77f7c9fc60`  
		Last Modified: Fri, 04 Mar 2022 04:13:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a104bf949c3d50c442f1f90d700a429a1af28768ee76c2ddbcc2194f0f522`  
		Last Modified: Fri, 04 Mar 2022 04:13:49 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e416530303efa0120263fbae55c5a16c025368abdfb72822b61b8a42fbca8174`  
		Last Modified: Fri, 04 Mar 2022 04:13:50 GMT  
		Size: 2.6 MB (2568574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:3d5336d9154a9409e65098389a9d2d24265c00af55bb5bd08e9bf9c8bb75c0ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118908669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8ff43d69ff5d9e2c7c1a410441abf268246d2fbfd69d74e0784e2919f2b8ab`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 03 Mar 2022 20:28:30 GMT
ADD file:039f04ac6c5dbbe3fb0a5eee16945cf7c5fb7565751d6bdf8ec0c1102798c1de in / 
# Thu, 03 Mar 2022 20:28:38 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 22:04:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 23:22:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:25:27 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1_openj9-0.30.1
# Thu, 03 Mar 2022 23:27:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7c639ec9fff1e9d401b9e616bd63bf5cf046bbe6381ba89fdc1b2a2aa31c22bd';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_aarch64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f2ac9794343a450d0fcf5be392ce4d6abd5f13a6a1c9beb9e69b0d29abc0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_ppc64le_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f8debbd4326883a47c8afe8bbaabb5ed63d1cd2d82ef42b0fea2c6e2e54f74f1';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_x64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        s390x)          ESUM='c0707d8389945f144f8910314ae8eed1d99dd7a653ae3d8e2f58ce656e3c7349';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_s390x_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 03 Mar 2022 23:27:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:27:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 03 Mar 2022 23:27:58 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 04 Mar 2022 04:13:51 GMT
ARG VERBOSE=false
# Fri, 04 Mar 2022 04:13:54 GMT
ARG OPENJ9_SCC=true
# Fri, 04 Mar 2022 04:13:56 GMT
ARG EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171
# Fri, 04 Mar 2022 04:13:59 GMT
ARG NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87
# Fri, 04 Mar 2022 04:14:01 GMT
ARG NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659
# Fri, 04 Mar 2022 04:14:06 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.2 org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 04 Mar 2022 04:14:09 GMT
ENV LIBERTY_VERSION=22.0.0_02
# Fri, 04 Mar 2022 04:14:11 GMT
ARG LIBERTY_URL
# Fri, 04 Mar 2022 04:14:13 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 04 Mar 2022 04:14:42 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 04:14:45 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 04:14:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.2 BuildLabel=cl220220220201-1901
# Fri, 04 Mar 2022 04:14:51 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 04 Mar 2022 04:15:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 04 Mar 2022 04:15:07 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Fri, 04 Mar 2022 04:15:10 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 04 Mar 2022 04:15:21 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 04 Mar 2022 04:15:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 04 Mar 2022 04:15:47 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 04 Mar 2022 04:15:51 GMT
USER 1001
# Fri, 04 Mar 2022 04:15:55 GMT
EXPOSE 9080 9443
# Fri, 04 Mar 2022 04:16:00 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 04 Mar 2022 04:16:03 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a16b43de69d1e799ea2cb675e7e605db0ff3a8d692fd326fbde80a370e0676d5`  
		Last Modified: Thu, 03 Mar 2022 20:33:55 GMT  
		Size: 33.3 MB (33292195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0daad88923e3aab34fc02032aaddf77f4caa3bd81fe7df9b280ef3fbd2796e10`  
		Last Modified: Thu, 03 Mar 2022 23:36:10 GMT  
		Size: 17.2 MB (17205102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6a2caa8a15b936231b7dc7f632a8b24a1fefd4a5e7a08f85ef7ca30c3a0374`  
		Last Modified: Thu, 03 Mar 2022 23:37:48 GMT  
		Size: 48.4 MB (48356017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a547b96114b0b18f0830306197c22bc2e45ab5527241e17e61df91d1a7d34f`  
		Last Modified: Thu, 03 Mar 2022 23:37:41 GMT  
		Size: 3.3 MB (3341625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87680871930532ba3807f9e030af302ad8ef32273bc209cd4a690b1ba9f16c4`  
		Last Modified: Fri, 04 Mar 2022 05:22:26 GMT  
		Size: 14.2 MB (14186830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf73464efb9fad31b035c8170bbb4c5e681260a7fb15562ca16ea590c3d49e3`  
		Last Modified: Fri, 04 Mar 2022 05:22:18 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23a2348d9ff73fa87e01bb452b57379b8a7d92e9a3733322c6167977e80403`  
		Last Modified: Fri, 04 Mar 2022 05:22:18 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d984215d77e8a05ffad3424a96999c2bb39ae1a56d6828b6385d876a3ba49fd2`  
		Last Modified: Fri, 04 Mar 2022 05:22:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5722658a8dda5776f852c67e8bb129fcf66f7b3297d8474405db3127d93df5a`  
		Last Modified: Fri, 04 Mar 2022 05:22:18 GMT  
		Size: 10.7 KB (10663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b183a8949475039ba8e9431438c43830850c51931307d34c5e865bf24a8a86a`  
		Last Modified: Fri, 04 Mar 2022 05:22:19 GMT  
		Size: 2.5 MB (2505593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:e76346b4395c667a857e564100beba3ee3e78c03696e015bfe99894ee708431e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110535586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd931e2611e52ddb50c17881a7c56e5c9f62843c36c34e0976fd243012bf4c0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:52 GMT
ADD file:3162233da685a36a9f274a7fa1d99452cab76f37e3640d38851c782ca506f75b in / 
# Thu, 03 Mar 2022 19:41:53 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 20:04:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:06:17 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1_openj9-0.30.1
# Thu, 03 Mar 2022 20:07:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7c639ec9fff1e9d401b9e616bd63bf5cf046bbe6381ba89fdc1b2a2aa31c22bd';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_aarch64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f2ac9794343a450d0fcf5be392ce4d6abd5f13a6a1c9beb9e69b0d29abc0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_ppc64le_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f8debbd4326883a47c8afe8bbaabb5ed63d1cd2d82ef42b0fea2c6e2e54f74f1';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_x64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        s390x)          ESUM='c0707d8389945f144f8910314ae8eed1d99dd7a653ae3d8e2f58ce656e3c7349';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_s390x_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 03 Mar 2022 20:07:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 20:07:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 03 Mar 2022 20:07:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 03 Mar 2022 21:40:42 GMT
ARG VERBOSE=false
# Thu, 03 Mar 2022 21:40:42 GMT
ARG OPENJ9_SCC=true
# Thu, 03 Mar 2022 21:40:42 GMT
ARG EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171
# Thu, 03 Mar 2022 21:40:42 GMT
ARG NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87
# Thu, 03 Mar 2022 21:40:43 GMT
ARG NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659
# Thu, 03 Mar 2022 21:40:43 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.2 org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 03 Mar 2022 21:40:43 GMT
ENV LIBERTY_VERSION=22.0.0_02
# Thu, 03 Mar 2022 21:40:43 GMT
ARG LIBERTY_URL
# Thu, 03 Mar 2022 21:40:43 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 03 Mar 2022 21:40:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:40:54 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 21:40:54 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.2 BuildLabel=cl220220220201-1901
# Thu, 03 Mar 2022 21:40:54 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 03 Mar 2022 21:40:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 03 Mar 2022 21:40:55 GMT
COPY dir:b44499731da0f244ad2e27b60beff4f4cda216316903b60ecb41a7fba3784b48 in /opt/ibm/helpers/ 
# Thu, 03 Mar 2022 21:40:55 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 03 Mar 2022 21:40:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 03 Mar 2022 21:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=de0dc0b4f90213bfa8bbe8a786af91504f78b1967775a31d46dc55ff14f2d171 NON_IBM_SHA=20a37b8cc381d969d985faebf766bfe5efa07b803d063e0f8739fbe571f43f87 NOTICES_SHA=eaa5532a956414b08a405c8fe78dd7295bfd1f37980b496dbe855def1432a659 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 03 Mar 2022 21:41:01 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 03 Mar 2022 21:41:01 GMT
USER 1001
# Thu, 03 Mar 2022 21:41:01 GMT
EXPOSE 9080 9443
# Thu, 03 Mar 2022 21:41:01 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 03 Mar 2022 21:41:01 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:ade7e68f4e34f438527a34c9761a285c3c3864e3daab0544b2c4f4163c7c3f56`  
		Last Modified: Thu, 03 Mar 2022 19:43:22 GMT  
		Size: 27.1 MB (27084671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6625b9cdb7a6f1a1f7715f9b1e2a04e2e285aa79c11778a4edeca0017ab83b5`  
		Last Modified: Thu, 03 Mar 2022 20:12:44 GMT  
		Size: 15.7 MB (15739982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706208334bd704c42d52eb92ef8018d846fd321bf5e403fde491557477c8bc8`  
		Last Modified: Thu, 03 Mar 2022 20:13:41 GMT  
		Size: 46.7 MB (46692257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eb36864da8ed2097d1a87555b6460db3184759a34200e5599c4e633bc8b11e`  
		Last Modified: Thu, 03 Mar 2022 20:13:35 GMT  
		Size: 4.3 MB (4258402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3045997aff2107079fcb4616a7e75530f863582b8578774af2e75283631d4936`  
		Last Modified: Thu, 03 Mar 2022 22:38:05 GMT  
		Size: 14.2 MB (14186545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b36268f10a9214054254578a264ee29c2f25a9aa7946bbea04425f31b3a4cb`  
		Last Modified: Thu, 03 Mar 2022 22:38:02 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec5404fd00dcc0272426f27a3aad106523462c837b67cc076468d5a096489`  
		Last Modified: Thu, 03 Mar 2022 22:38:02 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7733cffbc45000b0530f569ed4d37f8865100f40ae7b0b55a48eb17ab5c5a603`  
		Last Modified: Thu, 03 Mar 2022 22:38:02 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ec0c860428dca93422f884e9b7c18a42a6d7d0db78af6566f97e8ef9b25115`  
		Last Modified: Thu, 03 Mar 2022 22:38:02 GMT  
		Size: 10.6 KB (10642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949feb469385007c5e36aebb066eaf87dffebbcf036737743fe48f5972cf6fdd`  
		Last Modified: Thu, 03 Mar 2022 22:38:03 GMT  
		Size: 2.6 MB (2552452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
