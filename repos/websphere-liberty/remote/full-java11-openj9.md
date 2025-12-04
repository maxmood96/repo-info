## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:2abbeb4116187c6d47cb4f83cecf70b834d9caea17b4a1fd10ca4488df3eae0c
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

### `websphere-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:0ba4ef72539b86d69438d9537a613abd4bcc250e734bd650903df4f0cd9c59f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.4 MB (505350095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07dcf3317f37b49ef977a3ddc7fe74b7a9ef6acdd3b1ae236f91f75bc9a0c678`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:10:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 23:10:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:10:01 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 23:10:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 23:10:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:10:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 23:10:36 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:46:47 GMT
USER root
# Wed, 03 Dec 2025 21:46:47 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:46:47 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:46:47 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:46:47 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:46:47 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Wed, 03 Dec 2025 21:46:47 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:46:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 03 Dec 2025 21:46:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Wed, 03 Dec 2025 21:46:47 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:46:47 GMT
ARG LIBERTY_URL
# Wed, 03 Dec 2025 21:46:47 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 03 Dec 2025 21:46:55 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Dec 2025 21:46:55 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:46:56 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:46:56 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 03 Dec 2025 21:46:56 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 03 Dec 2025 21:46:56 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 03 Dec 2025 21:46:56 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:47:00 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 03 Dec 2025 21:47:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:47:00 GMT
USER 1001
# Wed, 03 Dec 2025 21:47:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:47:00 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:47:00 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 03 Dec 2025 22:20:17 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 22:20:17 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 03 Dec 2025 22:20:17 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 03 Dec 2025 22:20:17 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 03 Dec 2025 22:20:40 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b188f6006db07bd00eff78992b755ce608a5eecba224eb4feffe4cbc7dbe1f7`  
		Last Modified: Mon, 01 Dec 2025 23:11:00 GMT  
		Size: 12.2 MB (12171796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f1557af6a49327d510ee4f0e4c03c1ff87d137621f3a50fbb34ecd45e58ae7`  
		Last Modified: Mon, 01 Dec 2025 23:11:10 GMT  
		Size: 55.4 MB (55434639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c55fb663654ce7df6bb1f3d54c6205d9f3abbaa1e71a90f79e6963bcc48271`  
		Last Modified: Mon, 01 Dec 2025 23:10:58 GMT  
		Size: 4.4 MB (4392710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8671bb33b427b7e25ef73951c9bec2f8b368f3dbc145ca120c3a1caca99725`  
		Last Modified: Wed, 03 Dec 2025 21:47:17 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11970101e9d0baaa0f82319411d42b87ab3cc920dea4f34cd94b61f216e5c90f`  
		Last Modified: Wed, 03 Dec 2025 21:47:19 GMT  
		Size: 18.0 MB (18036132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71b11977f1580af3971996c06cbe87ef0b4a74caabd218775d14dc970ec6e20`  
		Last Modified: Wed, 03 Dec 2025 21:47:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104dd5aac0a5e600282e777c8589dbb8bd07e11152853e121c223906d9fe3f0f`  
		Last Modified: Wed, 03 Dec 2025 21:47:17 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8445715d68c008bfcd2f1005a7fecddd2e59bb9bf518cfb53eb8de4ec733e91`  
		Last Modified: Wed, 03 Dec 2025 21:47:17 GMT  
		Size: 14.1 KB (14120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c387bc9ef95558cc8bb2c6c36ca4b86b2f358df585651ab19a300979640510`  
		Last Modified: Wed, 03 Dec 2025 21:47:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a231ea0dba7a2d280a7b1e7bf6bc662b6b12dd541f1e4f113dd9e7040a2aa464`  
		Last Modified: Wed, 03 Dec 2025 21:47:17 GMT  
		Size: 15.0 KB (14985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e45b6bf841fd73906e7d56b19cec3f4b7404195c5f2f5db657be31bfde3b3`  
		Last Modified: Wed, 03 Dec 2025 21:47:17 GMT  
		Size: 2.7 MB (2738120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1cf5f9bd9bb090e6588965f8ad7c0b3e63c4b27a1959b587412588e9539f2e`  
		Last Modified: Thu, 04 Dec 2025 09:11:21 GMT  
		Size: 367.2 MB (367199406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4bab7c8863c23e3eaa175ac8b133dc0fa58caf986f253ec530e9d3ac9e8298`  
		Last Modified: Wed, 03 Dec 2025 22:21:22 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bc17074f7fc291dbd2b0cd99d427fd16a3b07c14dc560af6bc6a3279ac5dc2`  
		Last Modified: Wed, 03 Dec 2025 22:21:24 GMT  
		Size: 15.8 MB (15776449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:dfd724f6c857b9f4c8e0e245aa3cf7c340cfec21fb2f99537c2399e44d9e149c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336ca2c036c8b49b3baa2b17922183e3376ed0ba444f808d8f1f9b4061c7b581`

```dockerfile
```

-	Layers:
	-	`sha256:1b61aa0f79c270855e30389f82aa99d91669de62f451cd4ca286214156ec6d65`  
		Last Modified: Thu, 04 Dec 2025 01:21:44 GMT  
		Size: 5.9 MB (5945755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efe42323dc07d0d6f9ffebb16fa6da178c46e7bfba37c8b2c96a8ad8d8d0173`  
		Last Modified: Thu, 04 Dec 2025 01:21:45 GMT  
		Size: 19.6 KB (19631 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:ca18faf4e04dbd8554efc676bde202f6ded194d76a897f934177a7bdb7bbf88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.8 MB (500769397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3a593092208c9cc41750f322043dfe956540904b22bbbc06dafa748bdd6894`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:34 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 21:54:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:54:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:54:42 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:55:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:45:24 GMT
USER root
# Wed, 03 Dec 2025 21:45:24 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:45:24 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:45:24 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:45:24 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:45:24 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Wed, 03 Dec 2025 21:45:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 03 Dec 2025 21:45:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Wed, 03 Dec 2025 21:45:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:45:24 GMT
ARG LIBERTY_URL
# Wed, 03 Dec 2025 21:45:24 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 03 Dec 2025 21:45:36 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Dec 2025 21:45:36 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:45:36 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:45:36 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 03 Dec 2025 21:45:36 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 03 Dec 2025 21:45:36 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 03 Dec 2025 21:45:36 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:45:40 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 03 Dec 2025 21:45:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:45:40 GMT
USER 1001
# Wed, 03 Dec 2025 21:45:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:45:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:45:40 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 03 Dec 2025 22:18:47 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 22:18:47 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 03 Dec 2025 22:18:47 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 03 Dec 2025 22:18:47 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 03 Dec 2025 22:19:12 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe5c25ace4281cda0a6beee2f596c784279f3a2b466d176ba28026d25852efd`  
		Last Modified: Mon, 01 Dec 2025 21:54:57 GMT  
		Size: 12.1 MB (12129891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402e0557a5db00b5b60ff7e347babbfdd7696ef12e5e16eecd068bc841a89646`  
		Last Modified: Mon, 01 Dec 2025 21:55:46 GMT  
		Size: 53.7 MB (53713602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7386bf36af963403218ba8a8bb42e4ab32a270b6c8e6e6f1a5efe9ce234bbfa`  
		Last Modified: Mon, 01 Dec 2025 21:55:39 GMT  
		Size: 4.3 MB (4264010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c018f3c8ea4ae306ce142fefd17777205bd67a4708958884026173ec48ff25`  
		Last Modified: Wed, 03 Dec 2025 21:46:28 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1295cdf2f4ee8dddcec8cdf1b37f0e9d9d2af7058b229fb6dbe2ff3671a9c412`  
		Last Modified: Wed, 03 Dec 2025 21:46:30 GMT  
		Size: 18.0 MB (18036356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245aafa4c5a640deb1b75e8f1cbd025b6e27dc4b8d3bfaca4db0fb6c06bc7022`  
		Last Modified: Wed, 03 Dec 2025 21:46:28 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4a0e8bd3035063f05f26548a83f3c6d7e201eefd9f8999c0279a6ad1190859`  
		Last Modified: Wed, 03 Dec 2025 21:46:28 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966b4bde84c4d7c4fbbe96bb1da6f8fc2365272e9b0353e182504092b570be0b`  
		Last Modified: Wed, 03 Dec 2025 21:46:28 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b1c779cfaef1f98e94035db9da782c8785c3b13f03c7c46755c1b6b4185027`  
		Last Modified: Wed, 03 Dec 2025 21:46:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d711352141dc6d9c634ef324818ddd50475ee90bfef0f89753eeffb14a1ea5`  
		Last Modified: Wed, 03 Dec 2025 21:46:28 GMT  
		Size: 15.0 KB (14982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd20a4afde4b33ac275308b547a0cd1aa6777f7767ec2833cf69466cbd05bda`  
		Last Modified: Wed, 03 Dec 2025 21:46:28 GMT  
		Size: 2.8 MB (2766003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1da474fd8ff7565fccfb91539090c1115f9f2a604c40d7c9dcb46621d738e54`  
		Last Modified: Wed, 03 Dec 2025 22:34:05 GMT  
		Size: 367.2 MB (367201156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84e2a975ef98fe414eab8d0a1b4a23be4b0206b8c461d7b781167fc43229f8a`  
		Last Modified: Wed, 03 Dec 2025 22:20:04 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1d50666d38b4df12b03e65c64fb9194d4b65cead7d57a162807bf6db0e65d6`  
		Last Modified: Wed, 03 Dec 2025 22:20:05 GMT  
		Size: 15.2 MB (15199883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:028d71428114e4aaaef20cb1ab9817775e7722c8c7c401492152880e09f1ca30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5963829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873d8fd88c7c1b435a5ec7dfbdce2fd7ff171014e153f06d56177714f49cebd6`

```dockerfile
```

-	Layers:
	-	`sha256:c4faa315cdb172998ceb0483b624b04d4e8de1d5e766f973704426b73f56cea8`  
		Last Modified: Thu, 04 Dec 2025 01:21:52 GMT  
		Size: 5.9 MB (5944115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182cc3daad80c8bb3576e654186595fa4481efa97e34b26c51ffc2cb1e2f5a75`  
		Last Modified: Thu, 04 Dec 2025 01:21:53 GMT  
		Size: 19.7 KB (19714 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:fe86ef8ef409bd8ec45d0ad6dbcb2f90405d2952abcbf91b54ed52b3acf55f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.8 MB (509835978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6828d328e5a5864a90184f532d13c2f62e56125f64fc352346102152dfa3f4c2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:33 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 21:59:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:59:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:59:29 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 22:00:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:57:34 GMT
USER root
# Wed, 03 Dec 2025 21:57:34 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:57:34 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:57:34 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:57:34 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:57:34 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Wed, 03 Dec 2025 21:57:34 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 03 Dec 2025 21:57:34 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Wed, 03 Dec 2025 21:57:34 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:57:34 GMT
ARG LIBERTY_URL
# Wed, 03 Dec 2025 21:57:34 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 03 Dec 2025 21:57:52 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Dec 2025 21:57:52 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:57:53 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:57:54 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 03 Dec 2025 21:57:55 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 03 Dec 2025 21:57:56 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 03 Dec 2025 21:57:58 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:58:07 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 03 Dec 2025 21:58:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:58:07 GMT
USER 1001
# Wed, 03 Dec 2025 21:58:07 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:58:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:58:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 03 Dec 2025 22:19:57 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 22:19:57 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 03 Dec 2025 22:19:57 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 03 Dec 2025 22:19:58 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 03 Dec 2025 22:20:39 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed02c429613f0e247ffa449100a48c06fced187c5ce8d553e21c41a27e3ae784`  
		Last Modified: Mon, 01 Dec 2025 21:55:07 GMT  
		Size: 12.9 MB (12893867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37be6f838c1885e59c4695d4bd908e38e217defee79992e2c0c2b47e2ae483f6`  
		Last Modified: Mon, 01 Dec 2025 22:00:58 GMT  
		Size: 57.3 MB (57283319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19908eadfd213736cb484c33ffb1437e524e4182db21025aa46d929620f52b87`  
		Last Modified: Mon, 01 Dec 2025 22:00:48 GMT  
		Size: 3.5 MB (3478787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7aaf37d63604cea142b03e752bf01ef17a587f3f75283a152bb180cf082020`  
		Last Modified: Wed, 03 Dec 2025 21:58:42 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42171f39d4deed5b1a41c93bf66a50a2d5077ca229312188b0e660b7a39b7028`  
		Last Modified: Wed, 03 Dec 2025 21:58:43 GMT  
		Size: 18.0 MB (18036654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b78bd487bdaf4b04c1a4baf304daf24d171bdedde87387a850192e266c5296d`  
		Last Modified: Wed, 03 Dec 2025 21:58:42 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787ffb999b32f0d04c493b7635b9ac28ef0af5f23df3cbd9ae99915b7df1a17`  
		Last Modified: Wed, 03 Dec 2025 21:58:42 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90ee3725741c1cde840b66bc0625762b46b215f7a8e0ccc36c932286c4b8759`  
		Last Modified: Wed, 03 Dec 2025 21:58:42 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf536330eea673a9d1916c9ea373ca3f87cdaaa7f608ff5dacb2134f2d3c7801`  
		Last Modified: Wed, 03 Dec 2025 21:58:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382354d65f0f172ca3349f318318bbe89cea192e4ffd2b2dbdb5334eb9185782`  
		Last Modified: Wed, 03 Dec 2025 21:58:41 GMT  
		Size: 15.0 KB (15002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7a612f375be4ef85c48da8efad831c20ae6a1c8b6a50281eb59a43b481d03d`  
		Last Modified: Wed, 03 Dec 2025 21:58:44 GMT  
		Size: 2.7 MB (2733823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1747fee24891c0dd92253042c1e4d1dc48fa177fd4b8e5e8479abe9a4bad1cee`  
		Last Modified: Wed, 03 Dec 2025 22:22:08 GMT  
		Size: 367.2 MB (367202160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce94c921feef5e380522b141738a5ee987ad6c55c0b71ab030ff151ec25bdf7`  
		Last Modified: Wed, 03 Dec 2025 22:22:17 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7277e4181bfee5a5598c25e0ca07b7f2c91f7efc858f5433d43cc90f52ee2da5`  
		Last Modified: Wed, 03 Dec 2025 22:22:19 GMT  
		Size: 13.7 MB (13691834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ce1fc6a1f31a9c29ce2c2c4a91a7f90f9c6e930663ef718f97bae72d5c7f6d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b04ad4457385847879059b92f863ddbafcfbb1b52dca5a05abfa8d7868a5c3`

```dockerfile
```

-	Layers:
	-	`sha256:0e8285ae097561472cf09c24bd1a3777e5251848f6372370370634f8657207c9`  
		Last Modified: Thu, 04 Dec 2025 01:22:03 GMT  
		Size: 6.0 MB (5950376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7228289d0ce0530ae6d7bfcaffd1daddd355e9f8e970fcdcebabe9d3e346d20a`  
		Last Modified: Thu, 04 Dec 2025 01:22:04 GMT  
		Size: 19.7 KB (19658 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0ea0ff83c77ac6a2044eadc404c7ffb0a900b088fce4e6b62dff037baddadeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503877973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abf625ce7b9a02c6384068c19456821212c924a09c86ef8410d5b48f29efc60`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:32 GMT
ENV JAVA_VERSION=jdk-11.0.29+7_openj9-0.56.0
# Mon, 01 Dec 2025 21:55:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9fd5b1e5f18c80d945570cd86db46f737fdecbdcd8978d502c4a601f704c6676';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='16289eb013673a686abfef6631570e5b08c6171a1f7cf79fd495759d53393c38';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='474acb3b9c1ba608efe0c3aa0321a271cfbe2044e89d73e7129b0b013eb484df';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='42c7324f112975abc6a36c1cacad8f7515924cc60c21ac45e5985e7908d2c931';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.29%2B7_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_11.0.29_7_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:55:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:55:36 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:56:11 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:51:44 GMT
USER root
# Wed, 03 Dec 2025 21:51:44 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:51:44 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:51:44 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Wed, 03 Dec 2025 21:51:44 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:51:44 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Wed, 03 Dec 2025 21:51:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Wed, 03 Dec 2025 21:51:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Wed, 03 Dec 2025 21:51:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Wed, 03 Dec 2025 21:51:44 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:51:44 GMT
ARG LIBERTY_URL
# Wed, 03 Dec 2025 21:51:44 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 03 Dec 2025 21:52:14 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Dec 2025 21:52:14 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:52:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:52:15 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 03 Dec 2025 21:52:15 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 03 Dec 2025 21:52:15 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 03 Dec 2025 21:52:15 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:52:23 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 03 Dec 2025 21:52:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:52:23 GMT
USER 1001
# Wed, 03 Dec 2025 21:52:23 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:52:23 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:52:23 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 03 Dec 2025 22:22:17 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 22:22:17 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 03 Dec 2025 22:22:17 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 03 Dec 2025 22:22:18 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 03 Dec 2025 22:23:17 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729344b6db60e029cbcc5ef912d5e5debcd7c143dafbbe8c4f8b0b91566586f`  
		Last Modified: Mon, 01 Dec 2025 21:55:05 GMT  
		Size: 12.2 MB (12219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42d5a423a4f18d1f72410a67936ebbce038aea374d6b26269ed658d21d8f3e0`  
		Last Modified: Mon, 01 Dec 2025 21:56:56 GMT  
		Size: 54.4 MB (54423367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ede27f75c2972e60b04231060706a31e061bf6d324be517f4cfb9e297be56d`  
		Last Modified: Mon, 01 Dec 2025 21:56:50 GMT  
		Size: 4.7 MB (4703664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73582b95172caa088cf081bd07d6aeeed64862287ca6019eff7f6ed0cd69697e`  
		Last Modified: Wed, 03 Dec 2025 21:52:53 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95f0e691ec9a0f8a3284ea1f62993e4397f0aea0a48c947ad2bf6ce3a6291d`  
		Last Modified: Wed, 03 Dec 2025 21:53:00 GMT  
		Size: 18.0 MB (18035864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771af7e8faa0e15ba9182ca79a9c8a0ccc276c41f36ad4ac29c983e5e6a7631a`  
		Last Modified: Wed, 03 Dec 2025 21:52:53 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66ecbefe8793ca350a025c3bc012fee44044ce5c0fbff95ec033d468735503d`  
		Last Modified: Wed, 03 Dec 2025 21:52:53 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb309397306e3f2732ac4fdf6bd811af91bdd115cd44aaa8be2fe3ce1aac7e3`  
		Last Modified: Wed, 03 Dec 2025 21:52:53 GMT  
		Size: 14.1 KB (14115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b230d37d5ec2996fb046bfde739246ed2b9b45700a9ef51919ea6a4ff045d8b8`  
		Last Modified: Wed, 03 Dec 2025 21:52:53 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93f1bae7e7ccae218f491f56acd0e2b68d4d107df8e5be5bcf2ccaef8e2025`  
		Last Modified: Wed, 03 Dec 2025 21:52:53 GMT  
		Size: 15.0 KB (14999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18ac3fe3fbcf7c61183202baea85f7711ccc9610a9610402f603b18beaa5502`  
		Last Modified: Wed, 03 Dec 2025 21:52:53 GMT  
		Size: 2.9 MB (2930879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8026031d12024176a0d561d749baf37369206cad6f6366e707ddee588700f821`  
		Last Modified: Wed, 03 Dec 2025 22:24:27 GMT  
		Size: 367.2 MB (367203451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b1baa1555ead946641fd927ee5e9d701a9ea8585a1db1dec0de53f475ca311`  
		Last Modified: Wed, 03 Dec 2025 22:24:34 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e6afcbeb863064642f3ffa827eef0c0814acff9ec753e488151ce17783c0`  
		Last Modified: Wed, 03 Dec 2025 22:24:34 GMT  
		Size: 16.3 MB (16292147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:066bf3a46ce22224b73c14548525d24a464a5e231f84ec2da54598b275fd9ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5966403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24b5bafe28acc882ec4eb42bddfb7be2e923e4b79c32003dc25057585a972d9`

```dockerfile
```

-	Layers:
	-	`sha256:4e23cc4780ecf3274da75c84e3be0f115cfef20d4e52350684fcf191f0f488a1`  
		Last Modified: Thu, 04 Dec 2025 01:22:10 GMT  
		Size: 5.9 MB (5946772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f59e4ca7d2682a814fdde7cc9447413d8809014b273924fd1a934b082c7a86`  
		Last Modified: Thu, 04 Dec 2025 01:22:11 GMT  
		Size: 19.6 KB (19631 bytes)  
		MIME: application/vnd.in-toto+json
