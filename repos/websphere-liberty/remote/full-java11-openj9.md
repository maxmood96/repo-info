## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:5e9befd9bbca37ceed56d08be99fa7d96cf828cf1e15dddcd2ab07c48e20fbb4
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
$ docker pull websphere-liberty@sha256:69ba924aaa21d5ce8f7114bff3039a958227d7f47bf05debe5be1cd087519227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.7 MB (493726001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccecc171d99aade43381bff970e16996d68f5c7f28fa279b431e21e938584734`
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
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c9c0b51361b1eda41c01395310e238baf9800b1345686d550a69c94746465`  
		Last Modified: Mon, 24 Mar 2025 16:59:40 GMT  
		Size: 12.2 MB (12166941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17a8db65dfbbe61341fd826f92bd8ee0208baac02a83c286274303557793d57`  
		Last Modified: Mon, 24 Mar 2025 16:59:40 GMT  
		Size: 52.4 MB (52386330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a00f4e34f78e05f58ddce14e909ffc0d07b907df8f811e608b8d3a0fbdf3f2e`  
		Last Modified: Mon, 24 Mar 2025 16:59:40 GMT  
		Size: 4.4 MB (4445687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443cb73b09155a360ba21a64509152bed57e0fa1d835d0849aac7908360fd9a`  
		Last Modified: Thu, 27 Mar 2025 23:34:39 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d7c0c3f2a5ab4c402b1e6588b7c1b3216b3bc8f1c40d339bff77a2ddc1bb1`  
		Last Modified: Thu, 27 Mar 2025 23:34:39 GMT  
		Size: 17.5 MB (17548971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e57121f6662091d3f2dcd5585551df292a67b7369526f3254c8582b85cc36e`  
		Last Modified: Thu, 27 Mar 2025 23:34:39 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68aba319927ccfe4bf77917b3113641e3f0950cbf8fccbce90d29a4190f74f58`  
		Last Modified: Thu, 27 Mar 2025 23:34:39 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7e5e02ddd8d7c799fe78045d35253d970c04b92029cee65cdb59e95cccf2f5`  
		Last Modified: Thu, 27 Mar 2025 23:34:40 GMT  
		Size: 12.2 KB (12229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f1b18c630876b2b5af8277eff5eaad87e2e0484bed81ad3166ecb2324ecbf9`  
		Last Modified: Thu, 27 Mar 2025 23:34:40 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8480c5fc65743b095217f21a45d29832ec1d9c00d89015e0f51c01c47789648`  
		Last Modified: Thu, 27 Mar 2025 23:34:40 GMT  
		Size: 13.0 KB (13026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d76caf09fad5b562f2ccb5556daa2ac94bcb494b2b721671f2c86f1f5080c53`  
		Last Modified: Thu, 27 Mar 2025 23:34:41 GMT  
		Size: 2.8 MB (2822600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6426d506d49764d3153dddee2fd7fc0d1dea1c7df2a9583f9556b07bbe480b`  
		Last Modified: Thu, 27 Mar 2025 23:53:46 GMT  
		Size: 358.7 MB (358662696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86cabdfc2b3b13b313ed4aef220f4afb9be082749a6fd3bde13db93aef1a739`  
		Last Modified: Thu, 27 Mar 2025 23:53:40 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c4af1007b07fd9f41c7dcf491264efbe6699be446a638082b38eaa635d76e0`  
		Last Modified: Thu, 27 Mar 2025 23:53:41 GMT  
		Size: 16.1 MB (16096653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:4af637b1d4e232f2d90005727dd9215c9acfa28e210e4c286cf5f7514d69fb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5771268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f444beda3aadf8f05f2c91aa652bc36e1c1d403ccbbcc5fbdbdc3b4f5bc09fc1`

```dockerfile
```

-	Layers:
	-	`sha256:3f06295b0dc56006d5c0173a955aeba7b4e014dd6249837157029b96ef3c4479`  
		Last Modified: Thu, 27 Mar 2025 23:53:40 GMT  
		Size: 5.8 MB (5751661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65ff4d97cbbbc8477bccaf71fcde419f992f89aba1a91089e043ffba1b5ad93c`  
		Last Modified: Thu, 27 Mar 2025 23:53:40 GMT  
		Size: 19.6 KB (19607 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:eccba4a6d1b6e243d39b55d435a94c99959f358f8679cd1f815eb80976b7331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.5 MB (486547444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffa05cde24a8fbdaa6ead2d348a0b73a4d4343e50cc5e8167d7150f65aa8708`
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
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
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
	-	`sha256:f488e4d6c249fc50f450e06c50e6923a7760d0a0890f1ac781790e18f0212148`  
		Last Modified: Mon, 24 Mar 2025 17:11:19 GMT  
		Size: 48.8 MB (48787333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0490e7f6c6ae4946697c02f93de89888b284463c979419ea71797b5a456550d7`  
		Last Modified: Mon, 24 Mar 2025 17:11:18 GMT  
		Size: 4.2 MB (4182680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0daa8932701b10d390284fd34a987a022edf06592aa02642003b390789d98796`  
		Last Modified: Thu, 27 Mar 2025 23:48:05 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deadef5f33ad66492a85d56d2beb4fbfe9fa5842c28b28153a8b0469afe10ec7`  
		Last Modified: Thu, 27 Mar 2025 23:48:05 GMT  
		Size: 17.5 MB (17549115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aade1806b69e4a2b1e3e7ce7bf73be5c016328180d7e6a0a7c6dfd23edcdcd4b`  
		Last Modified: Thu, 27 Mar 2025 23:48:04 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72008f074c9a65bfd436c399c4bf59c8943332eb900a0038a88e81eee64bdfae`  
		Last Modified: Thu, 27 Mar 2025 23:48:04 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cc7bcc3cca989aa10962f8d23a74d44c13d3c0022ca82ed0dc3283ff131a87`  
		Last Modified: Thu, 27 Mar 2025 23:48:05 GMT  
		Size: 12.2 KB (12230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef035e09c7a226fbdd3a2d0234dcf6a9554dd4b6f4e459402bc5f887c03964fc`  
		Last Modified: Thu, 27 Mar 2025 23:48:05 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b4c19cbd4c87a2689ef62f3d60d2013d13409c51f0df324ba4225f29cccf5`  
		Last Modified: Thu, 27 Mar 2025 23:48:06 GMT  
		Size: 13.0 KB (13036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3876a5075934142a5de9fee3a2a6ba37344581aa5bee1eb1b4bc35fa31609e76`  
		Last Modified: Thu, 27 Mar 2025 23:48:06 GMT  
		Size: 2.8 MB (2781296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6913a0ab6d00548e6fc25557b51e1e221fb9ae7fd5485811a035ae962a0376`  
		Last Modified: Fri, 28 Mar 2025 00:57:24 GMT  
		Size: 358.7 MB (358661491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b614d365b7153734e7969e28f27bd2f39cc07a29742e5b49b927685a315c67`  
		Last Modified: Fri, 28 Mar 2025 00:57:16 GMT  
		Size: 940.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fd08bad7727f4a061cc93be88e0d14af99850ba201b1cb2b32f0ceb517ad40`  
		Last Modified: Fri, 28 Mar 2025 00:57:16 GMT  
		Size: 15.0 MB (15033058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:5b95965deaec0bbe495dd36ce592a12ed041582539ae0d8a1e848381fbe8463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5764686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3393bf4c61f389570203d23f607ca6e46150e91890c01debcc94c458ab33f318`

```dockerfile
```

-	Layers:
	-	`sha256:fa8f455afe51f2fcb0dd8ed3eeccb5ba60b91e61f9fa157c7be1fe2877a76439`  
		Last Modified: Fri, 28 Mar 2025 00:57:16 GMT  
		Size: 5.7 MB (5744995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85aa80db4eef59758a0c41ada28659882be41deb23525be63a62183a2c7506b4`  
		Last Modified: Fri, 28 Mar 2025 00:57:15 GMT  
		Size: 19.7 KB (19691 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:790e18ca8629c81ca1465670c2229d7c0db121e61d22b1a195fa24ca88cbdf2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.0 MB (496984016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe12cac48b9a3b77e9000751751832030e07f5aea99eaa0ea39fdbbe695374ed`
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
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
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
	-	`sha256:a805d9a753e7b0c206566ea7b0e5e37ae7caa5afa57f098034795404a612179b`  
		Last Modified: Mon, 24 Mar 2025 17:15:52 GMT  
		Size: 53.6 MB (53621041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1caa8f7f57a39d6abf489d3b014f6bb974c02c10da375c549867c2f0e2957f8`  
		Last Modified: Mon, 24 Mar 2025 17:15:50 GMT  
		Size: 3.4 MB (3407581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509bb5d95f7d7fe9c2409a1d258eadc9e6a74f17fbdfeb0883b5539b9e97790b`  
		Last Modified: Fri, 28 Mar 2025 00:01:39 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adcb2795837f62a0f523fdc1310cf50583927ed44760a723cb46f56d865dcfa`  
		Last Modified: Fri, 28 Mar 2025 00:01:40 GMT  
		Size: 17.5 MB (17549214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ce6cd45f4102298049e4623dea5d6db7ebd8b1ed40e6db5f9aba3b1646357`  
		Last Modified: Fri, 28 Mar 2025 00:01:38 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4056462a1add481eae64277c7595a903bcde4afe9e6fa9196a5059b337f3c9`  
		Last Modified: Fri, 28 Mar 2025 00:01:38 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d676ef2763118a9d96837ed4c58c0acbb69062294559b0eba05dec237dda08d`  
		Last Modified: Fri, 28 Mar 2025 00:01:39 GMT  
		Size: 12.2 KB (12229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328c5a1d56731a51b12221c72d980b731acafa9635f9d7c5417071a241eb9f07`  
		Last Modified: Fri, 28 Mar 2025 00:01:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356f1c4dfb203604b051f2aea60526163e8a95626c17714087fb4f3b8d17d5ce`  
		Last Modified: Fri, 28 Mar 2025 00:01:40 GMT  
		Size: 13.0 KB (13042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d75ddfde540da98018f43e9e3ab5a17cf471e8bf3fcf9993a49c479e61f42c`  
		Last Modified: Fri, 28 Mar 2025 00:01:41 GMT  
		Size: 2.7 MB (2676223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500f4d6858f1ed468d4529ad5dfdccdf6ce59320808139637fd9e8971fe34c0a`  
		Last Modified: Fri, 28 Mar 2025 00:41:34 GMT  
		Size: 358.7 MB (358661802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81f1398f9a94363fe2d87c369baacbbe7e621802a2314117bf4bbd09596e379`  
		Last Modified: Fri, 28 Mar 2025 00:41:10 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aab431aa1be61a94a6f7f80eee2c14267e8a642866899614edaa82ff7111cb3`  
		Last Modified: Fri, 28 Mar 2025 00:41:11 GMT  
		Size: 13.7 MB (13668582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:a2c18de68796662876e15f35765c220edd5e05592d5fc30a0c8bcf3cc078abd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d639633bab0472f911f1a72872d36bfd43d9462a0207cd77b9edd79fe5872354`

```dockerfile
```

-	Layers:
	-	`sha256:af528034b4f50afe76667313ae34ff096cb55ab4996ba7dfd04ff0586f1c865b`  
		Last Modified: Fri, 28 Mar 2025 00:41:10 GMT  
		Size: 5.8 MB (5753670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7294f6cc2aa8094d9c5fc39a965b01cc36fe0d555d1f3e5829223c743a825803`  
		Last Modified: Fri, 28 Mar 2025 00:41:10 GMT  
		Size: 19.6 KB (19636 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:7983d4ea630f20c61ac66a49511380e1d69fdf809f098f54fcfbd706a025b581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.9 MB (490932937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305ce08f154941c0af58aecc98b5473f66dee816e8ad919d2d05c2e5438f4bc2`
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
# Thu, 13 Mar 2025 08:54:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Mar 2025 08:54:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_VERSION=jdk-11.0.26+4_openj9-0.49.0
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2425d0daa7c0ef6603910c1c51ed7f3d8dbeb4dff8e1542957771ac5045fc21e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_aarch64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d013d38e03a3455c6867b10544dc30041bf7afdb595d60ee09af43d46cdb5720';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_ppc64le_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        amd64|x86_64)          ESUM='08586859b8a53aa9d5424a38838e8332664622049c3c33b1b0e5ea88b56ce2d9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_x64_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        s390x)          ESUM='84232088178d3886d2c6dff2621f60406390bc12c36752a3305799a87cefc255';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.26%2B4_openj9-0.49.0/ibm-semeru-open-jre_s390x_linux_11.0.26_4_openj9-0.49.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Mar 2025 08:54:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Mar 2025 08:54:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="cbe407f17c813d9f83cab459e603df171f2e5782c3a0cdb4cfa00b0391a89cedf865c6d8972fc7e12210c69a8467ede5939f35bb0f3b41fa173b9ee83199768a";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
USER root
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_VERSION=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_BUILD_LABEL=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=25.0.0.3 org.opencontainers.image.revision=cl250320250310-1902 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty liberty.version=25.0.0.3 com.ibm.websphere.liberty.version=25.0.0.3
# Tue, 25 Mar 2025 15:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Tue, 25 Mar 2025 15:38:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=25.0.0.3 BuildLabel=cl250320250310-1902
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ARG LIBERTY_URL
# Tue, 25 Mar 2025 15:38:11 GMT
ARG DOWNLOAD_OPTIONS=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R ug+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=25.0.0.3 LIBERTY_BUILD_LABEL=cl250320250310-1902 LIBERTY_SHA=f28041b7990da53aff2272a2fab58c9a1716a646 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 25 Mar 2025 15:38:11 GMT
USER 1001
# Tue, 25 Mar 2025 15:38:11 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 25 Mar 2025 15:38:11 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Tue, 25 Mar 2025 15:38:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Tue, 25 Mar 2025 15:38:11 GMT
ARG VERBOSE=false
# Tue, 25 Mar 2025 15:38:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Tue, 25 Mar 2025 15:38:11 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Tue, 25 Mar 2025 15:38:11 GMT
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
	-	`sha256:690e2211e5a3922edbe2fffc31a253d298413d68da672e1bec4a1cce512e9996`  
		Last Modified: Sat, 15 Feb 2025 08:15:23 GMT  
		Size: 50.9 MB (50913952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ebbfbaf0212d70feadcf2b61a903b83322f9513be8caeb105669891b96744b`  
		Last Modified: Mon, 24 Mar 2025 17:13:44 GMT  
		Size: 4.6 MB (4566946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6928ef887a70cdd63991dd5d536f149955330472347665ceb03768ddd22bf6`  
		Last Modified: Thu, 27 Mar 2025 23:53:16 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc1c936f525395ef973af0719f04c5e6f969aba85489201129eb021946174f`  
		Last Modified: Thu, 27 Mar 2025 23:53:16 GMT  
		Size: 18.0 MB (17952418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b37f65ab736856d884aa62dba5324d52ef18e8f790b429f834d74f66239e03`  
		Last Modified: Thu, 27 Mar 2025 23:53:16 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ac3782b7ae385db3604ecf411cd738318c74e4419a1eeb777c9718a95fb9c5`  
		Last Modified: Thu, 27 Mar 2025 23:53:16 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1218a82c80f9c73545c07c2212b244a765a29039e7bce50f1f8dd3a7c2a3447b`  
		Last Modified: Thu, 27 Mar 2025 23:53:16 GMT  
		Size: 12.2 KB (12231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0a43117d277a370660d1890a291d985ea5dc058ca4d81167ed87eb0179e9e`  
		Last Modified: Thu, 27 Mar 2025 23:53:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cd63078447562e7c00fba41cf395d038f5c34fd733115c9d2b1c7138772f88`  
		Last Modified: Thu, 27 Mar 2025 23:53:17 GMT  
		Size: 13.0 KB (13042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe993ce0009e5488da0a20c81ee82d9cf8a40dd277c9a379b1491a7944e1335`  
		Last Modified: Thu, 27 Mar 2025 23:53:17 GMT  
		Size: 2.8 MB (2819210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a7532aeadaf00fd3c1ebc5180602daafa970c650f87523b6255547a069ccc8`  
		Last Modified: Fri, 28 Mar 2025 00:32:40 GMT  
		Size: 358.7 MB (358661845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4006b411b8bee6d9121fd51e78fa6cc06d7a354e4ee94362f54620edd5f2761e`  
		Last Modified: Fri, 28 Mar 2025 00:32:34 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af643d1e57e9860bf94a2451b38566e3d7e4cfd7f0056dbe19e48550f94072`  
		Last Modified: Fri, 28 Mar 2025 00:32:35 GMT  
		Size: 15.7 MB (15743772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:b15fccc8b4d9cfde6b5df25c38b2fae35ee7b79333d8b0e7bb5def52b891c4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bada212726545fd6dca7b8a4fbf32dea17600111bfecea930b65bf9612f140d2`

```dockerfile
```

-	Layers:
	-	`sha256:b4cb764d58d77c17fe0b2028df045382af9c800da74a96e929438a5d95cb2f89`  
		Last Modified: Fri, 28 Mar 2025 00:32:34 GMT  
		Size: 5.7 MB (5748596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089cdbe9d080248f15e94c9269f1d028bbc3a849463b441f5c30e4c5fdff70b2`  
		Last Modified: Fri, 28 Mar 2025 00:32:34 GMT  
		Size: 19.6 KB (19607 bytes)  
		MIME: application/vnd.in-toto+json
