## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:d6aaecd753d7ba19e845c8e213d868cfe9b4ee7ef445cf6232c7a0b24edbeef5
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
$ docker pull websphere-liberty@sha256:8dbc3e4d8e9c756af6048294ec05f28b4cb6e67074b26aaf089b6ca4bca39b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.6 MB (493627591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a808015a14158ebf94a5a538c7ce3b341b05ff09e0c8fd36957cf93adba02163`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2025 14:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
USER root
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_VERSION=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.2 org.opencontainers.image.revision=cl250220250209-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.2 com.ibm.websphere.liberty.version=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.2 BuildLabel=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_URL
# Wed, 26 Feb 2025 14:51:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 26 Feb 2025 14:51:59 GMT
USER 1001
# Wed, 26 Feb 2025 14:51:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 26 Feb 2025 14:51:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 26 Feb 2025 14:51:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ae339e1ecda25aa01cf4c405ecc3339e3ba379f346e0e2e8ba327fe10b0a31`  
		Last Modified: Mon, 24 Mar 2025 16:59:44 GMT  
		Size: 12.2 MB (12166887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89e059daa51f3294ae04c2297c0df6c6e612e10c76cdc152809c3d82de3c82c`  
		Last Modified: Mon, 24 Mar 2025 16:59:45 GMT  
		Size: 51.7 MB (51659767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46042e8cfadfa4eb8d9ff49fba39363221a6dddd504dee4805484dbe995f5757`  
		Last Modified: Mon, 24 Mar 2025 16:59:44 GMT  
		Size: 5.1 MB (5074311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f93ff4d3ff5bcc3ec3d8a5366fad5b4e46fac3f40a9002fddbd902c9635547`  
		Last Modified: Mon, 24 Mar 2025 17:03:05 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f6739e2295c17d37b1191316866d79478fe458dcec0b136db39696c99cc1b5`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 17.5 MB (17506714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be053d4bf1e16a8c94f44f12e73a9c58a6f6a09a1caf035edd8c0cad341c0c8`  
		Last Modified: Mon, 24 Mar 2025 17:03:05 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734eed8516b23a87088c9f3147b37db5a255f9dd431e4d60e5cf07f43e4d123e`  
		Last Modified: Mon, 24 Mar 2025 17:03:05 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550157d138a45fa6701aed03178bb9b8a14a30595e27cab1012b9fddf1759108`  
		Last Modified: Mon, 24 Mar 2025 17:03:05 GMT  
		Size: 11.9 KB (11947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dba5338f5a7d05312d0080bbe2354ae5f8dbe8431798ff3eff3257ca567005`  
		Last Modified: Mon, 24 Mar 2025 17:03:05 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbf57c0fd76824e66c3a1d2925f390b3c107460d74ee7c99424a4decd31156d`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 12.8 KB (12751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8613e3514ea7be256a19ff8b7fb13698c8fbf1be3b8844c66479d874ae64c3`  
		Last Modified: Mon, 24 Mar 2025 17:03:06 GMT  
		Size: 2.8 MB (2838726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a00ec38e3a2fe41dd9a5e780c3a5065b82a729e19c9b96331447208b5e7125`  
		Last Modified: Mon, 24 Mar 2025 17:18:25 GMT  
		Size: 358.5 MB (358533641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87534bf5cf9d0f6af4eac60ff2b42debb32048f23e54cc194ba15e504acd51ce`  
		Last Modified: Mon, 24 Mar 2025 17:18:20 GMT  
		Size: 938.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0134a12ae7a9b2ea198c8877cbc26a54de941ab67af3f78ed5708cdafb5c5a`  
		Last Modified: Mon, 24 Mar 2025 17:18:20 GMT  
		Size: 16.3 MB (16251976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c7a88fe533578d4fe37b7d90085bdc0411101b6273f014e694594511895c0557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01423a4ca76c818f4f437e8ee96f137d75867e20ce876676b0ac565a31495799`

```dockerfile
```

-	Layers:
	-	`sha256:d86a3302ca86961aed5c08365f99fcd25fdb9a72b7ee10c92bdcbbc5d1511119`  
		Last Modified: Mon, 24 Mar 2025 17:18:20 GMT  
		Size: 5.7 MB (5737141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe393c4f1e4214720177d7fcc412fbcf6c8f5eae79946653c5c85e93b7b2e7d`  
		Last Modified: Mon, 24 Mar 2025 17:18:20 GMT  
		Size: 19.6 KB (19608 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:0d5f41c018c076fc39895856c93be5c2457f924464d14eec54ece07a52db33a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486315489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7202b7b8189ef7c3d09804fb592732e32ebc2fd06448530b4583ccfa0f5538`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2025 14:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
USER root
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_VERSION=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.2 org.opencontainers.image.revision=cl250220250209-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.2 com.ibm.websphere.liberty.version=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.2 BuildLabel=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_URL
# Wed, 26 Feb 2025 14:51:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 26 Feb 2025 14:51:59 GMT
USER 1001
# Wed, 26 Feb 2025 14:51:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 26 Feb 2025 14:51:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 26 Feb 2025 14:51:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e483842b440e4fd1b12a18bab983fb09c8751e230e70f7c022dae2765ea706a5`  
		Last Modified: Mon, 24 Mar 2025 17:01:02 GMT  
		Size: 12.1 MB (12123514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51776dd1b36a6774b3e410e2240d06d88f2438f6981ab29cca22ce5ddfa5c7a7`  
		Last Modified: Mon, 24 Mar 2025 17:17:44 GMT  
		Size: 48.1 MB (48083208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76ee805f80d071a780e257de1dd9de801efb61df1c3d9d001c9189e6fbf794e`  
		Last Modified: Mon, 24 Mar 2025 17:17:42 GMT  
		Size: 4.7 MB (4749183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42cc260384c7f174df1687392b411658125c1fe4797354959e56fb0debf6baa`  
		Last Modified: Mon, 24 Mar 2025 18:31:21 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59713b63961d468b2e3c75c73439e2a1623e58a748aee749ea29dd74a0dc57c`  
		Last Modified: Mon, 24 Mar 2025 18:31:22 GMT  
		Size: 17.5 MB (17506814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f97de347d49903288fdd9bf283791421253b2f4ac8bfad45bb07f019fb368bb`  
		Last Modified: Mon, 24 Mar 2025 18:31:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c595e33e5860d37cd0f08374a331baf798d32bc004c4f7e03124339694fe056`  
		Last Modified: Mon, 24 Mar 2025 18:31:21 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ccf573dae0899429d01c7b063d5283230851bb5e82daf56a1d7e7fa4e99201`  
		Last Modified: Mon, 24 Mar 2025 18:31:22 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9201acb03fc4ff7af2d517fbb145a77199d5d4978cf617218e6aa2abe50d98f0`  
		Last Modified: Mon, 24 Mar 2025 18:31:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b98c08766f44399086c304a83959a48639b9147b63e1c0897ad92848d9c2a16`  
		Last Modified: Mon, 24 Mar 2025 18:31:22 GMT  
		Size: 12.7 KB (12745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c92bf3b8094b347360808bc68d935d8bcd649de2f03f1f8c32127d66cbdf08`  
		Last Modified: Mon, 24 Mar 2025 18:31:23 GMT  
		Size: 2.8 MB (2779332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82dd1c90dcc03ba4fee5cdb914758ddd2261e5661e5e4e99212db0e628fbd5f9`  
		Last Modified: Mon, 24 Mar 2025 19:34:19 GMT  
		Size: 358.5 MB (358534231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d39968e8ef91c85209ab10c14c5f10da3395b584c6c10029a28e049eb8f1505`  
		Last Modified: Mon, 24 Mar 2025 19:34:11 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37175ba5f7f7030a05313e4f61ddd971eaee5984ca11c4ade7dad249021a664f`  
		Last Modified: Mon, 24 Mar 2025 19:34:12 GMT  
		Size: 15.1 MB (15110818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:dd25e31658891c2899ef06a7b63ba77244c49cdd1c48fda0b9b699a03d7397aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5750166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e1c291c8f243a8df98b2fbee4b5ab153aee434e2c50c93c0a20b49923f68f1`

```dockerfile
```

-	Layers:
	-	`sha256:92fc5c79d633125fe243a42f82022b0d3461def0ecb93b28bf6ae44641e8fec4`  
		Last Modified: Mon, 24 Mar 2025 19:34:11 GMT  
		Size: 5.7 MB (5730475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce4b34692fe4dec1120bd0e8bdfb637717a4c5097e89ce0c16ab59084bf747a5`  
		Last Modified: Mon, 24 Mar 2025 19:34:10 GMT  
		Size: 19.7 KB (19691 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a7296353d3841f39a05e85b1b6b00a744ec11ff3615f6fb79b19710e9d0e3853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.3 MB (496275460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70530a41067bcbee0c34ff14f6abd2d586c133d9e3dbdd206ac0e74630bd0cc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2025 14:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
USER root
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_VERSION=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.2 org.opencontainers.image.revision=cl250220250209-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.2 com.ibm.websphere.liberty.version=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.2 BuildLabel=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_URL
# Wed, 26 Feb 2025 14:51:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 26 Feb 2025 14:51:59 GMT
USER 1001
# Wed, 26 Feb 2025 14:51:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 26 Feb 2025 14:51:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 26 Feb 2025 14:51:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6a047babce01d9fd1ecd13e06fdd1fa8246e4c28a36772988cb5a72c0401af`  
		Last Modified: Mon, 24 Mar 2025 17:02:21 GMT  
		Size: 12.9 MB (12886676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb89c7adbd0ef0036365e6abc747aec5b816980cb153cd2d52f63ef79de4fd`  
		Last Modified: Mon, 24 Mar 2025 17:24:32 GMT  
		Size: 52.8 MB (52766915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de1666c6566f0f0e4360b9caf777c5620af11b712e9de379af59b2d3c1ea7d6`  
		Last Modified: Mon, 24 Mar 2025 17:24:31 GMT  
		Size: 3.8 MB (3807522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17a2e9226f9f0d7eb6564faa5a098286be347f89c3499f7cc301b72b5755690`  
		Last Modified: Mon, 24 Mar 2025 21:28:22 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc205fc0d0fc49b795e2578fde1794e16ee69c926e41c0143895bb144ef5998`  
		Last Modified: Mon, 24 Mar 2025 21:28:23 GMT  
		Size: 17.5 MB (17506936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5578930c7d919b22509fbde3771b70be5d3529b1f17005be85795c78a1136c`  
		Last Modified: Mon, 24 Mar 2025 21:28:22 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf89e0d421dba3f832f0b053456595f72ecf98481bd49e20b46427f5c612f66`  
		Last Modified: Mon, 24 Mar 2025 21:28:22 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539e62480758b01c9a4e8d6dace155c9386fc3970a8bd29c9c7c842f4e737aef`  
		Last Modified: Mon, 24 Mar 2025 21:28:23 GMT  
		Size: 12.0 KB (11952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ec49d3a00b55aa8ec86c74d3484c985d3fd0ad5a4080a52da3b2aaa896cef`  
		Last Modified: Mon, 24 Mar 2025 21:28:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cac6f7f5ee8fb7b0aa1e8b761473b35deaa797561e3f11d10e8ae3c73b24c1`  
		Last Modified: Mon, 24 Mar 2025 21:28:24 GMT  
		Size: 12.8 KB (12751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cdf57994c25aa8f79a76bf26480d320bc6e6964589d66daa730969482b24e5`  
		Last Modified: Mon, 24 Mar 2025 21:28:25 GMT  
		Size: 2.7 MB (2683663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bea092c11c34eca4cc411d1a0153ce86dff35b43c00e094a218274dd9727f6a`  
		Last Modified: Mon, 24 Mar 2025 22:22:01 GMT  
		Size: 358.5 MB (358533986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d15630026bf7ad81f2a5e847805751922888e47ec7c5477ec54e80fc21af45f`  
		Last Modified: Mon, 24 Mar 2025 22:21:44 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649a4aaa2c7dda36170603718e1394ae50e098433aedcf02abfc9af5a7ecb1d8`  
		Last Modified: Mon, 24 Mar 2025 22:21:46 GMT  
		Size: 13.6 MB (13577432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:54a85aecf7d085c9b916ecd9b56a39e34b84cb8d80cf1b218c25825ca3fce3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6579f32ca1a9aeb190a76c8941f3f0d8be1901c9ad22008c5e3476f3a1ca1d0e`

```dockerfile
```

-	Layers:
	-	`sha256:dd23afe6d421e5047bc176c28cfc270431ff2caf456f5418a398ee825db17050`  
		Last Modified: Mon, 24 Mar 2025 22:21:45 GMT  
		Size: 5.7 MB (5739150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9db8b3fd017d894c3cf8233c827d8dcb4a82b4406b5273ecd136fdffc5056ae4`  
		Last Modified: Mon, 24 Mar 2025 22:21:44 GMT  
		Size: 19.6 KB (19636 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:e9a8933029cd213ce1f544cd4019acb5f2682255438e82855d04103a1c0f8603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.1 MB (491100016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bda86e26f1844d1cadf81ce76796f6bd88f94fb706bea0ea35bda725826d038`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:03 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:03 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:05 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Sun, 26 Jan 2025 05:32:05 GMT
CMD ["/bin/bash"]
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Feb 2025 14:51:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_VERSION=jdk-17.0.14+7_openj9-0.49.0
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f26b2b2d8654a09fade4c0ce5819e72e00f1e751bb11a4731537e834900c3282';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='578a651e9e26de4ec30612afbd69c2530c8ed37db2c46bc62eb6a39dfa35c080';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e2469f16a616ee467d6a590ec043ee9464b039d2f9859327dd36d50953cd60bf';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='e96268d4daa6c5c2526f477ac563ef4851f0156ec67696fb855080704a5fd5c5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.14%2B7_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_17.0.14_7_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 14:51:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Feb 2025 14:51:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
USER root
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_VERSION=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_BUILD_LABEL=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.2 org.opencontainers.image.revision=cl250220250209-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.2 com.ibm.websphere.liberty.version=25.0.0.2
# Wed, 26 Feb 2025 14:51:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 26 Feb 2025 14:51:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.2 BuildLabel=cl250220250209-1902
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ARG LIBERTY_URL
# Wed, 26 Feb 2025 14:51:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.2 LIBERTY_BUILD_LABEL=cl250220250209-1902 LIBERTY_SHA=7a72444984453d9eede3253b5fb392c5fcd315ef LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 26 Feb 2025 14:51:59 GMT
USER 1001
# Wed, 26 Feb 2025 14:51:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 26 Feb 2025 14:51:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 26 Feb 2025 14:51:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 26 Feb 2025 14:51:59 GMT
ARG VERBOSE=false
# Wed, 26 Feb 2025 14:51:59 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 26 Feb 2025 14:51:59 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9a504edea95fbee01cd3ff3d84972a695acb9423b1d0fea8abc1fa3cac5e26`  
		Last Modified: Tue, 04 Feb 2025 08:13:22 GMT  
		Size: 12.2 MB (12212279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25177e93fa37880a2e2ccae237ff797be9876974c920901e302d5fdf003370e`  
		Last Modified: Sat, 15 Feb 2025 08:24:29 GMT  
		Size: 50.6 MB (50552916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943224d8881b66890ba0da5e5e0321ca37f9774acb064506e7d367f9e89e2938`  
		Last Modified: Mon, 24 Mar 2025 17:21:12 GMT  
		Size: 5.1 MB (5077304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7001301659e47d9b4afdd5c3992c60d9a237dfd80058b585691f215f6ad8407`  
		Last Modified: Mon, 24 Mar 2025 18:39:02 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6a27495aec1f0ae5bad47280046b19957a2fd1495ceb3c68c9b39a9e781779`  
		Last Modified: Mon, 24 Mar 2025 18:39:03 GMT  
		Size: 17.9 MB (17909647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae202889b7346a8ed55a77844fb4762fbd8488961ee12385a80c4f84e40f0bf0`  
		Last Modified: Mon, 24 Mar 2025 18:39:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec4eb3ff62a2bb69eea01c0f64f7da4c7ff9ca39603c6b7a88a1656d134e11b`  
		Last Modified: Mon, 24 Mar 2025 18:39:02 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3565712c0b47ec60edb93ad8cba31c69591351652579f4abf867ad31859b202c`  
		Last Modified: Mon, 24 Mar 2025 18:39:03 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6b6e4b95100fc72adbaf5cce47b4c416c805fb0ca86ae6363a26ea8f08c3a3`  
		Last Modified: Mon, 24 Mar 2025 18:39:03 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c963e45518ce14eeade3360053df83c2e8f056193d3c0774b7751583b5b340`  
		Last Modified: Mon, 24 Mar 2025 18:39:03 GMT  
		Size: 12.8 KB (12755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4322c54eb3ac12d0d9e0bf04d8d7160d0b602039e613251810c19e327906dc75`  
		Last Modified: Mon, 24 Mar 2025 18:39:04 GMT  
		Size: 2.8 MB (2789095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4901b1df1f98b2db09aa6d01359d0a12dc1ef880dbdecd4cc54120eb09fb0fe`  
		Last Modified: Mon, 24 Mar 2025 19:33:06 GMT  
		Size: 358.5 MB (358533790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c68bcf84d1bf676057193a590cad03ecf543bc38f6e34e498dae90c71f51968`  
		Last Modified: Mon, 24 Mar 2025 19:32:59 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63107f59fc1a958733b239fa9e8d4f8e963dbcf690b12b7184459409c2e7ea4c`  
		Last Modified: Mon, 24 Mar 2025 19:33:00 GMT  
		Size: 16.0 MB (15963046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3020ad5a3431274f4128499fdb4df8a5c5edb7f625f97f747f015ed7cb8f38a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5753684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc29e0b1c174450ef99fc0d443b26ba71d24a247ec8b5eed7c41d298fdd33949`

```dockerfile
```

-	Layers:
	-	`sha256:021a0d11a67bf96f2cb0768c8cc2e297a36ca51ca2f1c98edd58b6ca3f4ef60b`  
		Last Modified: Mon, 24 Mar 2025 19:32:59 GMT  
		Size: 5.7 MB (5734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564ecd67b96e2619b7ec0b94b33c720f9650bdfd2c9bfd4f695d200016849f32`  
		Last Modified: Mon, 24 Mar 2025 19:32:59 GMT  
		Size: 19.6 KB (19608 bytes)  
		MIME: application/vnd.in-toto+json
