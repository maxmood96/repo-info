## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:e96c2325fa8c545e5cdab1f98c9e22720d91cb47b3fedaff31873909fe26f9c8
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
$ docker pull websphere-liberty@sha256:53ae226f3896cac45c43b62da0cacd45457fec2d41eaeb59e2274b3f526884a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486987703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c24ecd5ddef6c49daa3490948dc6ca47ffb92f7e948e7820bb6ac8a77db0ff`
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
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
USER root
# Wed, 17 Jul 2024 15:21:21 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:21:21 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_VERSION=24.0.0.7
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c
# Wed, 17 Jul 2024 15:21:21 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.7 org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 17 Jul 2024 15:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 17 Jul 2024 15:21:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.7 BuildLabel=cl240720240701-1102
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_URL
# Wed, 17 Jul 2024 15:21:21 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:21:21 GMT
USER 1001
# Wed, 17 Jul 2024 15:21:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:21:21 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:21:21 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 17 Jul 2024 15:21:21 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:21:21 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9765d31e769ffc035796a2c119e0dc10b17341008440f0d809d796109893d68f`  
		Last Modified: Wed, 17 Jul 2024 17:56:13 GMT  
		Size: 12.2 MB (12156602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471dafd447c04176cdc2f0c546bc7a1bf7e1c99859603f1c0960eb6e899242c3`  
		Last Modified: Wed, 17 Jul 2024 17:56:14 GMT  
		Size: 51.9 MB (51931214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f005b9da1de2b37b4caa66a35370c10a2a308a66b65d7723d0d67b123822588b`  
		Last Modified: Wed, 17 Jul 2024 17:56:12 GMT  
		Size: 4.4 MB (4378458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581802aac01a1ad912202116373e5b3bf08e4b209e8d86cd023c6eb3a1e1abdd`  
		Last Modified: Thu, 18 Jul 2024 18:56:02 GMT  
		Size: 31.7 KB (31742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec329298a74a0a640e5e34410bf80c13634ed38b1dcfe5b3c63493edebd5db8`  
		Last Modified: Thu, 18 Jul 2024 18:56:03 GMT  
		Size: 17.4 MB (17426773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57216a3b2f9c7090af9c8932e264e35a1c01aa10706bdaf83f828b6be85d869`  
		Last Modified: Thu, 18 Jul 2024 18:56:02 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8238db3479903857a91f4b3af84315fc8e3608faa6d603b6097c89580122988`  
		Last Modified: Thu, 18 Jul 2024 18:56:02 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5a0759b775121b59d477cca452854e6114c8027aba2c68b53fc3ee4a9d960e`  
		Last Modified: Thu, 18 Jul 2024 18:56:03 GMT  
		Size: 11.8 KB (11829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe18e6d8c8e684c49d5fd552d235f32e53152411a837b545ab5605446ee3bfb`  
		Last Modified: Thu, 18 Jul 2024 18:56:03 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458f32707fb0697eb0a4b56ab709f4871166ddd94622ffd205005caa330ddfdf`  
		Last Modified: Thu, 18 Jul 2024 18:56:03 GMT  
		Size: 12.6 KB (12630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6e0f0887e340ac6c61f696cb7a0e84113639ea9ec5db5632d1b16f59b6d02a`  
		Last Modified: Thu, 18 Jul 2024 18:56:04 GMT  
		Size: 2.8 MB (2777860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c7adca1cb641dc374d9e4cbf1d21a904ce5e62fd8762cb00573c652d220d0`  
		Last Modified: Thu, 18 Jul 2024 19:58:24 GMT  
		Size: 353.0 MB (353046681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a901c832b0ca37e5a091889da17d113ecf91151a55c3dc3315b5c869be80a7a`  
		Last Modified: Thu, 18 Jul 2024 19:58:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc0ec6da6eee3c85bff7f65bc2d5c9b507300e0a02ca1cfaf7a114b5ebc0a44`  
		Last Modified: Thu, 18 Jul 2024 19:58:19 GMT  
		Size: 15.7 MB (15676673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:b068e497106f4b63e3edd148ee82b2d35729cd8658a89df4af98e9ce561c14e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18162c784d5bcf6ca4c1ff34b78fa375554b2b4a8830dbf76c4689a894e9a584`

```dockerfile
```

-	Layers:
	-	`sha256:4361280613dc39d000ef2f679b9d8dcae7d3fbbe3922d07896c75874a31c5f6c`  
		Last Modified: Thu, 18 Jul 2024 19:58:19 GMT  
		Size: 5.5 MB (5515512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c00c835953b9d4e738ad87284cd03f3d1d80618e88d642cda2ecf5bebefec61`  
		Last Modified: Thu, 18 Jul 2024 19:58:19 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:8a36338d55f9189201521d965b310ce7cbfbb64246560736414ac7dc947e0946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.1 MB (480124288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa42fb66dd3baf07b156ff9689ba4931fdb1374177060cfcb1fb764aa2e62205`
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
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
USER root
# Wed, 17 Jul 2024 15:21:21 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:21:21 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_VERSION=24.0.0.7
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c
# Wed, 17 Jul 2024 15:21:21 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.7 org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 17 Jul 2024 15:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 17 Jul 2024 15:21:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.7 BuildLabel=cl240720240701-1102
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_URL
# Wed, 17 Jul 2024 15:21:21 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:21:21 GMT
USER 1001
# Wed, 17 Jul 2024 15:21:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:21:21 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:21:21 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 17 Jul 2024 15:21:21 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:21:21 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a73c992d8ae249d8805479ac497dac9fa0b1b48ab385b7d65a1b68d7dd3f7e`  
		Last Modified: Wed, 17 Jul 2024 17:58:36 GMT  
		Size: 12.1 MB (12114226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db374f73c52ab08440f55d862929f19e0099fc10512477644151d0b9cf9a0ff`  
		Last Modified: Wed, 17 Jul 2024 18:05:14 GMT  
		Size: 48.3 MB (48326042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b53ae9469bc737cc8f50f8d21d0daf2e815f0d8ada06498b257a3dc1419492b`  
		Last Modified: Wed, 17 Jul 2024 18:05:12 GMT  
		Size: 4.2 MB (4188666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f59ed6dedfe2f86a15557b1ad6323f6df927ab4f437f044605c122ab9857beb`  
		Last Modified: Thu, 18 Jul 2024 19:11:57 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beeaa31c16e1fdf2f7a72ebd3bb9c44f2367d3356dbe6f3427a68cf266beb9e`  
		Last Modified: Thu, 18 Jul 2024 19:11:57 GMT  
		Size: 17.4 MB (17427190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59924123409d3c08a42a4d231e5cbfd8a0e0ac0257f4cafd32b7020c4899af2`  
		Last Modified: Thu, 18 Jul 2024 19:11:56 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f4d718bd1343bb697cf77267fceb3a3ff0b6fcfe3f3764b5020fc7c5e8d323`  
		Last Modified: Thu, 18 Jul 2024 19:11:57 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e576e5a3ee11a95dd1e2946cde12d155f8f6722e404b7d9db04fbaa822db74c`  
		Last Modified: Thu, 18 Jul 2024 19:11:57 GMT  
		Size: 11.8 KB (11831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99035a639515fbfb1dd27120414406ca641ce97d2d2782ecf1a80a0279dfa207`  
		Last Modified: Thu, 18 Jul 2024 19:11:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52cb3322ac89b2fdf420a924987461081e6de1256c4020ffc49dcd069e92b8d`  
		Last Modified: Thu, 18 Jul 2024 19:11:58 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3293bffe94bacc0ff89ef5b3ab9b4329d9d908f5ddceca51a6f975d37800ac99`  
		Last Modified: Thu, 18 Jul 2024 19:11:59 GMT  
		Size: 2.8 MB (2751273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecce632aaa6e5dcdc5b6de07699f3d0dfd37484a112bbfe64d902e44925c58e`  
		Last Modified: Thu, 18 Jul 2024 20:00:23 GMT  
		Size: 353.0 MB (353047426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138dafb50d6a32bcb863f11039571a2f41f653d810a6ef28b0ddb9e7898e9fd0`  
		Last Modified: Thu, 18 Jul 2024 20:00:16 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bcad886b7dfaa7c442d960e6706b8153a07aa71a212f2a3ae84fe6775d5708`  
		Last Modified: Thu, 18 Jul 2024 20:00:17 GMT  
		Size: 14.8 MB (14839460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:54c028e29de9265cc241bf069d4c21f6ad42e1d5cdf822a1ab19f4d739f6d430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705fc4d0dbb6db7b6bc842c8b6976adeb14a869b6a207f8fa1c6eb0d37d92450`

```dockerfile
```

-	Layers:
	-	`sha256:ac412841764c378ef16b3507e64257a3523891e1cacd777f7ed2ea93e7b015e7`  
		Last Modified: Thu, 18 Jul 2024 20:00:15 GMT  
		Size: 5.5 MB (5515765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5b6c1b6ba6dc98f97311b9cb7566d3c90fc7f9b46afeb779a4bfd3cf45d6287`  
		Last Modified: Thu, 18 Jul 2024 20:00:15 GMT  
		Size: 19.9 KB (19922 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:6b1970a7d26afbe704ac22793f3159a0e06bf757b33a58f9b90dc042a3444769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490999806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fd8ed7a78ca4afaa41a1a030cefd6d118e95741c76ea955ad436136aa004a8`
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
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
USER root
# Wed, 17 Jul 2024 15:21:21 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:21:21 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_VERSION=24.0.0.7
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c
# Wed, 17 Jul 2024 15:21:21 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.7 org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 17 Jul 2024 15:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 17 Jul 2024 15:21:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.7 BuildLabel=cl240720240701-1102
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_URL
# Wed, 17 Jul 2024 15:21:21 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:21:21 GMT
USER 1001
# Wed, 17 Jul 2024 15:21:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:21:21 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:21:21 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 17 Jul 2024 15:21:21 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:21:21 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba08511b677aee03243955ecffe2cf3bff11dcf9bbc6f35ad5e9deb073b144`  
		Last Modified: Tue, 02 Jul 2024 10:27:08 GMT  
		Size: 12.9 MB (12888223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb66836dd2d9507b338d0a186184038c56ce172a31e6e5efa432444b4d214f7`  
		Last Modified: Wed, 17 Jul 2024 18:08:54 GMT  
		Size: 53.6 MB (53571328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac6a8b9d8491240c4469752c73629aa6a4411e161e1c3e006a0a459632e0922`  
		Last Modified: Wed, 17 Jul 2024 18:08:52 GMT  
		Size: 3.4 MB (3425398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1b6614f4b77158a5b0c35d7bada8341dc8c39b1ccc546db2383fb765679f9`  
		Last Modified: Thu, 18 Jul 2024 22:19:27 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1015256339ef0ecbff100bbed1fb5ad85bde2239dc4394e4764c269341c80fb4`  
		Last Modified: Thu, 18 Jul 2024 22:19:28 GMT  
		Size: 17.4 MB (17427436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929dff8e88cffac89e15315f5efbe1cb11ef70c3d260aa2d2afafbc0c53276b0`  
		Last Modified: Thu, 18 Jul 2024 22:19:27 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dac6ce5ab11a26c47aa0f8cd95dd1879402691aaaa12f89907e32b800d4bd24`  
		Last Modified: Thu, 18 Jul 2024 22:19:27 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7062214da4bd0db78773a3f20eb6e837d4d8011a8adda07c0b24fb595e6dae1b`  
		Last Modified: Thu, 18 Jul 2024 22:19:28 GMT  
		Size: 11.8 KB (11833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f531dc36f8d0c829eb83e31d86a209ea440ba5f729ddadc75d2389290b4c7f8c`  
		Last Modified: Thu, 18 Jul 2024 22:19:28 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2030e6fe13b351dba4ce6912b97f88d43556a63d9fda84f89e4d632e514514`  
		Last Modified: Thu, 18 Jul 2024 22:19:28 GMT  
		Size: 12.6 KB (12640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2a56c2c4dc3521b60ecf836e625d5a3e816c7aaf8e94d75f1e842c14f4ec25`  
		Last Modified: Thu, 18 Jul 2024 22:19:30 GMT  
		Size: 2.7 MB (2656128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12bb712a9bcdd2fd29f3bb64cfc7d68a708825a59e0791767ede7082c486a02`  
		Last Modified: Thu, 18 Jul 2024 23:07:49 GMT  
		Size: 353.0 MB (353047272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3465e3e46d585699c5444b5db0eb31211ec94d9a63011c2944779350db54a44`  
		Last Modified: Thu, 18 Jul 2024 23:07:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a250930f02054bf6cf4b52797afab61ced3186405aa56bdbc5d4f05125c630`  
		Last Modified: Thu, 18 Jul 2024 23:07:41 GMT  
		Size: 13.5 MB (13458777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:793daa105fbb0861eab3e06affa35a79adb37734d5893cf53a0dd412993df1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5539592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c29b660f22fb0dd87ed3e3752ce4d76877d0a428ee3b889ef7d9cc887fb5064`

```dockerfile
```

-	Layers:
	-	`sha256:a7a556caacaa300ff78e6790aef98a934bd45b272547b2c7303d11aa8d7c48e4`  
		Last Modified: Thu, 18 Jul 2024 23:07:40 GMT  
		Size: 5.5 MB (5519990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb73e98ab03b7464948093120bc29745c744074e9bbd99b0a219b9cfc23e083`  
		Last Modified: Thu, 18 Jul 2024 23:07:39 GMT  
		Size: 19.6 KB (19602 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:12eca1dedf860497a30a609dafcfe12d971f08f3c48bffe0aa7fc566400a43da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484654687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b782c6d9a2cb62cc03c22fd62a4b790cdf568ca547005f77a28e07c8a3c1da90`
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
# Thu, 11 Jul 2024 09:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Jul 2024 09:08:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_VERSION=jdk-11.0.23+9_openj9-0.44.0
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8613dc2b6c403f48d2a8e25da92ab9f8a7b5dd63cb81d1917e4cb070ae371557';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='e2c5dc88e0701b067cde828f0f1c1593d81393de656a077bbb0baf8e5fdc7f7e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b9558416d6d773fce0d9b4d3f875fdfc5ffc1afd922570b0f7a6f7cbab7468ab';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='cd7bd3d5cd7bcb6f7884d55c73119e509fdb4fc5b0e88adfd7c5e6b3e549a3d5';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.23%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_11.0.23_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 09:08:13 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Jul 2024 09:08:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
USER root
# Wed, 17 Jul 2024 15:21:21 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:21:21 GMT
ARG OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_VERSION=24.0.0.7
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_BUILD_LABEL=cl240720240701-1102
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c
# Wed, 17 Jul 2024 15:21:21 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.7 org.opencontainers.image.revision=cl240720240701-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 17 Jul 2024 15:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 17 Jul 2024 15:21:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.7 BuildLabel=cl240720240701-1102
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ARG LIBERTY_URL
# Wed, 17 Jul 2024 15:21:21 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.7 LIBERTY_BUILD_LABEL=cl240720240701-1102 LIBERTY_SHA=df7d6b1d0d1e39b867bbb6305da13f9fadd70d8c LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 17 Jul 2024 15:21:21 GMT
USER 1001
# Wed, 17 Jul 2024 15:21:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 17 Jul 2024 15:21:21 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 17 Jul 2024 15:21:21 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 17 Jul 2024 15:21:21 GMT
ARG VERBOSE=false
# Wed, 17 Jul 2024 15:21:21 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw; # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
COPY --chown=1001:0 server.xml /config/ # buildkit
# Wed, 17 Jul 2024 15:21:21 GMT
# ARGS: VERBOSE=false REPOSITORIES_PROPERTIES=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx # buildkit
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac3110a5d1eebf9525a140f60c8dbde0133312ec7905bb4cff8ce58bfde450`  
		Last Modified: Tue, 02 Jul 2024 05:55:15 GMT  
		Size: 12.2 MB (12203618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974717a8dc82f7310bcdd38953a9c17858b41eae0d61aac5d4a4c42b6f1ef96c`  
		Last Modified: Tue, 02 Jul 2024 05:59:03 GMT  
		Size: 50.9 MB (50851650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83844364325398a05e53100e4d317a0d2cc462dcb776dcc50f7c8609fa473c98`  
		Last Modified: Wed, 17 Jul 2024 18:05:54 GMT  
		Size: 4.5 MB (4533608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5badcba1072a7052897a862d289ef0d8b1a58b6f2914f8f917525beb4436823`  
		Last Modified: Thu, 18 Jul 2024 19:15:43 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b02eb504366644687752fec2c8b1ceadd4da021d7b92d5dd309a74768ea7fc`  
		Last Modified: Thu, 18 Jul 2024 19:15:43 GMT  
		Size: 17.4 MB (17426925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5966c72649aad2ca67557433f34ff8ed7f69d70d415ae8e9725cbdb1fa7a62d`  
		Last Modified: Thu, 18 Jul 2024 19:15:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4806f38ebd128db4525bb9c1adb90f10ceaa92d80d6646943e9a9853d77bd7ec`  
		Last Modified: Thu, 18 Jul 2024 19:15:43 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d492047006127eb0dfe368107679cb90021d01b7774f3f8a8036180fb6a6a58`  
		Last Modified: Thu, 18 Jul 2024 19:15:44 GMT  
		Size: 11.8 KB (11826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c652e26379b6cda574466c6929b67b805de2b95d7ce6919843b140144683c003`  
		Last Modified: Thu, 18 Jul 2024 19:15:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f973b8eb018ca7728e39745a8a9521486dc3cd7b8833d25056945cb79e2d04ec`  
		Last Modified: Thu, 18 Jul 2024 19:15:44 GMT  
		Size: 12.6 KB (12634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f50891920e3c77c774c71ada77f6a7f174cd56c033f72909eb4ee1e806f396`  
		Last Modified: Thu, 18 Jul 2024 19:15:44 GMT  
		Size: 2.9 MB (2858609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eef147a721091d479076a1f4ee43ffb90d17bbcde8f6e2d269e4a962dff2dd`  
		Last Modified: Thu, 18 Jul 2024 20:10:52 GMT  
		Size: 353.0 MB (353047627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18aafa2cfd21b6368fc524a94616b6c52ba2dc91990a984e7948b1df81c74db`  
		Last Modified: Thu, 18 Jul 2024 20:10:46 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e992a0d1e2696b456a38ea44cada3bbe63a7b13bb331f65096652c69683ed098`  
		Last Modified: Thu, 18 Jul 2024 20:10:48 GMT  
		Size: 15.7 MB (15671350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:e3ecd6c2ba5a5807ebd2f82e7e2a773d33fd3fbbc6d10c3b10566995a49360bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b9ab00c5ef50fcbc58ac13a5b9e4b76baf5679ee458e83ac0bdc876231edd2`

```dockerfile
```

-	Layers:
	-	`sha256:a6258a7438f6e8533f0cce9b09444a8ebd35c25093122325f6223ac5738ccf80`  
		Last Modified: Thu, 18 Jul 2024 20:10:46 GMT  
		Size: 5.5 MB (5515547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e402c58962666202b2d355bd47b2470fc88f95bb4921d09ea02919a7834182f`  
		Last Modified: Thu, 18 Jul 2024 20:10:45 GMT  
		Size: 19.6 KB (19574 bytes)  
		MIME: application/vnd.in-toto+json
