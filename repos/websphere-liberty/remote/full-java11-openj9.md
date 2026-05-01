## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:7ae49e39fa7fe55326dfd6f6da3444a4c915f5635b006a53ea864363348b93eb
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
$ docker pull websphere-liberty@sha256:6b3ceb56c8e09ce8a890294c28dbd147d29ad0aa7804c48aa3078172c91183d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.6 MB (507625365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b326b272df59a3ae4fa4d953b08c46b4173ce1ada71a7b5181b6e3a0393652c5`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:44:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:44:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:44:55 GMT
ENV JAVA_VERSION=11.0.31.0
# Thu, 30 Apr 2026 23:44:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='587138f9b489026d0e9b733f5de5fe061079b59029993f7bf99ae8c79fcbce2d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_aarch64_linux_11.0.31.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b9b997d087549d7c9f054c1b755b13017dafccd21ab18a6f53fe856e2f83f20e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_ppc64le_linux_11.0.31.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e51820d8cb2f47c57d625943d0d65c0f2d10a06d88d6626fa7fa00fe4c1ecd44';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_x64_linux_11.0.31.0.tar.gz';          ;;        s390x)          ESUM='41ebc50a449603e813320c917f9ad66b26bbbbbd3a3ff32e8985e264b9115993';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_s390x_linux_11.0.31.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:44:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:44:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:46:00 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:15:31 GMT
USER root
# Fri, 01 May 2026 00:15:31 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:15:31 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:15:31 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 01 May 2026 00:15:31 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:15:31 GMT
ARG LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
# Fri, 01 May 2026 00:15:31 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.3 org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.3 com.ibm.websphere.liberty.version=26.0.0.3
# Fri, 01 May 2026 00:15:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 01 May 2026 00:15:31 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.3 BuildLabel=cl260320260309-1102
# Fri, 01 May 2026 00:15:31 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:15:31 GMT
ARG LIBERTY_URL
# Fri, 01 May 2026 00:15:31 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 01 May 2026 00:15:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:15:45 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 01 May 2026 00:15:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:15:45 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 01 May 2026 00:15:45 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 01 May 2026 00:15:45 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 01 May 2026 00:15:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:15:50 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 01 May 2026 00:15:50 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:15:50 GMT
USER 1001
# Fri, 01 May 2026 00:15:50 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:15:50 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:15:50 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 01 May 2026 01:24:40 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 01:24:40 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 01 May 2026 01:24:40 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 01 May 2026 01:24:41 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 01 May 2026 01:25:04 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855cf1f0ba4ff0e4e5105a883ec8fbe77e3ec7cdda83d219915ac27ccad64291`  
		Last Modified: Thu, 30 Apr 2026 23:46:12 GMT  
		Size: 12.8 MB (12805328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e17f1bc1581fcccb623dd0971b6dba127d74855effcb97a2575d2c017226356`  
		Last Modified: Thu, 30 Apr 2026 23:46:13 GMT  
		Size: 56.3 MB (56280537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e7c69ca9cef45d8929a714d2bdb7abdae76f6cae19381492e5741e66ca160d`  
		Last Modified: Thu, 30 Apr 2026 23:46:12 GMT  
		Size: 4.5 MB (4450238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ad457b908373ba5c2fef6a016e475cf9617a7d0eabb50be0a27c6f10fb7d62`  
		Last Modified: Fri, 01 May 2026 00:15:58 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf057486a46b6f14dddcdade644a24850fba5bff697d9a279c4115e87af22376`  
		Last Modified: Fri, 01 May 2026 00:15:59 GMT  
		Size: 17.8 MB (17838685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31468c0ee61ff443695ec40fac5914cc36108ec701c0d5c16026b611d29bf698`  
		Last Modified: Fri, 01 May 2026 00:15:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603d7a846c89daa2fe3f636385b135e8420f5c8be07b3b674477bb62c7900a4b`  
		Last Modified: Fri, 01 May 2026 00:15:58 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff2e1499faa3586171d5b46a1589e0d0c55bb4cf00578a04dc305e4380eece`  
		Last Modified: Fri, 01 May 2026 00:15:59 GMT  
		Size: 14.1 KB (14115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9a11c1ce272582dff3cfd928b86f72bb3e1d0f335c7a60537d3bce0653ec5`  
		Last Modified: Fri, 01 May 2026 00:15:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eca86bdd7537507da4938a737424bab1356454d33f66780156d23ac1b65d1a6`  
		Last Modified: Fri, 01 May 2026 00:15:59 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40d09eb2f826db91289cb8882b97a02a86b9f8b14bb150904ce4035b7551c5d`  
		Last Modified: Fri, 01 May 2026 00:16:00 GMT  
		Size: 2.8 MB (2810280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0e7fb4d989e242f425fb745605430dc047cb9ffd37d0e230b697fca5c96729`  
		Last Modified: Fri, 01 May 2026 01:25:39 GMT  
		Size: 368.0 MB (367993016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac432bcb390690e7eae5f55c7522c8247808f2e44e62faea68d9188c2b7b58f`  
		Last Modified: Fri, 01 May 2026 01:25:31 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed78ff301cea78f9c1ca1f8a596b7562ae44cffe3911a6fd2507633b7eaee64`  
		Last Modified: Fri, 01 May 2026 01:25:32 GMT  
		Size: 15.7 MB (15650265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e9127d981826380bd1c2149883d36ad258e95b263b490cd5eba0985c4d8eabce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5408069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9d21ab68091659d1e83b22947476144116964533297613320721cfdee35074`

```dockerfile
```

-	Layers:
	-	`sha256:2260cd0e88df21d2fd3b2c2fd5c7d4543d4bda380fc765404eac15e940d74c0b`  
		Last Modified: Fri, 01 May 2026 01:25:31 GMT  
		Size: 5.4 MB (5388474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5efca94843ff863f23ee0ef0f3452efd196ab84a04a52ffa6e8360ffa624a4`  
		Last Modified: Fri, 01 May 2026 01:25:31 GMT  
		Size: 19.6 KB (19595 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:f215b417d84693d004b534d88809cebc4fb1e232e953d4dd67264262dc8cb85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503862699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cd021d0f911d4358ffc6b2708d054cf9d282f5d107cb1960a469683e4a4f13`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Apr 2026 23:44:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:44:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:44:51 GMT
ENV JAVA_VERSION=11.0.31.0
# Thu, 30 Apr 2026 23:44:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='587138f9b489026d0e9b733f5de5fe061079b59029993f7bf99ae8c79fcbce2d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_aarch64_linux_11.0.31.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b9b997d087549d7c9f054c1b755b13017dafccd21ab18a6f53fe856e2f83f20e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_ppc64le_linux_11.0.31.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e51820d8cb2f47c57d625943d0d65c0f2d10a06d88d6626fa7fa00fe4c1ecd44';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_x64_linux_11.0.31.0.tar.gz';          ;;        s390x)          ESUM='41ebc50a449603e813320c917f9ad66b26bbbbbd3a3ff32e8985e264b9115993';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_s390x_linux_11.0.31.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:44:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:45:56 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:15:12 GMT
USER root
# Fri, 01 May 2026 00:15:12 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:15:12 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:15:12 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 01 May 2026 00:15:12 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:15:12 GMT
ARG LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
# Fri, 01 May 2026 00:15:12 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.3 org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.3 com.ibm.websphere.liberty.version=26.0.0.3
# Fri, 01 May 2026 00:15:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 01 May 2026 00:15:12 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.3 BuildLabel=cl260320260309-1102
# Fri, 01 May 2026 00:15:12 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:15:12 GMT
ARG LIBERTY_URL
# Fri, 01 May 2026 00:15:12 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 01 May 2026 00:15:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:15:30 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 01 May 2026 00:15:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:15:30 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 01 May 2026 00:15:30 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 01 May 2026 00:15:30 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 01 May 2026 00:15:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:15:35 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 01 May 2026 00:15:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:15:35 GMT
USER 1001
# Fri, 01 May 2026 00:15:35 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:15:35 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:15:35 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 01 May 2026 01:24:26 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 01:24:26 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 01 May 2026 01:24:26 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 01 May 2026 01:24:26 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 01 May 2026 01:24:52 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d42e71012d312a9431aa7e2e2e34a8e7e4da5cb5839bb027d2af2f4444749`  
		Last Modified: Thu, 30 Apr 2026 23:46:10 GMT  
		Size: 12.8 MB (12837772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcc198b8f4a0775d430689bdb0c3322cb808afb1a3943368ff9af3a5444ed55`  
		Last Modified: Thu, 30 Apr 2026 23:46:11 GMT  
		Size: 54.2 MB (54232415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbb232c2a5782022573c4323506af92d11b2b941f2181fbffdb0fa3eeab80b4`  
		Last Modified: Thu, 30 Apr 2026 23:46:09 GMT  
		Size: 4.3 MB (4281113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e038baa2be55856bda273cb07edec91122903c831b8f9cb715d3e134eb8fd`  
		Last Modified: Fri, 01 May 2026 00:15:43 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4f68bb90062c639836f7cdb83511df69624d8dc0e8cfa4484a240ca25bfef8`  
		Last Modified: Fri, 01 May 2026 00:15:43 GMT  
		Size: 17.8 MB (17838891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e78db81aff993e535b2ba324183fed1d72cfbb4f9630a5d26e8b4a83ff5551`  
		Last Modified: Fri, 01 May 2026 00:15:43 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416e9051b954087142d054567edb237cf4bac2989811b2c2d63923d895e772bf`  
		Last Modified: Fri, 01 May 2026 00:15:43 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8525824bde6842e4daba4ad12749c664f27fcd03f67fdbea7b9cbb6e06ec3305`  
		Last Modified: Fri, 01 May 2026 00:15:44 GMT  
		Size: 14.1 KB (14115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ba85f96cfbb0c5d4fdf71e60a639b5a284865af02b28646e5017fa6606e095`  
		Last Modified: Fri, 01 May 2026 00:15:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c2c31e77d23dcfbde92fc6858e3ebf38b66e064223d686d190337487146179`  
		Last Modified: Fri, 01 May 2026 00:15:44 GMT  
		Size: 15.0 KB (14975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd79db828f1b22e2442ff7bd9e4827b7a2a5071db54f50dccda7afd4b28f30f0`  
		Last Modified: Fri, 01 May 2026 00:15:45 GMT  
		Size: 2.8 MB (2840165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a320cf20955eba8634e2bbd93874e3361b3e1aa031d562bcff7a10069e9deb7`  
		Last Modified: Fri, 01 May 2026 01:25:27 GMT  
		Size: 368.0 MB (367993363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95429ee0427c0f8eaca2487c00bac0c1178f66eebe2acecf321b799949f54e`  
		Last Modified: Fri, 01 May 2026 01:25:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e45df978b34a6b4734ee3056c92fbe8a1082d43af0a8d84bf6f2395796cea65`  
		Last Modified: Fri, 01 May 2026 01:25:20 GMT  
		Size: 14.9 MB (14888589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f1e4cd64ccb4631a6964d4ac1609047e3fb5cf82d7b56c4e37432a4b8e14d23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1258f940a26b5413d55ae3a3d0934991348e9bc2c04ce9efddfceb52fb039ae5`

```dockerfile
```

-	Layers:
	-	`sha256:6397d52999b6e343a4c8f4f74e3425ea7b0018530b5ef52201353e9563063055`  
		Last Modified: Fri, 01 May 2026 01:25:19 GMT  
		Size: 5.4 MB (5387004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68e92b738256192e17ab5bab8a5537e68bfd341313e4fc030d7c94690fe2b8f4`  
		Last Modified: Fri, 01 May 2026 01:25:19 GMT  
		Size: 19.7 KB (19678 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:843af965defb74f293f237237b3341bca4e8622c7ee6a1479eab97e9b9557b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.0 MB (512014897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d09d81e357f4d0a420dff96f361445156044a0ff93773c9bd503a0f83dce6e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:39:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:39:02 GMT
ENV JAVA_VERSION=11.0.31.0
# Thu, 30 Apr 2026 23:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='587138f9b489026d0e9b733f5de5fe061079b59029993f7bf99ae8c79fcbce2d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_aarch64_linux_11.0.31.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b9b997d087549d7c9f054c1b755b13017dafccd21ab18a6f53fe856e2f83f20e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_ppc64le_linux_11.0.31.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e51820d8cb2f47c57d625943d0d65c0f2d10a06d88d6626fa7fa00fe4c1ecd44';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_x64_linux_11.0.31.0.tar.gz';          ;;        s390x)          ESUM='41ebc50a449603e813320c917f9ad66b26bbbbbd3a3ff32e8985e264b9115993';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_s390x_linux_11.0.31.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:47:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:47:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:48:16 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:40:35 GMT
USER root
# Fri, 01 May 2026 00:40:35 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:40:35 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:40:35 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 01 May 2026 00:40:35 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:40:35 GMT
ARG LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
# Fri, 01 May 2026 00:40:35 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.3 org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.3 com.ibm.websphere.liberty.version=26.0.0.3
# Fri, 01 May 2026 00:40:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 01 May 2026 00:40:35 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.3 BuildLabel=cl260320260309-1102
# Fri, 01 May 2026 00:40:35 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:40:35 GMT
ARG LIBERTY_URL
# Fri, 01 May 2026 00:40:35 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 01 May 2026 00:41:18 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:41:18 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 01 May 2026 00:41:19 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:41:19 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 01 May 2026 00:41:20 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 01 May 2026 00:41:20 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 01 May 2026 00:41:22 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:41:33 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 01 May 2026 00:41:33 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:41:33 GMT
USER 1001
# Fri, 01 May 2026 00:41:33 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:41:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:41:33 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 01 May 2026 01:27:51 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 01:27:51 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 01 May 2026 01:27:51 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 01 May 2026 01:27:57 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 01 May 2026 01:28:53 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccf3833ba70e5f487e107c0fc757f71c24195588839e7b794b482f819b1bf2d`  
		Last Modified: Wed, 15 Apr 2026 21:40:36 GMT  
		Size: 13.8 MB (13788494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08a61d045a66c408bcb49853bf52b4b7081d86b2de6cf76fe6c85bb79d59857`  
		Last Modified: Thu, 30 Apr 2026 23:48:41 GMT  
		Size: 58.2 MB (58237260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0aa9d26a1cd683ff21eeadbfd0e70cf336ccf821815f62aced4a13850786e3`  
		Last Modified: Thu, 30 Apr 2026 23:48:40 GMT  
		Size: 3.5 MB (3495351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52f55cb5acf630b9a8d8b55d253e6204db9524a22ebdcbf0339103f9296f3f7`  
		Last Modified: Fri, 01 May 2026 00:42:07 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167c8efb8720b23a0cd67b9ff94682676432325957046b5f12c5fcb4c2744c12`  
		Last Modified: Fri, 01 May 2026 00:42:08 GMT  
		Size: 17.8 MB (17839127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f2e842de4626fc8789afbb7700bcf989813770325de0ab4b71d0adbc2565bf`  
		Last Modified: Fri, 01 May 2026 00:42:07 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff760f554f6c231c5e9597d06fac621b5e7cd66ffe32a094f0d9136797d3f6e`  
		Last Modified: Fri, 01 May 2026 00:42:08 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbb07a3040723db2bb7ed3877f592cf8037647ac24462c6c495445b398f0fd`  
		Last Modified: Fri, 01 May 2026 00:42:09 GMT  
		Size: 14.1 KB (14117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0a70516f4ef0e1c2a25a74695313ca5f526437a64af40c10eabe733f976864`  
		Last Modified: Fri, 01 May 2026 00:42:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ae1f303a39cf79fc3699cfcd04640a74d11ab5bb8fadf3c8d6619bb2cda504`  
		Last Modified: Fri, 01 May 2026 00:42:09 GMT  
		Size: 15.0 KB (14986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b8efc5b106c967dad6ee02572acda5d03e7806ea8cd17423798a40aa7154f5`  
		Last Modified: Fri, 01 May 2026 00:42:10 GMT  
		Size: 2.7 MB (2720331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683fe28310d7b53b287c3c497c706343a3412070eab5e731d8cb59c7a217e8a`  
		Last Modified: Fri, 01 May 2026 01:29:53 GMT  
		Size: 368.0 MB (367993031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a29512f9bc26fc32242429fef4f605d647c9e46b6d0e62def28f6eabded3a7d`  
		Last Modified: Fri, 01 May 2026 01:29:45 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21532720a31e54df4f96c520edbd205da41d8bc9c0246378ba683de1a332ee60`  
		Last Modified: Fri, 01 May 2026 01:29:46 GMT  
		Size: 13.6 MB (13558326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:6231d30660388eb6ddca148713c687806b57e7cf83ca220104122bc3531b9b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d776fd157f08a71a99cb52048d10cf39e8496a4a9507ef314a5f0042042aec`

```dockerfile
```

-	Layers:
	-	`sha256:0e388ae5402d11148e41182042f73787a9f9f080456abe2d3edc3ece3092137a`  
		Last Modified: Fri, 01 May 2026 01:29:45 GMT  
		Size: 5.4 MB (5393096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f33ce8df86f8f434a822152488932e032c0f9a64f28deb20061309cbfcb062`  
		Last Modified: Fri, 01 May 2026 01:29:45 GMT  
		Size: 19.6 KB (19622 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ff205240667442c63b335a03e6b4c3379cc9880f91b7ff9e256e5ddb4cce9e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.4 MB (510395285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a56c07089cd840879f652881bab751adba51e7ae43df1e758c9f4f0055587b3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:55:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:55:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:19 GMT
ENV JAVA_VERSION=11.0.31.0
# Fri, 01 May 2026 04:19:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='587138f9b489026d0e9b733f5de5fe061079b59029993f7bf99ae8c79fcbce2d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_aarch64_linux_11.0.31.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b9b997d087549d7c9f054c1b755b13017dafccd21ab18a6f53fe856e2f83f20e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_ppc64le_linux_11.0.31.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e51820d8cb2f47c57d625943d0d65c0f2d10a06d88d6626fa7fa00fe4c1ecd44';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_x64_linux_11.0.31.0.tar.gz';          ;;        s390x)          ESUM='41ebc50a449603e813320c917f9ad66b26bbbbbd3a3ff32e8985e264b9115993';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_s390x_linux_11.0.31.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 May 2026 04:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 04:19:38 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 May 2026 04:20:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 05:11:12 GMT
USER root
# Fri, 01 May 2026 05:11:12 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 05:11:12 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 05:11:12 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 01 May 2026 05:11:12 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 05:11:12 GMT
ARG LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
# Fri, 01 May 2026 05:11:12 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.3 org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.3 com.ibm.websphere.liberty.version=26.0.0.3
# Fri, 01 May 2026 05:11:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 01 May 2026 05:11:12 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.3 BuildLabel=cl260320260309-1102
# Fri, 01 May 2026 05:11:12 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 05:11:12 GMT
ARG LIBERTY_URL
# Fri, 01 May 2026 05:11:12 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 01 May 2026 05:11:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 05:11:24 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 01 May 2026 05:11:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 05:11:24 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 01 May 2026 05:11:24 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 01 May 2026 05:11:24 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 01 May 2026 05:11:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 05:11:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.3 LIBERTY_BUILD_LABEL=cl260320260309-1102 LIBERTY_SHA=451c872ecc18593142c1fd45aa29f4191d5c23d4 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 01 May 2026 05:11:30 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 05:11:30 GMT
USER 1001
# Fri, 01 May 2026 05:11:30 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 05:11:30 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 05:11:30 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 01 May 2026 05:35:39 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 05:35:39 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 01 May 2026 05:35:39 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 01 May 2026 05:35:39 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 01 May 2026 05:36:05 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1dca01c7f8a5c02c033ddd80e1849e4d2dce0090b72e585925cee97f083f26`  
		Last Modified: Wed, 15 Apr 2026 20:56:59 GMT  
		Size: 13.1 MB (13117391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743013867de7f4a1fc79d77bf36472a366d9ced49e2d3eb4d0aa697c129ce394`  
		Last Modified: Fri, 01 May 2026 04:21:03 GMT  
		Size: 58.4 MB (58400840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581e218fbdbd99269133a85a10601d3fceea4860e77fe66a2c2c17adf14dbce9`  
		Last Modified: Fri, 01 May 2026 04:21:03 GMT  
		Size: 4.6 MB (4608341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ac2a3e46d6fb8c7eaadf4d1b4a9cb4bd1814470db29a9a04bee68e10737f3d`  
		Last Modified: Fri, 01 May 2026 05:11:43 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aef13dfdfbc0e524e994d261835ed1f719c6f294d949c4ca535bb199ee4cd9a`  
		Last Modified: Fri, 01 May 2026 05:11:43 GMT  
		Size: 17.8 MB (17838532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74b9d168b97eea150868096f0a5afcb5128d0f0a1e265b0e4742ab09d911b28`  
		Last Modified: Fri, 01 May 2026 05:11:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462044b63c14490e32ef4ca5213409cf46a88aa30775f0251996846b171cfa48`  
		Last Modified: Fri, 01 May 2026 05:11:43 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47cd7c7559e515f80335df973700680f14330dc060c35baed5c63de6d1b1a36`  
		Last Modified: Fri, 01 May 2026 05:11:44 GMT  
		Size: 14.1 KB (14116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c173688027f6707b159aa88ad84582bffd44d52ea7dc21f524f83c0d1cf4045d`  
		Last Modified: Fri, 01 May 2026 05:11:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faa94884fc3996b80b3b06f810873901d6cdc61e02503a9d5c402370251615c`  
		Last Modified: Fri, 01 May 2026 05:11:44 GMT  
		Size: 15.0 KB (14984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896a7d1e33e17c09fb36a7715aeffcfd7da3e64db0e37e662d6dbf7b8ec2dc6d`  
		Last Modified: Fri, 01 May 2026 05:11:45 GMT  
		Size: 2.9 MB (2859294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cda963f771cd0671490ac00a29700866e58e9f2686c0e108fb2c7eb2055d381`  
		Last Modified: Fri, 01 May 2026 05:36:55 GMT  
		Size: 368.0 MB (367992751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de61b7af12326bbb72a29262d4570aecfac3122a4c10f91d071d0f2bb76f06d6`  
		Last Modified: Fri, 01 May 2026 05:36:48 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9424d8907699e1808b8def3c87ff2ba3ae510526bc83636c65e11ec1775e770`  
		Last Modified: Fri, 01 May 2026 05:36:49 GMT  
		Size: 15.6 MB (15600585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c1bb5aef7dc079686dcfab9445a6a8b77303c42766062982b0ebc530dee9805c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5409065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff8a9a344da228a9ed961d95ea4db17fc791c8de3df7f2bce10c31a7fbbb1e1`

```dockerfile
```

-	Layers:
	-	`sha256:7d6ac3d28ef3bda9f7bf46ceee60bafecc3cc0cc64e46d99f37e5a7755190d4a`  
		Last Modified: Fri, 01 May 2026 05:36:50 GMT  
		Size: 5.4 MB (5389471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff246758d82dacd974e5e702b68abcf94f37eb827ca42e25471f5b9b9e5892a2`  
		Last Modified: Fri, 01 May 2026 05:36:49 GMT  
		Size: 19.6 KB (19594 bytes)  
		MIME: application/vnd.in-toto+json
