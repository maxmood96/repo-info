## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:dbf28717eec061769d770991f16cfd6b32cdd92b635dc1be0e97b2d2fa5e1508
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
$ docker pull websphere-liberty@sha256:80a0e9d33a044a18cb505ec3bb1bca6e2841938c48e883443a821de2de169e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487862514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9c915893396c218236750c8bf6f2a71972b085c9ba690ce61d5b46b8444d88`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a034c932d1cc74c1a4d980eb49330c931c9ea0f6191d6032ec1043bb147dcf98';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4076ed128c7e217ceccd27e67e5c8795caf807bf4de5c176d66c059c7693c4f2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7c0d0c44073568cf2e04d0f4df63546364f97cde4c856d608511ba3c9198b19';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='3cf6d35f81dcd8ba976d23d06333dedd03bfb1d366de2584a5940da5e113e0f5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
USER root
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_VERSION=24.0.0.8
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_BUILD_LABEL=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.8 org.opencontainers.image.revision=cl240820240729-1903 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Aug 2024 20:22:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.8 BuildLabel=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_URL
# Wed, 14 Aug 2024 20:22:25 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Aug 2024 20:22:25 GMT
USER 1001
# Wed, 14 Aug 2024 20:22:25 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 14 Aug 2024 20:22:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Aug 2024 20:22:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cee9ca828c62e3afeadc410eca3d4ee8a25f3416df0c510f36cb80f525da60`  
		Last Modified: Mon, 12 Aug 2024 17:59:18 GMT  
		Size: 12.2 MB (12156467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2282879d248ee453bdd65051fdd90db8a305ddd2baefddca877e3b0cd1dee`  
		Last Modified: Mon, 12 Aug 2024 17:59:18 GMT  
		Size: 52.0 MB (52021125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729a8573c77e572e08acc3dae0395893965a3bc53024b11674b5a1694e77b512`  
		Last Modified: Mon, 12 Aug 2024 17:59:18 GMT  
		Size: 4.5 MB (4507421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0865051060726e42a811bada49092eaa552e38a5afc811065876eed3e66bacba`  
		Last Modified: Thu, 15 Aug 2024 16:56:44 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5832ff049c30cf0f70e9389d82a4d0fc61bf2bdf5067266c3875a4b4d602190d`  
		Last Modified: Thu, 15 Aug 2024 16:56:45 GMT  
		Size: 17.4 MB (17432435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f182e2598a23babff98c7d4678f951c4dfb568502cfdfc509091085b809038`  
		Last Modified: Thu, 15 Aug 2024 16:56:44 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb903d9dcd8d512270a78fcddeef5ddb99793f1ff62c164f3165f6ee4fa9496e`  
		Last Modified: Thu, 15 Aug 2024 16:56:44 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9edc963263db728177e790d988c1484b483b43edca8ebfef0c3bf7748fc895`  
		Last Modified: Thu, 15 Aug 2024 16:56:45 GMT  
		Size: 11.8 KB (11830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f44093f78b8773001f0b1847af3ff631a282f782e5d0089873c9bc5008887c`  
		Last Modified: Thu, 15 Aug 2024 16:56:45 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c51343cacde160ee113ca0c934cd6066039bf9d2cd00d1315366c72cfd88bb`  
		Last Modified: Thu, 15 Aug 2024 16:56:45 GMT  
		Size: 12.6 KB (12635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66990c8c77414d807fb4f0feae6fd156838ec98abed545596dc339be3a25354f`  
		Last Modified: Thu, 15 Aug 2024 16:56:46 GMT  
		Size: 2.8 MB (2758301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b08fa827b67a4b95c574148837c4d450ac3210c0f9c172b4b9a22c6a3af1416`  
		Last Modified: Thu, 15 Aug 2024 18:07:07 GMT  
		Size: 353.4 MB (353430719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09afd367c05c59b54e3531f42c4dd5ec0b46d04c5dbf10203d30e2b2001ff8e5`  
		Last Modified: Thu, 15 Aug 2024 18:07:01 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cd4eab9da1a7385755b5b2890b4730f980d86e3ae3e5e61dc6a5dfcfb99c99`  
		Last Modified: Thu, 15 Aug 2024 18:07:02 GMT  
		Size: 16.0 MB (15962591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:87e0b1a68605a8967f2dd1094d8a0a385382cb163f2ea4534b4db2eb9b23afb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a64c8330a38446e3e7215e047ff8b01c4615097a7b769c1600025f06619e73`

```dockerfile
```

-	Layers:
	-	`sha256:76fab1e34818e2c3174d83211422155cea2cbe207a522e5720dba41f38e99654`  
		Last Modified: Thu, 15 Aug 2024 18:07:01 GMT  
		Size: 5.5 MB (5518685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec9cf36cefc653078770da9f2caa3706a9e2d1e18ff27adfbd53a49069cb56c`  
		Last Modified: Thu, 15 Aug 2024 18:07:01 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:5de9042222d69184d0483b0f5fff85a3572bab1b97b9eacff84790cb9f2ec0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.8 MB (480772471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9c9d2e0d88fc1051977e0f660c557c05a0aa07a0293804c3018953cf3fa284`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a034c932d1cc74c1a4d980eb49330c931c9ea0f6191d6032ec1043bb147dcf98';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4076ed128c7e217ceccd27e67e5c8795caf807bf4de5c176d66c059c7693c4f2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7c0d0c44073568cf2e04d0f4df63546364f97cde4c856d608511ba3c9198b19';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='3cf6d35f81dcd8ba976d23d06333dedd03bfb1d366de2584a5940da5e113e0f5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
USER root
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_VERSION=24.0.0.8
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_BUILD_LABEL=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.8 org.opencontainers.image.revision=cl240820240729-1903 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Aug 2024 20:22:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.8 BuildLabel=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_URL
# Wed, 14 Aug 2024 20:22:25 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Aug 2024 20:22:25 GMT
USER 1001
# Wed, 14 Aug 2024 20:22:25 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 14 Aug 2024 20:22:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Aug 2024 20:22:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bd8d80133d843daaa8d5b12adef4a1bb1a9950ef8a5bb999ca2111d459a677`  
		Last Modified: Mon, 12 Aug 2024 18:01:16 GMT  
		Size: 12.1 MB (12114290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de547aafba9c0ebaeb699f9834b505ee1942efb7a0425efb3633823b6d65449`  
		Last Modified: Mon, 12 Aug 2024 18:07:58 GMT  
		Size: 48.4 MB (48416900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8975f03e91d05f2030af20e5cdc9359b5e61a8cf8e5f2380dbef11b104ce5b34`  
		Last Modified: Mon, 12 Aug 2024 18:07:57 GMT  
		Size: 4.2 MB (4182784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5782e3f22b39847e10fc46357a394095f7ae8294067bbd1212bfd6584fed88`  
		Last Modified: Thu, 15 Aug 2024 17:07:20 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351e293ad452532466d2aff424d94b9642c7965a887c4ab767d35acee60d827c`  
		Last Modified: Thu, 15 Aug 2024 17:07:21 GMT  
		Size: 17.4 MB (17432793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c0d209fd91803391b840b12dbe311434c590dbe332386c4ecf55a317af19ef`  
		Last Modified: Thu, 15 Aug 2024 17:07:20 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254cfbece52bb599f1776caa644c3df26197333077dffed5855c9be61dcc09fb`  
		Last Modified: Thu, 15 Aug 2024 17:07:20 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6723a8bf4e032a16f38052ef9050520f8029549770e68a60c62d6e763217ff`  
		Last Modified: Thu, 15 Aug 2024 17:07:21 GMT  
		Size: 11.8 KB (11822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a67a5b6c6330de31bb0431cf5685c0fbc001321de63e0a7525088be40e784d`  
		Last Modified: Thu, 15 Aug 2024 17:07:21 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb96a61095621cc0c847fbb0a9c43beee97d376d4be80790e001d0f74003a564`  
		Last Modified: Thu, 15 Aug 2024 17:07:21 GMT  
		Size: 12.6 KB (12638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a7ea65e1079d42652c9812aef6ce65ddadbd1a0f0bef494514cc94fba0adde`  
		Last Modified: Thu, 15 Aug 2024 17:07:22 GMT  
		Size: 2.7 MB (2724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80417402ce7b0935e25697d1a8451f10c92bb8a54cfadb0c8c48f68365bff5fe`  
		Last Modified: Thu, 15 Aug 2024 20:53:43 GMT  
		Size: 353.4 MB (353434476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4e9bf29417907c45c4a3fdf7a52dbcfd9aa012766f39ea34442cf42400c69c`  
		Last Modified: Thu, 15 Aug 2024 20:53:36 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77afbc1d51f878c9576cb0b142f4bf55a9ca0287c29f5a3749a2924464d5afd5`  
		Last Modified: Thu, 15 Aug 2024 20:53:37 GMT  
		Size: 15.0 MB (15036873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:b644f129d94e03f2124e1f715d9fbccc477f0b6fe23aa2032a264b47a94b520c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6174838034375a3b7b33545f16e751b2dcc2e45eca24700537df670b9d9b87`

```dockerfile
```

-	Layers:
	-	`sha256:c667c027c0795d25070679f0ff12769380fab88965018ae9e6b4d017b8ea90e3`  
		Last Modified: Thu, 15 Aug 2024 21:50:07 GMT  
		Size: 5.5 MB (5518938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3352bf74401e68562ff9f098e2e075b5d7003a4365300110d8ae7231eb916f45`  
		Last Modified: Thu, 15 Aug 2024 21:50:06 GMT  
		Size: 19.9 KB (19923 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a2c05f1fa58adb0ad6e9d9742415cccb60f1b77ae634e817d7aad895c080d7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491532548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7aae518d7f93d121d53ee65146ee1a48e7682db63c6cc7e7924ef761a3f6de`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a034c932d1cc74c1a4d980eb49330c931c9ea0f6191d6032ec1043bb147dcf98';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4076ed128c7e217ceccd27e67e5c8795caf807bf4de5c176d66c059c7693c4f2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7c0d0c44073568cf2e04d0f4df63546364f97cde4c856d608511ba3c9198b19';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='3cf6d35f81dcd8ba976d23d06333dedd03bfb1d366de2584a5940da5e113e0f5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
USER root
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_VERSION=24.0.0.8
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_BUILD_LABEL=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.8 org.opencontainers.image.revision=cl240820240729-1903 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Aug 2024 20:22:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.8 BuildLabel=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_URL
# Wed, 14 Aug 2024 20:22:25 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Aug 2024 20:22:25 GMT
USER 1001
# Wed, 14 Aug 2024 20:22:25 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 14 Aug 2024 20:22:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Aug 2024 20:22:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f6b0caf9e82f11ff311008151b002cbef7156dabe22bc30c0b0bfab72dcb3`  
		Last Modified: Mon, 12 Aug 2024 18:04:26 GMT  
		Size: 12.9 MB (12888358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec4eda6def70bca9707b23eedbdda98db9884338cfae00a92951b9112339e1`  
		Last Modified: Mon, 12 Aug 2024 18:13:48 GMT  
		Size: 53.6 MB (53619797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8ea3052422fe08d790d1a5ad21ae80758109b738125570ce3b2e621968cae2`  
		Last Modified: Mon, 12 Aug 2024 18:13:46 GMT  
		Size: 3.4 MB (3436299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f9e14c26d2ec40a8e377908a99b07f4ce922853ded6e911e1ce6cbdf258329`  
		Last Modified: Thu, 15 Aug 2024 17:16:48 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bce45a88c25cba7dfac1127db816c58ddda2c0279b872614bb9cf60e80ccf7`  
		Last Modified: Thu, 15 Aug 2024 17:16:49 GMT  
		Size: 17.4 MB (17432992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7bc153ea009ae785d2f6238befe162addcd060cc69ba7f2b35f1cd936d20b7`  
		Last Modified: Thu, 15 Aug 2024 17:16:48 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6925bc44045af690db6be9055dee08ede85dfd1b4efe627885ff2ea3bf52e44`  
		Last Modified: Thu, 15 Aug 2024 17:16:48 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de835b3300b344fa2deb7431bcccfb9f8fd5eb555255babc4827bd2192f07048`  
		Last Modified: Thu, 15 Aug 2024 17:16:49 GMT  
		Size: 11.8 KB (11828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acbb9098866a7d0d3d54a03f195dbaf0ed2db1d0ca082b2244a9f8423c02c59`  
		Last Modified: Thu, 15 Aug 2024 17:16:49 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8a2b94e37a4258f83dd96a96f2c8403a2aba4a8ddfde0f5b19311177411b14`  
		Last Modified: Thu, 15 Aug 2024 17:16:49 GMT  
		Size: 12.6 KB (12643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9f5e5890c991b3178bacfda4620cfa1fc2f2200c134d776f0258c97d0bea81`  
		Last Modified: Thu, 15 Aug 2024 17:16:51 GMT  
		Size: 2.6 MB (2637183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6af7fc6148e9c89f673a9ca6cad29b85ac115dfe89ac6f518538ff1d954e51`  
		Last Modified: Thu, 15 Aug 2024 19:25:15 GMT  
		Size: 353.4 MB (353433390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd3422852f15e3d1b3813edd6f91c3948542c94daa52c33b56ae4238e1071dd`  
		Last Modified: Thu, 15 Aug 2024 19:25:07 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1715921b84f40e2b1683f92345e728b2cd5206667c7a441a6c9fa8c86da5186`  
		Last Modified: Thu, 15 Aug 2024 19:25:08 GMT  
		Size: 13.6 MB (13559287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:1b83659e4eddcd5dccad35d9de97ba4420f32858e64f4e72ae61fd40c243a592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208b807aed5f504fcce9011ac8e50c0b8ff3c54a43cb968531410de031c3dd09`

```dockerfile
```

-	Layers:
	-	`sha256:cf91360388f4e0c5bbc10014a4810dc6837656d61e5e70970a96512d0283be3f`  
		Last Modified: Thu, 15 Aug 2024 20:08:36 GMT  
		Size: 5.5 MB (5523167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc471d7dba2acfc397f50485b4373944b25a740f43c46b506747254e722d618d`  
		Last Modified: Thu, 15 Aug 2024 20:08:35 GMT  
		Size: 19.6 KB (19602 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:3f870b6accd7d65f115a4150c5f9f77ae1dceafeab6216b6238a6859e083b229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.1 MB (485059940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2529a61e4b23479e1dab41ecc364bbee555d98aa53204bd7028d0483aed2d9e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 02:58:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 12 Aug 2024 02:58:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.0
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a034c932d1cc74c1a4d980eb49330c931c9ea0f6191d6032ec1043bb147dcf98';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4076ed128c7e217ceccd27e67e5c8795caf807bf4de5c176d66c059c7693c4f2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7c0d0c44073568cf2e04d0f4df63546364f97cde4c856d608511ba3c9198b19';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        s390x)          ESUM='3cf6d35f81dcd8ba976d23d06333dedd03bfb1d366de2584a5940da5e113e0f5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.0/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Aug 2024 02:58:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 12 Aug 2024 02:58:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="3069924eb7041ccc0f2aeceb7d8626793a1a073a5b739a840d7974a18ebeb26cc3374cc5f4a3ffc74d3b019c0cb33e3d1fe96296e6663ac75a73c1171811726d";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.93/bin/apache-tomcat-9.0.93.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
USER root
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_VERSION=24.0.0.8
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_BUILD_LABEL=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.8 org.opencontainers.image.revision=cl240820240729-1903 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Aug 2024 20:22:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 14 Aug 2024 20:22:25 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.8 BuildLabel=cl240820240729-1903
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ARG LIBERTY_URL
# Wed, 14 Aug 2024 20:22:25 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.8 LIBERTY_BUILD_LABEL=cl240820240729-1903 LIBERTY_SHA=e53fa1e7c6d29800172008b20be9479a85afd5ab LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Aug 2024 20:22:25 GMT
USER 1001
# Wed, 14 Aug 2024 20:22:25 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 14 Aug 2024 20:22:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Aug 2024 20:22:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Aug 2024 20:22:25 GMT
ARG VERBOSE=false
# Wed, 14 Aug 2024 20:22:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 14 Aug 2024 20:22:25 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928fcb5dd7fd89cdaf703469776b84f22f2a0896c6669206b1c3e5fd07dd7ccf`  
		Last Modified: Mon, 12 Aug 2024 18:02:49 GMT  
		Size: 12.2 MB (12203937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64aa1a0712885951f4c82604c80c08958bd5d549f99f99a49f950e1ce02757b`  
		Last Modified: Mon, 12 Aug 2024 18:11:39 GMT  
		Size: 50.9 MB (50892182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00674f439326ffeb6d1e650a1e87c8aaad05f74437224ac09297bcb419640d79`  
		Last Modified: Mon, 12 Aug 2024 18:11:39 GMT  
		Size: 4.6 MB (4617298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059eb023e2540ab89213f8d59dbd894b573b3c1117fce483e54981637d83bb57`  
		Last Modified: Thu, 15 Aug 2024 17:14:04 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673352e320fd8553f63326bafe2af2a3ad20bf5fa148b975604142df4d1ee053`  
		Last Modified: Thu, 15 Aug 2024 17:14:04 GMT  
		Size: 17.4 MB (17432573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fdf656ebb7d59b1f7c458c750d8a56fe143d4a611229b27c521ee45b28da2d`  
		Last Modified: Thu, 15 Aug 2024 17:14:04 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a119babe8e9e48269b45ba71e1a756b1e1a2774cb6387ff166c50ab6c45552f`  
		Last Modified: Thu, 15 Aug 2024 17:14:03 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f91f63bb6de3f517cc199bcd3107b991de102012b0e6ed55c8afc75cc18bfd`  
		Last Modified: Thu, 15 Aug 2024 17:14:04 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5463911564f95ae59990e4529ea3f19cb82480e2d6e49fd86dc8f355f3bc5b`  
		Last Modified: Thu, 15 Aug 2024 17:14:04 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab904d89ff4de9552f41aa863058290e52d8305044576ad0421fac06783cf90`  
		Last Modified: Thu, 15 Aug 2024 17:14:04 GMT  
		Size: 12.6 KB (12630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a0e0c9cdb1af828d36f0aaf059ded3c8912aa13212c6fa2ea7ae06f048b9a9`  
		Last Modified: Thu, 15 Aug 2024 17:14:05 GMT  
		Size: 2.7 MB (2736238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94204ebf3bb6a21cd8778c2234d3499fdcef79e31b023238bb05ec6f566c45f2`  
		Last Modified: Thu, 15 Aug 2024 19:17:29 GMT  
		Size: 353.4 MB (353434229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf7cc7c77e02d56cd295b71deed6f9a86259384ff8fca753bd291a2740bba07`  
		Last Modified: Thu, 15 Aug 2024 19:17:24 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075dab2ed7294d2c35d9a1701393a5724500957ef07501b9d1e284792b6b3f97`  
		Last Modified: Thu, 15 Aug 2024 19:17:25 GMT  
		Size: 15.7 MB (15682183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:89411a6a3caaa750c3a2abf68a6e85e41d6493a3c0d6fbdeb61ea60090ddbd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db876320d5c3a4f57f8759713364d618eede4576059e0d031ecb301c181a7683`

```dockerfile
```

-	Layers:
	-	`sha256:300aa41fa834070094c225c44d65280a0a03a815e0fcb787df21d691483ccfaf`  
		Last Modified: Thu, 15 Aug 2024 19:17:24 GMT  
		Size: 5.5 MB (5518724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650294ef149949bba9cad25a4832501f46e90cd3411cb422b528344b2820dd84`  
		Last Modified: Thu, 15 Aug 2024 19:17:24 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json
