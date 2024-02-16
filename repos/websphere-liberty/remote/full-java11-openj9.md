## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:bc76e6e361e2ed6aa9da862ef4dadb353cdbf9519dd081416d9b4a83870f4a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:dd4f0a39ede7fd19f7201a30ceebe4a26191a426851ba1b49207d7cf4ede2fd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.3 MB (479310002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1077b3129f9232fac810ae2fbf2a8ea0fb4e844554d808cb7ae7080fbba07e07`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:10:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 02:11:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:12:47 GMT
ENV JAVA_VERSION=jdk-11.0.22+7_openj9-0.43.0
# Fri, 16 Feb 2024 02:13:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cf723eca95f805d5ba0dfc33aa798ccd9f2a1984d2dc72c0b2fed5df804e8edf';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ce87335076c236d5b8c63eec878492403ccd4354403ab25b24a8434ba7c84e3d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c0677152632c8da8b840b9b4475046318b25dcb3e15096f5f7fd6a49952afd6a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='7976a5076e484c3de391b25d6b4b06ac2102e0b8ea20f08787bc25c49d456112';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 16 Feb 2024 02:13:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 02:13:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 16 Feb 2024 02:14:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 16 Feb 2024 06:55:04 GMT
USER root
# Fri, 16 Feb 2024 06:55:04 GMT
ARG VERBOSE=false
# Fri, 16 Feb 2024 06:55:05 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Feb 2024 06:55:05 GMT
ARG LIBERTY_VERSION=24.0.0.1
# Fri, 16 Feb 2024 06:55:05 GMT
ARG LIBERTY_BUILD_LABEL=cl240120240115-2042
# Fri, 16 Feb 2024 06:55:05 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.1 org.opencontainers.image.revision=cl240120240115-2042 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 16 Feb 2024 06:55:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 16 Feb 2024 06:55:05 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.1 BuildLabel=cl240120240115-2042
# Fri, 16 Feb 2024 06:55:06 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Fri, 16 Feb 2024 06:55:06 GMT
ARG LIBERTY_URL
# Fri, 16 Feb 2024 06:55:06 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 16 Feb 2024 06:55:14 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 06:55:15 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 16 Feb 2024 06:55:16 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Fri, 16 Feb 2024 06:55:16 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Fri, 16 Feb 2024 06:55:16 GMT
COPY dir:ba06ea5999d3c0c20d75ac4b0523c2d35756230f633edc5b128a5b61353a1310 in /opt/ibm/helpers/ 
# Fri, 16 Feb 2024 06:55:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 16 Feb 2024 06:55:17 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 16 Feb 2024 06:55:23 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 16 Feb 2024 06:55:23 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Feb 2024 06:55:23 GMT
USER 1001
# Fri, 16 Feb 2024 06:55:23 GMT
EXPOSE 9080 9443
# Fri, 16 Feb 2024 06:55:23 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 16 Feb 2024 06:55:23 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Feb 2024 07:03:17 GMT
ARG VERBOSE=false
# Fri, 16 Feb 2024 07:03:17 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Feb 2024 07:10:07 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Fri, 16 Feb 2024 07:10:08 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 16 Feb 2024 07:10:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24423a8d55e991d630fc7cc3412fc01a7673a1df8a2a5fbbd4d3fdfff3ea0242`  
		Last Modified: Fri, 16 Feb 2024 02:18:27 GMT  
		Size: 12.2 MB (12158921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e9896316066fe6960a3dbf3e524870b3d2f9db02e703b3862069de4c659f71`  
		Last Modified: Fri, 16 Feb 2024 02:19:30 GMT  
		Size: 49.0 MB (49000318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3648d98d1122291fdb29670394c1ca92003a25622bda7c40375932d40dc7ef9e`  
		Last Modified: Fri, 16 Feb 2024 02:19:24 GMT  
		Size: 4.3 MB (4294555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54feeb78422b9036121dcfedb3cdb0231d0447f2a134a39890f0df823a1f4c`  
		Last Modified: Fri, 16 Feb 2024 08:07:04 GMT  
		Size: 31.8 KB (31750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ebbb3fd6d033cf68a39de040dc1c0b50f175953d6ef529dc99344f5f7293a1`  
		Last Modified: Fri, 16 Feb 2024 08:07:05 GMT  
		Size: 17.1 MB (17089075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c336035d3881cf24b37293c2f85795396d06d60e373f3e6fb98c7d63e6ae1b`  
		Last Modified: Fri, 16 Feb 2024 08:07:04 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23feee22350b48acf8ddbfbdf18f22bf183ea3464b7329512da51b1d9f373f6a`  
		Last Modified: Fri, 16 Feb 2024 08:07:01 GMT  
		Size: 1.5 KB (1518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b10a623959cfa02561f2c420bca5faa07429ba79c186307f0a545ff0de9b3e`  
		Last Modified: Fri, 16 Feb 2024 08:07:02 GMT  
		Size: 11.5 KB (11504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0571cfeeed67413b23b282d746b0caa8ea1a8a269d41ef1998d9da3b58ab00fe`  
		Last Modified: Fri, 16 Feb 2024 08:07:02 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e8d16be11a9db9039fb3518185dbc3c6c03f62f7919141bd7024085280068f`  
		Last Modified: Fri, 16 Feb 2024 08:07:02 GMT  
		Size: 12.4 KB (12424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8917e5bdf8f512b80e6c63ab40b3e2ce13de2b465b0dd8e4d884e64eefbb98`  
		Last Modified: Fri, 16 Feb 2024 08:07:02 GMT  
		Size: 2.7 MB (2741835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3668a620151f2c1fd7a28de077efa0a524969b9af47f6546e5acaec60baa1676`  
		Last Modified: Fri, 16 Feb 2024 08:08:07 GMT  
		Size: 349.2 MB (349217451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb8f08224aac1afd27024a03c59aab13f4fb27dff42abd681537d3cc82784e6`  
		Last Modified: Fri, 16 Feb 2024 08:07:50 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537e87668f98655b4984a6ccc10f1ae10fc2e7b2acce57e4617050020b41d663`  
		Last Modified: Fri, 16 Feb 2024 08:07:52 GMT  
		Size: 14.3 MB (14298750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:cd9ddd43a310262e9d39ada31c453de57800bf42fd12150fd61d4b2a41eb2fca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.1 MB (475119344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1078c686fe08244866f5d3c6093dd55704cbe2968ddde8be8b2d5efedcebcf07`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 05:04:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:06:18 GMT
ENV JAVA_VERSION=jdk-11.0.22+7_openj9-0.43.0
# Fri, 16 Feb 2024 05:07:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cf723eca95f805d5ba0dfc33aa798ccd9f2a1984d2dc72c0b2fed5df804e8edf';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ce87335076c236d5b8c63eec878492403ccd4354403ab25b24a8434ba7c84e3d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c0677152632c8da8b840b9b4475046318b25dcb3e15096f5f7fd6a49952afd6a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='7976a5076e484c3de391b25d6b4b06ac2102e0b8ea20f08787bc25c49d456112';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 16 Feb 2024 05:07:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:07:14 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 16 Feb 2024 05:07:45 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 16 Feb 2024 09:38:24 GMT
USER root
# Fri, 16 Feb 2024 09:38:24 GMT
ARG VERBOSE=false
# Fri, 16 Feb 2024 09:38:24 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Feb 2024 09:38:24 GMT
ARG LIBERTY_VERSION=24.0.0.1
# Fri, 16 Feb 2024 09:38:24 GMT
ARG LIBERTY_BUILD_LABEL=cl240120240115-2042
# Fri, 16 Feb 2024 09:38:24 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.1 org.opencontainers.image.revision=cl240120240115-2042 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 16 Feb 2024 09:38:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 16 Feb 2024 09:38:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.1 BuildLabel=cl240120240115-2042
# Fri, 16 Feb 2024 09:38:25 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Fri, 16 Feb 2024 09:38:25 GMT
ARG LIBERTY_URL
# Fri, 16 Feb 2024 09:38:25 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 16 Feb 2024 09:38:36 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 09:38:36 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 16 Feb 2024 09:38:37 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Fri, 16 Feb 2024 09:38:38 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Fri, 16 Feb 2024 09:38:38 GMT
COPY dir:ba06ea5999d3c0c20d75ac4b0523c2d35756230f633edc5b128a5b61353a1310 in /opt/ibm/helpers/ 
# Fri, 16 Feb 2024 09:38:38 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 16 Feb 2024 09:38:38 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 16 Feb 2024 09:38:43 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 16 Feb 2024 09:38:43 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Feb 2024 09:38:43 GMT
USER 1001
# Fri, 16 Feb 2024 09:38:43 GMT
EXPOSE 9080 9443
# Fri, 16 Feb 2024 09:38:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 16 Feb 2024 09:38:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Feb 2024 09:39:07 GMT
ARG VERBOSE=false
# Fri, 16 Feb 2024 09:39:07 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Feb 2024 09:45:42 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Fri, 16 Feb 2024 09:45:45 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 16 Feb 2024 09:46:17 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f839bf46a0451897938672ea164628a4ba318460978bb9015f5dd6757317f12e`  
		Last Modified: Fri, 16 Feb 2024 05:11:43 GMT  
		Size: 12.1 MB (12116589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c21b4b45696e9b2ab798439b1f5a35cb6b8cb4fab0af686ce5dc8accae39fa6`  
		Last Modified: Fri, 16 Feb 2024 05:12:40 GMT  
		Size: 48.2 MB (48208826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f05644188891701a8cfa8fb8223f1d1e9f659d16ec6b98fc86b810c38ab053b`  
		Last Modified: Fri, 16 Feb 2024 05:12:36 GMT  
		Size: 4.1 MB (4145682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace381ab5a63e50a625532c8a95b0bc7313c7c9e88ad66316f9af893cf160a30`  
		Last Modified: Fri, 16 Feb 2024 10:24:50 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94176c492e9fa670c136a8379de2679ece292cb9ace7d6c928ecd871d802810d`  
		Last Modified: Fri, 16 Feb 2024 10:24:51 GMT  
		Size: 17.1 MB (17089251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293028960b1d7b4693182d088124ddc18e5d4ab4c7f53aa70527749e1f550b63`  
		Last Modified: Fri, 16 Feb 2024 10:24:50 GMT  
		Size: 607.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2639faee7c67f36bb3a6aa7c03d7b55539491538cca6a56b33c630bd53b3ad80`  
		Last Modified: Fri, 16 Feb 2024 10:24:48 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99740cf9c6b0cf7a1584564e30f72d2660ddb3878e0e2cf9a3e6fa719fdbc365`  
		Last Modified: Fri, 16 Feb 2024 10:24:48 GMT  
		Size: 11.5 KB (11499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edd756e5c01e9e2f98d68f48edefcede2f90b51eff3529e6b04a90302418a13`  
		Last Modified: Fri, 16 Feb 2024 10:24:48 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b22412fc8ff13c42158d2423bf97003becb8c8e125d7f87bcc8d19f658a2c2`  
		Last Modified: Fri, 16 Feb 2024 10:24:48 GMT  
		Size: 12.4 KB (12427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7987541066ee388445003275905ec58d3021557336bc0a79e3d3a7de5ba368d7`  
		Last Modified: Fri, 16 Feb 2024 10:24:49 GMT  
		Size: 2.7 MB (2691100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcb11c4439b5b8c63345853e9db5a3f08824b190c38a517bb7e9570296fa73a`  
		Last Modified: Fri, 16 Feb 2024 10:25:20 GMT  
		Size: 349.2 MB (349216478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1155c1206b7747d6958c7c211802d224da92e24e6d7d9b1ac0534e39f46c7b1b`  
		Last Modified: Fri, 16 Feb 2024 10:25:06 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95941e25d73cfeabf29b537cf6bc5351d5c10f12280f4fa97542b313d72c86b6`  
		Last Modified: Fri, 16 Feb 2024 10:25:08 GMT  
		Size: 13.2 MB (13181516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:02a412c68a32448efff6bf89daf3f80f8ad28819a83b76d117f396d385009938
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.2 MB (483222468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2350f206f0783b53b4cd5aad360326bf160b60877956b772863cd625b6e9ced0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:15:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 04:16:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:18:28 GMT
ENV JAVA_VERSION=jdk-11.0.22+7_openj9-0.43.0
# Fri, 16 Feb 2024 04:19:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cf723eca95f805d5ba0dfc33aa798ccd9f2a1984d2dc72c0b2fed5df804e8edf';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ce87335076c236d5b8c63eec878492403ccd4354403ab25b24a8434ba7c84e3d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c0677152632c8da8b840b9b4475046318b25dcb3e15096f5f7fd6a49952afd6a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='7976a5076e484c3de391b25d6b4b06ac2102e0b8ea20f08787bc25c49d456112';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 16 Feb 2024 04:19:41 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:19:42 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 16 Feb 2024 04:20:16 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 16 Feb 2024 05:44:53 GMT
USER root
# Fri, 16 Feb 2024 05:44:53 GMT
ARG VERBOSE=false
# Fri, 16 Feb 2024 05:44:54 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Feb 2024 05:44:54 GMT
ARG LIBERTY_VERSION=24.0.0.1
# Fri, 16 Feb 2024 05:44:54 GMT
ARG LIBERTY_BUILD_LABEL=cl240120240115-2042
# Fri, 16 Feb 2024 05:44:55 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.1 org.opencontainers.image.revision=cl240120240115-2042 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 16 Feb 2024 05:44:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Fri, 16 Feb 2024 05:44:56 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.1 BuildLabel=cl240120240115-2042
# Fri, 16 Feb 2024 05:44:59 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Fri, 16 Feb 2024 05:44:59 GMT
ARG LIBERTY_URL
# Fri, 16 Feb 2024 05:45:00 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 16 Feb 2024 05:45:13 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 05:45:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 16 Feb 2024 05:45:16 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Fri, 16 Feb 2024 05:45:16 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Fri, 16 Feb 2024 05:45:17 GMT
COPY dir:ba06ea5999d3c0c20d75ac4b0523c2d35756230f633edc5b128a5b61353a1310 in /opt/ibm/helpers/ 
# Fri, 16 Feb 2024 05:45:17 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 16 Feb 2024 05:45:20 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 16 Feb 2024 05:45:29 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 16 Feb 2024 05:45:29 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Feb 2024 05:45:30 GMT
USER 1001
# Fri, 16 Feb 2024 05:45:30 GMT
EXPOSE 9080 9443
# Fri, 16 Feb 2024 05:45:31 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 16 Feb 2024 05:45:31 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 16 Feb 2024 05:54:49 GMT
ARG VERBOSE=false
# Fri, 16 Feb 2024 05:54:49 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 16 Feb 2024 06:02:02 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Fri, 16 Feb 2024 06:02:10 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 16 Feb 2024 06:02:52 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cd1f300bac50290323d2ea203621f2bacd89916fbf2bf31db65a72e985fe1a`  
		Last Modified: Fri, 16 Feb 2024 04:25:18 GMT  
		Size: 12.9 MB (12893887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a59d5db69a263f4a190c6d1b7274d00ceefaca68d82799c5f32897e4957ffb`  
		Last Modified: Fri, 16 Feb 2024 04:26:30 GMT  
		Size: 50.6 MB (50565715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0d9fb56560e37f3738fcdb2dcd466a82bd6585d5ad5aa8ea375f06bedb8d7`  
		Last Modified: Fri, 16 Feb 2024 04:26:24 GMT  
		Size: 3.4 MB (3409772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870f60c0c44f1affc3aade5f22c930196a709f4cc21ff567cddb8679fec22883`  
		Last Modified: Fri, 16 Feb 2024 07:05:04 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8813502e9e8ede7ea7b56cf4870aa33fa168dd424a3e7f2d52878cb36f775f03`  
		Last Modified: Fri, 16 Feb 2024 07:05:06 GMT  
		Size: 17.1 MB (17089943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7714e2e6ad917d9844540b5e9b6da8ad6e5bf18b7a59cf548d3f4e3bc54996`  
		Last Modified: Fri, 16 Feb 2024 07:05:05 GMT  
		Size: 608.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd37800573e7afd5950ccdc8b40845a6ba6a1250c41b81b9ee5b405316600df`  
		Last Modified: Fri, 16 Feb 2024 07:05:01 GMT  
		Size: 1.5 KB (1517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e02ce14ed600c24cc17bd1dcfb1920d5862ab2be0f0ddb8c1f9c9c3f57f42d`  
		Last Modified: Fri, 16 Feb 2024 07:05:01 GMT  
		Size: 11.5 KB (11501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcd7e4ca83913085927bbbff97fe69513ecc0fbedb74175baa031000007ed2a`  
		Last Modified: Fri, 16 Feb 2024 07:05:01 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5904c1fc8baaf11ad4bf53765cf571d5a707d719c895a55af9afad78d8219ce`  
		Last Modified: Fri, 16 Feb 2024 07:05:01 GMT  
		Size: 12.4 KB (12432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176293fae0d11fd2ae07d2930af231b7243ce8dac7ceb685f2bad8dc804af0aa`  
		Last Modified: Fri, 16 Feb 2024 07:05:02 GMT  
		Size: 2.6 MB (2612075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed63a184e5d0d1f33a5d8a94f2e0496ecca75e9410742681a657f580f82e059`  
		Last Modified: Fri, 16 Feb 2024 07:06:15 GMT  
		Size: 349.2 MB (349218323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ac5c2e641da9c5b943c30fcb0a26c7368962a5d42d4234bdd3fdec9bd14e5`  
		Last Modified: Fri, 16 Feb 2024 07:05:57 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085bf200a05a98c96c28b8112d821b966c032e6803b4716dfb26c68800cef4eb`  
		Last Modified: Fri, 16 Feb 2024 07:05:59 GMT  
		Size: 11.7 MB (11740145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:21f93e30af788c5c593896d435c03e3aa1ef3d88ca53942985216946322a251c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.0 MB (476978549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7d0c0307c399cd0adf85e2161ae7b099d625a07f471dcbdbc6a21279379b7a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:23:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 02:23:52 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Feb 2024 22:08:29 GMT
ENV JAVA_VERSION=jdk-11.0.22+7_openj9-0.43.0
# Wed, 14 Feb 2024 22:13:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cf723eca95f805d5ba0dfc33aa798ccd9f2a1984d2dc72c0b2fed5df804e8edf';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_aarch64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ce87335076c236d5b8c63eec878492403ccd4354403ab25b24a8434ba7c84e3d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_ppc64le_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c0677152632c8da8b840b9b4475046318b25dcb3e15096f5f7fd6a49952afd6a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_x64_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        s390x)          ESUM='7976a5076e484c3de391b25d6b4b06ac2102e0b8ea20f08787bc25c49d456112';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.22%2B7_openj9-0.43.0/ibm-semeru-open-jre_s390x_linux_11.0.22_7_openj9-0.43.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Feb 2024 22:13:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Feb 2024 22:13:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Feb 2024 22:14:29 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.85/bin/apache-tomcat-9.0.85.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Feb 2024 23:57:52 GMT
USER root
# Thu, 15 Feb 2024 01:06:52 GMT
ARG VERBOSE=false
# Thu, 15 Feb 2024 01:06:52 GMT
ARG OPENJ9_SCC=true
# Thu, 15 Feb 2024 01:06:52 GMT
ARG LIBERTY_VERSION=24.0.0.1
# Thu, 15 Feb 2024 01:06:53 GMT
ARG LIBERTY_BUILD_LABEL=cl240120240115-2042
# Thu, 15 Feb 2024 01:06:53 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.1 org.opencontainers.image.revision=cl240120240115-2042 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 15 Feb 2024 01:06:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Thu, 15 Feb 2024 01:06:53 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.1 BuildLabel=cl240120240115-2042
# Thu, 15 Feb 2024 01:06:54 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Thu, 15 Feb 2024 01:06:54 GMT
ARG LIBERTY_URL
# Thu, 15 Feb 2024 01:06:54 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 15 Feb 2024 01:07:01 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2024 01:07:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 15 Feb 2024 01:07:02 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env
# Thu, 15 Feb 2024 01:07:02 GMT
COPY file:7278f8f20139aab77b5c9fa76ad85e8a92836053c3ecfb9f5925f1a19788ef47 in /opt/ibm/NOTICES 
# Thu, 15 Feb 2024 01:07:02 GMT
COPY dir:ba06ea5999d3c0c20d75ac4b0523c2d35756230f633edc5b128a5b61353a1310 in /opt/ibm/helpers/ 
# Thu, 15 Feb 2024 01:07:02 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 15 Feb 2024 01:07:03 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 15 Feb 2024 01:07:07 GMT
# ARGS: DOWNLOAD_OPTIONS= LIBERTY_BUILD_LABEL=cl240120240115-2042 LIBERTY_VERSION=24.0.0.1 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 15 Feb 2024 01:07:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 15 Feb 2024 01:07:07 GMT
USER 1001
# Thu, 15 Feb 2024 01:07:07 GMT
EXPOSE 9080 9443
# Thu, 15 Feb 2024 01:07:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 15 Feb 2024 01:07:08 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 15 Feb 2024 01:11:02 GMT
ARG VERBOSE=false
# Thu, 15 Feb 2024 01:11:02 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 15 Feb 2024 01:17:23 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN set -eux;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     mkdir /opt/ibm/wlp/etc/;     echo "$REPOSITORIES_PROPERTIES" > /opt/ibm/wlp/etc/repositories.properties;   fi;   installUtility install --acceptLicense baseBundle;   if [ ! -z "$REPOSITORIES_PROPERTIES" ]; then     rm /opt/ibm/wlp/etc/repositories.properties;   fi;   rm -rf /output/workarea /output/logs;   find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw;
# Thu, 15 Feb 2024 01:17:31 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 15 Feb 2024 01:18:01 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6f31e20a5049cb980edfab79b8d30b3e1da57b77e93268b40d42bee17eabb1`  
		Last Modified: Fri, 02 Feb 2024 02:54:32 GMT  
		Size: 12.2 MB (12206869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25a8ff2d762793c4b141baa64ae0d776936a224b06aafe6473b70dc1af70045`  
		Last Modified: Wed, 14 Feb 2024 22:33:31 GMT  
		Size: 48.3 MB (48268520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8c28a6722e4ce1bca2ea907fcfa030ce2d03c3165ad5b9dd8e29f0ae69b052`  
		Last Modified: Wed, 14 Feb 2024 22:33:26 GMT  
		Size: 4.5 MB (4514025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e15b1148da24398b09b20e9eac0b1512703a458f3794f5668fcbdd4c27ac31`  
		Last Modified: Thu, 15 Feb 2024 02:18:33 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b121f79880faf0dbb5640d43086a2a2858c47d0e6c26f79ad6099d345ef0ed9e`  
		Last Modified: Thu, 15 Feb 2024 02:18:34 GMT  
		Size: 17.5 MB (17493027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a409799ccc342164e17b8c52243794d4b461996cedee1d4b8b77a1076749f711`  
		Last Modified: Thu, 15 Feb 2024 02:18:32 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caca87b4c2cd3977d515419b3e7e211c3043ad3c0731aab02ae597c7bd6306fa`  
		Last Modified: Thu, 15 Feb 2024 02:18:31 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960767be191213be98ca55feaf65b1996b026dae18f552f679ec3c01bc5d33f7`  
		Last Modified: Thu, 15 Feb 2024 02:18:31 GMT  
		Size: 11.5 KB (11500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80993e90f05f9314edee28b99f912dbf0f18c11e9a94f69c225f531b8266ee2d`  
		Last Modified: Thu, 15 Feb 2024 02:18:31 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e345bd0323029fc9f3663c38caefdb20cca255039f9b05457cd1845e8124c56`  
		Last Modified: Thu, 15 Feb 2024 02:18:31 GMT  
		Size: 12.4 KB (12431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3df5b7fe538088554b1e5e89356c2aeed0272853157d8290d9dee8e01932311`  
		Last Modified: Thu, 15 Feb 2024 02:18:32 GMT  
		Size: 2.7 MB (2724693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f15e7e3e31fe49c3fea1b576e987381bbe33f1b05e9c7e78b5883a78de2e71`  
		Last Modified: Thu, 15 Feb 2024 02:19:01 GMT  
		Size: 349.2 MB (349216304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f6d38b964ee347cd1a28bbb91fe0d268b3e595c9e3cbb1c2d2708b4a4ef6ac`  
		Last Modified: Thu, 15 Feb 2024 02:18:46 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c44614cae4fe9bf6e0984049fa56147be535d77d8279a20af7c565c3f27f9e`  
		Last Modified: Thu, 15 Feb 2024 02:18:47 GMT  
		Size: 13.8 MB (13839097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
