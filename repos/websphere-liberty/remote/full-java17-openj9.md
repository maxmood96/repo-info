## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:d498e457489ace1d1ecd8c544b30b87d0ddbad1ce57cf2388ee1ed8d9cf641d2
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
$ docker pull websphere-liberty@sha256:6e946fdc266d3c3ccd490a20ee0ceb7cf731925e79ef28f443915a3f45044632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.2 MB (530223366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54695d291a5b86eaca45d261a179710a9116d63d4f140bd5164178f55c2e5117`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:17:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:17:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:17:06 GMT
ENV JAVA_VERSION=17.0.19.0
# Tue, 02 Jun 2026 08:17:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 08:17:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:17:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 02 Jun 2026 08:18:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 02 Jun 2026 09:21:10 GMT
USER root
# Tue, 02 Jun 2026 09:21:10 GMT
ARG VERBOSE=false
# Tue, 02 Jun 2026 09:21:10 GMT
ARG OPENJ9_SCC=true
# Tue, 02 Jun 2026 09:21:10 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Tue, 02 Jun 2026 09:21:10 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Tue, 02 Jun 2026 09:21:10 GMT
ARG LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
# Tue, 02 Jun 2026 09:21:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.5 org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.5 com.ibm.websphere.liberty.version=26.0.0.5
# Tue, 02 Jun 2026 09:21:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 02 Jun 2026 09:21:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.5 BuildLabel=cl260520260430-1602
# Tue, 02 Jun 2026 09:21:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 02 Jun 2026 09:21:10 GMT
ARG LIBERTY_URL
# Tue, 02 Jun 2026 09:21:10 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 02 Jun 2026 09:21:22 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:21:22 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 02 Jun 2026 09:21:22 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 02 Jun 2026 09:21:22 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 02 Jun 2026 09:21:22 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 02 Jun 2026 09:21:22 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 02 Jun 2026 09:21:23 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 02 Jun 2026 09:21:27 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 02 Jun 2026 09:21:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 02 Jun 2026 09:21:27 GMT
USER 1001
# Tue, 02 Jun 2026 09:21:27 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 02 Jun 2026 09:21:27 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 02 Jun 2026 09:21:27 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 02 Jun 2026 10:30:53 GMT
ARG VERBOSE=false
# Tue, 02 Jun 2026 10:30:53 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 02 Jun 2026 10:30:53 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 02 Jun 2026 10:30:53 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 02 Jun 2026 10:31:17 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b5d6f00342a36a2b51a6a277f0347aa1a121e89897007764016d44ee9a3f6f`  
		Last Modified: Tue, 02 Jun 2026 08:18:26 GMT  
		Size: 12.8 MB (12807987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336b5f157fcbdbbbba7a7abbb7d54e82128ef0f0fc64dcea667c32fad101bfda`  
		Last Modified: Tue, 02 Jun 2026 08:18:27 GMT  
		Size: 56.1 MB (56093688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da0427ffbab629edb50d7544fc7c0c744b208a34e17c49d019887874468eff5`  
		Last Modified: Tue, 02 Jun 2026 08:18:26 GMT  
		Size: 5.1 MB (5066585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac98d72c60840e70d23480794f4ca6ba1dcfddb87f59b40c9527c925d3c5ae2`  
		Last Modified: Tue, 02 Jun 2026 09:21:36 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9baf1a41113acd3af61e9759c646ede635359e7a715b6f6a6ffeb2beea9930f`  
		Last Modified: Tue, 02 Jun 2026 09:21:36 GMT  
		Size: 18.1 MB (18114117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62831d2120d97e7c75193a127387400664bce9b21459660361ad2812d56921d`  
		Last Modified: Tue, 02 Jun 2026 09:21:36 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64fa03b59d6fee89c038d4d22b0ca8a6c41842c9c94b5b0e246f91391d740a7`  
		Last Modified: Tue, 02 Jun 2026 09:21:36 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20926da256bb622ee089d9c9f1c269c7c92bf2ade0c5134af2bfeac68ca5f7f9`  
		Last Modified: Tue, 02 Jun 2026 09:21:37 GMT  
		Size: 14.2 KB (14180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61f79d0ab5464d3447c4e577151de8228f8114fe100690257e6243bed872f62`  
		Last Modified: Tue, 02 Jun 2026 09:21:37 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688b27963af74dbe92083f4b1d6b9ad169a97a78afe3c2c3c7edfd94e10a20c0`  
		Last Modified: Tue, 02 Jun 2026 09:21:37 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc912c8734224003b73af7f21f7585ff650fb4af9de8b87312ff946a50efe7cd`  
		Last Modified: Tue, 02 Jun 2026 09:21:38 GMT  
		Size: 2.8 MB (2764744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc14cf6fdffe48999bfe26767da3825c2eb8ce59b556417a0d56a1c26c774441`  
		Last Modified: Tue, 02 Jun 2026 10:31:52 GMT  
		Size: 389.7 MB (389676648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba1b196d1fea40c6b0ae9328f1de5e4dd893ecc2b991f9fb4241267d48ffec`  
		Last Modified: Tue, 02 Jun 2026 10:31:44 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16ed0efaaf5d14df48f7a122c593da7c819a7e01e0d4499cd7525b3f95343b`  
		Last Modified: Tue, 02 Jun 2026 10:31:45 GMT  
		Size: 15.9 MB (15902622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:bb9df2e5c620abb26a6fe719b1cdc4ad1c86f9422c1976035094a529a38be48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5de97805132bc70e64fc1889b8ce3ecdc2bf27fd1bc8b6d4922dc90b0d9fb50`

```dockerfile
```

-	Layers:
	-	`sha256:19e309414fc1e02dd39c723a9ad1c65a90088a71409ec9c9539b44238837a90b`  
		Last Modified: Tue, 02 Jun 2026 10:31:44 GMT  
		Size: 5.4 MB (5426727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8fc93e0422b1df326fc80c301355e62cc1894d8db6055914bb42725458e94d`  
		Last Modified: Tue, 02 Jun 2026 10:31:44 GMT  
		Size: 19.6 KB (19595 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:3ec78eb47e857bf1a91992cae2f116c86ed08e35bc772ffd0b7f20e389ab3f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.4 MB (526371426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23150d5f0a8b07e20268ec359f79ef32252ee8674a91f01c9fbff02787d05126`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:18:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:18:07 GMT
ENV JAVA_VERSION=17.0.19.0
# Tue, 02 Jun 2026 08:18:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 08:18:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:18:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 02 Jun 2026 08:19:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 02 Jun 2026 09:30:25 GMT
USER root
# Tue, 02 Jun 2026 09:30:25 GMT
ARG VERBOSE=false
# Tue, 02 Jun 2026 09:30:25 GMT
ARG OPENJ9_SCC=true
# Tue, 02 Jun 2026 09:30:25 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Tue, 02 Jun 2026 09:30:25 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Tue, 02 Jun 2026 09:30:25 GMT
ARG LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
# Tue, 02 Jun 2026 09:30:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.5 org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.5 com.ibm.websphere.liberty.version=26.0.0.5
# Tue, 02 Jun 2026 09:30:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 02 Jun 2026 09:30:25 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.5 BuildLabel=cl260520260430-1602
# Tue, 02 Jun 2026 09:30:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 02 Jun 2026 09:30:25 GMT
ARG LIBERTY_URL
# Tue, 02 Jun 2026 09:30:25 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 02 Jun 2026 09:30:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 09:30:37 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 02 Jun 2026 09:30:38 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 02 Jun 2026 09:30:38 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 02 Jun 2026 09:30:38 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 02 Jun 2026 09:30:38 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 02 Jun 2026 09:30:38 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 02 Jun 2026 09:30:43 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 02 Jun 2026 09:30:43 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 02 Jun 2026 09:30:43 GMT
USER 1001
# Tue, 02 Jun 2026 09:30:43 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 02 Jun 2026 09:30:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 02 Jun 2026 09:30:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 02 Jun 2026 10:27:41 GMT
ARG VERBOSE=false
# Tue, 02 Jun 2026 10:27:41 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 02 Jun 2026 10:27:41 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 02 Jun 2026 10:27:42 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 02 Jun 2026 10:28:08 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e036a8199c39bf056939c5937985c6b0707122ac6d915b19df1d532466ba215`  
		Last Modified: Tue, 02 Jun 2026 08:19:26 GMT  
		Size: 12.8 MB (12841948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9f96a728a0be53cf12bd82c5b69eb3f175a70934791041115e8cff41fb46e3`  
		Last Modified: Tue, 02 Jun 2026 08:19:27 GMT  
		Size: 54.0 MB (54002698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9406974444fbbe917ff50cfd849678046f8e0a5418978ae660107d3b4a26488a`  
		Last Modified: Tue, 02 Jun 2026 08:19:26 GMT  
		Size: 4.7 MB (4744490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6b1750d67ca43f78e8b2936db3f4334a6e7430c24761810dac90dd6d8969f8`  
		Last Modified: Tue, 02 Jun 2026 09:30:51 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496375ace46b895bb3a834a7af3764386ba134b32d4d6597e46830633de2ddc1`  
		Last Modified: Tue, 02 Jun 2026 09:30:52 GMT  
		Size: 18.1 MB (18114257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3c43e2694524826cbec27365d77f9743a211f6c469a26a2349cf024e905af0`  
		Last Modified: Tue, 02 Jun 2026 09:30:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b25780c4cc2f43d4d76cba315a27e6e52192145f6f01c8a3baa10b9b2f297d9`  
		Last Modified: Tue, 02 Jun 2026 09:30:51 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecf5e576d4f671bb5f360da8ad6507cda2abae0db3d08948bd54b235dd05b8c`  
		Last Modified: Tue, 02 Jun 2026 09:30:52 GMT  
		Size: 14.2 KB (14183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fb5c50d4d0fbe4cf08cb2267149192ab56c5de83db9454d01f4d523a954d8`  
		Last Modified: Tue, 02 Jun 2026 09:30:52 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5201fd829de9ddc9b7c32aa94c10f5ff9c8936c7d32aad98258cbdee67b237da`  
		Last Modified: Tue, 02 Jun 2026 09:30:53 GMT  
		Size: 15.0 KB (15049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4e7124b026e8c5997d995111c63cafb1ae111c1bf928defecbe075f1985c78`  
		Last Modified: Tue, 02 Jun 2026 09:30:54 GMT  
		Size: 2.8 MB (2813282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d881ea74526cff477a26a8798819ed0c3c3fe520b54874e8e255bc349319c5e9`  
		Last Modified: Tue, 02 Jun 2026 10:28:45 GMT  
		Size: 389.7 MB (389676478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfa6adec303a2781e605efe6fab4d76898db1f7bc0b33c09d7d7cab34fe1dd9`  
		Last Modified: Tue, 02 Jun 2026 10:28:37 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f806f6e98c244f138c08e6b2eb0e44c551f9e71853c7ec66efa8e4b458ed9867`  
		Last Modified: Tue, 02 Jun 2026 10:28:37 GMT  
		Size: 15.2 MB (15227123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:01b83b2bd5263ec41ff7e9f6c88d1003a5411e2bdeed74c9954dee37668811b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15671af5b043f148abc1df6c5c1ea54b33ef3042e00b8ae338de3b35a0e9925e`

```dockerfile
```

-	Layers:
	-	`sha256:8f7ce7211e8553327bbacad5f14ada9bad2dd8144b44a2239dba2939e39bb3bf`  
		Last Modified: Tue, 02 Jun 2026 10:28:37 GMT  
		Size: 5.4 MB (5425257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6584e81219e1242e4dd203005b49a427dfd0f6810151e3e03a3a553fd617c59`  
		Last Modified: Tue, 02 Jun 2026 10:28:36 GMT  
		Size: 19.7 KB (19678 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:baecde3e378f51d253f23082287455ddbd32ec747177c0b84ac7e76c1fd88205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.3 MB (534267017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120e73fdb889083167022b3ac37bd6cd89bed19fb27ef7d33b3bf49009bf053d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:17:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:17:07 GMT
ENV JAVA_VERSION=17.0.19.0
# Tue, 02 Jun 2026 08:19:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 08:19:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:19:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 02 Jun 2026 08:20:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 02 Jun 2026 10:28:32 GMT
USER root
# Tue, 02 Jun 2026 10:28:32 GMT
ARG VERBOSE=false
# Tue, 02 Jun 2026 10:28:32 GMT
ARG OPENJ9_SCC=true
# Tue, 02 Jun 2026 10:28:32 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Tue, 02 Jun 2026 10:28:32 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Tue, 02 Jun 2026 10:28:32 GMT
ARG LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
# Tue, 02 Jun 2026 10:28:32 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.5 org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.5 com.ibm.websphere.liberty.version=26.0.0.5
# Tue, 02 Jun 2026 10:28:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 02 Jun 2026 10:28:32 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.5 BuildLabel=cl260520260430-1602
# Tue, 02 Jun 2026 10:28:32 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 02 Jun 2026 10:28:32 GMT
ARG LIBERTY_URL
# Tue, 02 Jun 2026 10:28:32 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 02 Jun 2026 10:28:49 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:28:49 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 02 Jun 2026 10:28:50 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 02 Jun 2026 10:28:51 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 02 Jun 2026 10:28:51 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 02 Jun 2026 10:28:51 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 02 Jun 2026 10:28:52 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 02 Jun 2026 10:29:02 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 02 Jun 2026 10:29:02 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 02 Jun 2026 10:29:02 GMT
USER 1001
# Tue, 02 Jun 2026 10:29:02 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 02 Jun 2026 10:29:02 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 02 Jun 2026 10:29:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 02 Jun 2026 11:27:05 GMT
ARG VERBOSE=false
# Tue, 02 Jun 2026 11:27:05 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 02 Jun 2026 11:27:05 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 02 Jun 2026 11:27:05 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 02 Jun 2026 11:27:49 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491c93e35a05ffe353530f7e5ceab2cc5c1254584ade6b6aa3a6c87e4fe85933`  
		Last Modified: Tue, 02 Jun 2026 08:18:45 GMT  
		Size: 13.8 MB (13792726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e620f192e02fec30fafdb536a3011a664bb7ecf9904373b2063a5e18d80128`  
		Last Modified: Tue, 02 Jun 2026 08:21:29 GMT  
		Size: 58.0 MB (58022946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdd29abbcc97ef46cd20808a3ceb018eb3ea283d5adfa5a48a36209cdd28063`  
		Last Modified: Tue, 02 Jun 2026 08:21:28 GMT  
		Size: 3.9 MB (3863961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fb5e5e224579508a55644d6381b151fb4dfcc24b67359fb287d46e8ac60b9b`  
		Last Modified: Tue, 02 Jun 2026 10:29:22 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee8a27b8e441faddc853eebcd08ffe61eabbe26c8c7bcbfd6205219e8a68e62`  
		Last Modified: Tue, 02 Jun 2026 10:29:22 GMT  
		Size: 18.1 MB (18114341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2ea53366c7ae9fce248239362a7e6f6adb3c4713ae7296cf44bf999d53891f`  
		Last Modified: Tue, 02 Jun 2026 10:29:22 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d117a9cd40ba256e70ce9289c87fb6ea9ada8c3138e89e95d3268003b168514b`  
		Last Modified: Tue, 02 Jun 2026 10:29:22 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fcb08e48e3412fc2d1cddf7d56dce923fb8b894c737f531799a39ba0d5a0fb`  
		Last Modified: Tue, 02 Jun 2026 10:29:23 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b52b6b0ceb6e12ec4a96690fdfa46569e0ac3c32e5bf8dada7bc8ec9d59b88`  
		Last Modified: Tue, 02 Jun 2026 10:29:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f46449289ddd8af9169f8239055b61ddf36f7bab682a0692701c83aa07e17e`  
		Last Modified: Tue, 02 Jun 2026 10:29:23 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb26e2d61e961ba3fedabac4174b6cd0ec9ba968e6ae3844c72f5c8541e19008`  
		Last Modified: Tue, 02 Jun 2026 10:29:24 GMT  
		Size: 2.7 MB (2716146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca33927a58bc2ab14da48d0f20c40548885db8e881b105c5dc9a6fd8c8ac160`  
		Last Modified: Tue, 02 Jun 2026 11:29:00 GMT  
		Size: 389.7 MB (389674077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea3a5369765274d8412f1aa7a5ddd8fe0b4fb15fbeb1ca453ab41c44407bf47`  
		Last Modified: Tue, 02 Jun 2026 11:28:51 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b52ce524c437f5dae3485b5f283835a019630011f2ce590babd3ae7c2bbf8`  
		Last Modified: Tue, 02 Jun 2026 11:28:52 GMT  
		Size: 13.7 MB (13699781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:b0e11dcb393cec0d0e5353b65e90f061a030b9b7b71799b6bbadb5cf7da4f6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe76c1daf44b11196035b7d9118b9bf41a2bcc458e1f0c6ccde4ae2b1f329ce8`

```dockerfile
```

-	Layers:
	-	`sha256:023f58272b77cca652d46db46f9b6300fd92a17d9b302bc73df3d04e4b7df80d`  
		Last Modified: Tue, 02 Jun 2026 11:28:51 GMT  
		Size: 5.4 MB (5431349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8712c95c420421cce13a3bf693f5277bd2cc27c46b9b0ce48b3dc05302d79888`  
		Last Modified: Tue, 02 Jun 2026 11:28:51 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:7005255a9b2c94c01af02e9f560a160bcf11800adccbca1715f6a1d2c89e2d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.4 MB (533417271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d1595cd7fca962643e49d0f8c0bef87d6916956c302cfe317639c0e0e7491e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:12:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:12:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:12:28 GMT
ENV JAVA_VERSION=17.0.19.0
# Tue, 02 Jun 2026 12:09:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 12:09:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 12:09:14 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 02 Jun 2026 12:10:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 02 Jun 2026 13:11:16 GMT
USER root
# Tue, 02 Jun 2026 13:11:16 GMT
ARG VERBOSE=false
# Tue, 02 Jun 2026 13:11:16 GMT
ARG OPENJ9_SCC=true
# Tue, 02 Jun 2026 13:11:16 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Tue, 02 Jun 2026 13:11:16 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Tue, 02 Jun 2026 13:11:16 GMT
ARG LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
# Tue, 02 Jun 2026 13:11:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=26.0.0.5 org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=26.0.0.5 com.ibm.websphere.liberty.version=26.0.0.5
# Tue, 02 Jun 2026 13:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Tue, 02 Jun 2026 13:11:16 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=26.0.0.5 BuildLabel=cl260520260430-1602
# Tue, 02 Jun 2026 13:11:16 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 02 Jun 2026 13:11:16 GMT
ARG LIBERTY_URL
# Tue, 02 Jun 2026 13:11:16 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 02 Jun 2026 13:11:27 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 13:11:27 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 02 Jun 2026 13:11:28 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 02 Jun 2026 13:11:28 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 02 Jun 2026 13:11:28 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 02 Jun 2026 13:11:28 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 02 Jun 2026 13:11:28 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 02 Jun 2026 13:11:34 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=26.0.0.5 LIBERTY_BUILD_LABEL=cl260520260430-1602 LIBERTY_SHA=0ee72713406be4ecab26ee46ab6202b606937fbf LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 02 Jun 2026 13:11:34 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 02 Jun 2026 13:11:34 GMT
USER 1001
# Tue, 02 Jun 2026 13:11:34 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 02 Jun 2026 13:11:34 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 02 Jun 2026 13:11:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 02 Jun 2026 14:22:34 GMT
ARG VERBOSE=false
# Tue, 02 Jun 2026 14:22:34 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 02 Jun 2026 14:22:34 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 02 Jun 2026 14:22:35 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 02 Jun 2026 14:23:05 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda4eabc74d921146722ef099fb63ad4a221eb7b4869e5b958d1369572dfdd8d`  
		Last Modified: Tue, 02 Jun 2026 08:13:52 GMT  
		Size: 13.1 MB (13118987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59143dc8211e5f304517025c56270235a4bf279654378325f17dc0204a116ef7`  
		Last Modified: Tue, 02 Jun 2026 12:10:39 GMT  
		Size: 58.3 MB (58298214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d6e5ecf7e9a93a26faba9b752021156d60815858ef307b8f8d1537d149e766`  
		Last Modified: Tue, 02 Jun 2026 12:10:37 GMT  
		Size: 5.2 MB (5192232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69559f8427868e9c8845e755f8f5b821cd8da0cd598ed02f8798a02027bdd63`  
		Last Modified: Tue, 02 Jun 2026 13:11:49 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df6ef983d0be2cedbcbc579c9502b5a44fec5791a9a5aece9fd171b412e28e4`  
		Last Modified: Tue, 02 Jun 2026 13:11:49 GMT  
		Size: 18.1 MB (18113872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b95e1187bfb36e44b25b58525c724a871e035a8240af12e8cd8bc630039e73a`  
		Last Modified: Tue, 02 Jun 2026 13:11:49 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6f1d3538da6a2f22d41d5fdda593afd9a39a11719fcaa3d1b93823281208b6`  
		Last Modified: Tue, 02 Jun 2026 13:11:48 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68123530adef8e06ab88ff904b1759936b0505c59628d1d7b4d9bc9a329e775f`  
		Last Modified: Tue, 02 Jun 2026 13:11:50 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708421cc9a96edec220eda0322d93937635bac68adad3d286293039e428db6f1`  
		Last Modified: Tue, 02 Jun 2026 13:11:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdc7e8bc4c6db12f57da9529e1ac43216d423931604fd609bab5713c7b0cdf0`  
		Last Modified: Tue, 02 Jun 2026 13:11:50 GMT  
		Size: 15.1 KB (15053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93869e0e41061c098b8f151907374d2fb4d18c838cdeb668f4c7459b8296b92`  
		Last Modified: Tue, 02 Jun 2026 13:11:51 GMT  
		Size: 2.8 MB (2846604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6d3fa275045c4a3ad641f622713391f82eb91e9bb7f0fec5ecd7ea77642297`  
		Last Modified: Tue, 02 Jun 2026 14:23:52 GMT  
		Size: 389.7 MB (389675326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b5ceb213328033de7b0ef6e4175ac9d5c16466e7703b119ec6d28f9be21fdc`  
		Last Modified: Tue, 02 Jun 2026 14:23:45 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8405232201b9af8770714044ca272404ddeec04e4feaf67816f3f5506510`  
		Last Modified: Tue, 02 Jun 2026 14:23:46 GMT  
		Size: 16.2 MB (16193655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:2befd9f948ca63e52868ba7ef4a32dc7b431b52fca999060f6e98a1dc19f8573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5447319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122968d71a4997cf39554263e45ed14cba28e68dc7658ca898c7985c134b9947`

```dockerfile
```

-	Layers:
	-	`sha256:5a660184b660816bc48e6bf46a41a51b42752a160e77226fec9959ab5afffc0b`  
		Last Modified: Tue, 02 Jun 2026 14:23:45 GMT  
		Size: 5.4 MB (5427724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b80c5cba0edf43e2c0a5ec9e88be6bd7a80e33dbc14592488b87238db83d0c8`  
		Last Modified: Tue, 02 Jun 2026 14:23:45 GMT  
		Size: 19.6 KB (19595 bytes)  
		MIME: application/vnd.in-toto+json
