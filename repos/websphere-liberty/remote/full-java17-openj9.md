## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:b25d3013e432abc7699d97b3e38ea55a28c82165a39fdc72cb90c82d0eb4434d
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
$ docker pull websphere-liberty@sha256:8a714819a31577bd4d99e1bed8b835157fbdb1849c6b77e7b8377f29e83035a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.1 MB (506054293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a341e4b6522d4ca401f208401e8d610fbf05bcecc74c37aeee3103cc27b153ad`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:27:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:27:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:27:14 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 15 Jan 2026 22:27:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:27:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:27:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:27:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 16 Jan 2026 01:33:13 GMT
USER root
# Fri, 16 Jan 2026 01:33:13 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 01:33:13 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jan 2026 01:33:13 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Fri, 16 Jan 2026 01:33:13 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Fri, 16 Jan 2026 01:33:13 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Fri, 16 Jan 2026 01:33:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Fri, 16 Jan 2026 01:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 16 Jan 2026 01:33:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Fri, 16 Jan 2026 01:33:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 16 Jan 2026 01:33:13 GMT
ARG LIBERTY_URL
# Fri, 16 Jan 2026 01:33:13 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 16 Jan 2026 01:33:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:33:24 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 16 Jan 2026 01:33:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 16 Jan 2026 01:33:24 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 16 Jan 2026 01:33:24 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 16 Jan 2026 01:33:24 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 16 Jan 2026 01:33:24 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 16 Jan 2026 01:33:28 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 16 Jan 2026 01:33:28 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Jan 2026 01:33:28 GMT
USER 1001
# Fri, 16 Jan 2026 01:33:28 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 16 Jan 2026 01:33:28 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 16 Jan 2026 01:33:28 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Jan 2026 02:38:36 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 02:38:36 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Jan 2026 02:38:36 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 16 Jan 2026 02:38:36 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 16 Jan 2026 02:38:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad96c1dea85f86acf9252b1bd3e4d4b5cd893cdb4f8ba18a6df444afd4ea1d9`  
		Last Modified: Thu, 15 Jan 2026 22:28:01 GMT  
		Size: 12.2 MB (12171783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcd7976482bebafb7cfd5d5794d319ed4d11a0cf175c3ff9cbe93e6b22a5585`  
		Last Modified: Thu, 15 Jan 2026 22:28:02 GMT  
		Size: 55.2 MB (55190779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8312ca06cf4dcf35a6056fe5f48377910aa5fe09695bbb706b8bb409a533b2b`  
		Last Modified: Thu, 15 Jan 2026 22:28:01 GMT  
		Size: 5.1 MB (5084580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3eae7f8f1bf930421cfb75affb3182db1677c411aec8c498f654260211ce03`  
		Last Modified: Fri, 16 Jan 2026 01:33:43 GMT  
		Size: 31.7 KB (31744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3677b2d003fa0f6c79c7593422554b2e3296fab603c6ad98f47f4cb4c8375f`  
		Last Modified: Fri, 16 Jan 2026 01:33:45 GMT  
		Size: 18.0 MB (18036158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d55a15ab26bfa4b83053541a7147deddcf9a656b528de2896315638919462d7`  
		Last Modified: Fri, 16 Jan 2026 01:33:37 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d34b14cb7d8e93651d1a48573cf77457827ee6b7e9c0b8a96355c211f72966`  
		Last Modified: Fri, 16 Jan 2026 01:33:37 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca4ccb92067b9c84e888617586fdb8004134a3d1b30cf76a028732b022b873d`  
		Last Modified: Fri, 16 Jan 2026 01:33:43 GMT  
		Size: 14.1 KB (14114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0008d4dfb0202835e731c2b3a088b3971081e02c958707e4bc34112711f19a`  
		Last Modified: Fri, 16 Jan 2026 01:33:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c9fc14418434c0fd5c9d2b6ed8ece2d97176910970ba2dc257d8dcc4b1a663`  
		Last Modified: Fri, 16 Jan 2026 01:33:43 GMT  
		Size: 15.0 KB (14984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f50e29c9b2e006ecad454f821f8c26b6495f186eac7bc868c758cc87f4d049`  
		Last Modified: Fri, 16 Jan 2026 01:33:39 GMT  
		Size: 2.7 MB (2739529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78957b67282a21ab8ca53fc10c1bfa0a42d208d2d3b624637b33fab2acf1b3de`  
		Last Modified: Fri, 16 Jan 2026 02:41:09 GMT  
		Size: 367.2 MB (367204618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89823440c96739a0775f5f877f12c2cb2e7f76ac6b5fe167d7f4fea8a0b9f644`  
		Last Modified: Fri, 16 Jan 2026 02:39:42 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6a821f66183c44b9f3e9f988fc4728dc6900083f5e377dc588e1ca5f20322c`  
		Last Modified: Fri, 16 Jan 2026 02:39:46 GMT  
		Size: 16.0 MB (16026145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:95a3bb1b2f4aa5a41aa9a4a607e8feba1093c96e4f231e83391f1b3da2c82c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5952272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1b8fbb5edb33ccb0017ce698dd24a5542b6896c5418af12d26229cf4c06c4d`

```dockerfile
```

-	Layers:
	-	`sha256:8b4e30e095a6704a6b793ad58f17564df79adf4cbbe50c77dce882d7e9455b33`  
		Last Modified: Fri, 16 Jan 2026 04:24:27 GMT  
		Size: 5.9 MB (5932640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b16c72ebd1a2006e93c1b650c4a47168a693b2df54c207cf82520f7963211c`  
		Last Modified: Fri, 16 Jan 2026 02:39:24 GMT  
		Size: 19.6 KB (19632 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:d38b1b602b31cfe0a5a2a9aeb64c4babf5e63b3640ccbd506af8672bf24c7b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.3 MB (501262933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6857dc75188630104677512f12903b6140716d019f7a162a9984e4585e81d1f0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:29:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:29:16 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 15 Jan 2026 22:29:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:29:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:29:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:29:51 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 16 Jan 2026 01:37:37 GMT
USER root
# Fri, 16 Jan 2026 01:37:37 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 01:37:37 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jan 2026 01:37:37 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Fri, 16 Jan 2026 01:37:37 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Fri, 16 Jan 2026 01:37:37 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Fri, 16 Jan 2026 01:37:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Fri, 16 Jan 2026 01:37:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 16 Jan 2026 01:37:37 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Fri, 16 Jan 2026 01:37:37 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 16 Jan 2026 01:37:37 GMT
ARG LIBERTY_URL
# Fri, 16 Jan 2026 01:37:37 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 16 Jan 2026 01:37:50 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 01:37:50 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 16 Jan 2026 01:37:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 16 Jan 2026 01:37:51 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 16 Jan 2026 01:37:51 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 16 Jan 2026 01:37:51 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 16 Jan 2026 01:37:51 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 16 Jan 2026 01:37:55 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 16 Jan 2026 01:37:55 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Jan 2026 01:37:55 GMT
USER 1001
# Fri, 16 Jan 2026 01:37:55 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 16 Jan 2026 01:37:55 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 16 Jan 2026 01:37:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Jan 2026 02:57:07 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 02:57:07 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Jan 2026 02:57:07 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 16 Jan 2026 02:57:07 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 16 Jan 2026 02:57:33 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ef9d3bfe660d622551b3c586de2f866b43b44f3ce75ef0c23b26339e6eb1eb`  
		Last Modified: Thu, 15 Jan 2026 22:30:03 GMT  
		Size: 12.1 MB (12132639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6b9251c4a9c14abe5526cdb8678e960f10ad19867712e0ad77ad7dcd436057`  
		Last Modified: Thu, 15 Jan 2026 22:30:04 GMT  
		Size: 53.5 MB (53468141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1786dbee4e241beca5a62c5c6e782ca848a0ba2d26f81700a2298991ec5385`  
		Last Modified: Thu, 15 Jan 2026 22:30:10 GMT  
		Size: 4.8 MB (4826598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60d402873e0176cc7fd9a60b68832a6855d6caf762d439b27046f0592dca622`  
		Last Modified: Fri, 16 Jan 2026 01:38:13 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020d877024e2cc6ff3372481d3a69faed7a0b8e7c1167104616615e2cedddc0a`  
		Last Modified: Fri, 16 Jan 2026 01:38:05 GMT  
		Size: 18.0 MB (18036229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42809921f5898cae1dc841bcd0ee16b7fad59c89323c34b22ac8904de64b4ff1`  
		Last Modified: Fri, 16 Jan 2026 01:38:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075fc4543e65ccf8c0b72d9d04da2b61ea5425458174fc4dfedb09ef31835eea`  
		Last Modified: Fri, 16 Jan 2026 01:38:13 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3414eb5b24a5f4d80ca9ec9ae839a3d7271dfd69fe50a39fc536138e9da50efa`  
		Last Modified: Fri, 16 Jan 2026 01:38:13 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22be216296e9de6f3a148a018af6c109f48ae16cdc552819d3c9a395298648c`  
		Last Modified: Fri, 16 Jan 2026 01:38:13 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418c25c4704ea223c97e098a59e710fc55ec4bc0bd5158f347e8b9d3ec132290`  
		Last Modified: Fri, 16 Jan 2026 01:38:06 GMT  
		Size: 15.0 KB (14994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59f1d697e8d4d011a93c4df5df5d288726b6d705c6bc9bf2b86ba8c5d8afcee`  
		Last Modified: Fri, 16 Jan 2026 01:38:14 GMT  
		Size: 2.8 MB (2829013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7513a3b2c473f4364d37dc77e66f9e6392114a11137d7a788431c014379d8`  
		Last Modified: Fri, 16 Jan 2026 02:58:49 GMT  
		Size: 367.2 MB (367202027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc7771a2986044ccd6cb5e8e4fe9cb2a8466f34c8b29528ff5998c3c132b147`  
		Last Modified: Fri, 16 Jan 2026 02:58:15 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9536ec9865bd2bf40cae22aad41ca876f26d318001e932cc33c232189dcabf80`  
		Last Modified: Fri, 16 Jan 2026 02:58:04 GMT  
		Size: 15.3 MB (15310168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4a058d01a096927b0ec55ed513a980eb55a484e45d1361c9540f01d9884d7d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5950716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb030af3012e29334d75cc70c2602b77ca79867108c3feb6fdb68886524e23d`

```dockerfile
```

-	Layers:
	-	`sha256:94824227457d4816c7a5b5bf775784ee2eb4b8873722287bd5b7eabbebd85924`  
		Last Modified: Fri, 16 Jan 2026 02:58:04 GMT  
		Size: 5.9 MB (5931000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9ed17c2d6feb31a44467ae625709ebdaeee5c57170b48c551b5007e7566144`  
		Last Modified: Fri, 16 Jan 2026 04:24:35 GMT  
		Size: 19.7 KB (19716 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:bd508d25c3609617b7a2f74d963b123b60002e6864494f8de002c10d618d2bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510017975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205437dce240ae364960052404532fb525a1d94c2ecfdf3c2374e3bd286e2f6c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:26:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:26:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:26:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 15 Jan 2026 22:37:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:37:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:37:32 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:38:07 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 16 Jan 2026 02:32:14 GMT
USER root
# Fri, 16 Jan 2026 02:32:14 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 02:32:14 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jan 2026 02:32:14 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Fri, 16 Jan 2026 02:32:14 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Fri, 16 Jan 2026 02:32:14 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Fri, 16 Jan 2026 02:32:14 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Fri, 16 Jan 2026 02:32:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Fri, 16 Jan 2026 02:32:14 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Fri, 16 Jan 2026 02:32:14 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 16 Jan 2026 02:32:14 GMT
ARG LIBERTY_URL
# Fri, 16 Jan 2026 02:32:14 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 16 Jan 2026 02:32:27 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:32:27 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 16 Jan 2026 02:32:28 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 16 Jan 2026 02:32:28 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Fri, 16 Jan 2026 02:32:29 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Fri, 16 Jan 2026 02:32:29 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Fri, 16 Jan 2026 02:32:31 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 16 Jan 2026 02:32:42 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Fri, 16 Jan 2026 02:32:42 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Jan 2026 02:32:42 GMT
USER 1001
# Fri, 16 Jan 2026 02:32:42 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 16 Jan 2026 02:32:42 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 16 Jan 2026 02:32:42 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Jan 2026 05:26:40 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 05:26:40 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Jan 2026 05:26:40 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 16 Jan 2026 05:26:41 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 16 Jan 2026 05:27:26 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd5d12a160f6d8dea2246e7b85a8df4b10ff68fb7e41da962d3021f6326151b`  
		Last Modified: Thu, 15 Jan 2026 22:28:33 GMT  
		Size: 12.9 MB (12893562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b3fcc0cb045357a148effdc87bd7c18ed2d44c685f9b4f77dd618a6fdef968`  
		Last Modified: Thu, 15 Jan 2026 22:38:47 GMT  
		Size: 57.0 MB (57019141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e391e4bb4d5182a64a63e4a0db567601465acda7995b4fafe8335622e6e3a00`  
		Last Modified: Thu, 15 Jan 2026 22:38:53 GMT  
		Size: 3.9 MB (3859939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450e9fc29d71aa51febdef93b88228ea3e07e0d08df4439d2cb42bbcf3eb7943`  
		Last Modified: Fri, 16 Jan 2026 02:33:25 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117aa877f156092d492636b423731449201f8021b9206429099a80a5784816fc`  
		Last Modified: Fri, 16 Jan 2026 02:33:19 GMT  
		Size: 18.0 MB (18036516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10351644fc5e6bd3bfa4697e099108ce9314e17915271c5d1eb8f9246a2ff311`  
		Last Modified: Fri, 16 Jan 2026 02:33:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acde4e5597e25aa04c94c4822406acb251b17b01d674dce1d8ee5c6e64731852`  
		Last Modified: Fri, 16 Jan 2026 02:33:25 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6aabea6b1b1ccfc22f0f028f5e7f51192b7afc76bbc58bfa2be124e384491f3`  
		Last Modified: Fri, 16 Jan 2026 02:33:19 GMT  
		Size: 14.1 KB (14120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c368fddfa4dcb449a1744822d282890184a7852deb66f444abe068a216925ef`  
		Last Modified: Fri, 16 Jan 2026 02:33:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae95e48b5bcaba0a6c7fb9c1a0fbfbe3916eab7f60afe1c6090604343e574279`  
		Last Modified: Fri, 16 Jan 2026 02:33:19 GMT  
		Size: 15.0 KB (15005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7862e0107c823464cde66525cdd9bd0b06361711e04ce06a07c06308751e6216`  
		Last Modified: Fri, 16 Jan 2026 02:33:25 GMT  
		Size: 2.7 MB (2725382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a89202eec21e665d12fdce48ad3ef90f1e17a8b74bd5ffd1a51d6f5ae8b45a`  
		Last Modified: Fri, 16 Jan 2026 05:33:04 GMT  
		Size: 367.2 MB (367201679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c341a8d137d133e73c92209aca35147c7c65c00beb22fc1fa22442e6887d4b`  
		Last Modified: Fri, 16 Jan 2026 05:28:28 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caffaa6cb5f2cbaa2634883b747f0981f499436cad5d9c750acec510b04482d1`  
		Last Modified: Fri, 16 Jan 2026 05:28:28 GMT  
		Size: 13.8 MB (13765974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:afb5e23d3274861bd3e88c506af2293eb7c7a52d3cb1680f271307fbfe3f0f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5685a973141c8f9b65a55c910dce61328baf988c72fc3b5856bc30634fcb5628`

```dockerfile
```

-	Layers:
	-	`sha256:b7f7b439e94377d52687062f9a8dbddd7eb1ccdcd1445452746929ceb49ed142`  
		Last Modified: Fri, 16 Jan 2026 07:21:39 GMT  
		Size: 5.9 MB (5937261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35532abf63a653429a196bd58d2492dcf78e247e0fb1c7b9e6e38c2cdb3d267`  
		Last Modified: Fri, 16 Jan 2026 07:21:40 GMT  
		Size: 19.7 KB (19661 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:4239628243c797c9e8b445ea7f1daaeed67f58935a2c3622a38d74a3ab2e8085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503928895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5f38d9f9f8a1bc2c2ef80b78e6338ee9cee01880b1de6e5ffa3ad144f5df53`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:11:59 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 15 Jan 2026 22:15:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:15:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:15:00 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:15:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 15 Jan 2026 23:59:08 GMT
USER root
# Thu, 15 Jan 2026 23:59:08 GMT
ARG VERBOSE=false
# Thu, 15 Jan 2026 23:59:08 GMT
ARG OPENJ9_SCC=true
# Thu, 15 Jan 2026 23:59:08 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Thu, 15 Jan 2026 23:59:08 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Thu, 15 Jan 2026 23:59:08 GMT
ARG LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
# Thu, 15 Jan 2026 23:59:08 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.12 org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.12 com.ibm.websphere.liberty.version=25.0.0.12
# Thu, 15 Jan 2026 23:59:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 15 Jan 2026 23:59:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.12 BuildLabel=cl251220251117-0302
# Thu, 15 Jan 2026 23:59:08 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 15 Jan 2026 23:59:08 GMT
ARG LIBERTY_URL
# Thu, 15 Jan 2026 23:59:08 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 15 Jan 2026 23:59:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:59:25 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 15 Jan 2026 23:59:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 15 Jan 2026 23:59:25 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 15 Jan 2026 23:59:25 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 15 Jan 2026 23:59:25 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 15 Jan 2026 23:59:26 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 15 Jan 2026 23:59:30 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.12 LIBERTY_BUILD_LABEL=cl251220251117-0302 LIBERTY_SHA=8628e03c14da383ea977cf5feb834b00b5d27840 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 15 Jan 2026 23:59:30 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 15 Jan 2026 23:59:30 GMT
USER 1001
# Thu, 15 Jan 2026 23:59:30 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 15 Jan 2026 23:59:30 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 15 Jan 2026 23:59:30 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Jan 2026 00:28:56 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 00:28:56 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Jan 2026 00:28:56 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Fri, 16 Jan 2026 00:28:56 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Fri, 16 Jan 2026 00:29:30 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1421ff1e62d1ac76e2d8a34fa67faf578cf114b64b34c9d5c7c3a05835f2924`  
		Last Modified: Thu, 15 Jan 2026 22:12:51 GMT  
		Size: 12.2 MB (12220151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef92bf2e1b5d43e6698078060d355356215e7242584485701fd3d0a6ac2dfce`  
		Last Modified: Thu, 15 Jan 2026 22:16:04 GMT  
		Size: 54.2 MB (54201865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d0c0eb1496269256c130258e30b475a6ea4f784ccf3d0d77d73239046eff9`  
		Last Modified: Thu, 15 Jan 2026 22:15:57 GMT  
		Size: 5.2 MB (5230921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395aeef21b971157266cc5530bc2d65bda5da38d2b002b4ff517bf9b96d9a71a`  
		Last Modified: Thu, 15 Jan 2026 23:59:52 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d520e7c05ea9a64837b5f722fa3516be7a8d163463dd9b84389193b8736dc49`  
		Last Modified: Thu, 15 Jan 2026 23:59:46 GMT  
		Size: 18.0 MB (18035707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45338bc4c13846cfb5be50bcb77f164e5f9d67982a3bb585a72467c17dec172`  
		Last Modified: Thu, 15 Jan 2026 23:59:52 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f9161df878de40d5042bda99f30af6898ae876dc5e16eef2d5ef8ada6b5f4`  
		Last Modified: Thu, 15 Jan 2026 23:59:52 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95a054d8175ec94a5e8ea1cbfd77684ed3e4f1e9c7a52ac12eaaa6ffa076c0d`  
		Last Modified: Thu, 15 Jan 2026 23:59:52 GMT  
		Size: 14.1 KB (14116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697fbecb079c512df9f70421fd5020334db94152ecb9c66d9b91803e6e12b15f`  
		Last Modified: Thu, 15 Jan 2026 23:59:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81cfb8c62a22cbc6f6dbdfa47a6d3bcc36c8cc3637d2fa4d28aca506f1fc490`  
		Last Modified: Thu, 15 Jan 2026 23:59:46 GMT  
		Size: 15.0 KB (14987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77792b4ed814ff1577a05d3f6571cc969cda3c7f1b8cd12cad1a9cfff0a8a928`  
		Last Modified: Thu, 15 Jan 2026 23:59:47 GMT  
		Size: 2.9 MB (2904752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3950052e31b18147ac6ae7f90cbe04ea3ed6e3ce5cc9ed8a935db83a18dfccc1`  
		Last Modified: Fri, 16 Jan 2026 00:31:56 GMT  
		Size: 367.2 MB (367200411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b5978a15242f85724d37b89e869e36204adfe8db1dd815901e52510b3f7e47`  
		Last Modified: Fri, 16 Jan 2026 00:30:29 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99eda6c11f3965f1ca6fa04305fb4fc657be74577ee6db82fa75767fbf6f6446`  
		Last Modified: Fri, 16 Jan 2026 00:30:30 GMT  
		Size: 16.1 MB (16066549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:107bcdd8d2abf2c3e3bcce261e3b375a66b407f8185b0b1b8cb0294d3a7990b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8669a28489645a1815135558446ae3b11351ff3da25f3ec55424dcb12a6fc8`

```dockerfile
```

-	Layers:
	-	`sha256:b6fcfe1465fd45231f050494e4e08c2ebf623a34c1daed207b3585a01edfb721`  
		Last Modified: Fri, 16 Jan 2026 01:24:13 GMT  
		Size: 5.9 MB (5933657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc276a668232e2f6461d72522a3a282c99d1a976283ccd865201d67384b6c0cb`  
		Last Modified: Fri, 16 Jan 2026 01:24:14 GMT  
		Size: 19.6 KB (19633 bytes)  
		MIME: application/vnd.in-toto+json
