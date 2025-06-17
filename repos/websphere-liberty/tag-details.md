<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `websphere-liberty`

-	[`websphere-liberty:25.0.0.3-full-java11-openj9`](#websphere-liberty25003-full-java11-openj9)
-	[`websphere-liberty:25.0.0.3-full-java17-openj9`](#websphere-liberty25003-full-java17-openj9)
-	[`websphere-liberty:25.0.0.3-full-java8-ibmjava`](#websphere-liberty25003-full-java8-ibmjava)
-	[`websphere-liberty:25.0.0.3-kernel-java11-openj9`](#websphere-liberty25003-kernel-java11-openj9)
-	[`websphere-liberty:25.0.0.3-kernel-java17-openj9`](#websphere-liberty25003-kernel-java17-openj9)
-	[`websphere-liberty:25.0.0.3-kernel-java8-ibmjava`](#websphere-liberty25003-kernel-java8-ibmjava)
-	[`websphere-liberty:25.0.0.6-full-java11-openj9`](#websphere-liberty25006-full-java11-openj9)
-	[`websphere-liberty:25.0.0.6-full-java17-openj9`](#websphere-liberty25006-full-java17-openj9)
-	[`websphere-liberty:25.0.0.6-full-java8-ibmjava`](#websphere-liberty25006-full-java8-ibmjava)
-	[`websphere-liberty:25.0.0.6-kernel-java11-openj9`](#websphere-liberty25006-kernel-java11-openj9)
-	[`websphere-liberty:25.0.0.6-kernel-java17-openj9`](#websphere-liberty25006-kernel-java17-openj9)
-	[`websphere-liberty:25.0.0.6-kernel-java8-ibmjava`](#websphere-liberty25006-kernel-java8-ibmjava)
-	[`websphere-liberty:full`](#websphere-libertyfull)
-	[`websphere-liberty:full-java11-openj9`](#websphere-libertyfull-java11-openj9)
-	[`websphere-liberty:full-java17-openj9`](#websphere-libertyfull-java17-openj9)
-	[`websphere-liberty:full-java8-ibmjava`](#websphere-libertyfull-java8-ibmjava)
-	[`websphere-liberty:kernel`](#websphere-libertykernel)
-	[`websphere-liberty:kernel-java11-openj9`](#websphere-libertykernel-java11-openj9)
-	[`websphere-liberty:kernel-java17-openj9`](#websphere-libertykernel-java17-openj9)
-	[`websphere-liberty:kernel-java8-ibmjava`](#websphere-libertykernel-java8-ibmjava)
-	[`websphere-liberty:latest`](#websphere-libertylatest)

## `websphere-liberty:25.0.0.3-full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:c8ec0f758c41f8c613e8b6bd924cc2133735bc0bff032c97bcdc253efb12d96a
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

### `websphere-liberty:25.0.0.3-full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:40f04c1ef3e1dbb0678914d3c973943ad6ed4e422c1df5594ef3334bb42ad16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.5 MB (493456826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814c22d31596045ec7904990d7ca73e4a87396f84844f426c022b4c9f1ba2cbf`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473154fee0b11bc4d722e43c237f237b69136a24301983502078bc9dc527d0bb`  
		Last Modified: Tue, 17 Jun 2025 17:12:24 GMT  
		Size: 12.2 MB (12172067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb6ba5b52910f78ab9354ac0ad75ba2f1a919068cd8106ef806ea4bc865d2f3`  
		Last Modified: Tue, 17 Jun 2025 17:12:26 GMT  
		Size: 52.5 MB (52456010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3b6884b3df4e65f651464ae3b2df0d53a464c4c7a76e9bcb1b39223e674f69`  
		Last Modified: Tue, 17 Jun 2025 17:12:22 GMT  
		Size: 4.4 MB (4407179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f253e02a1d82e301299973b8697a93f1d7847bbd0ded63f396a825480837c224`  
		Last Modified: Tue, 17 Jun 2025 18:08:14 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c9b35e6df7d5d4f360cbcbfe1efd42a9244e1c913211ee66b91c327d84cc0`  
		Last Modified: Tue, 17 Jun 2025 18:08:15 GMT  
		Size: 17.5 MB (17548974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ec357ae3b8cb15bc1bc8f1287f277bc43c461f95eaba6d107b10cfb510679`  
		Last Modified: Tue, 17 Jun 2025 18:08:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fe948ba37518c0caba3acb1e6b7835f05cad964ce69ac0c73ca051addf4bb9`  
		Last Modified: Tue, 17 Jun 2025 18:08:13 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca2df483fd3202f401ff6d39b1b092fbdf6a10064ca53f51e2ddc3318d91e6b`  
		Last Modified: Tue, 17 Jun 2025 18:08:13 GMT  
		Size: 12.3 KB (12306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d47062e33638cbb4f5616e78fb3a360b000d8e7d1a2e3939078b0fe89de097`  
		Last Modified: Tue, 17 Jun 2025 18:08:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86085e54b7097cf949f6b0978694bad145cdd9754e89e947b6d22852988c09c`  
		Last Modified: Tue, 17 Jun 2025 17:23:17 GMT  
		Size: 13.1 KB (13117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226bb9a0e1fb3b75aeeb8f10fef5caeeea11f1c6b83fcccb18ab9288cbda9f7`  
		Last Modified: Tue, 17 Jun 2025 17:23:17 GMT  
		Size: 2.8 MB (2794554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c30f4b2d45a149105b7b3394bda91ee937c7f6bfe07a6003edcd7b54e476c67`  
		Last Modified: Tue, 17 Jun 2025 18:20:51 GMT  
		Size: 358.7 MB (358661740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a96ccbf72707728c92e9d0d0fe606a31c2c34d71225eaf126ecff8f927fe4c`  
		Last Modified: Tue, 17 Jun 2025 19:22:38 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a900e90f1ecac991e73c3d463b1c2357eb9f25995cb96bf0d887678270bb8e6e`  
		Last Modified: Tue, 17 Jun 2025 18:20:46 GMT  
		Size: 15.8 MB (15822941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:6d94a7b5c267ece6f905a51e350a2ebf25c2bfa328ec4df7e0b86d63896ad46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5933353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f72aa2c145c1672bdedca6554c6524b88a67a2a346f3f3547513bcae6433bb9`

```dockerfile
```

-	Layers:
	-	`sha256:de7151a6dc1c333d06b748a5947080a91e35b2608e0ead30173f2d100840e293`  
		Last Modified: Tue, 17 Jun 2025 21:21:17 GMT  
		Size: 5.9 MB (5913700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ea769f4df65d68d79d5edcc67605579c4b92398c04c0065a30e3293c5a3efc`  
		Last Modified: Tue, 17 Jun 2025 21:21:18 GMT  
		Size: 19.7 KB (19653 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:d4f440329789bcdf91bbc7b4aeb00825e44873dc5f9b43ec71e9a2720205f101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.7 MB (486730713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5690a58cf28f0dd45947d8f2442f60cda382a25fddc37141bd13a2b732b08d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbff14187feb7082a330fc6604f5d950114fba77a27a3564014bdeb0c0a7e399`  
		Last Modified: Tue, 17 Jun 2025 17:39:17 GMT  
		Size: 12.1 MB (12129302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79aed8751db549046792bc777edcca525eedc89ebe93460c37e203404f05870`  
		Last Modified: Tue, 17 Jun 2025 17:46:33 GMT  
		Size: 48.9 MB (48888727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a052f878cd6890586d100378a6682fad252e4a82b6954453d38c3f7e738bc00`  
		Last Modified: Tue, 17 Jun 2025 17:46:30 GMT  
		Size: 4.2 MB (4197882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797fedeb23be889d0b30f85fb1efe5b858deac6b9fea619ff4df2a7616170d6`  
		Last Modified: Tue, 17 Jun 2025 20:19:09 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bdd6e20b67da0a847e9b8407d69511f4f79abfaf82dbb7308976776aecd923`  
		Last Modified: Tue, 17 Jun 2025 18:38:20 GMT  
		Size: 17.5 MB (17549146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775db8156f7d1e5ca49b54dd0de8bf3e4d9fdfde1b8ba4208e15e9c8059a6ce`  
		Last Modified: Tue, 17 Jun 2025 20:19:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e14da213dfe89dd911f966330862c7078a0d7e4fd6148502665992ffde6fda`  
		Last Modified: Tue, 17 Jun 2025 20:19:14 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615fb644c386391be338e2f582eebf297136e8fd3908f6c845fe29afa4bc3a5`  
		Last Modified: Tue, 17 Jun 2025 20:19:16 GMT  
		Size: 12.3 KB (12306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb6f3d4e75aac506db409464ff93dda077377bf5a1fecc7712ba3f2642cd54`  
		Last Modified: Tue, 17 Jun 2025 20:19:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb6ebe6508ae27cd63eb4254bffc07b64e7da4b6a6b947b81be6831fc6b7f27`  
		Last Modified: Tue, 17 Jun 2025 20:19:22 GMT  
		Size: 13.1 KB (13115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc810f71a1c2f5884f4376ff19d34c1095b233de0bff5ffb8bce727139d612d6`  
		Last Modified: Tue, 17 Jun 2025 20:19:25 GMT  
		Size: 2.7 MB (2742091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3351b3f88da9ebbae430263d96a285af11216db97641d1379cfcf74476185f6`  
		Last Modified: Tue, 17 Jun 2025 19:59:59 GMT  
		Size: 358.7 MB (358662047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd9f0acf111c84eddbcf92b138423f247a9ecae547ed1ae8e77270dc39899b6`  
		Last Modified: Tue, 17 Jun 2025 20:00:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb72acac9cc4496b6631b30922cffa1ea7f481ecdc1861217a9744aec243030`  
		Last Modified: Tue, 17 Jun 2025 20:00:22 GMT  
		Size: 15.1 MB (15135002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3399664f2fab96857a57644c56cd9e1731927f32b3378988df5d5c16d9e9682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df395f01b37b3ab02bfa24cf6ce29cc82c460634594619632ce7d685c90f8bc2`

```dockerfile
```

-	Layers:
	-	`sha256:12dfd24a6e17f1a3b976a17a58932c5de38177b02c84a1a23d004e5d4f1f884a`  
		Last Modified: Tue, 17 Jun 2025 21:21:23 GMT  
		Size: 5.9 MB (5907034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff554dd90e5d7fbcb3ddbf44dbae0cb8825b281a302c847655bc0bc554ac3bb`  
		Last Modified: Tue, 17 Jun 2025 21:21:24 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:0758ff12f786c24ddd09f395ba75b6c4681d3767ec01f0b6a62b6a3bebfe0e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.4 MB (497430308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d217f92fe4b9bcdd6baa6e2f5f50ba97c91f2a6329b13119da83525e85ed220`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c0a1fca7ea07c8c5a127826c7981b2bbb00fab8901f776e93777f6b6e7e19f`  
		Last Modified: Tue, 17 Jun 2025 17:55:19 GMT  
		Size: 12.9 MB (12893311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe643e2c62ba3b29b36e85d1c1b3ad4b19b8525dc1c11534591b5a897b87108`  
		Last Modified: Tue, 17 Jun 2025 18:04:01 GMT  
		Size: 54.1 MB (54102703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff5d8745a02d7d1739003a9cbb478252421dfc67060330461e18b9750223855`  
		Last Modified: Tue, 17 Jun 2025 18:03:48 GMT  
		Size: 3.5 MB (3464435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a33987f5b67e9ab8ced0e6028829f130114f59a3c08ae2786e5e2c2b665f6`  
		Last Modified: Tue, 17 Jun 2025 18:44:40 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fef314da6e05555f8bfe4231f612eac836d45ce987a316796f1f2ccb8389c48`  
		Last Modified: Tue, 17 Jun 2025 18:44:42 GMT  
		Size: 17.5 MB (17549347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8395adfbb6d00f2c074bf211dffee40de65078b2522688a783c995b2261d318`  
		Last Modified: Tue, 17 Jun 2025 18:44:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c74b667470251f3083ad7557a7a5498fb1bf03b763b82d6c1eea79ab434d379`  
		Last Modified: Tue, 17 Jun 2025 19:14:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f3302d77673f70fb8b340ba8edbd8842e938e05c66b9c16b47e625c09a197e`  
		Last Modified: Tue, 17 Jun 2025 19:15:00 GMT  
		Size: 12.3 KB (12309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea21c8b957b37cc6b2da010a9762f9404d32aa4193c342f7eb93cfce4b6aaf5`  
		Last Modified: Tue, 17 Jun 2025 19:15:04 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5146b32f13c4e27e0946d0aae93d2f4f7ea3ad39dbe665121d380f7861dbc4f4`  
		Last Modified: Tue, 17 Jun 2025 19:15:08 GMT  
		Size: 13.1 KB (13112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40387502de30f0c776ff631a797b2ab8a19657d0fed73e8381e34a92ecbf37c4`  
		Last Modified: Tue, 17 Jun 2025 19:15:14 GMT  
		Size: 2.7 MB (2666546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ba9ff55cd7d436d9844c5faa22af4d983c43726e75d0361358337e6a2ba8a9`  
		Last Modified: Tue, 17 Jun 2025 20:13:06 GMT  
		Size: 358.7 MB (358662964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d858555eb926fb74d8dca7626b7ae28b6e71c100e5df7c9023c84c87dd9e1ec7`  
		Last Modified: Tue, 17 Jun 2025 20:19:15 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6bcf8592b5b7ae33cfec87bbde386dfc1797128d7e2418a15f296a1da01c8d`  
		Last Modified: Tue, 17 Jun 2025 20:12:44 GMT  
		Size: 13.6 MB (13585535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c9bdfb378433edd13ab731b9740b7507fff335726d08fbab281def5643abd0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5938002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abff47d146832c8fc3c30d04c287a2ad757a06f33c027b22acc8d45e695e95f`

```dockerfile
```

-	Layers:
	-	`sha256:ac2b7ef0a43af89c7b8bf93e309c3f8f5c4bdc5cc2200b04952a4e16e30e58e3`  
		Last Modified: Tue, 17 Jun 2025 21:21:30 GMT  
		Size: 5.9 MB (5918321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f34446e262f81e8a67adaa5ca007fca42c95ae817a7a3ac4f9f89c6fe1254ad`  
		Last Modified: Tue, 17 Jun 2025 21:21:31 GMT  
		Size: 19.7 KB (19681 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:3a6a3a3bd3c21a806b2f71c66c325a4fcff90bc2f8febfc95a5d91307ccfb13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.9 MB (490882848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b0e6cb0332665649495c0c7b73305840725c2f863d014d47816b2cdcb09dd5`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 23 Apr 2025 12:53:39 GMT
ARG RELEASE
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 12:53:39 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Wed, 23 Apr 2025 12:53:39 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 12:53:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 12:53:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 23 Apr 2025 12:53:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 12:53:39 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Apr 2025 12:53:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
USER root
# Wed, 23 Apr 2025 12:53:39 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:53:39 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 23 Apr 2025 12:53:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_URL
# Wed, 23 Apr 2025 12:53:39 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Apr 2025 12:53:39 GMT
USER 1001
# Wed, 23 Apr 2025 12:53:39 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 23 Apr 2025 12:53:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 23 Apr 2025 12:53:39 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 23 Apr 2025 12:53:39 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:53:39 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
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
	-	`sha256:0262374bfd97f3bd75b20491f24b9937826c63aaf312d64408caf3704c44d14f`  
		Last Modified: Fri, 09 May 2025 19:03:54 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36afa484d60079569b7936f58360c056e5dd912711a3598a91f66ae097e75b25`  
		Last Modified: Fri, 09 May 2025 19:03:58 GMT  
		Size: 17.5 MB (17548736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0a64eb2abfb0bf9978f6fbac2ad15f7917892a3c0e93c28e599043254bd26d`  
		Last Modified: Fri, 09 May 2025 19:03:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf18d9cda9bf0d48f857debca5b9d3f3a8274db7e576a962b66f1c5505e5a20`  
		Last Modified: Fri, 09 May 2025 19:03:55 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703ea0664a306728895277e291926642ace395b5fa90c3eda828a35958ec7925`  
		Last Modified: Fri, 09 May 2025 19:03:54 GMT  
		Size: 12.3 KB (12311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a028d7fb8995e3d5777ce401f6e1bf577f2ed64081e8af9b6db299af4e54a6`  
		Last Modified: Fri, 09 May 2025 19:03:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9281005ca1dc62d5692ae4be50f27e36cc3509cc88df62313ac6eb6aeaef50b`  
		Last Modified: Fri, 09 May 2025 19:03:55 GMT  
		Size: 13.1 KB (13119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d019b268c49894baedd1ebfeed9a63e13367542e5c9582b48c288faa77fcb011`  
		Last Modified: Fri, 09 May 2025 19:03:56 GMT  
		Size: 2.8 MB (2796134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c1b0260f9817f2e57e36cfed3bbb1bf07d0aa3f043452ee817232dba844600`  
		Last Modified: Fri, 09 May 2025 21:18:07 GMT  
		Size: 358.7 MB (358660770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461277685a9733ffd197b1a7d263b7df84fdefec9b12dbcea436f22f995411f4`  
		Last Modified: Fri, 09 May 2025 21:18:00 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1032c8c195add568d22fa4394f66225ba0f94eb9356dfdd2ac5429383ebbd09c`  
		Last Modified: Fri, 09 May 2025 21:18:01 GMT  
		Size: 15.7 MB (15671795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f5e7991c16b09b5dd34f167f5fcfea5f4e9e8f192b8348763e213019d4e07a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827ad61d118be4182863916edbe4af7f4e3640cd0b4e5da35a9c6c9b7cedcabb`

```dockerfile
```

-	Layers:
	-	`sha256:509b6de34cd2698191c96229520796f31a10bd457124fafb91061128a9a754fd`  
		Last Modified: Tue, 17 Jun 2025 21:21:36 GMT  
		Size: 5.8 MB (5752384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd3e4238ccb1da5250c1e3dcba6244c0b7ef90998e1eb41b2601352e293a797`  
		Last Modified: Tue, 17 Jun 2025 21:21:37 GMT  
		Size: 19.7 KB (19653 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:25.0.0.3-full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:e26dddce57173b43986086dcf8bfc35c13fe2a949d3ccc9d05d14780b110e612
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

### `websphere-liberty:25.0.0.3-full-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:71fc39bbfc8ed87a285285cb1bb4bdb2816ea7dbc5a06a7541cab9ba26f9e75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.6 MB (493613230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5060bc99adfd4aad875f83843fe52d381b6bb41edb7d097acd7a884f191e12d0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe200c80616675d621c20320c6bbb63824ebb52e7f77cafc18893533d2fb4fe`  
		Last Modified: Tue, 17 Jun 2025 17:12:27 GMT  
		Size: 12.2 MB (12172168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3082e23860276aa9c4c2d43b942c9e25dd1e69cce4d58c23a39cb9f13dae081f`  
		Last Modified: Tue, 17 Jun 2025 17:12:32 GMT  
		Size: 51.7 MB (51747278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac736981419aba48890e57917cf88e9ccc539a4c3858ae03fd6c2d790e925db9`  
		Last Modified: Tue, 17 Jun 2025 17:12:27 GMT  
		Size: 5.0 MB (5015886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce2b7a772df81befc4fb1f50009d1aa66e4d4d5fbdae43fe9ae93875220c852`  
		Last Modified: Tue, 17 Jun 2025 17:23:14 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445b8c106b2980343a23d7297a28dd4a4595650b4f20715538e83b478bf751d1`  
		Last Modified: Tue, 17 Jun 2025 17:23:17 GMT  
		Size: 17.5 MB (17548969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4f5874fa4ca7cc76abbb6c841b5af7908d1014532e5a08052458ff3dbf7bf7`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dfa75de55a4e72bb3a44140b88c44e422bb9192603093c13de7526849dea01`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a160876bd288671d34c649daf03fc26290801f1bbb95c835d55d02f84efb11`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 12.3 KB (12308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf5c20227c0f80e3e955d634a8287d0a2229f01ca999c9ac357107bbfbe4d2d`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341404d690b84ad0c621dc4f4514baec757766c62cb9bba045cf36a346e152a4`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 13.1 KB (13124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a35921ba67d64292f36a2bac0219b1c350db0acdd35233ccf64cb2a2d6d10ac`  
		Last Modified: Tue, 17 Jun 2025 17:23:16 GMT  
		Size: 2.8 MB (2792510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0a686737854ede7b05c9cb6531a0b45b2b3e77cc4069ee7960cad56d1ecc1`  
		Last Modified: Tue, 17 Jun 2025 21:25:22 GMT  
		Size: 358.7 MB (358662027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cff605eb7542c9d1ff6e81fe9bcaaccd1311396c13edf44598e35eacb1ff79`  
		Last Modified: Tue, 17 Jun 2025 19:24:22 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fa6394bb150300e69716338a60a22238f14de57a5e5603eb566ecc9283e02f`  
		Last Modified: Tue, 17 Jun 2025 21:25:15 GMT  
		Size: 16.1 MB (16081016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:219101f05c7036b09aa5a9c4a11b25e1782d10a7c4a8307c543b861ea463f41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5920224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a081e1596dab1642f441a0bf09d80ef2aaf311f3b52dadaa3e445ecd288eeb`

```dockerfile
```

-	Layers:
	-	`sha256:ced167f4aa248fd41d057ef77b81d87138eb023663d8e1a44297f7cc3847e2fe`  
		Last Modified: Tue, 17 Jun 2025 21:21:31 GMT  
		Size: 5.9 MB (5900571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a320fa2a6c418d5f332f3298b1145a452f2bb6fb058042109e7b47a2887e`  
		Last Modified: Tue, 17 Jun 2025 21:21:32 GMT  
		Size: 19.7 KB (19653 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:4a79d01c9bb9b55c8b2c3ea44eca9d656f901359fe2e1a535d63e4ee171ce29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.7 MB (486725837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0dfa42f3ac874422651d580064a1f292c89b791394aea6a460a55160b10362`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbff14187feb7082a330fc6604f5d950114fba77a27a3564014bdeb0c0a7e399`  
		Last Modified: Tue, 17 Jun 2025 17:39:17 GMT  
		Size: 12.1 MB (12129302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326fb85a67774b17b7c5a12fd977330d9e887967a18c65bb56fb69873a7c1945`  
		Last Modified: Tue, 17 Jun 2025 17:51:11 GMT  
		Size: 48.2 MB (48190778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5845461e49b7f17a73c1fa99239aa56d56598a789b478642b473201b34ae43`  
		Last Modified: Tue, 17 Jun 2025 17:51:00 GMT  
		Size: 4.8 MB (4807240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8f0c47bd8478fdf1fc7ed948e06551476396eae8d6984624c535a67020ac95`  
		Last Modified: Tue, 17 Jun 2025 18:39:21 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53eaf58d0c43ea5989099ce7dd25144154a771b1f950cd90f84bd4927cf1379`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 17.5 MB (17549134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28fe897212ec6f5fab9dbf65de42971b3e94ea13abe7b5fb532491ab04eaccd`  
		Last Modified: Tue, 17 Jun 2025 18:39:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18666ac700e5501ec1ea53702a82c6f0d3ae217012c221e74f05add227baac0c`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c94eb2aeb858af32a68302246df7907fb69c0790ab8831341bd7ca4dae48745`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 12.3 KB (12307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bffc2b687009c58926b580de121d301f65f2e35f15ac838cafc8c32032963e`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ede735e232c48b192699e550c05540f1dc3ab10e0e0fa70b6cdad412f2889`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 13.1 KB (13115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6015864d2e723608f0144f87fdac0243b48ae26319ea1ed9139ecbdbefcec5`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 2.8 MB (2791866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e9f3f9792428fcc11a7cdc0e0582433e029bed3cbdfe820f6e6839cedfff`  
		Last Modified: Tue, 17 Jun 2025 20:17:24 GMT  
		Size: 358.7 MB (358662689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675a32b0225d6f9d0f5eab22fc3c048afeb83de1e98c7671bb9ce13cf19969e7`  
		Last Modified: Tue, 17 Jun 2025 22:00:31 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ba4fec2a3cc6a779f9a196dd5e2252493b4d80104fdc11de75efc9e88a4a9a`  
		Last Modified: Tue, 17 Jun 2025 20:17:16 GMT  
		Size: 15.2 MB (15168309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e02d693d39018a51fc3aa50a59a2b59ac2036ad5cf73243808ef916a33d9bd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5913640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50590b36342ed3a76e96a318ecdefa4ea404d98aa8249b5968b36c36079c372`

```dockerfile
```

-	Layers:
	-	`sha256:36d7d45ed59873ee2c8b68416625cd7f959be0e632e3fa287bb328aed5c6e715`  
		Last Modified: Tue, 17 Jun 2025 21:21:38 GMT  
		Size: 5.9 MB (5893905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdd7b74a82e807f86694e54b2952dff8b57d7b22ac4d9e6d516fe00cfb7aa3b`  
		Last Modified: Tue, 17 Jun 2025 21:21:39 GMT  
		Size: 19.7 KB (19735 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:941b1d762400b629c5475e4d5a73fb9742223552579f9920cd346eb0003e7abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.1 MB (497131800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f429fe06d7d73e7a54eea026030e3eb8f006e3d88ea0adeac46817e27b18a2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c0a1fca7ea07c8c5a127826c7981b2bbb00fab8901f776e93777f6b6e7e19f`  
		Last Modified: Tue, 17 Jun 2025 17:55:19 GMT  
		Size: 12.9 MB (12893311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5a341607cddf9964b5f321192ee5159f90ea1e77114afa75d67d56e09ff152`  
		Last Modified: Tue, 17 Jun 2025 18:09:11 GMT  
		Size: 53.4 MB (53352856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652393ec25233ac2529d30f8aedf8fae2534e6dbe003ed83ba345e7775d7e71e`  
		Last Modified: Tue, 17 Jun 2025 19:56:14 GMT  
		Size: 3.8 MB (3832349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abff2a84a658b02323f9f6a33c251ca1a805783be3b4ea7c8e3b4826adc847c`  
		Last Modified: Tue, 17 Jun 2025 19:56:19 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db2d2ce6a798183933de67fe00bc90457be5837a49e25fc02822cbda63b75df`  
		Last Modified: Tue, 17 Jun 2025 19:56:21 GMT  
		Size: 17.5 MB (17549364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d96fa53c08da8d805334fd78311a8e558e9e94f9a8ee014c174ced0e9df6771`  
		Last Modified: Tue, 17 Jun 2025 19:56:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e167db2b65a9b61d8814fb33de1f98450cd14bb47d49cc1425d1d89c18c93a0f`  
		Last Modified: Tue, 17 Jun 2025 19:56:17 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d034e14c81ac42aa6db6268a030411f81b081648b6dcd50c0fedf53a71657c5`  
		Last Modified: Tue, 17 Jun 2025 19:56:18 GMT  
		Size: 12.3 KB (12313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8aa037db5154ddcee578eae16e51d2c629bf2649bbe6ccdd0111039eb5761f`  
		Last Modified: Tue, 17 Jun 2025 19:56:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772894a21e0626867243f211517c14036c5bf38c84e923efe9357fcc19cb19c1`  
		Last Modified: Tue, 17 Jun 2025 19:56:18 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54359e10265f3db0b3c4a791fef2de501c9f56748549013cfe86a342cbac6ce`  
		Last Modified: Tue, 17 Jun 2025 19:56:19 GMT  
		Size: 2.7 MB (2684971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466939dac40791b341ec2ee983cb42aac4978167bc520ea9c88b4dee7e3c4180`  
		Last Modified: Tue, 17 Jun 2025 20:35:10 GMT  
		Size: 358.7 MB (358662861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4b73140a30aa0022aa99ba2b7c70d484b61bdbc430851756887d074462c83a`  
		Last Modified: Tue, 17 Jun 2025 20:40:56 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3286ced71ee886fcb5b350e9c0f84728ca000dfebf2a7b4684dfd1932423c98`  
		Last Modified: Tue, 17 Jun 2025 20:35:02 GMT  
		Size: 13.7 MB (13650600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:eeb2414ae06a8ed1968a0776d2883fd1be1a672143fd2b0bb1e534f6745ceace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5924873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1852041b8a6f1cadfc0b7cf00e898589e129a931a633d95f76c9d35bceb2cb`

```dockerfile
```

-	Layers:
	-	`sha256:d1603ea7e705973b01057f80a6103c0dedf999aed92d0b157e1e0420a9974b97`  
		Last Modified: Tue, 17 Jun 2025 21:21:44 GMT  
		Size: 5.9 MB (5905192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1897718f3ddae38df2c1833084218a96543bbe1f72cb8485db52d41ad0ba0b90`  
		Last Modified: Tue, 17 Jun 2025 21:21:45 GMT  
		Size: 19.7 KB (19681 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:14c34281999d9d56033b00e8d34e74b7cb01e9dd1d0169637b25e3afe5b7fcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491522185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e41c0b665b8b206d1873e3e34a1a88e091a1d729295003decc3e864d2ea78c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 23 Apr 2025 12:53:39 GMT
ARG RELEASE
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 23 Apr 2025 12:53:39 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Wed, 23 Apr 2025 12:53:39 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 12:53:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 12:53:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 23 Apr 2025 12:53:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 12:53:39 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Apr 2025 12:53:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
USER root
# Wed, 23 Apr 2025 12:53:39 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:53:39 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 23 Apr 2025 12:53:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 23 Apr 2025 12:53:39 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ARG LIBERTY_URL
# Wed, 23 Apr 2025 12:53:39 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Apr 2025 12:53:39 GMT
USER 1001
# Wed, 23 Apr 2025 12:53:39 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 23 Apr 2025 12:53:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 23 Apr 2025 12:53:39 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 23 Apr 2025 12:53:39 GMT
ARG VERBOSE=false
# Wed, 23 Apr 2025 12:53:39 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 23 Apr 2025 12:53:39 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 23 Apr 2025 12:53:39 GMT
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
	-	`sha256:87c722eb1e516a736ab709561aaa1b82a951c0d4904e0d46a859b928acffa44a`  
		Last Modified: Fri, 09 May 2025 17:06:04 GMT  
		Size: 51.1 MB (51093317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c467b8956cc0ad8f37d6a013e09e17d8d05f76375bb59636f4848010d0197`  
		Last Modified: Fri, 09 May 2025 17:05:52 GMT  
		Size: 5.2 MB (5177039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e64922e8cf7bdd561baecf5417e49987d52f0ae4afae8c2f746896fad7e8c2`  
		Last Modified: Fri, 09 May 2025 19:04:09 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f068f019a6486750c67f931a2230eb3112bfb68e91d3491fc913da4f87e405a`  
		Last Modified: Fri, 09 May 2025 19:04:14 GMT  
		Size: 17.5 MB (17548718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798926a9af2d1948c668945a85bf014498252ac6de616f3acaa55c5e8a89e769`  
		Last Modified: Fri, 09 May 2025 19:04:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac461507f68600147ce71d0dc163467e1848e81adba274c61f3efc4d072fcb74`  
		Last Modified: Fri, 09 May 2025 19:04:06 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e01a56a8f316883a0b3ce9b9d84a3bd9746c9840d2d849b6309237de417188a`  
		Last Modified: Fri, 09 May 2025 19:04:07 GMT  
		Size: 12.3 KB (12310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c2aab3c3203467acf779f377b0304c27d0e20d49dd8590a2a05b15fa77209a`  
		Last Modified: Fri, 09 May 2025 19:04:07 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce05075c16973552f1124055851a065d620055c6491bba1caa040cff34c58753`  
		Last Modified: Fri, 09 May 2025 19:04:07 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84dfa1b38e16bd2652158804fdf3349a8ce57c3545fbaf55181c6e1bb21bb60`  
		Last Modified: Fri, 09 May 2025 19:04:07 GMT  
		Size: 2.8 MB (2791892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338c231e29f7c85c9a4aa07c6a4f580ff8da697780496e2763249e445c54a656`  
		Last Modified: Fri, 09 May 2025 21:32:20 GMT  
		Size: 358.7 MB (358661971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f03338329a64a239e359081a766568cde9c74e1d1748b0c4932692707bc3a1`  
		Last Modified: Fri, 09 May 2025 21:32:14 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e212d07b6c4bbabc0569230c7616e26ce0ee83894bf5d857130daa467df5db`  
		Last Modified: Fri, 09 May 2025 21:32:16 GMT  
		Size: 16.0 MB (15968331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:61ac9cc70fefe8e9da88c0ed18aeb85303d6874f60a14d021b5232729cbcec5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5758908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ac2ab51aa794bb407d63d1267be045e6d30427c206b1314957ecbd0799b60a`

```dockerfile
```

-	Layers:
	-	`sha256:e8f9fdcd62e736315b56b4ee84a1596686c4e9b8278c79b7fb688e68b031f0fc`  
		Last Modified: Tue, 17 Jun 2025 21:21:51 GMT  
		Size: 5.7 MB (5739255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0f34dc1eec338f17f6a48810411621af322fe6de1eec7969e879e379ae8718`  
		Last Modified: Tue, 17 Jun 2025 21:21:51 GMT  
		Size: 19.7 KB (19653 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:25.0.0.3-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:f1262482fc9ec35c811c1d7580ed230ff62a8d11c4ef4b3210b6c030ce819233
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:25.0.0.3-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:2c89caa16ba6c7bbb74346611c113d7ce861fc9659ed5f220af0df6de5e4ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.7 MB (564653254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16b67ab7692ea1c17b482180d0288f66cc13265ecf32c4e9e4ffa72c87364bd`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a6eae1ced04a72a3e7964ca3af1d5775c7934f0bce2fac7626d1c924e20ab1`  
		Last Modified: Tue, 03 Jun 2025 16:06:17 GMT  
		Size: 113.7 KB (113705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1ada3fae0c70352747fb8df137c637ee3e233f4ceff2df47c267bec08d230`  
		Last Modified: Tue, 03 Jun 2025 16:06:18 GMT  
		Size: 17.5 MB (17535328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daefa2cabcd02e82430decf2785de235d7afb113be301c67e0469ad7766332d`  
		Last Modified: Tue, 03 Jun 2025 16:06:17 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231c74b99f2dab912410ebd914c8e042c922aa6aabf50df9ea90cb5ee622009e`  
		Last Modified: Tue, 03 Jun 2025 16:06:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7221d65a1e36b154e5b32ed5aeeb112cdf7750c901aba007346a1430d0467751`  
		Last Modified: Tue, 03 Jun 2025 16:06:19 GMT  
		Size: 12.3 KB (12318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29725d65fb0f7e7156d9f182f75439fd4c4a4a8712105dc049207bfec81af73`  
		Last Modified: Tue, 03 Jun 2025 16:06:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1ae8eb37f8eff86a3abec7fee59cb5cdc47407550c61b285ace5054f04c825`  
		Last Modified: Tue, 03 Jun 2025 16:06:20 GMT  
		Size: 13.1 KB (13124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c5fc3aa82ce3456016b4d46773db6920a0f2daec0f980e660381610b97f1ae`  
		Last Modified: Tue, 03 Jun 2025 16:06:21 GMT  
		Size: 5.8 MB (5827949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9598dab35bc7a8a8ab629a6730568c2f4ddcd9860a8fedf319f07b04dcf85c`  
		Last Modified: Tue, 03 Jun 2025 16:17:17 GMT  
		Size: 358.7 MB (358662066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4d7e49a86608730305bc3e484b05a1b6f2c434744d18663c55b44d0f345c43`  
		Last Modified: Tue, 03 Jun 2025 16:16:14 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8831a222f0407e55c55a14be020ae1cff16be9c23ebbc3e5fd3d683032546b1d`  
		Last Modified: Tue, 03 Jun 2025 16:16:15 GMT  
		Size: 15.7 MB (15717570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:8323f3ccd20a24042f7bfcab8b92902cf48e09d746448024ced37c1dc0bb21dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84db479cfea5531d55e7cc3af54da95814fdc25718c39169ea560496180c45c1`

```dockerfile
```

-	Layers:
	-	`sha256:e7f81150d70c0ecfb81ad5405953064a77c9d7fe46829d54f3047a40aa62e9b0`  
		Last Modified: Thu, 05 Jun 2025 00:21:42 GMT  
		Size: 4.2 MB (4230860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d871d854ed650d254462a15d3dbd4d2a713f346938cec628b6f302e9af6c6f8`  
		Last Modified: Thu, 05 Jun 2025 00:21:43 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:71f7a25c90598e37f18ae9f5f7f8d988d319a548ff192cebc0c6555d758c34c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.7 MB (567667957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895f640575a8c772e0776e7a72840dc9088eb3af59283338cd260d757cb8feaf`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891109dd0128b9f59129f4522b4284aca40ef5ea9f2dc570cb2c0b92efb59fa1`  
		Last Modified: Tue, 03 Jun 2025 16:10:52 GMT  
		Size: 1.5 MB (1536197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab497349841ae340f3b59cbd984d37ac2febc7260aed616d8c1b733e3b32db5`  
		Last Modified: Tue, 03 Jun 2025 16:11:06 GMT  
		Size: 136.6 MB (136628900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248859a2ea2da12f01695f930ec4bd4e6f35af255a85d044dd3b208a6fb9ccf6`  
		Last Modified: Wed, 04 Jun 2025 21:38:34 GMT  
		Size: 118.1 KB (118079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79733ff37d123ad353d874c5f1c3192a32c572d5bf6faf6afc6b2627210870e`  
		Last Modified: Tue, 03 Jun 2025 07:50:28 GMT  
		Size: 17.5 MB (17535684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016575d0d89512c625b2bacb887223ffa0824bf7713bd159f1257d0855801406`  
		Last Modified: Wed, 04 Jun 2025 21:35:38 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52e68ef10ee6a17b419e24b7076fce1ecd1b69a2def7d310f4df6387c6db00b`  
		Last Modified: Wed, 04 Jun 2025 21:43:50 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17864caaae63646cdfd3c81520e6882ecbe3b3c02fd0088f60e9a614f8409bf`  
		Last Modified: Wed, 04 Jun 2025 21:26:14 GMT  
		Size: 12.3 KB (12318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfffa525f363b20ff5f24db718fbd13e1d020815d419d53583a83903f0359d2`  
		Last Modified: Wed, 04 Jun 2025 21:33:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d753232f54d1f2a1350678a9e23b8a600dcf4013ac244ecfa6bd54633a77a600`  
		Last Modified: Wed, 04 Jun 2025 21:43:37 GMT  
		Size: 13.1 KB (13128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e172da3ed32e8b64a456218d7301af26a414636e82c98af5ea07c90417b391`  
		Last Modified: Wed, 04 Jun 2025 21:21:42 GMT  
		Size: 5.4 MB (5382224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb081e7eecc59bf428ef8c195087e38caac670aaca0c01b637bcefb016289182`  
		Last Modified: Tue, 03 Jun 2025 11:22:30 GMT  
		Size: 358.7 MB (358663804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065dd3748c4fd9184ccb6848a5aba8a62976b7bfec1f863b378c02d0a5b7429a`  
		Last Modified: Wed, 04 Jun 2025 16:32:37 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be3802b612798516df4e7a628bed5a3869854ce592c01b0d016f943f7a82f8`  
		Last Modified: Tue, 03 Jun 2025 11:22:08 GMT  
		Size: 13.3 MB (13333949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ff7d66d54dc9fbeebc2958270c751fa2bcdcb94821bdffc2034eed592eaf62d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9c89f7d54db387bd6f2fcfd84e5b9c941400317d5bcbaaef9b737746e74765`

```dockerfile
```

-	Layers:
	-	`sha256:f46cdddb86d6058ea83f4df5b8f8a8121d1e69bc5de3b8503580dcc4c11ae5b5`  
		Last Modified: Tue, 03 Jun 2025 11:22:08 GMT  
		Size: 4.2 MB (4234123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e77ec4a5d28dd97b70e11c8e49d83e535a8e2ac41953d16f864883db851838e`  
		Last Modified: Tue, 03 Jun 2025 11:22:07 GMT  
		Size: 18.5 KB (18509 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:25ec889288fac47860c6e1e10e96c6acb01340b9b2f58672a56efad829f319ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560334994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18101b7d6f01db7276b80d6390f3d16e45f8ddf82b1668ecfaf7ac75c36a7da8`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecd18cf58122413ddc47f9673d5c0e646a27dc2aa9df219441ec13443850950`  
		Last Modified: Wed, 04 Jun 2025 23:15:37 GMT  
		Size: 114.6 KB (114589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f5562f193e9eea946eda512e1471e9268dc375361248feea3c04e23c223ff`  
		Last Modified: Tue, 17 Jun 2025 04:20:10 GMT  
		Size: 17.5 MB (17535071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fb301a584caa38521dde3e532a4a6042aed3b60c7357d30233acce534e514c`  
		Last Modified: Wed, 04 Jun 2025 22:53:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427370a9426bb4e42f507efeefa6cac5901e2d365f6baa5041bf0d3406f1f634`  
		Last Modified: Wed, 04 Jun 2025 23:06:27 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fba098fa33b12ad39e4d189d786f2f19179dea0fecae51cc41ebad609bbdb35`  
		Last Modified: Wed, 04 Jun 2025 23:16:29 GMT  
		Size: 12.3 KB (12309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f1c3b7fa32ceec049d5acd8856f3e9faf62ae1f36911d20282bc8b25310468`  
		Last Modified: Wed, 04 Jun 2025 22:57:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23bcc5bc84f21da4ab65f29f8395b6d6299d7619f107898e0facd45a5e1b649`  
		Last Modified: Wed, 04 Jun 2025 23:00:40 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da1726655f207c0725d66d0e768b66fdd09eb24a62d4667c1088f355a3c9352`  
		Last Modified: Wed, 04 Jun 2025 23:12:55 GMT  
		Size: 6.0 MB (5976945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18b45d6a36af04c4d9bcc31ed6a61f78532ab1b2ce5470cf8d5f1df4b0ee96d`  
		Last Modified: Tue, 17 Jun 2025 04:20:21 GMT  
		Size: 358.7 MB (358662914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aa3f6876226d17f69fd87747c911496f8525860aa6fc53a76a6d9492ccbbb0`  
		Last Modified: Wed, 04 Jun 2025 21:32:30 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7cdda3e5c23b7a9162f875e924a0cad5f5991f0f8052ac08f51fbce3649434`  
		Last Modified: Tue, 17 Jun 2025 04:20:13 GMT  
		Size: 15.7 MB (15748567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:dad6fb8ee9a62ee373ff4eec34ccaef6915d0b63de1bc5963c6bcf00de244c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bee3df68eafd24f9d11476741d34a49d5822b549cac687c18534f1ed1170a0`

```dockerfile
```

-	Layers:
	-	`sha256:f29eff3806d1fb4e4d294099cadf79ec3703e55c7a1f23f609250be77c5d3ac5`  
		Last Modified: Tue, 03 Jun 2025 07:44:34 GMT  
		Size: 4.2 MB (4229621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b48594ee7108922fd9e88e714f99e7052b74cfdaee64d18137d6a9a0be9965d`  
		Last Modified: Tue, 03 Jun 2025 07:44:34 GMT  
		Size: 18.5 KB (18480 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:25.0.0.3-kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:136efedbac84a92e3c83dd1391e9f48b5ff89fbf74745833c6d24106581bbde4
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

### `websphere-liberty:25.0.0.3-kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:2fbf9052a35d9a2cd85466e9c99e490eeefcc60f9ddc31e4908ff0b572dd44b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118971202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d084d662e0ff083b8b80d7abbd4b993864bfc2de2520ea312e77b64907994c95`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473154fee0b11bc4d722e43c237f237b69136a24301983502078bc9dc527d0bb`  
		Last Modified: Tue, 17 Jun 2025 17:12:24 GMT  
		Size: 12.2 MB (12172067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb6ba5b52910f78ab9354ac0ad75ba2f1a919068cd8106ef806ea4bc865d2f3`  
		Last Modified: Tue, 17 Jun 2025 17:12:26 GMT  
		Size: 52.5 MB (52456010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3b6884b3df4e65f651464ae3b2df0d53a464c4c7a76e9bcb1b39223e674f69`  
		Last Modified: Tue, 17 Jun 2025 17:12:22 GMT  
		Size: 4.4 MB (4407179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f253e02a1d82e301299973b8697a93f1d7847bbd0ded63f396a825480837c224`  
		Last Modified: Tue, 17 Jun 2025 18:08:14 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c9b35e6df7d5d4f360cbcbfe1efd42a9244e1c913211ee66b91c327d84cc0`  
		Last Modified: Tue, 17 Jun 2025 18:08:15 GMT  
		Size: 17.5 MB (17548974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ec357ae3b8cb15bc1bc8f1287f277bc43c461f95eaba6d107b10cfb510679`  
		Last Modified: Tue, 17 Jun 2025 18:08:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fe948ba37518c0caba3acb1e6b7835f05cad964ce69ac0c73ca051addf4bb9`  
		Last Modified: Tue, 17 Jun 2025 18:08:13 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca2df483fd3202f401ff6d39b1b092fbdf6a10064ca53f51e2ddc3318d91e6b`  
		Last Modified: Tue, 17 Jun 2025 18:08:13 GMT  
		Size: 12.3 KB (12306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d47062e33638cbb4f5616e78fb3a360b000d8e7d1a2e3939078b0fe89de097`  
		Last Modified: Tue, 17 Jun 2025 18:08:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86085e54b7097cf949f6b0978694bad145cdd9754e89e947b6d22852988c09c`  
		Last Modified: Tue, 17 Jun 2025 17:23:17 GMT  
		Size: 13.1 KB (13117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226bb9a0e1fb3b75aeeb8f10fef5caeeea11f1c6b83fcccb18ab9288cbda9f7`  
		Last Modified: Tue, 17 Jun 2025 17:23:17 GMT  
		Size: 2.8 MB (2794554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:238f3375c25c44dd3f97fba06da15e7a6d1a68a50c943d3b61d8e773b097fe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270598a8fb424d26afa11ca3a506ff059578940fef2d06a1bdb89a88b4664d06`

```dockerfile
```

-	Layers:
	-	`sha256:9042c0757ccf5cd6f43a11f24f1ff9f309338e67e12572938c80c5f637b0cb26`  
		Last Modified: Tue, 17 Jun 2025 18:20:39 GMT  
		Size: 3.9 MB (3886357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993911e369a632845f6f6c25d4b0c1abea95da3181ead20a687125799fb13170`  
		Last Modified: Tue, 17 Jun 2025 18:20:40 GMT  
		Size: 39.8 KB (39788 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-kernel-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:692fadcc78f1b4620fe1b26bd08c643570bb585fd3dc440fd17b6740df038e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112932719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4158f44bfd4169092a6c43182c56c2fb958a9c13a8f63c5a5029b219dd584030`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbff14187feb7082a330fc6604f5d950114fba77a27a3564014bdeb0c0a7e399`  
		Last Modified: Tue, 17 Jun 2025 17:39:17 GMT  
		Size: 12.1 MB (12129302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79aed8751db549046792bc777edcca525eedc89ebe93460c37e203404f05870`  
		Last Modified: Tue, 17 Jun 2025 17:46:33 GMT  
		Size: 48.9 MB (48888727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a052f878cd6890586d100378a6682fad252e4a82b6954453d38c3f7e738bc00`  
		Last Modified: Tue, 17 Jun 2025 17:46:30 GMT  
		Size: 4.2 MB (4197882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797fedeb23be889d0b30f85fb1efe5b858deac6b9fea619ff4df2a7616170d6`  
		Last Modified: Tue, 17 Jun 2025 20:19:09 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bdd6e20b67da0a847e9b8407d69511f4f79abfaf82dbb7308976776aecd923`  
		Last Modified: Tue, 17 Jun 2025 18:38:20 GMT  
		Size: 17.5 MB (17549146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775db8156f7d1e5ca49b54dd0de8bf3e4d9fdfde1b8ba4208e15e9c8059a6ce`  
		Last Modified: Tue, 17 Jun 2025 20:19:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e14da213dfe89dd911f966330862c7078a0d7e4fd6148502665992ffde6fda`  
		Last Modified: Tue, 17 Jun 2025 20:19:14 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615fb644c386391be338e2f582eebf297136e8fd3908f6c845fe29afa4bc3a5`  
		Last Modified: Tue, 17 Jun 2025 20:19:16 GMT  
		Size: 12.3 KB (12306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb6f3d4e75aac506db409464ff93dda077377bf5a1fecc7712ba3f2642cd54`  
		Last Modified: Tue, 17 Jun 2025 20:19:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb6ebe6508ae27cd63eb4254bffc07b64e7da4b6a6b947b81be6831fc6b7f27`  
		Last Modified: Tue, 17 Jun 2025 20:19:22 GMT  
		Size: 13.1 KB (13115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc810f71a1c2f5884f4376ff19d34c1095b233de0bff5ffb8bce727139d612d6`  
		Last Modified: Tue, 17 Jun 2025 20:19:25 GMT  
		Size: 2.7 MB (2742091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:16836fd400d2a027ce932744c67a57fd23a1fc0226f625d16791293d4d4cd809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c01b588b5d0db07a2ad503642b5f8446296a8ce105fcf7653c005f0ca78129e`

```dockerfile
```

-	Layers:
	-	`sha256:c8c7083dbd9f6b57da614b08a1aee2b1f3bf235d9f73f507b0a90a3d2382633e`  
		Last Modified: Tue, 17 Jun 2025 21:21:46 GMT  
		Size: 3.9 MB (3879691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a706fb502eaf83aa387ecf13b56be6c4395bcd657443b4f0955ee5158f8d298`  
		Last Modified: Tue, 17 Jun 2025 21:21:47 GMT  
		Size: 39.9 KB (39916 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:2fca3fa7ff8afdaaa14414505bda1f53c9f8475dd28b7474635c2e02d42f1ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125180862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e8ec7c2766fa89216ec3860ac6459d7b6f1893adbd854ff2cabc24311de541`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c0a1fca7ea07c8c5a127826c7981b2bbb00fab8901f776e93777f6b6e7e19f`  
		Last Modified: Tue, 17 Jun 2025 17:55:19 GMT  
		Size: 12.9 MB (12893311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe643e2c62ba3b29b36e85d1c1b3ad4b19b8525dc1c11534591b5a897b87108`  
		Last Modified: Tue, 17 Jun 2025 18:04:01 GMT  
		Size: 54.1 MB (54102703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff5d8745a02d7d1739003a9cbb478252421dfc67060330461e18b9750223855`  
		Last Modified: Tue, 17 Jun 2025 18:03:48 GMT  
		Size: 3.5 MB (3464435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a33987f5b67e9ab8ced0e6028829f130114f59a3c08ae2786e5e2c2b665f6`  
		Last Modified: Tue, 17 Jun 2025 18:44:40 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fef314da6e05555f8bfe4231f612eac836d45ce987a316796f1f2ccb8389c48`  
		Last Modified: Tue, 17 Jun 2025 18:44:42 GMT  
		Size: 17.5 MB (17549347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8395adfbb6d00f2c074bf211dffee40de65078b2522688a783c995b2261d318`  
		Last Modified: Tue, 17 Jun 2025 18:44:41 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c74b667470251f3083ad7557a7a5498fb1bf03b763b82d6c1eea79ab434d379`  
		Last Modified: Tue, 17 Jun 2025 19:14:56 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f3302d77673f70fb8b340ba8edbd8842e938e05c66b9c16b47e625c09a197e`  
		Last Modified: Tue, 17 Jun 2025 19:15:00 GMT  
		Size: 12.3 KB (12309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea21c8b957b37cc6b2da010a9762f9404d32aa4193c342f7eb93cfce4b6aaf5`  
		Last Modified: Tue, 17 Jun 2025 19:15:04 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5146b32f13c4e27e0946d0aae93d2f4f7ea3ad39dbe665121d380f7861dbc4f4`  
		Last Modified: Tue, 17 Jun 2025 19:15:08 GMT  
		Size: 13.1 KB (13112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40387502de30f0c776ff631a797b2ab8a19657d0fed73e8381e34a92ecbf37c4`  
		Last Modified: Tue, 17 Jun 2025 19:15:14 GMT  
		Size: 2.7 MB (2666546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a1d4f42d406038b6c74865be7f863088f788b98b9eee2f19fc3ccc047c52bd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ff96727f52dd398604d24247fe81f8610a33e02f07dd288f8c0e0fd2350f34`

```dockerfile
```

-	Layers:
	-	`sha256:27de8f464c59252417b40a39d00b526ec95ba46e5a662a007c78d8373e9f4180`  
		Last Modified: Tue, 17 Jun 2025 21:21:57 GMT  
		Size: 3.9 MB (3890978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db6dfd6ff2653bda4a4949231d4220bff046d17cecd0c94fa744291bfb61ef58`  
		Last Modified: Tue, 17 Jun 2025 21:21:57 GMT  
		Size: 39.8 KB (39822 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:27679c47e9b48e8d8b18d4677b19052726fc31292851fb1c3445ece0bb1b1d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116611876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5b235979e17b9ad5e6dbd3caa433bdc7dcca563626564f164ea3dc36c91397`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a592dff2b7023a1eb4d0588791417d7ab44efe41ce34295948fbb1653b7e87`  
		Last Modified: Tue, 17 Jun 2025 21:00:33 GMT  
		Size: 12.2 MB (12219457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae0bc1b527924c0ace1e0d04d6fd3c57ee65b1970ba12cd17e99e38e1cc6712`  
		Last Modified: Tue, 17 Jun 2025 18:19:08 GMT  
		Size: 51.3 MB (51349445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6724620859c92111104b1ce73e900908380d478be466a4911b4227f1035d41`  
		Last Modified: Tue, 17 Jun 2025 18:19:03 GMT  
		Size: 4.6 MB (4583329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b894b2ce4aeaf849b030b8c529766614c0bffe1d8c6a28ac79f887c53c9bb2`  
		Last Modified: Tue, 17 Jun 2025 21:50:29 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077e1ed8f401e668c4e7a9dd0e4036e876c9e599a397d8bd871a9e92ff87168`  
		Last Modified: Tue, 17 Jun 2025 20:18:02 GMT  
		Size: 17.5 MB (17548697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92008142433156668722bde0834b28db7caa20e6c0a7fb25fb89a0878707dc8e`  
		Last Modified: Tue, 17 Jun 2025 21:50:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b986275fd43559b4b62e46382c14e48da9364d4cfa3c07b940f872b68c4b795`  
		Last Modified: Tue, 17 Jun 2025 21:50:34 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a95bb7782a47745ad82f3ec2dcc1eaf8596050a3b845fa137c0104e3ea5ff3`  
		Last Modified: Tue, 17 Jun 2025 21:50:36 GMT  
		Size: 12.3 KB (12308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b525e530faae69d1d48a1b6db1190c1ef9fe20b2115788f3686d66509116e73`  
		Last Modified: Tue, 17 Jun 2025 21:50:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7776a57a629d05957c8471dd70f1ff3da2ba0dc8aa5059a7f55a3b0baa85e92`  
		Last Modified: Tue, 17 Jun 2025 21:50:44 GMT  
		Size: 13.1 KB (13117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ac5cd510e357de3526d324a7ab248bd20fe429813c9d09d0778a2c0b34bf43`  
		Last Modified: Tue, 17 Jun 2025 21:50:48 GMT  
		Size: 2.8 MB (2849567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:537670a830803ffcc6e6075015f803e3dda61d594d1563420491f11dbc883c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ca90e78845e22f28b9cbcfd36a9d37bc8a9e32fdea322010d8407464f9f27f`

```dockerfile
```

-	Layers:
	-	`sha256:4278ab23c142300c1b0948106593128b25003ebf30a789bca7b3bf4bdaebda32`  
		Last Modified: Tue, 17 Jun 2025 21:22:03 GMT  
		Size: 3.9 MB (3887374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63efd2e166a2d3e14fd39e2e29328974e5c79ecca883c8d6bb2307b699db9597`  
		Last Modified: Tue, 17 Jun 2025 21:22:03 GMT  
		Size: 39.8 KB (39788 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:25.0.0.3-kernel-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:927fe9f6d382d04e259962ecf4462e500480493130c1a7fbbeffec3887ee5556
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

### `websphere-liberty:25.0.0.3-kernel-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:41c77c824bd3098accc1d0b415a26d66ab24f6d2e30f64cfda5f318532f3483b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118869242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4bd4797df3f1130b151f252cbde1d6796ded87d7df4902b5a58698e5fa8be1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe200c80616675d621c20320c6bbb63824ebb52e7f77cafc18893533d2fb4fe`  
		Last Modified: Tue, 17 Jun 2025 17:12:27 GMT  
		Size: 12.2 MB (12172168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3082e23860276aa9c4c2d43b942c9e25dd1e69cce4d58c23a39cb9f13dae081f`  
		Last Modified: Tue, 17 Jun 2025 17:12:32 GMT  
		Size: 51.7 MB (51747278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac736981419aba48890e57917cf88e9ccc539a4c3858ae03fd6c2d790e925db9`  
		Last Modified: Tue, 17 Jun 2025 17:12:27 GMT  
		Size: 5.0 MB (5015886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce2b7a772df81befc4fb1f50009d1aa66e4d4d5fbdae43fe9ae93875220c852`  
		Last Modified: Tue, 17 Jun 2025 17:23:14 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445b8c106b2980343a23d7297a28dd4a4595650b4f20715538e83b478bf751d1`  
		Last Modified: Tue, 17 Jun 2025 17:23:17 GMT  
		Size: 17.5 MB (17548969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4f5874fa4ca7cc76abbb6c841b5af7908d1014532e5a08052458ff3dbf7bf7`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dfa75de55a4e72bb3a44140b88c44e422bb9192603093c13de7526849dea01`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a160876bd288671d34c649daf03fc26290801f1bbb95c835d55d02f84efb11`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 12.3 KB (12308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf5c20227c0f80e3e955d634a8287d0a2229f01ca999c9ac357107bbfbe4d2d`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341404d690b84ad0c621dc4f4514baec757766c62cb9bba045cf36a346e152a4`  
		Last Modified: Tue, 17 Jun 2025 17:23:15 GMT  
		Size: 13.1 KB (13124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a35921ba67d64292f36a2bac0219b1c350db0acdd35233ccf64cb2a2d6d10ac`  
		Last Modified: Tue, 17 Jun 2025 17:23:16 GMT  
		Size: 2.8 MB (2792510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:edcba99136cd11e0f67cb63ba259d7aa3251f0b346c3fbb7a48aad8154b5f1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e860284bfc25e034b85e921cf1c58a3a938d7941d24522b5769e82be9e3bea`

```dockerfile
```

-	Layers:
	-	`sha256:0f92ac4efd9e10fc351d787ebe707c6862af4c2fcf3a652945a2fe012cc73baf`  
		Last Modified: Tue, 17 Jun 2025 18:20:46 GMT  
		Size: 3.9 MB (3873228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8a11ac30e7853af51db57de12d17869397cbf8b7486a413d7bd4be8b82b26c`  
		Last Modified: Tue, 17 Jun 2025 18:20:47 GMT  
		Size: 39.8 KB (39788 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-kernel-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:5f9a5d4e4eecb8452b9d7853d666da092f035dcd92bc393e48ffce5dd22da35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112893894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3748a96fefee1fcf4bd470e24dc9a08e423a1a112de7f0da25878fc761c62d21`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbff14187feb7082a330fc6604f5d950114fba77a27a3564014bdeb0c0a7e399`  
		Last Modified: Tue, 17 Jun 2025 17:39:17 GMT  
		Size: 12.1 MB (12129302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326fb85a67774b17b7c5a12fd977330d9e887967a18c65bb56fb69873a7c1945`  
		Last Modified: Tue, 17 Jun 2025 17:51:11 GMT  
		Size: 48.2 MB (48190778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5845461e49b7f17a73c1fa99239aa56d56598a789b478642b473201b34ae43`  
		Last Modified: Tue, 17 Jun 2025 17:51:00 GMT  
		Size: 4.8 MB (4807240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8f0c47bd8478fdf1fc7ed948e06551476396eae8d6984624c535a67020ac95`  
		Last Modified: Tue, 17 Jun 2025 18:39:21 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53eaf58d0c43ea5989099ce7dd25144154a771b1f950cd90f84bd4927cf1379`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 17.5 MB (17549134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28fe897212ec6f5fab9dbf65de42971b3e94ea13abe7b5fb532491ab04eaccd`  
		Last Modified: Tue, 17 Jun 2025 18:39:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18666ac700e5501ec1ea53702a82c6f0d3ae217012c221e74f05add227baac0c`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c94eb2aeb858af32a68302246df7907fb69c0790ab8831341bd7ca4dae48745`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 12.3 KB (12307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bffc2b687009c58926b580de121d301f65f2e35f15ac838cafc8c32032963e`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ede735e232c48b192699e550c05540f1dc3ab10e0e0fa70b6cdad412f2889`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 13.1 KB (13115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6015864d2e723608f0144f87fdac0243b48ae26319ea1ed9139ecbdbefcec5`  
		Last Modified: Tue, 17 Jun 2025 18:39:23 GMT  
		Size: 2.8 MB (2791866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f8044bdcdbddfc2271084371f452ac80477aa186d486557dbf922d4e1c62de6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3906478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52db41c97c132ba9499be9a8c3afa1c63a621b2d52aacb23eb8c9afcfe318bdd`

```dockerfile
```

-	Layers:
	-	`sha256:e8b4c9ae2d0b9b7d32f19e2995cd1f62baf52223f06f4708151d2c7a65413f7b`  
		Last Modified: Tue, 17 Jun 2025 21:21:57 GMT  
		Size: 3.9 MB (3866562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c46408886af45dfbf27e5e574989a7223b3a6a3cb034bb7fb54212b2ecec8c05`  
		Last Modified: Tue, 17 Jun 2025 21:21:58 GMT  
		Size: 39.9 KB (39916 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-kernel-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:676dd9b2f22428b9ba91dfc404a969513f242d410d7efc82638e2584ea4d91d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124817390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1c274a07296340c6ccdf6e2a89d5e2e0c5b599924f14a784a1ececeefae233`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c0a1fca7ea07c8c5a127826c7981b2bbb00fab8901f776e93777f6b6e7e19f`  
		Last Modified: Tue, 17 Jun 2025 17:55:19 GMT  
		Size: 12.9 MB (12893311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5a341607cddf9964b5f321192ee5159f90ea1e77114afa75d67d56e09ff152`  
		Last Modified: Tue, 17 Jun 2025 18:09:11 GMT  
		Size: 53.4 MB (53352856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652393ec25233ac2529d30f8aedf8fae2534e6dbe003ed83ba345e7775d7e71e`  
		Last Modified: Tue, 17 Jun 2025 19:56:14 GMT  
		Size: 3.8 MB (3832349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abff2a84a658b02323f9f6a33c251ca1a805783be3b4ea7c8e3b4826adc847c`  
		Last Modified: Tue, 17 Jun 2025 19:56:19 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db2d2ce6a798183933de67fe00bc90457be5837a49e25fc02822cbda63b75df`  
		Last Modified: Tue, 17 Jun 2025 19:56:21 GMT  
		Size: 17.5 MB (17549364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d96fa53c08da8d805334fd78311a8e558e9e94f9a8ee014c174ced0e9df6771`  
		Last Modified: Tue, 17 Jun 2025 19:56:17 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e167db2b65a9b61d8814fb33de1f98450cd14bb47d49cc1425d1d89c18c93a0f`  
		Last Modified: Tue, 17 Jun 2025 19:56:17 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d034e14c81ac42aa6db6268a030411f81b081648b6dcd50c0fedf53a71657c5`  
		Last Modified: Tue, 17 Jun 2025 19:56:18 GMT  
		Size: 12.3 KB (12313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8aa037db5154ddcee578eae16e51d2c629bf2649bbe6ccdd0111039eb5761f`  
		Last Modified: Tue, 17 Jun 2025 19:56:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772894a21e0626867243f211517c14036c5bf38c84e923efe9357fcc19cb19c1`  
		Last Modified: Tue, 17 Jun 2025 19:56:18 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54359e10265f3db0b3c4a791fef2de501c9f56748549013cfe86a342cbac6ce`  
		Last Modified: Tue, 17 Jun 2025 19:56:19 GMT  
		Size: 2.7 MB (2684971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c7ad52b0412f26cc38643622330373bbcbd4d48257cf050135e7e5a9359c18b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31ab7550bf9e53f7e639a9bceb7ff26f443c81bb902e0df22f6a8e4a996b14f`

```dockerfile
```

-	Layers:
	-	`sha256:164cdaf1d525d365e52d3ed9b03ee4b32ae7cd3c3f9beea48a950d519d9f9e2a`  
		Last Modified: Tue, 17 Jun 2025 21:22:02 GMT  
		Size: 3.9 MB (3877849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b58973bc6a8e874ef95a6efa52a20cafe2d7830b71c53a8a0f13387a851407`  
		Last Modified: Tue, 17 Jun 2025 21:22:03 GMT  
		Size: 39.8 KB (39822 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-kernel-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:8ab740475f70d412df473443281e5b38f0e2871197d14b39c3b09f0591566b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116915856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fb81319478fd62174d354a2f3355ea2acf9df226624f8f4f263fbd2f650c9e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 21 May 2025 02:47:06 GMT
ARG RELEASE
# Wed, 21 May 2025 02:47:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 21 May 2025 02:47:06 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 02:47:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 21 May 2025 02:47:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 May 2025 02:47:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 21 May 2025 02:47:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
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
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a592dff2b7023a1eb4d0588791417d7ab44efe41ce34295948fbb1653b7e87`  
		Last Modified: Tue, 17 Jun 2025 21:00:33 GMT  
		Size: 12.2 MB (12219457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd49d9c0e72875c8ee3927ea4d11b86f03fb1e60bdc8402234c9dff63a37373c`  
		Last Modified: Tue, 17 Jun 2025 18:24:04 GMT  
		Size: 51.1 MB (51093325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b573c2992387ba62243bdc87758146bf1036caa096e7c095f417dabebdb5a7db`  
		Last Modified: Tue, 17 Jun 2025 18:23:57 GMT  
		Size: 5.2 MB (5172773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77613a98ab599e0b7832531e31e7c60d3cd0043051732a81036626f8db3b037`  
		Last Modified: Tue, 17 Jun 2025 20:19:40 GMT  
		Size: 33.1 KB (33109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ad7ec48202ae771064f3bf49698d83c020bd4f4b5c0aa9c69372dcaaaac81a`  
		Last Modified: Tue, 17 Jun 2025 20:19:42 GMT  
		Size: 17.5 MB (17548698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924715a843a499a4640de39975e751f95ace604ff27dd6e6de881c83e31ce3ae`  
		Last Modified: Tue, 17 Jun 2025 20:19:41 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad18a12b32387aa9cbede99302f2cc26c3453da6832f49b1579e22500efd1d2f`  
		Last Modified: Tue, 17 Jun 2025 20:19:41 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd846b4080b255bdc103cc886dc124ed8eee3e50414ca9efccb41b242c5a978`  
		Last Modified: Tue, 17 Jun 2025 20:19:42 GMT  
		Size: 12.3 KB (12312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d33a033bc396adce1a551b38d27993796786259b7af7f24955d3971ee72005`  
		Last Modified: Tue, 17 Jun 2025 20:19:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94344850a47176afd9743371d6da34d60181f952c0b86e161d688d11030fe7`  
		Last Modified: Tue, 17 Jun 2025 20:19:43 GMT  
		Size: 13.1 KB (13119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f74f1c857a0535b5797a8e097f9fabab5202f01717d8a2415fba45639cb821e`  
		Last Modified: Tue, 17 Jun 2025 20:19:44 GMT  
		Size: 2.8 MB (2820213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:28a09fc905a2eaac094835cc8468825cfa016e895c25c4e4a1c21dfedd43f151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3914033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5002f68e0890427a1b41e9dfa092e2b727e06c750cd4351bdbf5afc45f61da03`

```dockerfile
```

-	Layers:
	-	`sha256:67ce6b87486af386e323cd780865b7aebc1e7e672289663795f4c4d3e1133d94`  
		Last Modified: Tue, 17 Jun 2025 21:22:13 GMT  
		Size: 3.9 MB (3874245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7182460c004eca250f0ab5870d89d2e17ee26aaf67aa8b8c7c089482a6da54b`  
		Last Modified: Tue, 17 Jun 2025 21:22:14 GMT  
		Size: 39.8 KB (39788 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:25.0.0.3-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:26aebe6cf0e2aceb71e2870a308dd7351886a275fad145f6caa0d96971d227bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:25.0.0.3-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:427b64f163865042871bdfc9b5eb1a24d9e48bd2525841d16ded491dd91d723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190272669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8615d626a4aeffc801a1a38463e377a68f9f76652b9971ccaad9f9b919275c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a6eae1ced04a72a3e7964ca3af1d5775c7934f0bce2fac7626d1c924e20ab1`  
		Last Modified: Tue, 03 Jun 2025 16:06:17 GMT  
		Size: 113.7 KB (113705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f1ada3fae0c70352747fb8df137c637ee3e233f4ceff2df47c267bec08d230`  
		Last Modified: Tue, 03 Jun 2025 16:06:18 GMT  
		Size: 17.5 MB (17535328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daefa2cabcd02e82430decf2785de235d7afb113be301c67e0469ad7766332d`  
		Last Modified: Tue, 03 Jun 2025 16:06:17 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231c74b99f2dab912410ebd914c8e042c922aa6aabf50df9ea90cb5ee622009e`  
		Last Modified: Tue, 03 Jun 2025 16:06:19 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7221d65a1e36b154e5b32ed5aeeb112cdf7750c901aba007346a1430d0467751`  
		Last Modified: Tue, 03 Jun 2025 16:06:19 GMT  
		Size: 12.3 KB (12318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29725d65fb0f7e7156d9f182f75439fd4c4a4a8712105dc049207bfec81af73`  
		Last Modified: Tue, 03 Jun 2025 16:06:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1ae8eb37f8eff86a3abec7fee59cb5cdc47407550c61b285ace5054f04c825`  
		Last Modified: Tue, 03 Jun 2025 16:06:20 GMT  
		Size: 13.1 KB (13124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c5fc3aa82ce3456016b4d46773db6920a0f2daec0f980e660381610b97f1ae`  
		Last Modified: Tue, 03 Jun 2025 16:06:21 GMT  
		Size: 5.8 MB (5827949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f9cacd09167259589453149f44ba226be22e8eaf6abb5bcec515825907e6902b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5b4a848d8381f8e5cb5ff2856d7d15f40ea1513bae6a74c5dcb62448335361`

```dockerfile
```

-	Layers:
	-	`sha256:8609b09ce466e61ae5cdcc8828326f6ee7dbdcb29d358e9e7bf88ab413a7d8ed`  
		Last Modified: Thu, 05 Jun 2025 00:23:03 GMT  
		Size: 2.2 MB (2203517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84cc91f5c99bc16ecb7342b3d3ed915bbf64ff22ff35ad00a8b2b8a8122f70e1`  
		Last Modified: Thu, 05 Jun 2025 00:23:04 GMT  
		Size: 37.6 KB (37630 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:4aba245af1f97091474423c706d0ea5a0f49046ef5ef64d5055b146da4824ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b30ab077c89c9aa5348f307f534c17cbb5477926cff0cea4b41f0655464bf1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891109dd0128b9f59129f4522b4284aca40ef5ea9f2dc570cb2c0b92efb59fa1`  
		Last Modified: Tue, 03 Jun 2025 16:10:52 GMT  
		Size: 1.5 MB (1536197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab497349841ae340f3b59cbd984d37ac2febc7260aed616d8c1b733e3b32db5`  
		Last Modified: Tue, 03 Jun 2025 16:11:06 GMT  
		Size: 136.6 MB (136628900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248859a2ea2da12f01695f930ec4bd4e6f35af255a85d044dd3b208a6fb9ccf6`  
		Last Modified: Wed, 04 Jun 2025 21:38:34 GMT  
		Size: 118.1 KB (118079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79733ff37d123ad353d874c5f1c3192a32c572d5bf6faf6afc6b2627210870e`  
		Last Modified: Tue, 03 Jun 2025 07:50:28 GMT  
		Size: 17.5 MB (17535684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016575d0d89512c625b2bacb887223ffa0824bf7713bd159f1257d0855801406`  
		Last Modified: Wed, 04 Jun 2025 21:35:38 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52e68ef10ee6a17b419e24b7076fce1ecd1b69a2def7d310f4df6387c6db00b`  
		Last Modified: Wed, 04 Jun 2025 21:43:50 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17864caaae63646cdfd3c81520e6882ecbe3b3c02fd0088f60e9a614f8409bf`  
		Last Modified: Wed, 04 Jun 2025 21:26:14 GMT  
		Size: 12.3 KB (12318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfffa525f363b20ff5f24db718fbd13e1d020815d419d53583a83903f0359d2`  
		Last Modified: Wed, 04 Jun 2025 21:33:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d753232f54d1f2a1350678a9e23b8a600dcf4013ac244ecfa6bd54633a77a600`  
		Last Modified: Wed, 04 Jun 2025 21:43:37 GMT  
		Size: 13.1 KB (13128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e172da3ed32e8b64a456218d7301af26a414636e82c98af5ea07c90417b391`  
		Last Modified: Wed, 04 Jun 2025 21:21:42 GMT  
		Size: 5.4 MB (5382224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:091c117c743f5c8413aa33e97bbd62b9f70dec58a478fe9f17692a1f783415b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98796a70a7a697796db37414abb28868350bb2e5cf6506a243c7b433fb96d575`

```dockerfile
```

-	Layers:
	-	`sha256:6d9ce562b43b1789ad9c31b260ae9a65beaa034e4285155d02700a43aebad775`  
		Last Modified: Tue, 03 Jun 2025 07:50:27 GMT  
		Size: 2.2 MB (2206780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3702cbb9fe950760aaece2453f737eb03449e439e5939d3617dc68aa995483fb`  
		Last Modified: Tue, 03 Jun 2025 07:50:27 GMT  
		Size: 37.7 KB (37664 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:25.0.0.3-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ad3a8ceb16235a2dc628d73ca6855c56d3816a8601514c717c44d5b524975d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185922561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860fb19d009c0dadfe8b061e052bd78fe4aa8164cae43542671980afc1cd686`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER root
# Wed, 21 May 2025 02:47:06 GMT
ARG VERBOSE=false
# Wed, 21 May 2025 02:47:06 GMT
ARG OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Wed, 21 May 2025 02:47:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Wed, 21 May 2025 02:47:06 GMT
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecd18cf58122413ddc47f9673d5c0e646a27dc2aa9df219441ec13443850950`  
		Last Modified: Wed, 04 Jun 2025 23:15:37 GMT  
		Size: 114.6 KB (114589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f5562f193e9eea946eda512e1471e9268dc375361248feea3c04e23c223ff`  
		Last Modified: Tue, 17 Jun 2025 04:20:10 GMT  
		Size: 17.5 MB (17535071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fb301a584caa38521dde3e532a4a6042aed3b60c7357d30233acce534e514c`  
		Last Modified: Wed, 04 Jun 2025 22:53:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427370a9426bb4e42f507efeefa6cac5901e2d365f6baa5041bf0d3406f1f634`  
		Last Modified: Wed, 04 Jun 2025 23:06:27 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fba098fa33b12ad39e4d189d786f2f19179dea0fecae51cc41ebad609bbdb35`  
		Last Modified: Wed, 04 Jun 2025 23:16:29 GMT  
		Size: 12.3 KB (12309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f1c3b7fa32ceec049d5acd8856f3e9faf62ae1f36911d20282bc8b25310468`  
		Last Modified: Wed, 04 Jun 2025 22:57:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23bcc5bc84f21da4ab65f29f8395b6d6299d7619f107898e0facd45a5e1b649`  
		Last Modified: Wed, 04 Jun 2025 23:00:40 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da1726655f207c0725d66d0e768b66fdd09eb24a62d4667c1088f355a3c9352`  
		Last Modified: Wed, 04 Jun 2025 23:12:55 GMT  
		Size: 6.0 MB (5976945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:25.0.0.3-kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ea4d491bae242e8126edce234d4ac2a1e34c6a3b1a07693f26c56714bcbd98e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2239908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684ad8824b2ff2bc4590c740f465c2494afaba3bde28e355a2b5b4e80aa2253b`

```dockerfile
```

-	Layers:
	-	`sha256:fde81f2596e54ca89db03b2a22f32a9cfa6d8c402fadb4ad0c0e8463f9113abb`  
		Last Modified: Tue, 03 Jun 2025 05:54:05 GMT  
		Size: 2.2 MB (2202278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d86bb5ebfe9f7423c38c6675ae122d74913a914e6a04336f5ddad1115a5610a`  
		Last Modified: Tue, 03 Jun 2025 05:54:05 GMT  
		Size: 37.6 KB (37630 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:25.0.0.6-full-java11-openj9`

**does not exist** (yet?)

## `websphere-liberty:25.0.0.6-full-java17-openj9`

**does not exist** (yet?)

## `websphere-liberty:25.0.0.6-full-java8-ibmjava`

**does not exist** (yet?)

## `websphere-liberty:25.0.0.6-kernel-java11-openj9`

**does not exist** (yet?)

## `websphere-liberty:25.0.0.6-kernel-java17-openj9`

**does not exist** (yet?)

## `websphere-liberty:25.0.0.6-kernel-java8-ibmjava`

**does not exist** (yet?)

## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:0cda5f600207107e39e2a468f97a0287de449fad65767e1d09e2b295d21f3083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:47c75ddb034d2f2b52705a1cdac6bba5733ffab8498da95afb2c8806ebedea22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564608948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca78369e926edc12d3ad2c04854d17d1a0a8f9d919a9724c284d893d189bfc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75415249802d68499f7a1941c7251d11f4d9391ee70c7f0df518d0be883ba7e`  
		Last Modified: Tue, 03 Jun 2025 14:16:51 GMT  
		Size: 113.7 KB (113726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edc80817afad38e3785d0bc7f3d91828ee3134158a3409f3aba86e4e7aa5776`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 17.6 MB (17550494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36eead5fb6241f13557437967b02b83bc8dc7d08863223d4abe925ba85f8df1`  
		Last Modified: Tue, 03 Jun 2025 14:16:52 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad27209f5960e2b8879bcef1305b85508c3d6bdae7f61526d1ae6c7d721edd`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ab040de8607f25406752c9918d3c7caa0e7e8b0d0b86e29e8fef97022db64e`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 12.3 KB (12319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80a3f11f0b7b959c5607128adae26e0a53a2da9e9a8bd10d704e38346b68b0a`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f995b38748aa1f8ea7c95daf6c5d8fbb028082c48f8db9212d250445e7454146`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfe6d502e6b3addffbbeec97f7511919c759f4e3973dd56c7eeb5c9eb6eda3`  
		Last Modified: Tue, 03 Jun 2025 14:16:55 GMT  
		Size: 5.8 MB (5823975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3641934bf84333179274429afe221f0ff69ed444d8b2d59b9bf89d0230bbdf84`  
		Last Modified: Tue, 03 Jun 2025 14:17:15 GMT  
		Size: 358.6 MB (358568735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63547b71219d23c6134704852e9a7f563ff55097a07a64d0ac376a1a131325a9`  
		Last Modified: Tue, 03 Jun 2025 14:16:55 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6ba16b932f323ebc435a78303d0820609877a094623ad5c338be9fb73c2d75`  
		Last Modified: Tue, 03 Jun 2025 14:16:57 GMT  
		Size: 15.8 MB (15755383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ce20f432dde03200506a7307f9c33747c1be2565f0fbe54959c9bc7f9d5705df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4259497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb9f6177227c75cdf2453404ddffd432ab3beca52b370fb57927a5c346e9386`

```dockerfile
```

-	Layers:
	-	`sha256:14a4bc6d5404ab54ae1faf17aea5bde8147b4efb307d5f370e2be6f7ef5777f6`  
		Last Modified: Wed, 04 Jun 2025 05:12:16 GMT  
		Size: 4.2 MB (4240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30cd05474323ac7ea0f051871bba399e786c5d45496751624b11828a19189b4a`  
		Last Modified: Wed, 04 Jun 2025 05:12:15 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:e9d390c6147d6f70f19ae7261752476ea1b487c0d5c9502e4756c14525d18827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.6 MB (567616908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e7210c546a4590a8bab3f61fa260015e00480163fa00d1bf5a862c5704daa3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891109dd0128b9f59129f4522b4284aca40ef5ea9f2dc570cb2c0b92efb59fa1`  
		Last Modified: Tue, 03 Jun 2025 16:10:52 GMT  
		Size: 1.5 MB (1536197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab497349841ae340f3b59cbd984d37ac2febc7260aed616d8c1b733e3b32db5`  
		Last Modified: Tue, 03 Jun 2025 16:11:06 GMT  
		Size: 136.6 MB (136628900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b26050dbd70055fa94a2da973196f876da0abde8792c43affce987c73c1aa0`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 118.1 KB (118091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27079afba53f0e88887b24a16f942d42eccc606b18bdc07669969f59b85c7e2a`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 17.6 MB (17550846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf3bcc8757703456b292b2f799919849ef6066510ec79d05bc21d8ea983a47`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0434563abbb7ed9e55e070d9a8ea3598f9bf9749b32cfee52d213a29c41ea06`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c07c4d903aa42a243323bae348cd3aea27a547d87bdeb9edfdfe1524e97a5c`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 12.3 KB (12313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98b78706b42542cc9172c24cc28f75eaf3535da7430d6e1e1dda1fe84affb38`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8b72d2d4070334ead73504059918753c1d903a7b1c3e00b5b5065c98e769d`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 13.1 KB (13123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53959a503575f9e849b4cf9239c93c87532996a43a678e79c2998d640a0694`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 5.4 MB (5421942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaa7826ebd1b87521364bd0ae2ec2385aee49c4954198bfbc28f5ac0d74f243`  
		Last Modified: Wed, 04 Jun 2025 05:13:08 GMT  
		Size: 358.6 MB (358569873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7eebd4b74493ffbd28f5b5e48fa6271b325b11e39b48b28a445a2ede2c6e5f`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7008729647354a9b0e3cbf52f9c4c0e3f7b67ccfc10aabff18ab94846bc28c99`  
		Last Modified: Wed, 04 Jun 2025 05:12:27 GMT  
		Size: 13.3 MB (13321968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:cb627fd9e535dac57e43546563348cab2b84fc48fbda7fef8ad62e718b072172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4262812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051e5b337e803d1b779513d2e15d1142269a6befb594568a9f21b6ba88fc5cb1`

```dockerfile
```

-	Layers:
	-	`sha256:f1ceb13861906380c2003f41436f5cfd45be261502f1676933eee6e194f0c368`  
		Last Modified: Wed, 04 Jun 2025 05:12:45 GMT  
		Size: 4.2 MB (4243700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bed80af09e1ba1261a8b5b397c12ca24b2f41e8532fa0d89589113e1c61ed4c6`  
		Last Modified: Wed, 04 Jun 2025 05:12:45 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:aa9f26c6c3051b93a9517887e970501afaea282a9c60539d58774853992a8ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560298713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99b8ab2566500278e3eda621dd33cde1895117938aa93c815569dba6412a65a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc15cdcb77a0512baaf4cb0f2730505d8e69f2911c19853c7e981358bba8d62`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 114.6 KB (114588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff40b64b9af4bc8ab52ec9bd63b3b25bd2d440b1201007c0e812ee2c1852d36`  
		Last Modified: Wed, 04 Jun 2025 05:02:36 GMT  
		Size: 17.6 MB (17550225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42118c9e0c1a65af1ad88f5cde841bfb428ae6528aa35d9ab8cc7d810d8f45`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdae2fab9a2e4966319247c3a80d2b05d5f017f59587dd4b9bec711b180c7e`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a72f89d59315ca50a13f1dc1eba87d1e6dc849ffd0a5580c7e04b46b29f155`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 12.3 KB (12316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee99aa24c6fe3e59a0be139877d5b4903a69aa98e544da72347a44318d4b07`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f9f6a1366e4d4e23057b4d1c0f2442ae367cc0b567feaddafcbd5bbc845c17`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a7a3b31eca3818d52e31f9f288cb5e3ea43b7430afa552f6a9548571db371`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 5.9 MB (5932082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac86a6685eec20c9a4b40deefec34d3790b1934282e8822d8834396c26e3dfc`  
		Last Modified: Wed, 04 Jun 2025 05:02:46 GMT  
		Size: 358.6 MB (358570357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c44bf93f309a857c4ac362365f8d3176e30142386fb84e26115c85e2052c2f`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d976d31a9bc2b46120521375d77aed71c2f6546ff60474d7a2e98c86b26b1a0`  
		Last Modified: Wed, 04 Jun 2025 05:02:36 GMT  
		Size: 15.8 MB (15834538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e9d0cbd120c61cff600c9f318346a653eb1d68667cde359601d59467b05d0512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4258258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8027d18be2982405cb2532639842936b2ef66c9e7d36afc1011615ce0ce51e8`

```dockerfile
```

-	Layers:
	-	`sha256:469047e5cc94a05805092adb0a73dc740f3ea33d6181ee37609035c8ec2b77b4`  
		Last Modified: Wed, 04 Jun 2025 05:02:59 GMT  
		Size: 4.2 MB (4239186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f4912b081875f1b2404f65f31523101149dcdebeca3b886cfb630900595f84a`  
		Last Modified: Wed, 04 Jun 2025 05:02:59 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

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
		Last Modified: Thu, 05 Jun 2025 00:19:42 GMT  
		Size: 5.8 MB (5803141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c19178fc8cffd13abb189db9b8fad487b9f22b84582e042c2d430e282f18ace5`  
		Last Modified: Thu, 05 Jun 2025 00:19:44 GMT  
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
		Last Modified: Sun, 15 Jun 2025 18:51:41 GMT  
		Size: 36.5 KB (36501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a58aa4b2024924db977d17ab2fd3caf12d4571ddfbee6d2d3330aaabcebbf5`  
		Last Modified: Wed, 21 May 2025 18:06:03 GMT  
		Size: 17.6 MB (17561350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cc197f05aa36ccbd374a8ec7badcda06d65d2d3de66c52a39e037e860531df`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917e64cc886d2ef11e3ff36c46d506fe48759c45ed90a3f8c92b215e62eac6e`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92d93d73c0d3706db19d4bb6c06f7fc87136b190fa162c9c78cba222fc80bc`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 12.3 KB (12310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0d149692bc57f4b195b5f42a331ecc56735d5e55785d9f4f8e7449dd9a26f4`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5233e77b413ba5c4aa8ce78f29eb598b76353518214fb19b0c52246d25a29d`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
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

## `websphere-liberty:full-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:c6c3c5e05feb128a3a9de0e6fa5cb9da4c77faa1dfa6b74864bcd2bd305f8d09
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
$ docker pull websphere-liberty@sha256:e0152285b88679f4de553b20eeec954c671c123ed32a0fadfcd561702b20e13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.5 MB (493544619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944960e05253c6d61927514bf7c23c83f26e0a77c8cbb77bdcac245a5db52322`
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
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:33f177f5db89270b070e1644af124a467a0c875ee09cfc1fa9239b72eea64c0c`  
		Last Modified: Fri, 09 May 2025 16:44:19 GMT  
		Size: 12.2 MB (12172112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688483665c04fc1d231ea5dbc2ea70ccbc9c8d122bfc6b7e099fb087cf466b2`  
		Last Modified: Fri, 09 May 2025 16:44:25 GMT  
		Size: 51.7 MB (51747279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b08cf00ef33c315cf466a143b8b007197e30ed1139cf5830bea6d5c390206b`  
		Last Modified: Fri, 09 May 2025 16:44:18 GMT  
		Size: 5.0 MB (4978829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175c0d505316a2c055673fbe9a5cca1b8637ead503ca434c9301f3b56e1cff8`  
		Last Modified: Tue, 03 Jun 2025 15:32:59 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fb34af86fa29ac26af1ad00ef61675ec4a6b7cdfc6c84e3466fa0682d03e2e`  
		Last Modified: Tue, 03 Jun 2025 15:33:01 GMT  
		Size: 17.6 MB (17561046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde9a7bb49df78419330de1ad03a5d6c45cef5b314ef6a24ce764e055b4e13c5`  
		Last Modified: Tue, 03 Jun 2025 15:33:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b97fbe96d2a999315a689052499bcf3488b5a4708f5eb684f2e6cf72c210d0d`  
		Last Modified: Tue, 03 Jun 2025 15:33:00 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0527d54ebf3d3ee6b73dd45a2cd8e892524cdb03f82d1f7d5de709aa02eb1bf`  
		Last Modified: Tue, 03 Jun 2025 15:33:01 GMT  
		Size: 12.3 KB (12312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dda1fa7d68fb8e0c823a4f5f93bef2571eb4cf0a47b652315b0228c0ca14ee`  
		Last Modified: Tue, 03 Jun 2025 15:33:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c65b6bba5aab8a79b3f32fff42baeeceb82cbaa411b284373b928c8060173e`  
		Last Modified: Tue, 03 Jun 2025 15:33:02 GMT  
		Size: 13.1 KB (13118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17667b5fd5c5e34b4cebd0ac012f55b27f97a4ebd5ec58f83921c31d2493ab8`  
		Last Modified: Tue, 03 Jun 2025 15:33:03 GMT  
		Size: 2.8 MB (2829545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9c2ec437a647f95ded2cfe0ff226ed489711aee550f00aa06490ccb00328c6`  
		Last Modified: Tue, 03 Jun 2025 15:43:38 GMT  
		Size: 358.6 MB (358571945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7033ca8172c0dc86e3066961f3cabbbc0bf9d4721d15079f6a2aaabe8011eae0`  
		Last Modified: Tue, 03 Jun 2025 15:43:17 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf74f9a4ec9c08dfa3678061f540ac2879fb02c6f780eb963592458b45650e`  
		Last Modified: Tue, 03 Jun 2025 15:43:19 GMT  
		Size: 16.1 MB (16090884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a6ebd41217666bf6ad75c24d81d83948f5cbd3acbcab870e9075f979722bb773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5809619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874e07788d3b98ccdf53e8b999ee39acbfc4ab682b6227e6ea296f37a858e853`

```dockerfile
```

-	Layers:
	-	`sha256:5d232e0674f25f2404399be91125df2bdfeb5afc9e732020dbab5905491b27fe`  
		Last Modified: Thu, 05 Jun 2025 00:19:28 GMT  
		Size: 5.8 MB (5790012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff2410ce65bd15bb37460be698efab5990f0fc08cc9c49d59e5a319d9e1d873b`  
		Last Modified: Thu, 05 Jun 2025 00:19:29 GMT  
		Size: 19.6 KB (19607 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:923a934df48f5926bafa81c68cf25e3c24f9e4efa717ad7f860139105ed12396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.6 MB (486626829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a3d820a9bb10f782073c8add305c7dcc7bfa9987b66d80b5ba86f1bdf70c9f`
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
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:87dacafeafdeb88805872487016c74fd9df84de6f2f46dc3979ebbbf50389bf4`  
		Last Modified: Fri, 09 May 2025 17:01:24 GMT  
		Size: 48.2 MB (48190754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94a0d837c9514d458b3301307a2a14be1df802d94a9f125d286ae35ed868894`  
		Last Modified: Fri, 09 May 2025 17:01:12 GMT  
		Size: 4.8 MB (4759116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d393e4c4b0bee9a6f9d88495065877f0c522355586f8dcfac896f69b59c8c`  
		Last Modified: Tue, 17 Jun 2025 14:54:03 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388d777effad922349aeec967ef58c833b8ceac1eba24744f82000192c101cf`  
		Last Modified: Tue, 17 Jun 2025 14:54:11 GMT  
		Size: 17.6 MB (17561071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee078ddf572f5e406ae2d7e26086c5d9bd3e38bf86ce4a491a0c14dc913ff70`  
		Last Modified: Tue, 17 Jun 2025 14:54:05 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c4391ab2375ab60ff438d80f6928027e0c39454107b7055358ba9b5014dd5`  
		Last Modified: Tue, 17 Jun 2025 14:54:06 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fce6626cc2a221247d60d6a6b756072688ac21ad91238bb9c196a266cf2a7a`  
		Last Modified: Tue, 17 Jun 2025 14:54:08 GMT  
		Size: 12.3 KB (12309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9765a28c73d7c3f810ea9a48dbf61d4bcc3da10b20ce9e6005de325d5636113`  
		Last Modified: Tue, 17 Jun 2025 14:54:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3ff3d13783317d0a4534222cbfad572aaa0dd38535043ef3d3d5341be3cb5`  
		Last Modified: Tue, 17 Jun 2025 14:54:11 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca36a58b6515df925d2897d930a3a1c4481635c6d5d331a6bc07e87ab4a2d724`  
		Last Modified: Tue, 17 Jun 2025 14:54:13 GMT  
		Size: 2.7 MB (2742928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7216125fb177e71f49106dded6233b3bce65688ef3f8d4865b0429ed9f14ec4`  
		Last Modified: Wed, 21 May 2025 18:26:15 GMT  
		Size: 358.6 MB (358572913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98691502a04753ac730d60c03451d3008e985f0f1607a5ed8e3cbb1c69ee87db`  
		Last Modified: Wed, 21 May 2025 18:26:06 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f3c0dca5a2dd08463be94388080d60b9945e70faa77cca6e8965de9cdb3c37`  
		Last Modified: Wed, 21 May 2025 18:26:07 GMT  
		Size: 15.2 MB (15245483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:d11926b2fc75d4e9ac1987ae529dba6bfc384f7d55ef9cc2b2b8c00b6c1d9e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5803036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72254ae43b0e0028bddaba4e31570338e437d8aca3547cc9fcce11089b011bbd`

```dockerfile
```

-	Layers:
	-	`sha256:02a02fa5c527eb59b1e44474db751a475447a67aacb4020bba92a93dbed7d893`  
		Last Modified: Wed, 21 May 2025 18:26:06 GMT  
		Size: 5.8 MB (5783346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee39f99b96b3c14ef519a9faf67f860b47e4cb779e3f9285aa0ff7662814202`  
		Last Modified: Wed, 21 May 2025 18:26:06 GMT  
		Size: 19.7 KB (19690 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:4ce58ec3768adadfa28c6d69930d67da258031b7ce6cfaccb245c7d9cebe085a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.1 MB (497105667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9e2030dcb9e9d187b2a016c6c6d36b8e72c20b6e2a9754a81d55187ff35a8c`
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
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:190e6ee8a32dac2fb076f7645a0a113debd4b90af043fc447fe5e6e1c8d31868`  
		Last Modified: Fri, 09 May 2025 17:12:00 GMT  
		Size: 53.4 MB (53352875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd62acbf6795d22ba91011f6f0cf82c1f69a670578ca56391061054ea0aa2f41`  
		Last Modified: Fri, 09 May 2025 17:11:55 GMT  
		Size: 3.8 MB (3838355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b929a95b4a625b14aed068639e20e0a70114788627b46079c022ed666361348`  
		Last Modified: Wed, 21 May 2025 18:06:57 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469430594495bcbac84031b0ce849a9b1f3966f3abd7d6285b030388eeef294d`  
		Last Modified: Wed, 21 May 2025 18:06:58 GMT  
		Size: 17.6 MB (17561370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b41159037b417ce73d0e2cc8ab25c40487bc5154f552539a84fa81f630a610`  
		Last Modified: Wed, 21 May 2025 18:06:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb13f776ac80f64601b4a180c0cd1bb1a650360865bf70e3ab38c0ca3a7df1f`  
		Last Modified: Wed, 21 May 2025 18:06:57 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdb896391185516595e4478fb19a7678c809c4ba6c9e2083762756b22cb5820`  
		Last Modified: Wed, 21 May 2025 18:06:58 GMT  
		Size: 12.3 KB (12308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95ea371e3af8a70bf034079946a9fb87ee01ff7ee68ef029b354bad12c7c84`  
		Last Modified: Wed, 21 May 2025 18:06:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510a2346a093679bac5f53ab39185fb0b8718aca2f1b4604f190dad8aa2fb3e`  
		Last Modified: Wed, 21 May 2025 18:06:58 GMT  
		Size: 13.1 KB (13123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc53d24134c0e9cfd8f8ed08219ab920c796157245969676fffde3acd6ece18`  
		Last Modified: Wed, 21 May 2025 18:06:59 GMT  
		Size: 2.7 MB (2702259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ee84204644d16e140ad532d989f879c7c58341a5053a789369f8744776641f`  
		Last Modified: Wed, 21 May 2025 19:02:18 GMT  
		Size: 358.6 MB (358573232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec1810843fa0c8f143cc122561676cdc6a886d6787f78a5b3e43688a0de31f1`  
		Last Modified: Wed, 21 May 2025 19:02:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83943573cef234c68fa26f1206ca154999fa5868bdaea6af3224fb94c5f098f3`  
		Last Modified: Wed, 21 May 2025 19:02:10 GMT  
		Size: 13.7 MB (13676207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4ab7834518f6190e1b4f2a3eaed23d7bd3d6e07d3a4670fbc1f1bd610278ff89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5814269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92762738d639fd605c949983b66a8822b9731e5052393c96c54bf25d84d2380f`

```dockerfile
```

-	Layers:
	-	`sha256:6f18de99dd1ab566fd94c48a8be94adc755ffe95d71dd22fd6565b89c1e76358`  
		Last Modified: Wed, 21 May 2025 19:02:08 GMT  
		Size: 5.8 MB (5794633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c9c99f8d8c22066dee82f2d75d029921c45d76822a3d0c1de9724e736595042`  
		Last Modified: Wed, 21 May 2025 19:02:08 GMT  
		Size: 19.6 KB (19636 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:191316d8c56fe4383310a4f352cc977a5ed411514a258fd3991fd897cc69e50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.4 MB (491391025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dceb93efa8691453d5499322f51cfc827d8ebe3f9fead1cdf4f9cd1c60ea7475`
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
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:87c722eb1e516a736ab709561aaa1b82a951c0d4904e0d46a859b928acffa44a`  
		Last Modified: Fri, 09 May 2025 17:06:04 GMT  
		Size: 51.1 MB (51093317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c467b8956cc0ad8f37d6a013e09e17d8d05f76375bb59636f4848010d0197`  
		Last Modified: Fri, 09 May 2025 17:05:52 GMT  
		Size: 5.2 MB (5177039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74756497ad3aa835317da3674eb9697fc82e694df130eec33f3f4022487a7c5f`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3584ae9358356483393e4702dc9a14071caee4e7e85cf174fa66841dc88bd`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 17.6 MB (17560545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef83df25c66c8bda50a94f1ae58ee54612a29185152707365ebff26fb5589600`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5abc8026d1af1b39acc755aeb109fb9b8e35ec55dce0c8785bb07578e5d1e8`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a83fa3acf4b7927d5c4752dc5c9eae66ce81264c4ab160711ea7fbf067f1fa9`  
		Last Modified: Wed, 21 May 2025 18:08:27 GMT  
		Size: 12.3 KB (12312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44877ad4825c56fba8c4965a09beb718a147e4d1303754413b7b9bce39c9403a`  
		Last Modified: Wed, 21 May 2025 18:08:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1256994eb13f67647b48d04e5b114b975c892c20c014210e40e743b909331a`  
		Last Modified: Wed, 21 May 2025 18:08:27 GMT  
		Size: 13.1 KB (13111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6446c7fa4c9da7c2f49f2c6a69d2eadef324f87360aabfb71e7cb09c720829b5`  
		Last Modified: Wed, 21 May 2025 18:08:27 GMT  
		Size: 2.8 MB (2827348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a7668a043630129ab7bd6ae3d8020af96a9d8499c669339a5352d06b37412`  
		Last Modified: Wed, 21 May 2025 21:04:15 GMT  
		Size: 358.6 MB (358571580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af98c2774ea508d4f43cd7021f6bbdadd74469e63933b4e187e10a842c472f7`  
		Last Modified: Wed, 21 May 2025 21:04:09 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acbf14b92e554e6e8db0164d120081ff33d89f3fc6a883a3961146bc98f359a`  
		Last Modified: Wed, 21 May 2025 21:04:10 GMT  
		Size: 15.9 MB (15880287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:32085644cbee2e4931fc752803ba86f33bceab56138a1d5224b61c95b20e6715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3880c43e21339cf09efe648ad692002d71de0744d3295c74b28a9d5aeaa365`

```dockerfile
```

-	Layers:
	-	`sha256:1ea7eef994fe64b0ca881b9d7fec96683ac4ee2ed85ccad1a75427fd07bec430`  
		Last Modified: Wed, 21 May 2025 21:04:09 GMT  
		Size: 5.8 MB (5791029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072dc006ebdfbaf2eb8bdb2682f642662392987b8febc93f391c43eb74e16ffb`  
		Last Modified: Wed, 21 May 2025 21:04:09 GMT  
		Size: 19.6 KB (19608 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:0cda5f600207107e39e2a468f97a0287de449fad65767e1d09e2b295d21f3083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:47c75ddb034d2f2b52705a1cdac6bba5733ffab8498da95afb2c8806ebedea22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564608948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca78369e926edc12d3ad2c04854d17d1a0a8f9d919a9724c284d893d189bfc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75415249802d68499f7a1941c7251d11f4d9391ee70c7f0df518d0be883ba7e`  
		Last Modified: Tue, 03 Jun 2025 14:16:51 GMT  
		Size: 113.7 KB (113726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edc80817afad38e3785d0bc7f3d91828ee3134158a3409f3aba86e4e7aa5776`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 17.6 MB (17550494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36eead5fb6241f13557437967b02b83bc8dc7d08863223d4abe925ba85f8df1`  
		Last Modified: Tue, 03 Jun 2025 14:16:52 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad27209f5960e2b8879bcef1305b85508c3d6bdae7f61526d1ae6c7d721edd`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ab040de8607f25406752c9918d3c7caa0e7e8b0d0b86e29e8fef97022db64e`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 12.3 KB (12319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80a3f11f0b7b959c5607128adae26e0a53a2da9e9a8bd10d704e38346b68b0a`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f995b38748aa1f8ea7c95daf6c5d8fbb028082c48f8db9212d250445e7454146`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfe6d502e6b3addffbbeec97f7511919c759f4e3973dd56c7eeb5c9eb6eda3`  
		Last Modified: Tue, 03 Jun 2025 14:16:55 GMT  
		Size: 5.8 MB (5823975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3641934bf84333179274429afe221f0ff69ed444d8b2d59b9bf89d0230bbdf84`  
		Last Modified: Tue, 03 Jun 2025 14:17:15 GMT  
		Size: 358.6 MB (358568735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63547b71219d23c6134704852e9a7f563ff55097a07a64d0ac376a1a131325a9`  
		Last Modified: Tue, 03 Jun 2025 14:16:55 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6ba16b932f323ebc435a78303d0820609877a094623ad5c338be9fb73c2d75`  
		Last Modified: Tue, 03 Jun 2025 14:16:57 GMT  
		Size: 15.8 MB (15755383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ce20f432dde03200506a7307f9c33747c1be2565f0fbe54959c9bc7f9d5705df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4259497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb9f6177227c75cdf2453404ddffd432ab3beca52b370fb57927a5c346e9386`

```dockerfile
```

-	Layers:
	-	`sha256:14a4bc6d5404ab54ae1faf17aea5bde8147b4efb307d5f370e2be6f7ef5777f6`  
		Last Modified: Wed, 04 Jun 2025 05:12:16 GMT  
		Size: 4.2 MB (4240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30cd05474323ac7ea0f051871bba399e786c5d45496751624b11828a19189b4a`  
		Last Modified: Wed, 04 Jun 2025 05:12:15 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:e9d390c6147d6f70f19ae7261752476ea1b487c0d5c9502e4756c14525d18827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.6 MB (567616908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e7210c546a4590a8bab3f61fa260015e00480163fa00d1bf5a862c5704daa3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891109dd0128b9f59129f4522b4284aca40ef5ea9f2dc570cb2c0b92efb59fa1`  
		Last Modified: Tue, 03 Jun 2025 16:10:52 GMT  
		Size: 1.5 MB (1536197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab497349841ae340f3b59cbd984d37ac2febc7260aed616d8c1b733e3b32db5`  
		Last Modified: Tue, 03 Jun 2025 16:11:06 GMT  
		Size: 136.6 MB (136628900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b26050dbd70055fa94a2da973196f876da0abde8792c43affce987c73c1aa0`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 118.1 KB (118091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27079afba53f0e88887b24a16f942d42eccc606b18bdc07669969f59b85c7e2a`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 17.6 MB (17550846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf3bcc8757703456b292b2f799919849ef6066510ec79d05bc21d8ea983a47`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0434563abbb7ed9e55e070d9a8ea3598f9bf9749b32cfee52d213a29c41ea06`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c07c4d903aa42a243323bae348cd3aea27a547d87bdeb9edfdfe1524e97a5c`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 12.3 KB (12313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98b78706b42542cc9172c24cc28f75eaf3535da7430d6e1e1dda1fe84affb38`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8b72d2d4070334ead73504059918753c1d903a7b1c3e00b5b5065c98e769d`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 13.1 KB (13123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53959a503575f9e849b4cf9239c93c87532996a43a678e79c2998d640a0694`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 5.4 MB (5421942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaa7826ebd1b87521364bd0ae2ec2385aee49c4954198bfbc28f5ac0d74f243`  
		Last Modified: Wed, 04 Jun 2025 05:13:08 GMT  
		Size: 358.6 MB (358569873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7eebd4b74493ffbd28f5b5e48fa6271b325b11e39b48b28a445a2ede2c6e5f`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7008729647354a9b0e3cbf52f9c4c0e3f7b67ccfc10aabff18ab94846bc28c99`  
		Last Modified: Wed, 04 Jun 2025 05:12:27 GMT  
		Size: 13.3 MB (13321968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:cb627fd9e535dac57e43546563348cab2b84fc48fbda7fef8ad62e718b072172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4262812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051e5b337e803d1b779513d2e15d1142269a6befb594568a9f21b6ba88fc5cb1`

```dockerfile
```

-	Layers:
	-	`sha256:f1ceb13861906380c2003f41436f5cfd45be261502f1676933eee6e194f0c368`  
		Last Modified: Wed, 04 Jun 2025 05:12:45 GMT  
		Size: 4.2 MB (4243700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bed80af09e1ba1261a8b5b397c12ca24b2f41e8532fa0d89589113e1c61ed4c6`  
		Last Modified: Wed, 04 Jun 2025 05:12:45 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:aa9f26c6c3051b93a9517887e970501afaea282a9c60539d58774853992a8ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560298713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99b8ab2566500278e3eda621dd33cde1895117938aa93c815569dba6412a65a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc15cdcb77a0512baaf4cb0f2730505d8e69f2911c19853c7e981358bba8d62`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 114.6 KB (114588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff40b64b9af4bc8ab52ec9bd63b3b25bd2d440b1201007c0e812ee2c1852d36`  
		Last Modified: Wed, 04 Jun 2025 05:02:36 GMT  
		Size: 17.6 MB (17550225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42118c9e0c1a65af1ad88f5cde841bfb428ae6528aa35d9ab8cc7d810d8f45`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdae2fab9a2e4966319247c3a80d2b05d5f017f59587dd4b9bec711b180c7e`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a72f89d59315ca50a13f1dc1eba87d1e6dc849ffd0a5580c7e04b46b29f155`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 12.3 KB (12316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee99aa24c6fe3e59a0be139877d5b4903a69aa98e544da72347a44318d4b07`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f9f6a1366e4d4e23057b4d1c0f2442ae367cc0b567feaddafcbd5bbc845c17`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a7a3b31eca3818d52e31f9f288cb5e3ea43b7430afa552f6a9548571db371`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 5.9 MB (5932082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac86a6685eec20c9a4b40deefec34d3790b1934282e8822d8834396c26e3dfc`  
		Last Modified: Wed, 04 Jun 2025 05:02:46 GMT  
		Size: 358.6 MB (358570357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c44bf93f309a857c4ac362365f8d3176e30142386fb84e26115c85e2052c2f`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d976d31a9bc2b46120521375d77aed71c2f6546ff60474d7a2e98c86b26b1a0`  
		Last Modified: Wed, 04 Jun 2025 05:02:36 GMT  
		Size: 15.8 MB (15834538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e9d0cbd120c61cff600c9f318346a653eb1d68667cde359601d59467b05d0512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4258258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8027d18be2982405cb2532639842936b2ef66c9e7d36afc1011615ce0ce51e8`

```dockerfile
```

-	Layers:
	-	`sha256:469047e5cc94a05805092adb0a73dc740f3ea33d6181ee37609035c8ec2b77b4`  
		Last Modified: Wed, 04 Jun 2025 05:02:59 GMT  
		Size: 4.2 MB (4239186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f4912b081875f1b2404f65f31523101149dcdebeca3b886cfb630900595f84a`  
		Last Modified: Wed, 04 Jun 2025 05:02:59 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:8203760d764ca9eede11e6e04ed9058c183a2ef6a0598d0e491c86ad2916d170
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:9c32b3e6f480653edae3b95a315997c8823bc6261e3d5065d96f159347a36dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190283883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e2d5dea50bfbd20ddd4f6b22b8e015a31c41bea3399e9f5ea0875a358b4484`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75415249802d68499f7a1941c7251d11f4d9391ee70c7f0df518d0be883ba7e`  
		Last Modified: Tue, 03 Jun 2025 14:16:51 GMT  
		Size: 113.7 KB (113726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edc80817afad38e3785d0bc7f3d91828ee3134158a3409f3aba86e4e7aa5776`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 17.6 MB (17550494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36eead5fb6241f13557437967b02b83bc8dc7d08863223d4abe925ba85f8df1`  
		Last Modified: Tue, 03 Jun 2025 14:16:52 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad27209f5960e2b8879bcef1305b85508c3d6bdae7f61526d1ae6c7d721edd`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ab040de8607f25406752c9918d3c7caa0e7e8b0d0b86e29e8fef97022db64e`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 12.3 KB (12319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80a3f11f0b7b959c5607128adae26e0a53a2da9e9a8bd10d704e38346b68b0a`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f995b38748aa1f8ea7c95daf6c5d8fbb028082c48f8db9212d250445e7454146`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfe6d502e6b3addffbbeec97f7511919c759f4e3973dd56c7eeb5c9eb6eda3`  
		Last Modified: Tue, 03 Jun 2025 14:16:55 GMT  
		Size: 5.8 MB (5823975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a33d27ad1e73d957c2ddd1ff00d959b3dfdb93de32c5c6f5886e530323b5390a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfc7fd86a6f0f32648626e546a99b01391ac26edd356bcabb3ad7374c4bee75`

```dockerfile
```

-	Layers:
	-	`sha256:2555a62c18d84931b1db262f07e166748e237895b3073711b44d063099b2aa16`  
		Last Modified: Thu, 05 Jun 2025 00:22:47 GMT  
		Size: 2.2 MB (2204453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a267eb69307b9fd0c1e3a9fe46df30116acc87c020000f44f8fe494e1873776d`  
		Last Modified: Thu, 05 Jun 2025 00:22:49 GMT  
		Size: 38.3 KB (38291 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:169a43ad776406272dae87aa80679c7ef78976df5b40546d6cbc4c1288d29622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195724120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e76d8c94dc5608764c55617100352500ba952b1c83268caed26851870f4cd94`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891109dd0128b9f59129f4522b4284aca40ef5ea9f2dc570cb2c0b92efb59fa1`  
		Last Modified: Tue, 03 Jun 2025 16:10:52 GMT  
		Size: 1.5 MB (1536197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab497349841ae340f3b59cbd984d37ac2febc7260aed616d8c1b733e3b32db5`  
		Last Modified: Tue, 03 Jun 2025 16:11:06 GMT  
		Size: 136.6 MB (136628900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b26050dbd70055fa94a2da973196f876da0abde8792c43affce987c73c1aa0`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 118.1 KB (118091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27079afba53f0e88887b24a16f942d42eccc606b18bdc07669969f59b85c7e2a`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 17.6 MB (17550846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf3bcc8757703456b292b2f799919849ef6066510ec79d05bc21d8ea983a47`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0434563abbb7ed9e55e070d9a8ea3598f9bf9749b32cfee52d213a29c41ea06`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c07c4d903aa42a243323bae348cd3aea27a547d87bdeb9edfdfe1524e97a5c`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 12.3 KB (12313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98b78706b42542cc9172c24cc28f75eaf3535da7430d6e1e1dda1fe84affb38`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8b72d2d4070334ead73504059918753c1d903a7b1c3e00b5b5065c98e769d`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 13.1 KB (13123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53959a503575f9e849b4cf9239c93c87532996a43a678e79c2998d640a0694`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 5.4 MB (5421942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a5f919393c6d7f5519a80ea5ee951ae2836248ac26c5c0f00a9c68dd760b2ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c79be1fed7286e7efcaebd2d753ce33c7c3bc0585b1abcd1234644b0fc3af2e`

```dockerfile
```

-	Layers:
	-	`sha256:3f984f5f92f3b58718dac4f86c9d5690adce44a31abb560ca48d0ae4fff6f997`  
		Last Modified: Fri, 06 Jun 2025 21:13:30 GMT  
		Size: 2.2 MB (2207728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb392a624524771a1f09a35ef5ec42175eb64ef04b409d825852076347cc80bf`  
		Last Modified: Fri, 06 Jun 2025 21:13:28 GMT  
		Size: 38.3 KB (38337 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0f95c28b52ca89c78cc3a76924bf194bc5f59ed582bb1ff5e7e48130be6c2972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185892869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737fff0a53e892e2ad9388d35ee939d7f7105c6b45eaedbe8300351b68fee3b3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc15cdcb77a0512baaf4cb0f2730505d8e69f2911c19853c7e981358bba8d62`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 114.6 KB (114588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff40b64b9af4bc8ab52ec9bd63b3b25bd2d440b1201007c0e812ee2c1852d36`  
		Last Modified: Wed, 04 Jun 2025 05:02:36 GMT  
		Size: 17.6 MB (17550225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42118c9e0c1a65af1ad88f5cde841bfb428ae6528aa35d9ab8cc7d810d8f45`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdae2fab9a2e4966319247c3a80d2b05d5f017f59587dd4b9bec711b180c7e`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a72f89d59315ca50a13f1dc1eba87d1e6dc849ffd0a5580c7e04b46b29f155`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 12.3 KB (12316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee99aa24c6fe3e59a0be139877d5b4903a69aa98e544da72347a44318d4b07`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f9f6a1366e4d4e23057b4d1c0f2442ae367cc0b567feaddafcbd5bbc845c17`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a7a3b31eca3818d52e31f9f288cb5e3ea43b7430afa552f6a9548571db371`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 5.9 MB (5932082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:db009199ea870b1773ffedea76fe434e4b45d763dd5030369e5ad9f374f432ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6095c1d5180dcd82adc6b4be0b5d7569778c8e9e44f08456e32404c764c80fa`

```dockerfile
```

-	Layers:
	-	`sha256:4c57e795ac58e77f375a1c28d745fd73a167bb6f6a0d10a10142f883993bcdfa`  
		Last Modified: Fri, 06 Jun 2025 21:13:37 GMT  
		Size: 2.2 MB (2203214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16693d462339b88617d554006114d08a520f9e34d2f7dae90228d02ba2d8d445`  
		Last Modified: Fri, 06 Jun 2025 21:13:36 GMT  
		Size: 38.3 KB (38291 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:7dc66a4afc65e7e1dc159b54491a12d74ef100198a8c126154e25b25b27882b0
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

### `websphere-liberty:kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:a3c19467e37e514df4cbd411b89feabafd921a5600d0c0211b0e191165cadc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119040603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb398ac22582df47c95012aedabd9474cb5a9b5350c0818b68aafc2607fea094`
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

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:776fff2c52bbe4c8a7f5b03ff5ff5d720c826d8820af7db820941492766f884b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9d99a66a2071ce45b2f2f1043cc8ce4ee77a1abc994e43dc5eaa21c63fe712`

```dockerfile
```

-	Layers:
	-	`sha256:7447425232321a59f7df1bc13270a013b2283916637ec941d9c31b1c1881dc0a`  
		Last Modified: Thu, 05 Jun 2025 00:21:02 GMT  
		Size: 3.8 MB (3767485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d26b1b6cc281d9752250a2dd26304afbbe35b8066247b63ccdef9bffca7546`  
		Last Modified: Thu, 05 Jun 2025 00:21:04 GMT  
		Size: 40.1 KB (40130 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:09b7f0a51dbbaaffc227da179e548b95975828e158d6be97185151d2ff359056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112939591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e8d08daca2d14315afb9b44ae5059f005acd4d4b7b2b5e27b9f2f6f8189197`
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

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:98158f27965b6a48e303f9758f70a09f08cb452843ac546f152a9013adbe2f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b8bc74801861f572af0121eb14de33c71d98b1aedf0b998425af4bbdd952a2`

```dockerfile
```

-	Layers:
	-	`sha256:3d26eab9cebb9eb5db83418b9b11c4579f4b0e9ec607809ca887f8a43e337925`  
		Last Modified: Wed, 21 May 2025 17:50:47 GMT  
		Size: 3.8 MB (3760831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62747800cef3d238cf3d2e99ef52a6a42adaf81d9a28d268df0f0184239adac`  
		Last Modified: Wed, 21 May 2025 17:50:48 GMT  
		Size: 40.3 KB (40270 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:9d2663670e2d8110f1cd5b26728ebf0056ca2cc8ff09aa37b0641fca113c4558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125207497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986832b066337cf591832f0d523ab397832afe11ba734125f1ed7ee6eb6d4f7d`
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
		Last Modified: Sun, 15 Jun 2025 18:51:41 GMT  
		Size: 36.5 KB (36501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a58aa4b2024924db977d17ab2fd3caf12d4571ddfbee6d2d3330aaabcebbf5`  
		Last Modified: Wed, 21 May 2025 18:06:03 GMT  
		Size: 17.6 MB (17561350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cc197f05aa36ccbd374a8ec7badcda06d65d2d3de66c52a39e037e860531df`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917e64cc886d2ef11e3ff36c46d506fe48759c45ed90a3f8c92b215e62eac6e`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92d93d73c0d3706db19d4bb6c06f7fc87136b190fa162c9c78cba222fc80bc`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 12.3 KB (12310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0d149692bc57f4b195b5f42a331ecc56735d5e55785d9f4f8e7449dd9a26f4`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5233e77b413ba5c4aa8ce78f29eb598b76353518214fb19b0c52246d25a29d`  
		Last Modified: Sun, 15 Jun 2025 18:51:42 GMT  
		Size: 13.1 KB (13117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5db835dc9a52db58b35e127c2533ec506fa9d0c85e44989e65c06f32cf3d649`  
		Last Modified: Wed, 21 May 2025 18:06:05 GMT  
		Size: 2.7 MB (2695977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:700605fd4ebc8146633e3df169eb04ae9a8e26c1e0101646f2dad0fec9d3e2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7720f5bb5a6789e246111fc5a9632bcbf356f5aaac30a2d206d10d1114e13497`

```dockerfile
```

-	Layers:
	-	`sha256:c51eef85164e46dee3ab46c03a5fad2c80a462095d65c57b804cb3e1f28bac90`  
		Last Modified: Wed, 21 May 2025 18:06:03 GMT  
		Size: 3.8 MB (3772112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120456c1a411e0d3dcce3d2a50ea0a0da06c525e300d7eb69b6bfc4185020a66`  
		Last Modified: Wed, 21 May 2025 18:06:02 GMT  
		Size: 40.2 KB (40170 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:4b538049c516aef15ac0caa4922dbe7ab87ab1436670070b894d78ac6e566701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116588942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a293fd5032a949a4896d4971a080836c1722db2c27ff3eb63bae063cabf14af0`
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

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:3a5a8bf1fd7a297b90a1b8101bea82c915b0dc71674108f5f9dc14b330379755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468c54b170d78c55963ccaf78ee1a18548562ed23f35a2acf4c2245502437c0a`

```dockerfile
```

-	Layers:
	-	`sha256:1d2d9aaedd6c1f6b5a91c2fc5ad5faa65fa481356caa0dcce9b987831ae9f01e`  
		Last Modified: Wed, 21 May 2025 18:07:31 GMT  
		Size: 3.8 MB (3768502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbff7b33e858382967841e2a36bb9d1366632729a9f9cfb735f2b697f498063`  
		Last Modified: Wed, 21 May 2025 18:07:31 GMT  
		Size: 40.1 KB (40130 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:kernel-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:a36beb8295beb862f0e1ba51aabe2311d85f9772a5c2c0e6a3e27b8a4648f97d
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

### `websphere-liberty:kernel-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:d9482a20272b97e54536cf3a7919b80d858d6d12daeecd1a3f82027004bf6731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118880847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4879f9aee4a11d825d31ba686390eed2a1fecae248c723414d26aec45db4c3fe`
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
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f177f5db89270b070e1644af124a467a0c875ee09cfc1fa9239b72eea64c0c`  
		Last Modified: Fri, 09 May 2025 16:44:19 GMT  
		Size: 12.2 MB (12172112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688483665c04fc1d231ea5dbc2ea70ccbc9c8d122bfc6b7e099fb087cf466b2`  
		Last Modified: Fri, 09 May 2025 16:44:25 GMT  
		Size: 51.7 MB (51747279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b08cf00ef33c315cf466a143b8b007197e30ed1139cf5830bea6d5c390206b`  
		Last Modified: Fri, 09 May 2025 16:44:18 GMT  
		Size: 5.0 MB (4978829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175c0d505316a2c055673fbe9a5cca1b8637ead503ca434c9301f3b56e1cff8`  
		Last Modified: Tue, 03 Jun 2025 15:32:59 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fb34af86fa29ac26af1ad00ef61675ec4a6b7cdfc6c84e3466fa0682d03e2e`  
		Last Modified: Tue, 03 Jun 2025 15:33:01 GMT  
		Size: 17.6 MB (17561046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde9a7bb49df78419330de1ad03a5d6c45cef5b314ef6a24ce764e055b4e13c5`  
		Last Modified: Tue, 03 Jun 2025 15:33:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b97fbe96d2a999315a689052499bcf3488b5a4708f5eb684f2e6cf72c210d0d`  
		Last Modified: Tue, 03 Jun 2025 15:33:00 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0527d54ebf3d3ee6b73dd45a2cd8e892524cdb03f82d1f7d5de709aa02eb1bf`  
		Last Modified: Tue, 03 Jun 2025 15:33:01 GMT  
		Size: 12.3 KB (12312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dda1fa7d68fb8e0c823a4f5f93bef2571eb4cf0a47b652315b0228c0ca14ee`  
		Last Modified: Tue, 03 Jun 2025 15:33:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c65b6bba5aab8a79b3f32fff42baeeceb82cbaa411b284373b928c8060173e`  
		Last Modified: Tue, 03 Jun 2025 15:33:02 GMT  
		Size: 13.1 KB (13118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17667b5fd5c5e34b4cebd0ac012f55b27f97a4ebd5ec58f83921c31d2493ab8`  
		Last Modified: Tue, 03 Jun 2025 15:33:03 GMT  
		Size: 2.8 MB (2829545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:71630df5049c94804d9e205b457eaaf1d35ce680e1cfce59699dcc0d827aac7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2304d82ade6364202da2e1c9f90c522e36f57fd395f4e7aeb31e760e2bf2f756`

```dockerfile
```

-	Layers:
	-	`sha256:d8b2e412933da879e23ef6ebc6efdc8852466e491047d8b234f7a593f2ce328f`  
		Last Modified: Thu, 05 Jun 2025 00:20:50 GMT  
		Size: 3.8 MB (3754356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fcc8e8a8bf1d295bd0ab77775c6028f2141ab4865295d8af1cbc03471f48d21`  
		Last Modified: Thu, 05 Jun 2025 00:20:51 GMT  
		Size: 40.1 KB (40130 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:1f73e7578cec52262d23f0fdf2d7480caa30bfb6a3e0b0dd2ae2af288874059a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112807490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f098524058349df09d094aa34220a7337685490f2d01263cfbfd2e844fe041b6`
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
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:87dacafeafdeb88805872487016c74fd9df84de6f2f46dc3979ebbbf50389bf4`  
		Last Modified: Fri, 09 May 2025 17:01:24 GMT  
		Size: 48.2 MB (48190754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94a0d837c9514d458b3301307a2a14be1df802d94a9f125d286ae35ed868894`  
		Last Modified: Fri, 09 May 2025 17:01:12 GMT  
		Size: 4.8 MB (4759116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d393e4c4b0bee9a6f9d88495065877f0c522355586f8dcfac896f69b59c8c`  
		Last Modified: Tue, 17 Jun 2025 14:54:03 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1388d777effad922349aeec967ef58c833b8ceac1eba24744f82000192c101cf`  
		Last Modified: Tue, 17 Jun 2025 14:54:11 GMT  
		Size: 17.6 MB (17561071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee078ddf572f5e406ae2d7e26086c5d9bd3e38bf86ce4a491a0c14dc913ff70`  
		Last Modified: Tue, 17 Jun 2025 14:54:05 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021c4391ab2375ab60ff438d80f6928027e0c39454107b7055358ba9b5014dd5`  
		Last Modified: Tue, 17 Jun 2025 14:54:06 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fce6626cc2a221247d60d6a6b756072688ac21ad91238bb9c196a266cf2a7a`  
		Last Modified: Tue, 17 Jun 2025 14:54:08 GMT  
		Size: 12.3 KB (12309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9765a28c73d7c3f810ea9a48dbf61d4bcc3da10b20ce9e6005de325d5636113`  
		Last Modified: Tue, 17 Jun 2025 14:54:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff3ff3d13783317d0a4534222cbfad572aaa0dd38535043ef3d3d5341be3cb5`  
		Last Modified: Tue, 17 Jun 2025 14:54:11 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca36a58b6515df925d2897d930a3a1c4481635c6d5d331a6bc07e87ab4a2d724`  
		Last Modified: Tue, 17 Jun 2025 14:54:13 GMT  
		Size: 2.7 MB (2742928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:55cf57da4c24d30475b64b05dbd001258b07046c70e9d6c289a4fe3a0e149c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3787972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220186ecfcdd348bf3bdebcae7fc2dcc531b16725bc243b0ed52a6559cc67ed8`

```dockerfile
```

-	Layers:
	-	`sha256:1857ee4ad4db7f55cf86a293ba6b311b2b557f060edcba271e745c7dd7d72bd5`  
		Last Modified: Wed, 21 May 2025 17:51:24 GMT  
		Size: 3.7 MB (3747702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1080f7bbba5d74d61cfcad025871ad5258bb033280531553acf55d575372febb`  
		Last Modified: Wed, 21 May 2025 17:51:24 GMT  
		Size: 40.3 KB (40270 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:4892779473157ff87125758bd525b5844d37aa8e88eb650bc6028cfa0ad7960e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124855279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f56d30c52c6f58f38726406462535b3c5b24a5d2434ef7479e85a4135d4cd44`
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
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:190e6ee8a32dac2fb076f7645a0a113debd4b90af043fc447fe5e6e1c8d31868`  
		Last Modified: Fri, 09 May 2025 17:12:00 GMT  
		Size: 53.4 MB (53352875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd62acbf6795d22ba91011f6f0cf82c1f69a670578ca56391061054ea0aa2f41`  
		Last Modified: Fri, 09 May 2025 17:11:55 GMT  
		Size: 3.8 MB (3838355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b929a95b4a625b14aed068639e20e0a70114788627b46079c022ed666361348`  
		Last Modified: Wed, 21 May 2025 18:06:57 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469430594495bcbac84031b0ce849a9b1f3966f3abd7d6285b030388eeef294d`  
		Last Modified: Wed, 21 May 2025 18:06:58 GMT  
		Size: 17.6 MB (17561370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b41159037b417ce73d0e2cc8ab25c40487bc5154f552539a84fa81f630a610`  
		Last Modified: Wed, 21 May 2025 18:06:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb13f776ac80f64601b4a180c0cd1bb1a650360865bf70e3ab38c0ca3a7df1f`  
		Last Modified: Wed, 21 May 2025 18:06:57 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdb896391185516595e4478fb19a7678c809c4ba6c9e2083762756b22cb5820`  
		Last Modified: Wed, 21 May 2025 18:06:58 GMT  
		Size: 12.3 KB (12308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb95ea371e3af8a70bf034079946a9fb87ee01ff7ee68ef029b354bad12c7c84`  
		Last Modified: Wed, 21 May 2025 18:06:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510a2346a093679bac5f53ab39185fb0b8718aca2f1b4604f190dad8aa2fb3e`  
		Last Modified: Wed, 21 May 2025 18:06:58 GMT  
		Size: 13.1 KB (13123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc53d24134c0e9cfd8f8ed08219ab920c796157245969676fffde3acd6ece18`  
		Last Modified: Wed, 21 May 2025 18:06:59 GMT  
		Size: 2.7 MB (2702259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:28eb36021f620cff62849cb9f35cdd04dfb585912ee786823762032d22c756e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642409dce5e3bb8792ff87aed64802cf6bff3a1db55c9410b163b69e15f287f8`

```dockerfile
```

-	Layers:
	-	`sha256:5eb3c948e1483d6c608f4db793eec684b35fbe22395d858e317c547b47778f98`  
		Last Modified: Wed, 21 May 2025 18:06:57 GMT  
		Size: 3.8 MB (3758983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01a14b2b5b8cd83759ccc4df8cf348ae6172bff5e255dc0f34c327916763d3a7`  
		Last Modified: Wed, 21 May 2025 18:06:57 GMT  
		Size: 40.2 KB (40170 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:a376016f08e53d2b0111f2becc3001ac12c49a850112a77b2480ed3acedfc892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116938215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074126d41f96aeb3ec6a96f8579c77a3c79178298438646f6a90415ff154fdd7`
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
ENV JAVA_VERSION=jdk-17.0.15+6_openj9-0.51.0
# Wed, 07 May 2025 17:42:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9a44da58055525719ddb87b2fe21a02562a0897b8b537a65b7a94b1ab28f7eb0';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e852a334a4a3f59bd8478ffe3190bbdb520fa37d8954e17fc7842ede979b15fa';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c4cc045bfd63fc6412251fef184c91a1acad76d74ee48561fd48c174fb1278d3';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='6e1afeea17e8d9538bf65c0672482e3813f13a7d61ee74ad75b2372225df53ba';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.15%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_17.0.15_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:87c722eb1e516a736ab709561aaa1b82a951c0d4904e0d46a859b928acffa44a`  
		Last Modified: Fri, 09 May 2025 17:06:04 GMT  
		Size: 51.1 MB (51093317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c467b8956cc0ad8f37d6a013e09e17d8d05f76375bb59636f4848010d0197`  
		Last Modified: Fri, 09 May 2025 17:05:52 GMT  
		Size: 5.2 MB (5177039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74756497ad3aa835317da3674eb9697fc82e694df130eec33f3f4022487a7c5f`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3584ae9358356483393e4702dc9a14071caee4e7e85cf174fa66841dc88bd`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 17.6 MB (17560545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef83df25c66c8bda50a94f1ae58ee54612a29185152707365ebff26fb5589600`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5abc8026d1af1b39acc755aeb109fb9b8e35ec55dce0c8785bb07578e5d1e8`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a83fa3acf4b7927d5c4752dc5c9eae66ce81264c4ab160711ea7fbf067f1fa9`  
		Last Modified: Wed, 21 May 2025 18:08:27 GMT  
		Size: 12.3 KB (12312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44877ad4825c56fba8c4965a09beb718a147e4d1303754413b7b9bce39c9403a`  
		Last Modified: Wed, 21 May 2025 18:08:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1256994eb13f67647b48d04e5b114b975c892c20c014210e40e743b909331a`  
		Last Modified: Wed, 21 May 2025 18:08:27 GMT  
		Size: 13.1 KB (13111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6446c7fa4c9da7c2f49f2c6a69d2eadef324f87360aabfb71e7cb09c720829b5`  
		Last Modified: Wed, 21 May 2025 18:08:27 GMT  
		Size: 2.8 MB (2827348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java17-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:c2de0c26e91f24ebbd45daae916b8426607ea4ff42a721c60460cbe761bb8edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f73f58edf15c03259d22a4b0e591d02a20269a903097a9b44b3a6c71b564eef`

```dockerfile
```

-	Layers:
	-	`sha256:090f44268204e72a0c338177c719988f86f1c6f2c2515aae84536acfa5d4c456`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 3.8 MB (3755373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a7457accdb2e926d62ace247755235d83b00a133ad40f42a9aad185607e4db4`  
		Last Modified: Wed, 21 May 2025 18:08:26 GMT  
		Size: 40.1 KB (40130 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:8203760d764ca9eede11e6e04ed9058c183a2ef6a0598d0e491c86ad2916d170
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:9c32b3e6f480653edae3b95a315997c8823bc6261e3d5065d96f159347a36dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190283883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e2d5dea50bfbd20ddd4f6b22b8e015a31c41bea3399e9f5ea0875a358b4484`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75415249802d68499f7a1941c7251d11f4d9391ee70c7f0df518d0be883ba7e`  
		Last Modified: Tue, 03 Jun 2025 14:16:51 GMT  
		Size: 113.7 KB (113726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edc80817afad38e3785d0bc7f3d91828ee3134158a3409f3aba86e4e7aa5776`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 17.6 MB (17550494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36eead5fb6241f13557437967b02b83bc8dc7d08863223d4abe925ba85f8df1`  
		Last Modified: Tue, 03 Jun 2025 14:16:52 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad27209f5960e2b8879bcef1305b85508c3d6bdae7f61526d1ae6c7d721edd`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ab040de8607f25406752c9918d3c7caa0e7e8b0d0b86e29e8fef97022db64e`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 12.3 KB (12319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80a3f11f0b7b959c5607128adae26e0a53a2da9e9a8bd10d704e38346b68b0a`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f995b38748aa1f8ea7c95daf6c5d8fbb028082c48f8db9212d250445e7454146`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfe6d502e6b3addffbbeec97f7511919c759f4e3973dd56c7eeb5c9eb6eda3`  
		Last Modified: Tue, 03 Jun 2025 14:16:55 GMT  
		Size: 5.8 MB (5823975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a33d27ad1e73d957c2ddd1ff00d959b3dfdb93de32c5c6f5886e530323b5390a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfc7fd86a6f0f32648626e546a99b01391ac26edd356bcabb3ad7374c4bee75`

```dockerfile
```

-	Layers:
	-	`sha256:2555a62c18d84931b1db262f07e166748e237895b3073711b44d063099b2aa16`  
		Last Modified: Thu, 05 Jun 2025 00:22:47 GMT  
		Size: 2.2 MB (2204453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a267eb69307b9fd0c1e3a9fe46df30116acc87c020000f44f8fe494e1873776d`  
		Last Modified: Thu, 05 Jun 2025 00:22:49 GMT  
		Size: 38.3 KB (38291 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:169a43ad776406272dae87aa80679c7ef78976df5b40546d6cbc4c1288d29622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195724120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e76d8c94dc5608764c55617100352500ba952b1c83268caed26851870f4cd94`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891109dd0128b9f59129f4522b4284aca40ef5ea9f2dc570cb2c0b92efb59fa1`  
		Last Modified: Tue, 03 Jun 2025 16:10:52 GMT  
		Size: 1.5 MB (1536197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab497349841ae340f3b59cbd984d37ac2febc7260aed616d8c1b733e3b32db5`  
		Last Modified: Tue, 03 Jun 2025 16:11:06 GMT  
		Size: 136.6 MB (136628900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b26050dbd70055fa94a2da973196f876da0abde8792c43affce987c73c1aa0`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 118.1 KB (118091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27079afba53f0e88887b24a16f942d42eccc606b18bdc07669969f59b85c7e2a`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 17.6 MB (17550846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf3bcc8757703456b292b2f799919849ef6066510ec79d05bc21d8ea983a47`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0434563abbb7ed9e55e070d9a8ea3598f9bf9749b32cfee52d213a29c41ea06`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c07c4d903aa42a243323bae348cd3aea27a547d87bdeb9edfdfe1524e97a5c`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 12.3 KB (12313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98b78706b42542cc9172c24cc28f75eaf3535da7430d6e1e1dda1fe84affb38`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8b72d2d4070334ead73504059918753c1d903a7b1c3e00b5b5065c98e769d`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 13.1 KB (13123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53959a503575f9e849b4cf9239c93c87532996a43a678e79c2998d640a0694`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 5.4 MB (5421942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a5f919393c6d7f5519a80ea5ee951ae2836248ac26c5c0f00a9c68dd760b2ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c79be1fed7286e7efcaebd2d753ce33c7c3bc0585b1abcd1234644b0fc3af2e`

```dockerfile
```

-	Layers:
	-	`sha256:3f984f5f92f3b58718dac4f86c9d5690adce44a31abb560ca48d0ae4fff6f997`  
		Last Modified: Fri, 06 Jun 2025 21:13:30 GMT  
		Size: 2.2 MB (2207728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb392a624524771a1f09a35ef5ec42175eb64ef04b409d825852076347cc80bf`  
		Last Modified: Fri, 06 Jun 2025 21:13:28 GMT  
		Size: 38.3 KB (38337 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0f95c28b52ca89c78cc3a76924bf194bc5f59ed582bb1ff5e7e48130be6c2972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185892869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737fff0a53e892e2ad9388d35ee939d7f7105c6b45eaedbe8300351b68fee3b3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 May 2025 02:47:06 GMT
USER 1001
# Wed, 21 May 2025 02:47:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 21 May 2025 02:47:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 May 2025 02:47:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc15cdcb77a0512baaf4cb0f2730505d8e69f2911c19853c7e981358bba8d62`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 114.6 KB (114588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff40b64b9af4bc8ab52ec9bd63b3b25bd2d440b1201007c0e812ee2c1852d36`  
		Last Modified: Wed, 04 Jun 2025 05:02:36 GMT  
		Size: 17.6 MB (17550225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42118c9e0c1a65af1ad88f5cde841bfb428ae6528aa35d9ab8cc7d810d8f45`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdae2fab9a2e4966319247c3a80d2b05d5f017f59587dd4b9bec711b180c7e`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a72f89d59315ca50a13f1dc1eba87d1e6dc849ffd0a5580c7e04b46b29f155`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 12.3 KB (12316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee99aa24c6fe3e59a0be139877d5b4903a69aa98e544da72347a44318d4b07`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f9f6a1366e4d4e23057b4d1c0f2442ae367cc0b567feaddafcbd5bbc845c17`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a7a3b31eca3818d52e31f9f288cb5e3ea43b7430afa552f6a9548571db371`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 5.9 MB (5932082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java8-ibmjava` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:db009199ea870b1773ffedea76fe434e4b45d763dd5030369e5ad9f374f432ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6095c1d5180dcd82adc6b4be0b5d7569778c8e9e44f08456e32404c764c80fa`

```dockerfile
```

-	Layers:
	-	`sha256:4c57e795ac58e77f375a1c28d745fd73a167bb6f6a0d10a10142f883993bcdfa`  
		Last Modified: Fri, 06 Jun 2025 21:13:37 GMT  
		Size: 2.2 MB (2203214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16693d462339b88617d554006114d08a520f9e34d2f7dae90228d02ba2d8d445`  
		Last Modified: Fri, 06 Jun 2025 21:13:36 GMT  
		Size: 38.3 KB (38291 bytes)  
		MIME: application/vnd.in-toto+json

## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:0cda5f600207107e39e2a468f97a0287de449fad65767e1d09e2b295d21f3083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:47c75ddb034d2f2b52705a1cdac6bba5733ffab8498da95afb2c8806ebedea22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564608948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca78369e926edc12d3ad2c04854d17d1a0a8f9d919a9724c284d893d189bfc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f06ff4237d1798f0ebd3851a8941e8b612bbe8d75ff294ec581b79cd412b52`  
		Last Modified: Tue, 03 Jun 2025 13:43:27 GMT  
		Size: 1.5 MB (1450052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe1b43d619ec15a97053ad201ebe19da2ce6c863499cee12c5632f29b2df627`  
		Last Modified: Tue, 03 Jun 2025 13:43:35 GMT  
		Size: 135.8 MB (135784832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75415249802d68499f7a1941c7251d11f4d9391ee70c7f0df518d0be883ba7e`  
		Last Modified: Tue, 03 Jun 2025 14:16:51 GMT  
		Size: 113.7 KB (113726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edc80817afad38e3785d0bc7f3d91828ee3134158a3409f3aba86e4e7aa5776`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 17.6 MB (17550494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36eead5fb6241f13557437967b02b83bc8dc7d08863223d4abe925ba85f8df1`  
		Last Modified: Tue, 03 Jun 2025 14:16:52 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ad27209f5960e2b8879bcef1305b85508c3d6bdae7f61526d1ae6c7d721edd`  
		Last Modified: Tue, 03 Jun 2025 14:16:53 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ab040de8607f25406752c9918d3c7caa0e7e8b0d0b86e29e8fef97022db64e`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 12.3 KB (12319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80a3f11f0b7b959c5607128adae26e0a53a2da9e9a8bd10d704e38346b68b0a`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f995b38748aa1f8ea7c95daf6c5d8fbb028082c48f8db9212d250445e7454146`  
		Last Modified: Tue, 03 Jun 2025 14:16:54 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfe6d502e6b3addffbbeec97f7511919c759f4e3973dd56c7eeb5c9eb6eda3`  
		Last Modified: Tue, 03 Jun 2025 14:16:55 GMT  
		Size: 5.8 MB (5823975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3641934bf84333179274429afe221f0ff69ed444d8b2d59b9bf89d0230bbdf84`  
		Last Modified: Tue, 03 Jun 2025 14:17:15 GMT  
		Size: 358.6 MB (358568735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63547b71219d23c6134704852e9a7f563ff55097a07a64d0ac376a1a131325a9`  
		Last Modified: Tue, 03 Jun 2025 14:16:55 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6ba16b932f323ebc435a78303d0820609877a094623ad5c338be9fb73c2d75`  
		Last Modified: Tue, 03 Jun 2025 14:16:57 GMT  
		Size: 15.8 MB (15755383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:ce20f432dde03200506a7307f9c33747c1be2565f0fbe54959c9bc7f9d5705df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4259497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb9f6177227c75cdf2453404ddffd432ab3beca52b370fb57927a5c346e9386`

```dockerfile
```

-	Layers:
	-	`sha256:14a4bc6d5404ab54ae1faf17aea5bde8147b4efb307d5f370e2be6f7ef5777f6`  
		Last Modified: Wed, 04 Jun 2025 05:12:16 GMT  
		Size: 4.2 MB (4240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30cd05474323ac7ea0f051871bba399e786c5d45496751624b11828a19189b4a`  
		Last Modified: Wed, 04 Jun 2025 05:12:15 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:e9d390c6147d6f70f19ae7261752476ea1b487c0d5c9502e4756c14525d18827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.6 MB (567616908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e7210c546a4590a8bab3f61fa260015e00480163fa00d1bf5a862c5704daa3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891109dd0128b9f59129f4522b4284aca40ef5ea9f2dc570cb2c0b92efb59fa1`  
		Last Modified: Tue, 03 Jun 2025 16:10:52 GMT  
		Size: 1.5 MB (1536197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab497349841ae340f3b59cbd984d37ac2febc7260aed616d8c1b733e3b32db5`  
		Last Modified: Tue, 03 Jun 2025 16:11:06 GMT  
		Size: 136.6 MB (136628900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b26050dbd70055fa94a2da973196f876da0abde8792c43affce987c73c1aa0`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 118.1 KB (118091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27079afba53f0e88887b24a16f942d42eccc606b18bdc07669969f59b85c7e2a`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 17.6 MB (17550846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaf3bcc8757703456b292b2f799919849ef6066510ec79d05bc21d8ea983a47`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0434563abbb7ed9e55e070d9a8ea3598f9bf9749b32cfee52d213a29c41ea06`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c07c4d903aa42a243323bae348cd3aea27a547d87bdeb9edfdfe1524e97a5c`  
		Last Modified: Wed, 04 Jun 2025 05:12:24 GMT  
		Size: 12.3 KB (12313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98b78706b42542cc9172c24cc28f75eaf3535da7430d6e1e1dda1fe84affb38`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8b72d2d4070334ead73504059918753c1d903a7b1c3e00b5b5065c98e769d`  
		Last Modified: Wed, 04 Jun 2025 05:12:25 GMT  
		Size: 13.1 KB (13123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53959a503575f9e849b4cf9239c93c87532996a43a678e79c2998d640a0694`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 5.4 MB (5421942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaa7826ebd1b87521364bd0ae2ec2385aee49c4954198bfbc28f5ac0d74f243`  
		Last Modified: Wed, 04 Jun 2025 05:13:08 GMT  
		Size: 358.6 MB (358569873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7eebd4b74493ffbd28f5b5e48fa6271b325b11e39b48b28a445a2ede2c6e5f`  
		Last Modified: Wed, 04 Jun 2025 05:12:26 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7008729647354a9b0e3cbf52f9c4c0e3f7b67ccfc10aabff18ab94846bc28c99`  
		Last Modified: Wed, 04 Jun 2025 05:12:27 GMT  
		Size: 13.3 MB (13321968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:cb627fd9e535dac57e43546563348cab2b84fc48fbda7fef8ad62e718b072172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4262812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051e5b337e803d1b779513d2e15d1142269a6befb594568a9f21b6ba88fc5cb1`

```dockerfile
```

-	Layers:
	-	`sha256:f1ceb13861906380c2003f41436f5cfd45be261502f1676933eee6e194f0c368`  
		Last Modified: Wed, 04 Jun 2025 05:12:45 GMT  
		Size: 4.2 MB (4243700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bed80af09e1ba1261a8b5b397c12ca24b2f41e8532fa0d89589113e1c61ed4c6`  
		Last Modified: Wed, 04 Jun 2025 05:12:45 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:aa9f26c6c3051b93a9517887e970501afaea282a9c60539d58774853992a8ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560298713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99b8ab2566500278e3eda621dd33cde1895117938aa93c815569dba6412a65a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 14 May 2025 06:59:54 GMT
ARG RELEASE
# Wed, 14 May 2025 06:59:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 06:59:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 14 May 2025 06:59:54 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Wed, 14 May 2025 06:59:54 GMT
CMD ["/bin/bash"]
# Wed, 14 May 2025 06:59:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 May 2025 06:59:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_VERSION=8.0.8.45
# Wed, 14 May 2025 06:59:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='06679e59bc2ed91a926de6c2d3b3503d6527f0db5b572e1918fa6ccce64248c3';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5fe78fcd5e5042d8dab6b049b2bdd0c399538788ca59e54ef29d3fa28ba9a2b1';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='64b1aa214933ab12bc3c8cbd7024a9eb49d851f5e1abc13209686b3135919dbf';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d2d37a14471206e95564f2ac443f7cdbc984ed7d18275a6775493d0acf28e0b1';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 14 May 2025 06:59:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
ENV PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 21 May 2025 02:47:06 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.5 BuildLabel=cl250520250504-1901
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a
RUN set -eux;     apt-get update;     apt-get install -y curl;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;     apt-get purge --auto-remove -y curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 21 May 2025 02:47:06 GMT
ARG LIBERTY_URL
# Wed, 21 May 2025 02:47:06 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 May 2025 02:47:06 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.5 LIBERTY_BUILD_LABEL=cl250520250504-1901 LIBERTY_SHA=2acea83026ce278918fe4a2ee8f1565708f3bc3a LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
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
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
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
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30e76d3aedea451d5ac821c6d47a00547b6514a71e4871e6eaed7f8f119305`  
		Last Modified: Tue, 03 Jun 2025 14:27:40 GMT  
		Size: 1.5 MB (1455728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8cb2f20eda1bf805a37fca24093c7056a71eb1c0e2458628418f78a48bc1`  
		Last Modified: Tue, 03 Jun 2025 14:27:46 GMT  
		Size: 132.8 MB (132811854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc15cdcb77a0512baaf4cb0f2730505d8e69f2911c19853c7e981358bba8d62`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 114.6 KB (114588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff40b64b9af4bc8ab52ec9bd63b3b25bd2d440b1201007c0e812ee2c1852d36`  
		Last Modified: Wed, 04 Jun 2025 05:02:36 GMT  
		Size: 17.6 MB (17550225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac42118c9e0c1a65af1ad88f5cde841bfb428ae6528aa35d9ab8cc7d810d8f45`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefdae2fab9a2e4966319247c3a80d2b05d5f017f59587dd4b9bec711b180c7e`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a72f89d59315ca50a13f1dc1eba87d1e6dc849ffd0a5580c7e04b46b29f155`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 12.3 KB (12316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee99aa24c6fe3e59a0be139877d5b4903a69aa98e544da72347a44318d4b07`  
		Last Modified: Wed, 04 Jun 2025 05:02:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f9f6a1366e4d4e23057b4d1c0f2442ae367cc0b567feaddafcbd5bbc845c17`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 13.1 KB (13125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a7a3b31eca3818d52e31f9f288cb5e3ea43b7430afa552f6a9548571db371`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 5.9 MB (5932082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac86a6685eec20c9a4b40deefec34d3790b1934282e8822d8834396c26e3dfc`  
		Last Modified: Wed, 04 Jun 2025 05:02:46 GMT  
		Size: 358.6 MB (358570357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c44bf93f309a857c4ac362365f8d3176e30142386fb84e26115c85e2052c2f`  
		Last Modified: Wed, 04 Jun 2025 05:02:34 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d976d31a9bc2b46120521375d77aed71c2f6546ff60474d7a2e98c86b26b1a0`  
		Last Modified: Wed, 04 Jun 2025 05:02:36 GMT  
		Size: 15.8 MB (15834538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:latest` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e9d0cbd120c61cff600c9f318346a653eb1d68667cde359601d59467b05d0512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4258258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8027d18be2982405cb2532639842936b2ef66c9e7d36afc1011615ce0ce51e8`

```dockerfile
```

-	Layers:
	-	`sha256:469047e5cc94a05805092adb0a73dc740f3ea33d6181ee37609035c8ec2b77b4`  
		Last Modified: Wed, 04 Jun 2025 05:02:59 GMT  
		Size: 4.2 MB (4239186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f4912b081875f1b2404f65f31523101149dcdebeca3b886cfb630900595f84a`  
		Last Modified: Wed, 04 Jun 2025 05:02:59 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json
