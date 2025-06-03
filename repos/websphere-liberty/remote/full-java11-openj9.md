## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:9b64e4346b4f5ff236ee54f2c317e1aba61c7e88a20e8cf455905c1eb282420c
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
$ docker pull websphere-liberty@sha256:5dd40d43efe77c479fd42e3488728c0a1a471f0260dcc939d22b6f650f81347b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.3 MB (493335252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14118c3cef4de9fe230c29d7ca365d66d6fd076506b60b31853ee7f57181c8d3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.5 org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.5 com.ibm.websphere.liberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1aba4a94830318865573d0e54fdd738096d9fb1f25b59503c7dfbe9b8cd28e9`  
		Last Modified: Fri, 09 May 2025 17:07:38 GMT  
		Size: 12.2 MB (12172136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22da1132c6ae2a163c075a21e0e3d0161f38ed1fd9d2550b2c0ce958430920f5`  
		Last Modified: Fri, 09 May 2025 17:07:41 GMT  
		Size: 52.5 MB (52455999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b90c1a3e099b20a67ae2096d380f50ac8e1856cd2ce472d3834b1b160350dac`  
		Last Modified: Fri, 09 May 2025 17:07:37 GMT  
		Size: 4.5 MB (4466313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168419789ba12b63393fa946986083017ced7dd3dc41b3bbb1a83971ef9251fd`  
		Last Modified: Tue, 03 Jun 2025 15:29:28 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33942765fac9318146371cbc147b03201eb5ef41c23fde4cda6a189128078f37`  
		Last Modified: Tue, 03 Jun 2025 15:29:29 GMT  
		Size: 17.6 MB (17561070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c20065ea83d1b54f9bfe04d85636076d6e88f11ca3b5f01635e4dbe12a42f2`  
		Last Modified: Tue, 03 Jun 2025 15:29:28 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2115fbd8cb1c168cf13a5c6c7646017e901ba6d4ee62b77cd74bc050ae26ea`  
		Last Modified: Tue, 03 Jun 2025 15:29:29 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38872ff70331aacdb734a4321018416fbf358942f4fb953ce1437665a3dde888`  
		Last Modified: Tue, 03 Jun 2025 15:29:29 GMT  
		Size: 12.3 KB (12311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a320ec9e8a08b70432c8f1b8e62c10626bf0bbfe9bad88d326e64bd3e750b89`  
		Last Modified: Tue, 03 Jun 2025 15:29:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b281b6805c79fa6e40b74c277e606f9a8983314453b443decdced6bcc82752a`  
		Last Modified: Tue, 03 Jun 2025 15:29:31 GMT  
		Size: 13.1 KB (13114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dba8f27c7ba29a72074b81367407b22c0cb805c70182beb64115b1a5882ca25`  
		Last Modified: Tue, 03 Jun 2025 15:29:32 GMT  
		Size: 2.8 MB (2793051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c309ed1d81837632ac44b3149d74c4e93dad4e197baacabf757a26c3bea9d4`  
		Last Modified: Tue, 03 Jun 2025 15:39:48 GMT  
		Size: 358.6 MB (358571453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ef7955540956c18a9ed74405698348659dc099381a969495922e28df1f4d9`  
		Last Modified: Tue, 03 Jun 2025 15:39:09 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb5ad30d9773999dcf1e497c33ff81b45d7ba5fcdc67f1ec31190b4bd56f869`  
		Last Modified: Tue, 03 Jun 2025 15:39:11 GMT  
		Size: 15.7 MB (15722253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:6a0aed28cc0e99d3837ed98e61a9f7ca12c513a8d7e20eb7c8b98e9439cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fff38b87ee990afc285f08fec2febf2987966e79e8a47910173e2e183881ee`

```dockerfile
```

-	Layers:
	-	`sha256:f9fb598a4ae27d104d9f488a56b882b5c19a8e03c612d9e3cc968005417ce7ed`  
		Last Modified: Wed, 21 May 2025 18:15:40 GMT  
		Size: 5.8 MB (5803141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c19178fc8cffd13abb189db9b8fad487b9f22b84582e042c2d430e282f18ace5`  
		Last Modified: Wed, 21 May 2025 18:15:40 GMT  
		Size: 19.6 KB (19608 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:1a56481d211a1de758dcb1df56f17750d639ff20df4a5cf27e6c32223be14b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.7 MB (486684584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b3f955ce6d216bca6f69f3f142c6c1abb7b577485e211542abaa42037bff9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.5 org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.5 com.ibm.websphere.liberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78892370879d09e257e1f423fb01169148aa714423fd175a7a3f0933ae6673e`  
		Last Modified: Thu, 08 May 2025 17:57:19 GMT  
		Size: 12.1 MB (12129417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac61e1105185e15d0582c5260aeba5bbfaa3b95b8b650d56029725f4a55df82`  
		Last Modified: Fri, 09 May 2025 16:54:48 GMT  
		Size: 48.9 MB (48888727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42089243838a6d937791f1e97d65589176852b83c8876aadb53b43e379125092`  
		Last Modified: Fri, 09 May 2025 16:54:33 GMT  
		Size: 4.2 MB (4199269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75cba9c77d3660514ff0954826cb1b31d6d0d50faa36e263cde1edd07ddcfe5`  
		Last Modified: Wed, 21 May 2025 17:50:46 GMT  
		Size: 42.3 KB (42327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536f7bb3f23286bdfbec45504ffff92568569390f3962fa86578ada275f1710`  
		Last Modified: Wed, 21 May 2025 17:50:47 GMT  
		Size: 17.6 MB (17561051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a30e54cb5147528b0edc171114e18d431fe4c59833236aa5391e95560912823`  
		Last Modified: Wed, 21 May 2025 17:50:46 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c725a0a9b1125deb94f18a82f16df85355ff1f29377ff400ed830ccfcdb42a`  
		Last Modified: Wed, 21 May 2025 17:50:46 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a4a89bce54c40300b94add1e9ffa7bf12bdfed9292a11ee0742f7f4055cf7b`  
		Last Modified: Wed, 21 May 2025 17:50:48 GMT  
		Size: 12.3 KB (12303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4b1cd85e4c61c689d853f738a1bdd3971e36b4d2eda174710d8a0e67fff41`  
		Last Modified: Wed, 21 May 2025 17:50:47 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0dd2657505cdf6e5fb3ba81e5e29b390be571aa7b86317c3b198c034cc843`  
		Last Modified: Wed, 21 May 2025 17:50:48 GMT  
		Size: 13.1 KB (13105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9936d2494f49d3604947831cef61e885beac94c8c4ca9c08b1925d926bb8225`  
		Last Modified: Wed, 21 May 2025 17:50:49 GMT  
		Size: 2.7 MB (2736938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197160777c9cdb6202fb506f3c14642bfa53ede02b44ae6c5478205fe34f08cb`  
		Last Modified: Wed, 21 May 2025 18:16:40 GMT  
		Size: 358.6 MB (358572777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fab9691c41a54a110cbfa9ac86c911d89834fbfe551f3705cf2263c66aa9fd`  
		Last Modified: Wed, 21 May 2025 18:16:31 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7710f6be929afc455b0b6324216731dbfc0af2b4470b8e012bad8f3a983ccf4`  
		Last Modified: Wed, 21 May 2025 18:16:32 GMT  
		Size: 15.2 MB (15171274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:942498d3bd70ba731f2c224b53bbe2bdb944b2af6ebac73aa5ed685018bd9c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5816166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11389dca5b79257c590411486037f2c05ceb50c44ca311e8bf99b4f6dc4ce66`

```dockerfile
```

-	Layers:
	-	`sha256:7b88571991739401b8e76b858df3e2ed9292e4a480a4902f2b4b2841c7f06c63`  
		Last Modified: Wed, 21 May 2025 18:16:31 GMT  
		Size: 5.8 MB (5796475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258a76e935df96fda1bb050dfd8f77c581e88d5b74800a7ab6af4c449abfab68`  
		Last Modified: Wed, 21 May 2025 18:16:30 GMT  
		Size: 19.7 KB (19691 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:d60095bda0b741dbfdc3c1044c749a0afea48ebd3b5eee54cb7e2ff263bc1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.5 MB (497491389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67f9d032fafc0aa2368cac5ff5ee028879cf4cb076ddeb127c37ee27063092a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.5 org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.5 com.ibm.websphere.liberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Thu, 08 May 2025 17:15:30 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a64c9f5a72745f3bafe1231a1d79f060f125195fbcd3f510afac643f962e127`  
		Last Modified: Fri, 09 May 2025 09:51:07 GMT  
		Size: 12.9 MB (12893020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65fa0d1d8a641189f3439423a8e4c02fed940b0c94ad70d5301438065f33e96`  
		Last Modified: Fri, 09 May 2025 17:01:59 GMT  
		Size: 54.1 MB (54102700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082d6bd9ee6c9ef7d0c65ef62514262d0cc907747a26d3294f809956296d5cc6`  
		Last Modified: Fri, 09 May 2025 17:01:47 GMT  
		Size: 3.4 MB (3447062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a43778c93a6217d3b705dcc69ef073781e2dccbfdb1e0973598360a063f5501`  
		Last Modified: Wed, 21 May 2025 18:06:02 GMT  
		Size: 36.5 KB (36501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a58aa4b2024924db977d17ab2fd3caf12d4571ddfbee6d2d3330aaabcebbf5`  
		Last Modified: Wed, 21 May 2025 18:06:03 GMT  
		Size: 17.6 MB (17561350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cc197f05aa36ccbd374a8ec7badcda06d65d2d3de66c52a39e037e860531df`  
		Last Modified: Wed, 21 May 2025 18:06:02 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917e64cc886d2ef11e3ff36c46d506fe48759c45ed90a3f8c92b215e62eac6e`  
		Last Modified: Wed, 21 May 2025 18:06:02 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92d93d73c0d3706db19d4bb6c06f7fc87136b190fa162c9c78cba222fc80bc`  
		Last Modified: Wed, 21 May 2025 18:06:03 GMT  
		Size: 12.3 KB (12310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0d149692bc57f4b195b5f42a331ecc56735d5e55785d9f4f8e7449dd9a26f4`  
		Last Modified: Wed, 21 May 2025 18:06:04 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5233e77b413ba5c4aa8ce78f29eb598b76353518214fb19b0c52246d25a29d`  
		Last Modified: Wed, 21 May 2025 18:06:04 GMT  
		Size: 13.1 KB (13117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5db835dc9a52db58b35e127c2533ec506fa9d0c85e44989e65c06f32cf3d649`  
		Last Modified: Wed, 21 May 2025 18:06:05 GMT  
		Size: 2.7 MB (2695977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5116c24146c540c05c4dd8cbf9094a1e93c697f1a6ae1a917197c6f508858345`  
		Last Modified: Wed, 21 May 2025 18:44:41 GMT  
		Size: 358.6 MB (358572889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632a211e41949cfc26a8879812e49d34c7437135642b504c2811bc7385b90d66`  
		Last Modified: Wed, 21 May 2025 18:44:30 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c10e71b767fc4c7263c6bf7becaa12ea03d7b7577fff1f538504c2a0d78df6`  
		Last Modified: Wed, 21 May 2025 18:44:33 GMT  
		Size: 13.7 MB (13710056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e940637c32c16496db283a4deb76f05190ea227dcb899873ab0e255ca3bdd42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb140a2b7344977c93175d33d238d0f10b101d69842008f2f96886414c2214ef`

```dockerfile
```

-	Layers:
	-	`sha256:07ca0c82314b07638e03223b0672a8054084762e0e8b763abc833325c854911c`  
		Last Modified: Wed, 21 May 2025 18:44:30 GMT  
		Size: 5.8 MB (5807762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c99a9de4ced2511736b5e0dc2df1feb83e97f756ddc36672713c5c84bc2392f`  
		Last Modified: Wed, 21 May 2025 18:44:29 GMT  
		Size: 19.6 KB (19636 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ce894b2346dba9b20f729a15faac5c613969f2234a2577744c77db9757c0e208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (491013320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b24d9787769de523e96d9f586cfbd910bae9bbc4fdb51bef2d2ab517b12565a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
CMD ["/bin/bash"]
# Wed, 07 May 2025 17:42:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 May 2025 17:42:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 May 2025 17:42:21 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.5 org.opencontainers.image.revision=cl250520250504-1901 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.5 com.ibm.websphere.liberty.version=25.0.0.5
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Thu, 08 May 2025 17:06:03 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573305c63c6b8034a976ad865f575e2879ba561788a75b917f925a7f6f45b358`  
		Last Modified: Fri, 09 May 2025 07:53:46 GMT  
		Size: 12.2 MB (12219201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfea94de6ef97d7acac465b880aa8d301bf8849c4c03df599b9500725a5ae22`  
		Last Modified: Fri, 09 May 2025 16:57:56 GMT  
		Size: 51.3 MB (51349442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c794941181d8530d3de9ed4ebb498531d6d8599d992edc712f6332606ee9be7d`  
		Last Modified: Fri, 09 May 2025 16:57:49 GMT  
		Size: 4.6 MB (4575053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc04ae228bcce8697af1a66c3e846019db9e751c2e8b920d3e91eeab501beb2`  
		Last Modified: Wed, 21 May 2025 18:07:31 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9b4f0de18d53c3bd109a9be3df53f569d14be2ee192a95b4302867fed72168`  
		Last Modified: Wed, 21 May 2025 18:07:31 GMT  
		Size: 17.6 MB (17560626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72269a1bcd960e6d5495540c9d95394e7f2e04c092a1137b68f4308b6efbdeec`  
		Last Modified: Wed, 21 May 2025 18:07:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df430f2b12a6e3ac3e2cf9742b053a25da77fd22f79bebd35e23840393f10b`  
		Last Modified: Wed, 21 May 2025 18:07:31 GMT  
		Size: 1.5 KB (1520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e07ea8e62d605c2b9fa96abd527c467cbc531f31cb1482051b4fa7ac7f33461`  
		Last Modified: Wed, 21 May 2025 18:07:32 GMT  
		Size: 12.3 KB (12313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55415abdd9d278f04800d2b2456f2671a13d573f6c48cdbc84bb2021468219b7`  
		Last Modified: Wed, 21 May 2025 18:07:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c42f82ad82648dbca066a267b0be1e0ed2c69b4ee66af6378f95ad84bcd23d`  
		Last Modified: Wed, 21 May 2025 18:07:32 GMT  
		Size: 13.1 KB (13118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86da43b004bd8feaafbc36cd35f9db303a968d0da356fc6c4383db0dd5779275`  
		Last Modified: Wed, 21 May 2025 18:07:33 GMT  
		Size: 2.8 MB (2823839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616657a0fd76cddafa9a6c969a11702bbc5b4cfdc1c4e80ed1c0356e430bd4e3`  
		Last Modified: Wed, 21 May 2025 20:54:26 GMT  
		Size: 358.6 MB (358572085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a6843654f735f01a65153f6e729f9942d1c27d60c48e158d94b29051f55789`  
		Last Modified: Wed, 21 May 2025 20:54:21 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9ee9751d7cf26cc972d9961a5c69f27db7f60b5086a9381cd4e21cac0a6b98`  
		Last Modified: Wed, 21 May 2025 20:54:21 GMT  
		Size: 15.9 MB (15851349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:8f02901b86a2bd5012279951480aa7edc50802206a55c73d9ffda750b3c22cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5823766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605767b6cf575c172c2d5d4dde8134d298e27099886abc82b09d4c9f55295f5`

```dockerfile
```

-	Layers:
	-	`sha256:df7f75abbc993658d8f6e03fb36aaefebc30ed306fb4c609ba487034cdfed153`  
		Last Modified: Wed, 21 May 2025 20:54:20 GMT  
		Size: 5.8 MB (5804158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc5dff76a822f896a8ed98137754108d4e7195abff213c9a10095f3ea328070`  
		Last Modified: Wed, 21 May 2025 20:54:20 GMT  
		Size: 19.6 KB (19608 bytes)  
		MIME: application/vnd.in-toto+json
