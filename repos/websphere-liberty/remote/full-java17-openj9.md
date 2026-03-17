## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:3d1c1a80cbef006bfbaeb8206fc2111fbd5be0117d79e26d017913d3345bec96
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

### `websphere-liberty:full-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:7cee2af37ccd1f8b7f270a73f585d17ff2bf176dba905a76dd030eaeea15851d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.2 MB (507222597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78da80d6a12eaf926e6f1cf1bb3a68f88a096207067a281f06f84eb986019529`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:36:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:36:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:36:02 GMT
ENV JAVA_VERSION=jdk-17.0.18+8.1_openj9-0.57.0
# Tue, 17 Mar 2026 01:36:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='af8099780c9558602b4af15b80e0b4cfd55b7434d97e086d01087685f388df15';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_17.0.18.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='26a89d3b401881cce54aa4e3a0d2251ada51e937fb9b5bdb9a2717dbc28c3632';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_17.0.18.1.tar.gz';          ;;        amd64|x86_64)          ESUM='8f7d27633cdd7d66ebd63ccf5b653b7605c76c35189ca1459b4826ec2654c7a4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_17.0.18.1.tar.gz';          ;;        s390x)          ESUM='3ce902b2922fe5c03c4da2f806e737e0a881510da5bf7de4267e469dea59291e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_17.0.18.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 01:36:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:36:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 01:37:07 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 02:54:10 GMT
USER root
# Tue, 17 Mar 2026 02:54:10 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 02:54:10 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:54:10 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 02:54:10 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 02:54:10 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Tue, 17 Mar 2026 02:54:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Tue, 17 Mar 2026 02:54:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 17 Mar 2026 02:54:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Tue, 17 Mar 2026 02:54:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Mar 2026 02:54:10 GMT
ARG LIBERTY_URL
# Tue, 17 Mar 2026 02:54:10 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 17 Mar 2026 02:54:26 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:54:26 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:54:26 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 02:54:26 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 17 Mar 2026 02:54:26 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 17 Mar 2026 02:54:26 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 17 Mar 2026 02:54:26 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 02:54:31 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 17 Mar 2026 02:54:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Mar 2026 02:54:31 GMT
USER 1001
# Tue, 17 Mar 2026 02:54:31 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 02:54:31 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 02:54:31 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 17 Mar 2026 03:42:21 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 03:42:21 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 17 Mar 2026 03:42:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 17 Mar 2026 03:42:21 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 17 Mar 2026 03:42:44 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85238ca697e53a258c4fcac9d67d0356184243c19c05b892dfa6a40e952bca89`  
		Last Modified: Tue, 17 Mar 2026 01:37:20 GMT  
		Size: 12.8 MB (12805284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a9a45a0930e98711dc26252b5b6aa80cb8abdb638f19466de3338fd3a7f0ce`  
		Last Modified: Tue, 17 Mar 2026 01:37:21 GMT  
		Size: 55.4 MB (55436323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378ad9c27c391105e768ab94a283e4f42088b087dbb0f8dddf481dd671ed63f0`  
		Last Modified: Tue, 17 Mar 2026 01:37:20 GMT  
		Size: 5.0 MB (4970030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e137d4b8665af57a524cd30886087fb9a620d86326adb166857ffd34f0ab3621`  
		Last Modified: Tue, 17 Mar 2026 02:54:40 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b887fdb7f3ad88c74ee904555c7935e4156e678b0f74a7109b527fb09ed9b4d`  
		Last Modified: Tue, 17 Mar 2026 02:54:41 GMT  
		Size: 18.0 MB (18040622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99522548945c18c691fa4618818271f00072333205668d370c74105c43159e8b`  
		Last Modified: Tue, 17 Mar 2026 02:54:40 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b174c23f9eab54e993104c371975d4b2816bbdf362137166c43dd0ca5c404b98`  
		Last Modified: Tue, 17 Mar 2026 02:54:41 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad039f00438b3cb2955924a407db6015746bf9b2d997fd11eedcf4c6e9cafab`  
		Last Modified: Tue, 17 Mar 2026 02:54:41 GMT  
		Size: 14.1 KB (14112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34204d669dd7021c359c6cbfad7f068d66254b42f20aaa7d4f6e20349338f`  
		Last Modified: Tue, 17 Mar 2026 02:54:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1361197b9b1eab5cc5c932ef516ad70e93961b07e874f6137223459bf5a33977`  
		Last Modified: Tue, 17 Mar 2026 02:54:42 GMT  
		Size: 15.0 KB (14977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72354752220f4d58444dd94a096d5c903a2ec31cbc3c879c3bc226b1c09fdf2a`  
		Last Modified: Tue, 17 Mar 2026 02:54:43 GMT  
		Size: 2.7 MB (2745854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d324f383419d71e00d5ac505b528b5516670f37c91f8c09fd62e4b2d60e069`  
		Last Modified: Tue, 17 Mar 2026 03:43:16 GMT  
		Size: 367.8 MB (367826469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5967b318297da9163a8ba1aeb80417170e369cdc5e777aa658b5808a668ccb`  
		Last Modified: Tue, 17 Mar 2026 03:43:09 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b016d13fdaec4c7a28689667e20cecabb1fb1367241f1e75742e4e61bfadeed2`  
		Last Modified: Tue, 17 Mar 2026 03:43:10 GMT  
		Size: 15.6 MB (15602000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3e610e52179452067c850fd47d1976af231f69b5998b7ff20854af3b40e1582a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3184f29024537acf742186be043dc80354471ef11ae063bdefa89f8ef5212305`

```dockerfile
```

-	Layers:
	-	`sha256:c3f96bc2651793f8eb5cd6a1e35e650d4ac2c4e1d4628f9cdb3307db478af7bc`  
		Last Modified: Tue, 17 Mar 2026 03:43:09 GMT  
		Size: 5.4 MB (5375343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5132adc699b6c1f9d1f6a5a6ac4d39fdd1327ef830a636c400179c63f31220`  
		Last Modified: Tue, 17 Mar 2026 03:43:09 GMT  
		Size: 19.6 KB (19634 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:497384ee899ee30a1d449d1c800b76c6fd8739a3fa058f3585c1c92953fa92a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.1 MB (504119543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639e85ffdd2bd2d187124ed7d906f3b115205082a65d97d14398f24c1905aaba`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:35:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:35:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:35:45 GMT
ENV JAVA_VERSION=jdk-17.0.18+8.1_openj9-0.57.0
# Tue, 17 Mar 2026 01:37:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='af8099780c9558602b4af15b80e0b4cfd55b7434d97e086d01087685f388df15';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_17.0.18.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='26a89d3b401881cce54aa4e3a0d2251ada51e937fb9b5bdb9a2717dbc28c3632';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_17.0.18.1.tar.gz';          ;;        amd64|x86_64)          ESUM='8f7d27633cdd7d66ebd63ccf5b653b7605c76c35189ca1459b4826ec2654c7a4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_17.0.18.1.tar.gz';          ;;        s390x)          ESUM='3ce902b2922fe5c03c4da2f806e737e0a881510da5bf7de4267e469dea59291e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_17.0.18.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 01:37:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:37:32 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 01:38:35 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 02:58:31 GMT
USER root
# Tue, 17 Mar 2026 02:58:31 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 02:58:31 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:58:31 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 02:58:31 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 02:58:31 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Tue, 17 Mar 2026 02:58:31 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Tue, 17 Mar 2026 02:58:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 17 Mar 2026 02:58:31 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Tue, 17 Mar 2026 02:58:31 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Mar 2026 02:58:31 GMT
ARG LIBERTY_URL
# Tue, 17 Mar 2026 02:58:31 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 17 Mar 2026 02:58:48 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:58:48 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:58:48 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 02:58:48 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 17 Mar 2026 02:58:48 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 17 Mar 2026 02:58:48 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 17 Mar 2026 02:58:49 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 02:58:53 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 17 Mar 2026 02:58:53 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Mar 2026 02:58:53 GMT
USER 1001
# Tue, 17 Mar 2026 02:58:53 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 02:58:53 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 02:58:53 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 17 Mar 2026 03:45:35 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 03:45:35 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 17 Mar 2026 03:45:35 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 17 Mar 2026 03:45:35 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 17 Mar 2026 03:46:04 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954dbd6e658b4f0975e6d417ec4a7da0d11e2940e9b8c885c12a7ec6dc44288c`  
		Last Modified: Tue, 17 Mar 2026 01:37:14 GMT  
		Size: 12.8 MB (12837488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468675e692104a6aa32b3bc4a5bcfb92648f2b7813278fb5315871509adbc3b3`  
		Last Modified: Tue, 17 Mar 2026 01:38:48 GMT  
		Size: 53.7 MB (53699096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c8385b032a563d10c02b241d321668afffdd044e3920fba008a9f3f6779975`  
		Last Modified: Tue, 17 Mar 2026 01:38:47 GMT  
		Size: 4.8 MB (4760911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9965eb369e8ab28e3a9ce8d6c2d6fcf0822269d2036dd0d080f5469e24d4713`  
		Last Modified: Tue, 17 Mar 2026 02:59:03 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50469ea856b5c87db0195dcda63f9f8ae9a1dfb2dc3b0f44d3221f03be17d96`  
		Last Modified: Tue, 17 Mar 2026 02:59:04 GMT  
		Size: 18.0 MB (18040781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdf0c0dd2c50bfbbb055a7bf5bc500f33550c634e4245c35e13b44c0a87e800`  
		Last Modified: Tue, 17 Mar 2026 02:59:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9016afa1aa922497a0908887e1b3c836bb26ea63114ea23d8c4c10c09a48c09c`  
		Last Modified: Tue, 17 Mar 2026 02:59:03 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ad32cf67f6391ab34eff5b6f16103a24a76b8b466df17f740cdaebca3a611a`  
		Last Modified: Tue, 17 Mar 2026 02:59:04 GMT  
		Size: 14.1 KB (14119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99717538a88c14a9be1dfc11d784f9fda3ba335ab29d93d95ce526de60bbb2b3`  
		Last Modified: Tue, 17 Mar 2026 02:59:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175436e9ddf85ab769788c65d8c4568c222b6de17ece528c44ea4c79cbd5306f`  
		Last Modified: Tue, 17 Mar 2026 02:59:04 GMT  
		Size: 15.0 KB (14992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a800a6021e5aee9642a2f97efc943de60c6028f16e7e95f5245b490dabe0071f`  
		Last Modified: Tue, 17 Mar 2026 02:59:05 GMT  
		Size: 2.8 MB (2837733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3058e29979019bbafefe32c34c9cc7ee3c36108856705b7f80e27f549846af`  
		Last Modified: Tue, 17 Mar 2026 03:46:41 GMT  
		Size: 367.8 MB (367826989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4b924e6eba7fc950e17e9c4123e9e8373aa9242f56805d055813cbc308ba9`  
		Last Modified: Tue, 17 Mar 2026 03:46:35 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7616deec292ec1fa571abda23ab290c724f36c79d02f1c7e9065c4ffe0996eb7`  
		Last Modified: Tue, 17 Mar 2026 03:46:35 GMT  
		Size: 15.2 MB (15172209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:545ad96efc40c2c8976d06c7e1cf2c3a6d76988307114d148726d46c3f462320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c43c04000cd29b9fe86c4a61386974bc8f2dfb3c454cf2af87b35a9a1e1a81e`

```dockerfile
```

-	Layers:
	-	`sha256:4c362d7f906f4a5325962dc175a27b1d31b0ee25a56e11852930d91e640a4c8e`  
		Last Modified: Tue, 17 Mar 2026 03:46:35 GMT  
		Size: 5.4 MB (5373873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b169731417c71c9a72a240c9db0ebfb5e168c99429c35769e0769762070d2f35`  
		Last Modified: Tue, 17 Mar 2026 03:46:34 GMT  
		Size: 19.7 KB (19718 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:30fbdae0bb7b534301a205ff1371ab63fa1bf71badc5d54aa61ee7d355905933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.5 MB (511527009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e4fe34954f3e4fb353df1c5d2d7f87224879e83b6d7003d67f3991c58ba717`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:28:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:28:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:28:56 GMT
ENV JAVA_VERSION=jdk-17.0.18+8.1_openj9-0.57.0
# Tue, 03 Mar 2026 20:18:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='af8099780c9558602b4af15b80e0b4cfd55b7434d97e086d01087685f388df15';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_17.0.18.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='26a89d3b401881cce54aa4e3a0d2251ada51e937fb9b5bdb9a2717dbc28c3632';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_17.0.18.1.tar.gz';          ;;        amd64|x86_64)          ESUM='8f7d27633cdd7d66ebd63ccf5b653b7605c76c35189ca1459b4826ec2654c7a4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_17.0.18.1.tar.gz';          ;;        s390x)          ESUM='3ce902b2922fe5c03c4da2f806e737e0a881510da5bf7de4267e469dea59291e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_17.0.18.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 20:18:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:18:12 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 20:19:17 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Mar 2026 22:53:03 GMT
USER root
# Tue, 03 Mar 2026 22:53:03 GMT
ARG VERBOSE=false
# Tue, 03 Mar 2026 22:53:03 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Mar 2026 22:53:03 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 03 Mar 2026 22:53:03 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 03 Mar 2026 22:53:03 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Tue, 03 Mar 2026 22:53:03 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Tue, 03 Mar 2026 22:53:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 03 Mar 2026 22:53:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Tue, 03 Mar 2026 22:53:03 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Mar 2026 22:53:03 GMT
ARG LIBERTY_URL
# Tue, 03 Mar 2026 22:53:03 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Mar 2026 22:53:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 22:53:21 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Mar 2026 22:53:23 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Mar 2026 22:53:23 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 03 Mar 2026 22:53:25 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 03 Mar 2026 22:53:25 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 03 Mar 2026 22:53:27 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 03 Mar 2026 22:53:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 03 Mar 2026 22:53:37 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Mar 2026 22:53:37 GMT
USER 1001
# Tue, 03 Mar 2026 22:53:37 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Mar 2026 22:53:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Mar 2026 22:53:37 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 04 Mar 2026 00:10:45 GMT
ARG VERBOSE=false
# Wed, 04 Mar 2026 00:10:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 04 Mar 2026 00:10:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 04 Mar 2026 00:10:45 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 04 Mar 2026 00:11:27 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc74705b5205a118b6fdfc67d17a8b658c02f7792610bbbab1a9a9579b5bc8`  
		Last Modified: Tue, 17 Feb 2026 20:30:36 GMT  
		Size: 13.8 MB (13799621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f18f5bb68e55bda22eebd0b78a4e2caddc6325db75348c5f4e52e2d0ca90f58`  
		Last Modified: Tue, 03 Mar 2026 20:19:43 GMT  
		Size: 57.3 MB (57293467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632ab70a60e367be519cf4d8df80ddbf034143d018aeee4ef43eb5ae7f5515e9`  
		Last Modified: Tue, 03 Mar 2026 20:19:42 GMT  
		Size: 3.8 MB (3839051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429df2cc9b8275b31b7998043a2e8c9bd67e6aab180497378543f4c40b3703a`  
		Last Modified: Tue, 03 Mar 2026 22:53:55 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1962dcae71dd279bfac61b48883295dc40caf9ea9b04d86b7d9094bf090a124a`  
		Last Modified: Tue, 03 Mar 2026 22:53:56 GMT  
		Size: 18.0 MB (18041141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d431fd57351b4134d801f7cca78eb4e5753af7fa69b7ba7c75f32f13ac72cf44`  
		Last Modified: Tue, 03 Mar 2026 22:53:55 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6bdea16e577902ad464d6b6363b79c09af01283c3a35d42442133c002a50e4`  
		Last Modified: Tue, 03 Mar 2026 22:53:55 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedc63e8f901085e1934484d4ad093422d74beea0a10429e55a23fad9f918eba`  
		Last Modified: Tue, 03 Mar 2026 22:53:56 GMT  
		Size: 14.1 KB (14116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbfcd59f146687cfe0909c62125190109a4f66a5dfad62c0d0697dc1c6fe1ed`  
		Last Modified: Tue, 03 Mar 2026 22:53:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72febd62079a37dfbc83662c3330c51f7bae855f231722de416ffa6118357c1`  
		Last Modified: Tue, 03 Mar 2026 22:53:56 GMT  
		Size: 15.0 KB (14996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4745eae06a2d1fab6fe5a85eaef6c8de149a914f080313bccdc4fa68fe6ab57d`  
		Last Modified: Tue, 03 Mar 2026 22:53:58 GMT  
		Size: 2.7 MB (2721903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c0589472328a514b739e409ea0f83e49fc5681052d9133ecb9f05c3c915cf2`  
		Last Modified: Wed, 04 Mar 2026 00:12:25 GMT  
		Size: 367.8 MB (367825497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1633d99c6a48c91f3e0112e7ac37da496535072ef0a183280c9bd1e90092e9cc`  
		Last Modified: Wed, 04 Mar 2026 00:12:17 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4e9e3f6eb27fd4b6355b444f80731448da077ccf027f930733affa1bdcc51b`  
		Last Modified: Wed, 04 Mar 2026 00:12:18 GMT  
		Size: 13.6 MB (13630612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:06c71ff952911c30769aed6274b3a4db2bf2e5f6aa5767f51343824851ce6a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75325eaf01bbfd87b6ca6754a30c39eefe72345295fe2486875fab3d8e888080`

```dockerfile
```

-	Layers:
	-	`sha256:576993c65b06742fc82598ad355d46d79a8321c31b19706dc6aa1788df8bd803`  
		Last Modified: Wed, 04 Mar 2026 00:12:17 GMT  
		Size: 5.4 MB (5379937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c413e706bcdcc6e0cc7d04abbc313c9622bc24f228e895f04d42615566e6d1a5`  
		Last Modified: Wed, 04 Mar 2026 00:12:17 GMT  
		Size: 19.7 KB (19663 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ad2678967e866a00bdf952b8f4450f0d91e18a21961089e1c92563a62aa8b75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.4 MB (507385038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2224da8a5309efd2c32579032ff126ecd9a2aa68b5abca0893521c720523b2fd`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:51 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:51 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:52 GMT
ADD file:be1799101a7a15f881e3aebea1e86fa6a156760dc7688b1affe179e948814a3b in / 
# Tue, 10 Feb 2026 16:50:52 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:17:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:17:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:17:22 GMT
ENV JAVA_VERSION=jdk-17.0.18+8.1_openj9-0.57.0
# Tue, 03 Mar 2026 21:27:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='af8099780c9558602b4af15b80e0b4cfd55b7434d97e086d01087685f388df15';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_17.0.18.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='26a89d3b401881cce54aa4e3a0d2251ada51e937fb9b5bdb9a2717dbc28c3632';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_17.0.18.1.tar.gz';          ;;        amd64|x86_64)          ESUM='8f7d27633cdd7d66ebd63ccf5b653b7605c76c35189ca1459b4826ec2654c7a4';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_17.0.18.1.tar.gz';          ;;        s390x)          ESUM='3ce902b2922fe5c03c4da2f806e737e0a881510da5bf7de4267e469dea59291e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.18+8.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_17.0.18.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 03 Mar 2026 21:27:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 21:27:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 03 Mar 2026 21:28:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 03 Mar 2026 22:22:45 GMT
USER root
# Tue, 03 Mar 2026 22:22:45 GMT
ARG VERBOSE=false
# Tue, 03 Mar 2026 22:22:45 GMT
ARG OPENJ9_SCC=true
# Tue, 03 Mar 2026 22:22:45 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 03 Mar 2026 22:22:45 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 03 Mar 2026 22:22:45 GMT
ARG LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
# Tue, 03 Mar 2026 22:22:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.2 org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.2 com.ibm.websphere.liberty.version=26.0.0.2
# Tue, 03 Mar 2026 22:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 03 Mar 2026 22:22:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.2 BuildLabel=cl260220260207-1901
# Tue, 03 Mar 2026 22:22:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 03 Mar 2026 22:22:45 GMT
ARG LIBERTY_URL
# Tue, 03 Mar 2026 22:22:45 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 03 Mar 2026 22:22:55 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 22:22:55 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 03 Mar 2026 22:22:55 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 03 Mar 2026 22:22:55 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 03 Mar 2026 22:22:55 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 03 Mar 2026 22:22:55 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 03 Mar 2026 22:22:55 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 03 Mar 2026 22:23:00 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.2 LIBERTY_BUILD_LABEL=cl260220260207-1901 LIBERTY_SHA=23a9ee4c5b7bea935aac3f250ada5acffb9c4f25 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 03 Mar 2026 22:23:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 03 Mar 2026 22:23:00 GMT
USER 1001
# Tue, 03 Mar 2026 22:23:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 03 Mar 2026 22:23:00 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 03 Mar 2026 22:23:00 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 03 Mar 2026 23:21:56 GMT
ARG VERBOSE=false
# Tue, 03 Mar 2026 23:21:56 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 03 Mar 2026 23:21:56 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 03 Mar 2026 23:21:56 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 03 Mar 2026 23:22:29 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:8b6ba492713239cba0554ce53d24405e1285684fa64bcfb05df4af8037ba5836`  
		Last Modified: Tue, 10 Feb 2026 17:42:12 GMT  
		Size: 29.9 MB (29909784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2ce3b2a70015000a5b0ceaa4885f1aceec67cb23d3ef542311e0f5506c39b0`  
		Last Modified: Tue, 17 Feb 2026 20:19:02 GMT  
		Size: 13.1 MB (13118433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f7f88277df3764de61074811f8b760ba68ac2e3a1fb51c66dbce0979116da`  
		Last Modified: Tue, 03 Mar 2026 21:29:12 GMT  
		Size: 54.3 MB (54319441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c274e4bf5959477f02b9c56ff4131641b77446975ab9aaf597f2b2753e0ad4`  
		Last Modified: Tue, 03 Mar 2026 21:29:10 GMT  
		Size: 5.2 MB (5208126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df89314ed73efff20105fd13c7b137eaad301e6aa48529ae5df04d0e98e51d6d`  
		Last Modified: Tue, 03 Mar 2026 22:23:12 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e872f51cab3d4d09a262441c6250bd508776a1f915eeed79ff87f55183208e4`  
		Last Modified: Tue, 03 Mar 2026 22:23:12 GMT  
		Size: 18.0 MB (18040555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16085f213012aa13d87b8df7df32ef1bd6b2f228b72f1b9b55c5a65f2d934737`  
		Last Modified: Tue, 03 Mar 2026 22:23:12 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd39cad3da46e4470a63c6aeb3fe1b897016c75010d3af5cd895ce25d7bff49`  
		Last Modified: Tue, 03 Mar 2026 22:23:12 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec351a194286a7dd675b0d19966b8eca8f0dd6d1599883c5776875d02c67d5f`  
		Last Modified: Tue, 03 Mar 2026 22:23:13 GMT  
		Size: 14.1 KB (14115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f41544247de3af97b5c6a55ac6b954dd9a0a578b593408bb173de089b8d3264`  
		Last Modified: Tue, 03 Mar 2026 22:23:13 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0627cf06f1de4eec366510f0150306e032be6baaa1157285da8d9d33cddf4c9a`  
		Last Modified: Tue, 03 Mar 2026 22:23:13 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e03d0f81e7517d947b63985c7d6e17977b7e7abdf3336b216c0e3aef892ece`  
		Last Modified: Tue, 03 Mar 2026 22:23:14 GMT  
		Size: 2.9 MB (2853150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976c60b10aabe18137b1c81600f712187f98f70972d3bf2946722297e6bd545d`  
		Last Modified: Tue, 03 Mar 2026 23:23:18 GMT  
		Size: 367.8 MB (367824800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b2b2f149320d5603ebf5c2e5882b81d1db0705d93d1d05d9249ff671fe6fe7`  
		Last Modified: Tue, 03 Mar 2026 23:23:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639077a5ea45b280c62fbec309187262704c3d36f3dcec4e00a5ca73aeed5d17`  
		Last Modified: Tue, 03 Mar 2026 23:23:11 GMT  
		Size: 16.0 MB (16045350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:8b72f41438714f04fea8191447de8a3feced03dbad86f9206defc45856c6f7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5395947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463ca523da21fb7473eabf417a21f1eb87940c5d970af1a155110debfbee0951`

```dockerfile
```

-	Layers:
	-	`sha256:2ecbf363a2290afd25662e78c8ad32ea8067f6e159e0b8e50667cf1d50523ae1`  
		Last Modified: Tue, 03 Mar 2026 23:23:11 GMT  
		Size: 5.4 MB (5376312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1256cccf60009d4db1098a8d87dafa7760a1b4b2b13646fb7885a33ccfb307`  
		Last Modified: Tue, 03 Mar 2026 23:23:11 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
