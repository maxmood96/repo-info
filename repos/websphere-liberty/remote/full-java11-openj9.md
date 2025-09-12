## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:57abe80e3c121b9e3388a0c43e960632be244141886a90b6c80df65907de257a
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
$ docker pull websphere-liberty@sha256:89210870c4b30606cf45df187b7b1c020b01694757d2cb525eea1c467cea0bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.6 MB (503583690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281dbda31a98204dde2d1ad01da729e728503210ac2a2b83c1b13e91d1fc5ed4`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d820471914609b5371f6a5a577d11e27c985cb27ca0ae470feef38d6c676c161`  
		Last Modified: Tue, 02 Sep 2025 00:13:24 GMT  
		Size: 12.2 MB (12171849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2387d18a60d0ba5cc1e81ae3fcbf7cde8081281fc50ae1a8bbd21b65cf299e05`  
		Last Modified: Tue, 02 Sep 2025 00:13:27 GMT  
		Size: 55.8 MB (55756697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a00d87b8283a411ed62847249c1bddb6221b9acbfd6858645c9b58569a320`  
		Last Modified: Tue, 02 Sep 2025 00:13:24 GMT  
		Size: 4.5 MB (4510996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be8f378fc44edae0fd3601ff42aafda5633ee4ac8e4063193165ec6648f767b`  
		Last Modified: Thu, 11 Sep 2025 17:08:15 GMT  
		Size: 31.7 KB (31744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7bdf22a06a0bc6caa190cbd40a86c29359301b9494d45f6a0d2aff7c15d695`  
		Last Modified: Thu, 11 Sep 2025 17:08:21 GMT  
		Size: 17.7 MB (17672189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c792f3540c2916b05277d9a3293627a9a338c8c91e469b6924e99b7e5b9df8e`  
		Last Modified: Thu, 11 Sep 2025 17:08:15 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96c07c362cdb1b7d3571d770b8af9cb8eef4fdc0df95b89f8e18ef15bcd5c89`  
		Last Modified: Thu, 11 Sep 2025 17:08:15 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5b018d23baf694f13c6b834bf6ac010dfcbcf7c8034e4fdc1a8fb1d3f00cd8`  
		Last Modified: Thu, 11 Sep 2025 17:08:14 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b085c9e8252135beb8be54188394e0b0b8c67ca91ed7e0e407881730dcdb9a`  
		Last Modified: Thu, 11 Sep 2025 17:08:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954fdd81b252947bd8b52f3b43a6dd04d933865c344291d2621df77f5a2156c8`  
		Last Modified: Thu, 11 Sep 2025 17:08:14 GMT  
		Size: 15.1 KB (15104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c966a20a885b0ebafa7118921b76a085018dd9e6ce6f0313f0068450c6402d1`  
		Last Modified: Thu, 11 Sep 2025 17:08:14 GMT  
		Size: 2.8 MB (2809398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255214e073b3665e86f961fd38346cc375688fa4f4abdc7db41f23c907087023`  
		Last Modified: Thu, 11 Sep 2025 21:40:20 GMT  
		Size: 364.9 MB (364948928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0e775ff29d65b278b8ab8bfe5a3ada0653ccc4fe0b67df6c031005f5f9854`  
		Last Modified: Thu, 11 Sep 2025 17:16:55 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfac08b783e3ff939a050c145f6f8be390e02325720a3528e8df41ed5d91259`  
		Last Modified: Thu, 11 Sep 2025 17:16:58 GMT  
		Size: 16.1 MB (16112388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e1c04c60895f5850882b001ab44a7ce8250a770c8879a4c4cde2c7e529e7fec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5961343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ef92f26b3b52bee219dd1281eb0aea0f1dbc8d75ceea930cef6d032faf8299`

```dockerfile
```

-	Layers:
	-	`sha256:58c82100ecbbc4cbd4b9dbe7001b1361f7cd36386a135f3a4a2b24e77053a28d`  
		Last Modified: Thu, 11 Sep 2025 18:22:07 GMT  
		Size: 5.9 MB (5941685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:780c6aa41face428761cc442b5364af0fd58dac6c436d46006118f4b975b1f04`  
		Last Modified: Thu, 11 Sep 2025 18:22:08 GMT  
		Size: 19.7 KB (19658 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:8163ff21b73f7613bb1f48c84c5a01bc8a6445bf648e5a2ecbe2e7a72926f9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.3 MB (498278261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13359ea23110fc004ec39f55471aa0b9908584b3153fbb66674aa33cdee753e6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ae624de3eeb0edb3e4a120905423464cf816ca0d11b0b199c055f29c2e6609`  
		Last Modified: Tue, 02 Sep 2025 01:29:48 GMT  
		Size: 12.1 MB (12130364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f476b0a9b46a567ec6ac2f3ca3531c161fb736e6f16e7f71e0b9224d64c1b0`  
		Last Modified: Tue, 02 Sep 2025 01:35:52 GMT  
		Size: 54.0 MB (54012643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac97f82108888e43ccadfb43f296c6e547e0318b241744c4db85e4b5ccd1eb6`  
		Last Modified: Tue, 02 Sep 2025 01:35:49 GMT  
		Size: 4.3 MB (4254857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccf6140826c84562b078b0ea56bb47b6253cba5c094516d465dfbbd74a74dbd`  
		Last Modified: Thu, 11 Sep 2025 17:58:05 GMT  
		Size: 42.3 KB (42321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e78f855185353478b5e9eff6346247dba8a121fc5e97690d996a7b59915d98`  
		Last Modified: Thu, 11 Sep 2025 18:08:45 GMT  
		Size: 17.7 MB (17672439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a60cc0f9eab4d98206862329671d7d1f72ab5004ca36f8f9353e247805e078`  
		Last Modified: Thu, 11 Sep 2025 17:58:04 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f836b0fabbf037ca23e234269e5bb12be0c08518a0ee7afa0f0852ab9793c454`  
		Last Modified: Thu, 11 Sep 2025 17:58:04 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a02947387e26424ae06b3ec2cd7f1119a8439d779675f27f3df4c9b8597b98d`  
		Last Modified: Thu, 11 Sep 2025 17:58:05 GMT  
		Size: 14.3 KB (14278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557e1fd514af7b8ae49e05c278b7d89bb303ec7d5419275364e592f61f0de9b7`  
		Last Modified: Thu, 11 Sep 2025 17:58:04 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71e9261e4e09b3ad4f6eab9927e9c3163cbe5c56e7c29c8b21d9c98d5e10fb6`  
		Last Modified: Thu, 11 Sep 2025 17:58:04 GMT  
		Size: 15.1 KB (15107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c101fd48df8c528a2fdf23e51551b57c019bf78c6085afc695a3971b869b03a5`  
		Last Modified: Thu, 11 Sep 2025 17:58:05 GMT  
		Size: 2.8 MB (2818769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfeb50591c55a04b6eec31417874214ba17fb65f91d89c2147cae62b87bd00b`  
		Last Modified: Thu, 11 Sep 2025 21:41:36 GMT  
		Size: 364.9 MB (364948619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64f24b72bd51e0a97ce280e42ed9eb1b4cea907c734a9350f208c201265381e`  
		Last Modified: Thu, 11 Sep 2025 18:18:26 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de759b14912efe58a39bd0c56d107cde42e180e7133c28a0eb89c3eb19d66a59`  
		Last Modified: Thu, 11 Sep 2025 18:18:27 GMT  
		Size: 15.0 MB (15004211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:055af7ffc086210c9f6ff0f075900b42b256fb00122443974829ab2e155e083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5959786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde0634879762a918e14fad9d4a0750239acc2bd5c9574b1d9f2c7ed3954b2f0`

```dockerfile
```

-	Layers:
	-	`sha256:a2c1f05aa2d23c2e401628feca6260859c496c4b5c64b93a9595744bfd1a572b`  
		Last Modified: Thu, 11 Sep 2025 21:22:11 GMT  
		Size: 5.9 MB (5940045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4facdd9ea83f996916597a657ee5b5698d06988cbf65904661ed213f808a037c`  
		Last Modified: Thu, 11 Sep 2025 21:22:12 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:406a0fe469068c152f6ee543f4be94dd2ed9fb0b2bc75d38b372c4ea6406dc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.5 MB (507541031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e698f77209dc3cbf906d17ce507f7c960515ad5fef20782680cb184a95b359a6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd05e0384f89e87f39bbca5882dc09e12e30daf4c6b9267897a05fc765378ae`  
		Last Modified: Tue, 02 Sep 2025 00:35:06 GMT  
		Size: 12.9 MB (12894660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ec2c99ca76967222d47b87ab651022c177583d30b6ba6e52d9d053a13b1acd`  
		Last Modified: Tue, 02 Sep 2025 00:44:06 GMT  
		Size: 57.6 MB (57604774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d287cf69b9554d2cfdbfc670598312ba27a69c49097f699dcdf54f605938086b`  
		Last Modified: Tue, 02 Sep 2025 00:43:59 GMT  
		Size: 3.5 MB (3511616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e8b2c8275726f1e904f52ff9ee86a8e4b5e28497606c12686809c528ad9b9c`  
		Last Modified: Thu, 11 Sep 2025 18:22:39 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4ee06e2ff541a623cdd5a0f72abb616514d007539c3d15963307e9682e5b98`  
		Last Modified: Thu, 11 Sep 2025 18:22:42 GMT  
		Size: 17.7 MB (17672600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59059e4166e27698f8a5fb565df296fb456a491b1c7f08083b120a72ee79104b`  
		Last Modified: Thu, 11 Sep 2025 18:22:39 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a217010c55b88aaff660a18ca2bfa7ac0e2741408a6e24a786e636c850e385`  
		Last Modified: Thu, 11 Sep 2025 18:22:40 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470ee88495fa8dae6247765fc63adb05b7054edec3f3e2f060da464547f300f4`  
		Last Modified: Thu, 11 Sep 2025 18:22:40 GMT  
		Size: 14.3 KB (14278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753569bcdc3db5334bc0d0a1cfce57f549a581a9e3c6db2f88d5df3301386fe2`  
		Last Modified: Thu, 11 Sep 2025 18:22:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0a4e680c96b24ee2c327c9355ccb4185fd8eb5142af7fca5b6ca6946feef76`  
		Last Modified: Thu, 11 Sep 2025 18:22:40 GMT  
		Size: 15.1 KB (15111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09e566bd2e46f0e552be20f85fd0df9f3414a32fd1b11e6f6ebd7f201eb5d0c`  
		Last Modified: Thu, 11 Sep 2025 18:22:41 GMT  
		Size: 2.7 MB (2687868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c34f81e54ff6c095472761fd027d83d8f0e232b950f4790a59567107aa2e37`  
		Last Modified: Thu, 11 Sep 2025 19:32:48 GMT  
		Size: 365.0 MB (364951427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad33b89cee8bcca5f2f18cd318a127a80f252376d3823e328704f930e099bb5`  
		Last Modified: Thu, 11 Sep 2025 19:31:49 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104df9c56510451905399b2004ea49fcb6e688455cd8dd6fd653232a719c8e20`  
		Last Modified: Thu, 11 Sep 2025 19:31:50 GMT  
		Size: 13.7 MB (13705782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d519e26ba069377b1d31f61e1a470a70e928e1f2e6fb83dc242974774ef135fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f39d2b3d5cfd16524ba7a7f08b75043d60ddb5e65122066f574cea14a3b9a3b`

```dockerfile
```

-	Layers:
	-	`sha256:006a60ca315eed3d43031d274117a914e0f1fdfe44bd3b826cdc00d772cc62af`  
		Last Modified: Thu, 11 Sep 2025 21:22:17 GMT  
		Size: 5.9 MB (5946306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94a68ff927bfaca71667c8e46d43932857ca75ccef9fb0fdda6f9006000366e`  
		Last Modified: Thu, 11 Sep 2025 21:22:18 GMT  
		Size: 19.7 KB (19685 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:211fa7968fcaa329ff5cc06e61352b02fb4a8e3db0d143a58af4e287f157b1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.6 MB (500558569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2885da4c62c11ca2ccbe82b3a78cfc4a44afcc710b331c7ee97926b1093e55`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
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
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69dd744c6ce11f9bcc42b570d4944d0ecf9b125f3d1c222308ced56deb59072`  
		Last Modified: Mon, 01 Sep 2025 23:24:49 GMT  
		Size: 12.2 MB (12219976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f642f9167f61ba7b21e62a718d8c297bcf9e48728dcd239c5c9a7019e06704ca`  
		Last Modified: Mon, 01 Sep 2025 23:33:46 GMT  
		Size: 54.3 MB (54330700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611ab9bf5fc6a77b653a681f0f3b8a631253a3064c83f66011df823e04531ab`  
		Last Modified: Mon, 01 Sep 2025 23:33:42 GMT  
		Size: 4.6 MB (4606409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942b152eb90b6507bb295be0daf63c0f6c0e5b5fd411b17e43f9e5357de5d3fc`  
		Last Modified: Thu, 11 Sep 2025 17:51:58 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1804d2905aed0280229e26e12ad0c3456045c35e84c8e2938d01ead7b83940`  
		Last Modified: Thu, 11 Sep 2025 17:52:00 GMT  
		Size: 17.7 MB (17671933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9a34d0bfaa89bbbd30a560788a3da98385cf1fb079b831302c70e8d0f52faa`  
		Last Modified: Thu, 11 Sep 2025 17:51:58 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ebc705d5ce779baecd9722c27cad9688b6042337155563d725a1fd8133b56`  
		Last Modified: Thu, 11 Sep 2025 17:51:58 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da54a6984b3806fb3fa44aaa4d55edf1be4a4d1fe72b6930c50823febc91ab99`  
		Last Modified: Thu, 11 Sep 2025 17:51:58 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a149cf2397ae56d1dd76b16bcc0f8b45029c48415697322ab27305a7ddef4a`  
		Last Modified: Thu, 11 Sep 2025 17:51:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3f4e6e7e2aa14ab59f069f217eeb6c7487e0c8b97eea72f41573aa30bc90d5`  
		Last Modified: Thu, 11 Sep 2025 17:51:58 GMT  
		Size: 15.1 KB (15114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299ab75c0196eaa2826aba6a922d84f0cdc6ca59907d305206ef67cb318b5ee8`  
		Last Modified: Thu, 11 Sep 2025 17:51:58 GMT  
		Size: 2.8 MB (2839261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0aa2746b0b42bfba54ac4b7a7e68ef43d0469eaf68834cfb95db36ebc6620f`  
		Last Modified: Fri, 12 Sep 2025 19:22:34 GMT  
		Size: 365.0 MB (364950706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c9ecdcac28dfdaa6dcc55879e634ed9d5d53194d19dfaa691a4f05990689c`  
		Last Modified: Thu, 11 Sep 2025 18:41:42 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfd72cf261faabd9d83234a36b6cc8f09e5bc840f9fa3d4461c5552de2965a0`  
		Last Modified: Thu, 11 Sep 2025 18:41:43 GMT  
		Size: 15.9 MB (15870218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3dda3e3ba5ae9e53bc90ac359f95b62327abb0bf24378b24efc6777ebc7260e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4469aeec813e423bfa371a6d63a2cc9d56b1c59d3cabd90cbabfef8658f0849`

```dockerfile
```

-	Layers:
	-	`sha256:bf2350e10c623394a0a2cf4b48b09650dfd5552a80f111306f0b8f4c4ecc2cf9`  
		Last Modified: Thu, 11 Sep 2025 21:22:22 GMT  
		Size: 5.9 MB (5942702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b39793828ad600e16053d5a161db2050759b6191d9fc4abf86c1e06498404bd3`  
		Last Modified: Thu, 11 Sep 2025 21:22:23 GMT  
		Size: 19.7 KB (19658 bytes)  
		MIME: application/vnd.in-toto+json
