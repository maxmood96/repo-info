## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:687fbb87a0deeee448d3fa564e0eeefb52af3f48ab15ce64e66f099a61d4fab5
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
$ docker pull websphere-liberty@sha256:f52c9b7bbb1dafea369900a07d2d5608f6405ae75cf1fb7f838cf8a2f075d427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.1 MB (503089165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd4c3533a3ff48ac4d1a84acc64e4a3f50c9d347b98328ce31b07d82262d8e6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 11 Sep 2025 16:08:13 GMT
ARG RELEASE
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Sep 2025 16:08:13 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 11 Sep 2025 16:08:13 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 16:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Sep 2025 16:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Thu, 11 Sep 2025 16:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f80dcecc7ea669de08fc8ac807e9360fecaa0199051d6f23ececbb5089af3fb7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d61683565e694404ba09b2104c0cbbcde50c03b97bad50cb50ed7b324a08fca7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='348de4a541d7e679e027942c4f056fa7c2151711cd3c86d0b582879add89fea8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='f9cbae653a4f93dbb249e345c0f2957ec9423a913865efb000b62282425ced5d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Sep 2025 16:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Sep 2025 16:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
USER root
# Thu, 11 Sep 2025 16:08:13 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:08:13 GMT
ARG OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_VERSION=25.0.0.9
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_BUILD_LABEL=cl250920250821-1629
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.9 org.opencontainers.image.revision=cl250920250821-1629 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.9 com.ibm.websphere.liberty.version=25.0.0.9
# Thu, 11 Sep 2025 16:08:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 11 Sep 2025 16:08:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.9 BuildLabel=cl250920250821-1629
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ARG LIBERTY_URL
# Thu, 11 Sep 2025 16:08:13 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.9 LIBERTY_BUILD_LABEL=cl250920250821-1629 LIBERTY_SHA=7bfd3fb8cb8034df7e237e354af8da53892df731 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 11 Sep 2025 16:08:13 GMT
USER 1001
# Thu, 11 Sep 2025 16:08:13 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 11 Sep 2025 16:08:13 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 11 Sep 2025 16:08:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 11 Sep 2025 16:08:13 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:08:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 11 Sep 2025 16:08:13 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1ec9aed2824f4513766db45aa1577fac2ff7e022b96768aea46d6260150bc9`  
		Last Modified: Thu, 02 Oct 2025 05:07:03 GMT  
		Size: 12.2 MB (12171685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5042844227d7a55769451cce26ebdb77cd5883d853828e653c23c3e7a3e689cf`  
		Last Modified: Thu, 02 Oct 2025 05:07:12 GMT  
		Size: 55.1 MB (55093190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6314efc4ba11e8aa44e4ccdd8d04de7cfd49246531be0af0d51b1df29a1f9ed3`  
		Last Modified: Thu, 02 Oct 2025 05:07:02 GMT  
		Size: 5.1 MB (5087330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136628c26a956f3fdebbd9fb9236fa8c1c4826f313dc1936a615a6fd5df18897`  
		Last Modified: Thu, 02 Oct 2025 08:52:00 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9610929ea7b877e118dc73a4d7b0dc892a3d6309c22fdc150b8f43f6f4cdaeaa`  
		Last Modified: Thu, 02 Oct 2025 08:52:03 GMT  
		Size: 17.7 MB (17672166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10475e168849366c83ff183c1fd525d8560c239c248e7bc1b1d53da7c766df88`  
		Last Modified: Thu, 02 Oct 2025 08:52:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe227ef1de1c624515a1c1b26219775ac8b32498bca304a2c806256779714164`  
		Last Modified: Thu, 02 Oct 2025 08:52:00 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac5c08307412caabdb06099e6a9e19f20732cb1b338f3a8ca1b857a257495de`  
		Last Modified: Thu, 02 Oct 2025 08:52:00 GMT  
		Size: 14.3 KB (14280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de26e37eb88ea3bd5f4c1c487f457c4daf0c63ee173bfce6b9d87646256d6142`  
		Last Modified: Thu, 02 Oct 2025 08:52:00 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76233acae617e3c6d03484101098d62f22c8b2372ab309e38ab9839d68ad515`  
		Last Modified: Thu, 02 Oct 2025 08:52:00 GMT  
		Size: 15.1 KB (15112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1add842820f6eda7b0d2676fb82270ce75c174f4dc845500d82a203760444d18`  
		Last Modified: Thu, 02 Oct 2025 08:52:00 GMT  
		Size: 2.7 MB (2744852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a651069d0e5b4a5ed6e17f5e7ed8cbf9b6ac4b91aab7a3013e5dea24d5f6da`  
		Last Modified: Thu, 02 Oct 2025 18:26:38 GMT  
		Size: 364.9 MB (364949837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c859241717c78eead4bff37708f3dd406b757403aeb7f2f84d79d7f9532991ac`  
		Last Modified: Thu, 02 Oct 2025 12:21:22 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1839a57bf82fbf4257ec96827b5a14baa92315be9f7fb67ac913c6061d7bb2a4`  
		Last Modified: Thu, 02 Oct 2025 12:21:23 GMT  
		Size: 15.8 MB (15768961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:5e9eeb045fda23157efda32e75ecccbbaaf877dc74d93583843e8462d48c04fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b848477427929a0dd1a327f86deee17dc2ed248e5fdad81f0d8c11377ca5d4`

```dockerfile
```

-	Layers:
	-	`sha256:dce8a3f45e2311ed3da7ab206d1d134f2edf4e28eeed4ea1576045247f23c449`  
		Last Modified: Thu, 02 Oct 2025 15:22:02 GMT  
		Size: 5.9 MB (5928556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:069710f3131e21e5e8cbadb0637a3806be97f162b70fca66041cab765b26becb`  
		Last Modified: Thu, 02 Oct 2025 15:22:03 GMT  
		Size: 19.7 KB (19658 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:28aa469af3e3de5ade3ee21d546e79069e2eedc4d6cee9cde1ebf84b6182b549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 MB (498934261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5488ce637d1d1c537e3669e9f8f4036ea8c6cee68a64f7da8cb27ff55c635d26`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f80dcecc7ea669de08fc8ac807e9360fecaa0199051d6f23ececbb5089af3fb7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d61683565e694404ba09b2104c0cbbcde50c03b97bad50cb50ed7b324a08fca7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='348de4a541d7e679e027942c4f056fa7c2151711cd3c86d0b582879add89fea8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='f9cbae653a4f93dbb249e345c0f2957ec9423a913865efb000b62282425ced5d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
USER root
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_URL
# Thu, 09 Oct 2025 13:18:45 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 09 Oct 2025 13:18:45 GMT
USER 1001
# Thu, 09 Oct 2025 13:18:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:18:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:18:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f68d6552cb847c7f48c9ebd9966e3859ee1bf8e909bc7f2aa1df07f1412153e`  
		Last Modified: Thu, 02 Oct 2025 02:23:41 GMT  
		Size: 12.1 MB (12129415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619f37526bc7148153316158d49cbaa5917181395d36d75d68f069fb017d61cc`  
		Last Modified: Thu, 02 Oct 2025 02:23:46 GMT  
		Size: 53.4 MB (53357599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22cc98b0d4801bab687b7cf032a04923693a1bb4a4573740dc8e163513b018f`  
		Last Modified: Thu, 02 Oct 2025 02:23:41 GMT  
		Size: 4.8 MB (4798026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e123565a3c81e12675a28463a1bb55475fc9cdd6122d5f481579900110ec64f6`  
		Last Modified: Thu, 16 Oct 2025 00:42:25 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1848f0d0dec5f691ad699ae4c3d81b4e4399d5400cb599f4d10797e36647b002`  
		Last Modified: Thu, 16 Oct 2025 00:42:27 GMT  
		Size: 17.7 MB (17668836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be1a3ab938a67e0e9b93e79292bf3b2ada42c5777bed1a766fae50454110a21`  
		Last Modified: Thu, 16 Oct 2025 00:42:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24217faa42a4cd09521417d122df51d40e5810aa157ab6a46e3c77c4ad641d71`  
		Last Modified: Thu, 16 Oct 2025 00:42:25 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358cfa86f192bc9e56331492c3570a578e000fd7db43ec95324ceb662ef92597`  
		Last Modified: Thu, 16 Oct 2025 00:42:25 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd0a4a6f136edcd26f88a07f668ef8fba5066aa985feeef635c1b81effca4ea`  
		Last Modified: Thu, 16 Oct 2025 00:42:25 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd33485357cb5c6f4752dd43b0cec5d9f279a30362457b0ce5a111bf422af9be`  
		Last Modified: Thu, 16 Oct 2025 00:42:25 GMT  
		Size: 15.3 KB (15261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd02413dfec6798a5e7c1fdbd2499190c1ac1cd1a2915b485f5358ff135cb97`  
		Last Modified: Thu, 16 Oct 2025 00:42:25 GMT  
		Size: 2.8 MB (2768969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab0f54443207b95805b4ede690f094ab0ef1e9fe5230e492f65d894e8484c01`  
		Last Modified: Thu, 16 Oct 2025 01:20:38 GMT  
		Size: 365.5 MB (365506757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c26ca76cf12dd9497d1bfd358b86cb9c834828b38cec8ee40b63fadf085d3`  
		Last Modified: Thu, 16 Oct 2025 01:20:43 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312eb4e8232cd09c45ec8569d75e8a2c7569668303d50a40d0cde7784d623547`  
		Last Modified: Thu, 16 Oct 2025 01:20:45 GMT  
		Size: 15.2 MB (15246384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:9ecb22df418f9f29d738ae16adc902671f8e893ab08792b27ed68a475eaf9069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5948039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a90c2fcd666ce4e8adf8b86aecb8b037bc3a26b35f42613148573798a0601dc`

```dockerfile
```

-	Layers:
	-	`sha256:4b73a5022b85adc90261ba9521772da5c6e481173b26cd52ce85432bbda0649e`  
		Last Modified: Thu, 16 Oct 2025 03:22:33 GMT  
		Size: 5.9 MB (5928282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b59bc85a5bc78ad699b2a339339bfba7fcd5d9407bdb0c9caeeb9598a567ba7e`  
		Last Modified: Thu, 16 Oct 2025 03:22:34 GMT  
		Size: 19.8 KB (19757 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:b3ccc555135d5d3157d88543d7d6488d71693571979a2c814f49e420a4432d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.9 MB (507901552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61cf0f3aebe29dfcb87fbbde09429d8a220bb16066ac653244bbe62c75a2b5b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f80dcecc7ea669de08fc8ac807e9360fecaa0199051d6f23ececbb5089af3fb7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d61683565e694404ba09b2104c0cbbcde50c03b97bad50cb50ed7b324a08fca7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='348de4a541d7e679e027942c4f056fa7c2151711cd3c86d0b582879add89fea8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='f9cbae653a4f93dbb249e345c0f2957ec9423a913865efb000b62282425ced5d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
USER root
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_URL
# Thu, 09 Oct 2025 13:18:45 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 09 Oct 2025 13:18:45 GMT
USER 1001
# Thu, 09 Oct 2025 13:18:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:18:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:18:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f986968cada567143a317eb39ea1ab589db364ae569c4ecbd454ac3aa78be10`  
		Last Modified: Thu, 02 Oct 2025 03:15:18 GMT  
		Size: 12.9 MB (12893853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df56fcf10a04c3902c0af5f83afe148d363489c93f76d621b38c53080309b5b`  
		Last Modified: Thu, 02 Oct 2025 02:08:24 GMT  
		Size: 56.9 MB (56920779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918a0028cdf60b31503eef4e5ec1d76a39c997e57b173b6c1d56e05c2cbeda31`  
		Last Modified: Thu, 02 Oct 2025 02:08:20 GMT  
		Size: 3.9 MB (3864674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efef69881f45ade286dc33954baf455e8b63c36100c24e538a470ebbc0ff48d5`  
		Last Modified: Thu, 16 Oct 2025 01:08:13 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516b76b6ecf86552a4e52d87415970e58577111814ddec25f33142806fc34015`  
		Last Modified: Thu, 16 Oct 2025 01:08:15 GMT  
		Size: 17.7 MB (17668929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7138de41284f3ec044262361dea65d875b62dcb10349dcd2e867aee7776183`  
		Last Modified: Thu, 16 Oct 2025 01:08:13 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8da53c4ea7ffdd40a29af49d3827898e7c76abca27635bb3ea4451b8385c2e4`  
		Last Modified: Thu, 16 Oct 2025 01:08:13 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bc07894171a32539867e3ed3374c6d106eb2ac9583e85006dbae9ba3d534d5`  
		Last Modified: Thu, 16 Oct 2025 01:08:13 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c78920adc80a0e13b4f123f5e3b203c1d5e84e8b6d09adf0808d680aa9a371`  
		Last Modified: Thu, 16 Oct 2025 01:08:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79978714404ffaec7d8589afd57d9539c5cf8dee5bdd35fca86fa707202918f6`  
		Last Modified: Thu, 16 Oct 2025 01:08:13 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3423aeb628ca0fd9aab4baf55ad04098daa7ff25bfc5e6881be378de54dc2e4`  
		Last Modified: Thu, 16 Oct 2025 01:08:14 GMT  
		Size: 2.7 MB (2707681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd91ae8d3b8cba24252f894a714bb4da339b9958fea5da8251b5260d26ce10b`  
		Last Modified: Thu, 16 Oct 2025 02:23:32 GMT  
		Size: 365.5 MB (365506813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02897001aed7d931701135dfe0afd99620b1b14fe56587896b2c727b5ead900d`  
		Last Modified: Thu, 16 Oct 2025 02:21:18 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d59c1aa541fb14bc1e9a2a143ec9006a5cf6bc62c8c38a7f3ec2b544204832`  
		Last Modified: Thu, 16 Oct 2025 02:21:22 GMT  
		Size: 13.8 MB (13822692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:b24615c3323246c0d7f8e9b981ab5fd6681da75b3a0d4a6fc2970496f4355a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5954245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7affd952b6b06fccce64c3fd988c2f1ff7d468448510bd54e0727392003dd569`

```dockerfile
```

-	Layers:
	-	`sha256:8ad8276c45efae6efa6dd3fd83328b22b9cd7d13b6d782ec4a584e974a969ab3`  
		Last Modified: Thu, 16 Oct 2025 03:22:38 GMT  
		Size: 5.9 MB (5934543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f0c2d8454b0b4c01a78f0e9d8d0edd608e5e2596806d0ba007a401b29d1f31`  
		Last Modified: Thu, 16 Oct 2025 03:22:39 GMT  
		Size: 19.7 KB (19702 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:69c77788a26bcd675112704cdca552deb38556446a74dd5f100cb05776c8fba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.6 MB (501624422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738f577b0152c8c404b1210bda2f27b920abb3beba8ec53ff4ee7120a3940c20`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 29 Sep 2025 16:59:55 GMT
ARG RELEASE
# Mon, 29 Sep 2025 16:59:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Sep 2025 16:59:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Sep 2025 16:59:55 GMT
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
# Mon, 29 Sep 2025 16:59:55 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Sep 2025 16:59:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f80dcecc7ea669de08fc8ac807e9360fecaa0199051d6f23ececbb5089af3fb7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d61683565e694404ba09b2104c0cbbcde50c03b97bad50cb50ed7b324a08fca7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='348de4a541d7e679e027942c4f056fa7c2151711cd3c86d0b582879add89fea8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='f9cbae653a4f93dbb249e345c0f2957ec9423a913865efb000b62282425ced5d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Sep 2025 16:59:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 29 Sep 2025 16:59:55 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
USER root
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_VERSION=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_BUILD_LABEL=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.10 org.opencontainers.image.revision=cl251020250923-1355 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.10 com.ibm.websphere.liberty.version=25.0.0.10
# Thu, 09 Oct 2025 13:18:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/helpers/runtime
# Thu, 09 Oct 2025 13:18:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.10 BuildLabel=cl251020250923-1355
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ARG LIBERTY_URL
# Thu, 09 Oct 2025 13:18:45 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.10 LIBERTY_BUILD_LABEL=cl251020250923-1355 LIBERTY_SHA=5b79d37e3815f53d14fe72e9cd90dd803fd5dafa LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 09 Oct 2025 13:18:45 GMT
USER 1001
# Thu, 09 Oct 2025 13:18:45 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 09 Oct 2025 13:18:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 09 Oct 2025 13:18:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 09 Oct 2025 13:18:45 GMT
ARG VERBOSE=false
# Thu, 09 Oct 2025 13:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Thu, 09 Oct 2025 13:18:45 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e783d3ecc7650f1487649a3d3acaf91cf431f4d1c5824fec7b102501fe16e7be`  
		Last Modified: Thu, 02 Oct 2025 03:16:37 GMT  
		Size: 12.2 MB (12219551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843ab858c6b4f7d64d4087891540fccc1542dbfb76253516044e34192b5bdc8`  
		Last Modified: Thu, 02 Oct 2025 01:44:28 GMT  
		Size: 54.1 MB (54108962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d137860efc2efb8f5f61fb2d5e4a7147fce66050794108c2253b98bd9a11e8e3`  
		Last Modified: Thu, 02 Oct 2025 01:44:19 GMT  
		Size: 5.2 MB (5172720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e7d02830946a17529a195ac151e673141f1163621569d0e7a47144738a0a5f`  
		Last Modified: Thu, 16 Oct 2025 01:02:10 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62d02c4a8399e8ce7fd23c39a1d6113d036c864deae8ef05887e3db9a33a36d`  
		Last Modified: Thu, 16 Oct 2025 01:02:12 GMT  
		Size: 17.7 MB (17668567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97734e90d2021cbe132a8a179fbca750917892fe69bc5712091e4e00031c1f9`  
		Last Modified: Thu, 16 Oct 2025 01:02:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2baf49f8f2afed75767338dfc218ffc13a65b8f9496dedc918ad0aaea8c0eba`  
		Last Modified: Thu, 16 Oct 2025 01:02:10 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81003c6e74bea46acbbbb502cf44673505134efeb4d63a962b600701432d775`  
		Last Modified: Thu, 16 Oct 2025 01:02:10 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57bfb9f6066fcc7099aaa7baed4cb8faf14900e610bff12ba0e36751c13dbb8`  
		Last Modified: Thu, 16 Oct 2025 01:02:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347fd6756771d7ea24f603aaccb802d204857e6f21c560673db06f3dace0bdd5`  
		Last Modified: Thu, 16 Oct 2025 01:02:10 GMT  
		Size: 15.3 KB (15264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5133cf24f595843c96b67decc5ffb9a026b001f3323991a1c0f11bb0dedd4328`  
		Last Modified: Thu, 16 Oct 2025 01:02:11 GMT  
		Size: 2.9 MB (2861880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ec0eaf814e11ab0066e990698447cc9108e71786be7d0d2092cad4777b8d92`  
		Last Modified: Thu, 16 Oct 2025 03:11:03 GMT  
		Size: 365.5 MB (365507245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aca942ba5d2570e873f1dcbe9bb14a46f2e5b7e4c1e207a89bd08635bf927d`  
		Last Modified: Thu, 16 Oct 2025 02:17:10 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e12250725cc700774832a8ab0005306344b7c7e71dfb7a9651085b0ec841f4`  
		Last Modified: Thu, 16 Oct 2025 02:17:13 GMT  
		Size: 16.0 MB (16016131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:2c1fe92cc587fd2c8af9959465700feee19405876dd1abb942d64b3ca5247268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5950613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03e7e78148d96a9fc30d34c83f923071b9d6d720c4cea7b1b6356e3b709ae3c`

```dockerfile
```

-	Layers:
	-	`sha256:aa136af13440d00e4fbb361548b833bd7bc30b28ef5e36deb64e0dfb8de1b224`  
		Last Modified: Thu, 16 Oct 2025 03:22:44 GMT  
		Size: 5.9 MB (5930939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aecea8dfee51de3014f2dc270253f3aba3342ca51abecbddfe788c51d745b87`  
		Last Modified: Thu, 16 Oct 2025 03:22:45 GMT  
		Size: 19.7 KB (19674 bytes)  
		MIME: application/vnd.in-toto+json
