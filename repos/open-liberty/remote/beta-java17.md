## `open-liberty:beta-java17`

```console
$ docker pull open-liberty@sha256:da91e5717507db33ab5b22c1e1292496959f5f0da6cfd6c897b09111d3e97350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:beta-java17` - linux; amd64

```console
$ docker pull open-liberty@sha256:f3e4f6868a9603c6fd7560cea5ff2fe5748e0107f46e4bf80647e84551d759d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.9 MB (469863988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d562df80c2f98cc8b0b6130c9c0d1b21d6f0ddde18ee52fdc7acfb8a25a1fb1`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 15:47:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 15:47:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:51:28 GMT
ENV JAVA_VERSION=jdk-17.0.7+7_openj9-0.38.0
# Wed, 16 Aug 2023 15:52:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='601dba428fe9d9b5a883aaccbdd37f88c1fb0da2e5b5de65b40cf0a4a0e5fccb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dee6b87258ceba918543956dddf97291cbc2735ffa0288d25239a07c7766d567';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ffda41aa8390d14edbce1775d652f0e4e779df025ac1404c1970802697963aab';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='ee08d6830990562fcc45bec336748390d15357028d3ca0cf4a78bcea7bdfaefe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 16 Aug 2023 15:52:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 15:52:36 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 16 Aug 2023 15:53:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 17 Aug 2023 08:12:03 GMT
USER root
# Thu, 17 Aug 2023 09:04:55 GMT
ARG LIBERTY_VERSION=23.0.0.8-beta
# Thu, 17 Aug 2023 09:04:55 GMT
ARG LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4
# Thu, 17 Aug 2023 09:04:55 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip
# Thu, 17 Aug 2023 09:04:55 GMT
ARG LIBERTY_BUILD_LABEL=cl230720230710-1201
# Thu, 17 Aug 2023 09:04:55 GMT
ARG OPENJ9_SCC=true
# Thu, 17 Aug 2023 09:04:55 GMT
ARG VERBOSE=false
# Thu, 17 Aug 2023 09:04:56 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230720230710-1201 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=23.0.0.8-beta
# Thu, 17 Aug 2023 09:04:56 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Thu, 17 Aug 2023 09:04:56 GMT
COPY dir:0c9b294d41044aadfdfa715e426d188c2e110fe670ffece13814d3dccfec754e in /opt/ol/helpers 
# Thu, 17 Aug 2023 09:04:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 17 Aug 2023 09:04:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Thu, 17 Aug 2023 09:05:12 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 17 Aug 2023 09:05:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 17 Aug 2023 09:05:14 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Thu, 17 Aug 2023 09:05:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 17 Aug 2023 09:05:39 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 17 Aug 2023 09:05:39 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 17 Aug 2023 09:05:39 GMT
USER 1001
# Thu, 17 Aug 2023 09:05:39 GMT
EXPOSE 9080 9443
# Thu, 17 Aug 2023 09:05:39 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 17 Aug 2023 09:05:39 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab3fd228352238bb1856524b5a72c3fc8010fcaf4d2e94b2b3f4fa5561a6566`  
		Last Modified: Wed, 16 Aug 2023 15:56:02 GMT  
		Size: 12.2 MB (12155838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e984c52399ca357e48b8b95d7ce8b16adea6a2cf2ba86cf59a671f57690f65`  
		Last Modified: Wed, 16 Aug 2023 15:57:49 GMT  
		Size: 48.5 MB (48538523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589c288ca0f22bf3c4836d433c4d4acec4f9c33354ae990a3df7c9f8db6544e1`  
		Last Modified: Wed, 16 Aug 2023 15:57:43 GMT  
		Size: 4.7 MB (4746675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60aef30ccc70451c9872dbdeacd15be2bbf65459bf030dfb32a851f4bb37c68c`  
		Last Modified: Thu, 17 Aug 2023 09:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f264a28337ac8239703e134294ca31ac390b9b6d3ff3305d2b36cc617ebd121`  
		Last Modified: Thu, 17 Aug 2023 09:11:17 GMT  
		Size: 9.2 KB (9226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05bd7d2d0e36fc3bdeff53f7e904906909e6e55bd47b3d8de76524e47eb3ce8`  
		Last Modified: Thu, 17 Aug 2023 09:11:16 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d0a3031f0ae5efcdfe22507e60d147c3b4293cfc834a9e0792cace350b823f`  
		Last Modified: Thu, 17 Aug 2023 09:11:14 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd431ea00382b90054904f1c379bef9bedcfd76e373215d495871dfe36de17b`  
		Last Modified: Thu, 17 Aug 2023 09:11:44 GMT  
		Size: 361.1 MB (361102600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e85ef2e739cf8e093f83c01e72b8d3bef682f781e21fc234f7ed8291607650`  
		Last Modified: Thu, 17 Aug 2023 09:11:14 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd7dc67d27efb3052c18e619eba50f088255e345151578287f3f13a86f3eeb4`  
		Last Modified: Thu, 17 Aug 2023 09:11:15 GMT  
		Size: 10.7 KB (10691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ecaaddcb1009180c73ffc8c8927dd33e05d66756661b52ec7c42fc98e0aa69`  
		Last Modified: Thu, 17 Aug 2023 09:11:17 GMT  
		Size: 12.8 MB (12828199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta-java17` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:a7b108a547801b6c18bf54ef023c2dc86c57212b3687463543081e7ae99bf6e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464876979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670122ce53ceff42932ceeb13f29b2a63b72465d44f8ff714ba72d63ea12ce38`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:30:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 14:30:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:33:56 GMT
ENV JAVA_VERSION=jdk-17.0.7+7_openj9-0.38.0
# Wed, 16 Aug 2023 14:35:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='601dba428fe9d9b5a883aaccbdd37f88c1fb0da2e5b5de65b40cf0a4a0e5fccb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dee6b87258ceba918543956dddf97291cbc2735ffa0288d25239a07c7766d567';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ffda41aa8390d14edbce1775d652f0e4e779df025ac1404c1970802697963aab';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='ee08d6830990562fcc45bec336748390d15357028d3ca0cf4a78bcea7bdfaefe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 16 Aug 2023 14:35:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 14:35:01 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 16 Aug 2023 14:35:42 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 16 Aug 2023 16:15:30 GMT
USER root
# Wed, 16 Aug 2023 16:39:15 GMT
ARG LIBERTY_VERSION=23.0.0.8-beta
# Wed, 16 Aug 2023 16:39:15 GMT
ARG LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4
# Wed, 16 Aug 2023 16:39:15 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip
# Wed, 16 Aug 2023 16:39:16 GMT
ARG LIBERTY_BUILD_LABEL=cl230720230710-1201
# Wed, 16 Aug 2023 16:39:16 GMT
ARG OPENJ9_SCC=true
# Wed, 16 Aug 2023 16:39:16 GMT
ARG VERBOSE=false
# Wed, 16 Aug 2023 16:39:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230720230710-1201 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=23.0.0.8-beta
# Wed, 16 Aug 2023 16:39:16 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 16 Aug 2023 16:39:16 GMT
COPY dir:0c9b294d41044aadfdfa715e426d188c2e110fe670ffece13814d3dccfec754e in /opt/ol/helpers 
# Wed, 16 Aug 2023 16:39:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 16 Aug 2023 16:39:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 16 Aug 2023 16:39:32 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 16 Aug 2023 16:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 16 Aug 2023 16:39:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 16 Aug 2023 16:39:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 16 Aug 2023 16:39:54 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 16 Aug 2023 16:39:55 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 16 Aug 2023 16:39:55 GMT
USER 1001
# Wed, 16 Aug 2023 16:39:55 GMT
EXPOSE 9080 9443
# Wed, 16 Aug 2023 16:39:55 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 16 Aug 2023 16:39:55 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac60ed8a72576022d43698a13e953c7c74dac694b1a5a12ed5cebf1ae17c140`  
		Last Modified: Wed, 16 Aug 2023 14:38:10 GMT  
		Size: 12.1 MB (12113460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7016a60878d25d7d670b73380f64c3c45a8a97992c977361023b6aff47e9320`  
		Last Modified: Wed, 16 Aug 2023 14:39:49 GMT  
		Size: 46.5 MB (46514261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5d705eddd7c4128ce13ef6e4b3985796c1ab1e400293d0d0ca408bf0c0ef1c`  
		Last Modified: Wed, 16 Aug 2023 14:39:44 GMT  
		Size: 4.6 MB (4608546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3381db76cabf1c3cab5debc19dd28c2511ae6becb8b864466ead78e1665a3b3e`  
		Last Modified: Wed, 16 Aug 2023 16:45:02 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d4aaaeccc30bae52d75581be9c47c313a3bdcbf8826e2ebf9c69c21308ed52`  
		Last Modified: Wed, 16 Aug 2023 16:45:02 GMT  
		Size: 9.2 KB (9222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7566ab56d5957977801e42516a523946b69616e2b99401ad19f69f3ce77c18c`  
		Last Modified: Wed, 16 Aug 2023 16:45:02 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3b91782435b7a1206534d0419bc2f495ae6c36abf39733c3480e6321faaed1`  
		Last Modified: Wed, 16 Aug 2023 16:45:00 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4476b63d710604f02220f6d8d518f7c70473830c4651f595cf1ffa756e0dd30e`  
		Last Modified: Wed, 16 Aug 2023 16:45:20 GMT  
		Size: 361.1 MB (361104180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6636a066362b514879895901131eaff8aaaec9394a00f285168d812b8d1c816`  
		Last Modified: Wed, 16 Aug 2023 16:45:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d004195ee2a6fa99f15857be04d4723156f8abfdea2da31f5d8810d059caba2`  
		Last Modified: Wed, 16 Aug 2023 16:45:00 GMT  
		Size: 10.7 KB (10689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedf5c238c2c0de6ec98e44da9c8fed53c3397d48927e9ebd1867735a2141f9f`  
		Last Modified: Wed, 16 Aug 2023 16:45:02 GMT  
		Size: 12.1 MB (12079866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta-java17` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:82402c79bda5c0f0917bd18a1dc5c9188130fc23e1644cbbebca08c3f5bf6c40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.4 MB (474374793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbbd4e796b32159d9e101ac4da1eebb12425565d865a7c463d535574a6c7d6a`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Thu, 27 Jul 2023 22:00:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jul 2023 22:01:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jul 2023 22:06:43 GMT
ENV JAVA_VERSION=jdk-17.0.7+7_openj9-0.38.0
# Thu, 27 Jul 2023 22:08:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='601dba428fe9d9b5a883aaccbdd37f88c1fb0da2e5b5de65b40cf0a4a0e5fccb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dee6b87258ceba918543956dddf97291cbc2735ffa0288d25239a07c7766d567';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ffda41aa8390d14edbce1775d652f0e4e779df025ac1404c1970802697963aab';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='ee08d6830990562fcc45bec336748390d15357028d3ca0cf4a78bcea7bdfaefe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 27 Jul 2023 22:08:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jul 2023 22:08:28 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 27 Jul 2023 22:09:09 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 29 Jul 2023 09:33:03 GMT
USER root
# Sat, 29 Jul 2023 09:33:04 GMT
ARG LIBERTY_VERSION=23.0.0.8-beta
# Sat, 29 Jul 2023 09:33:04 GMT
ARG LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4
# Sat, 29 Jul 2023 09:33:07 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip
# Sat, 29 Jul 2023 09:33:09 GMT
ARG LIBERTY_BUILD_LABEL=cl230720230710-1201
# Sat, 29 Jul 2023 09:33:14 GMT
ARG OPENJ9_SCC=true
# Sat, 29 Jul 2023 09:33:17 GMT
ARG VERBOSE=false
# Sat, 29 Jul 2023 09:33:20 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230720230710-1201 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=23.0.0.8-beta
# Sat, 29 Jul 2023 09:33:22 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Sat, 29 Jul 2023 09:33:24 GMT
COPY dir:0c9b294d41044aadfdfa715e426d188c2e110fe670ffece13814d3dccfec754e in /opt/ol/helpers 
# Sat, 29 Jul 2023 09:33:24 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Sat, 29 Jul 2023 09:33:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 29 Jul 2023 09:34:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Sat, 29 Jul 2023 09:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Sat, 29 Jul 2023 09:34:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Sat, 29 Jul 2023 09:34:28 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Sat, 29 Jul 2023 09:35:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Sat, 29 Jul 2023 09:35:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 29 Jul 2023 09:35:17 GMT
USER 1001
# Sat, 29 Jul 2023 09:35:18 GMT
EXPOSE 9080 9443
# Sat, 29 Jul 2023 09:35:18 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Sat, 29 Jul 2023 09:35:19 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f7d78cc0ad5cb61c300b15ac5450a3e09bae8c790cfad3e3a6ea8bf221e7cd`  
		Last Modified: Thu, 27 Jul 2023 22:13:25 GMT  
		Size: 12.9 MB (12895204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d65ea6edf7e49eec77927f1b0eecce93a99bed7ed53db02bf3b85bb4a874696`  
		Last Modified: Thu, 27 Jul 2023 22:16:22 GMT  
		Size: 49.6 MB (49646455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b825268c25ee0a36573787a321cd5c3054f238a669765ea6461b6096df01090`  
		Last Modified: Thu, 27 Jul 2023 22:16:11 GMT  
		Size: 3.8 MB (3780628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0ad71d7c436b35436250b73306312c507d258d62ec56f6de3e9e3fe40e6547`  
		Last Modified: Sat, 29 Jul 2023 09:46:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef344f3444fdd2f10a02b0643d0095eac33be617623534f96746dd6497267d04`  
		Last Modified: Sat, 29 Jul 2023 09:46:18 GMT  
		Size: 9.2 KB (9228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54513266cb1dd5bc29b35810c572f2d90d83bd67a0b0a8163e4765d58cfa5fb0`  
		Last Modified: Sat, 29 Jul 2023 09:46:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e786c8b3fd4aa6dae42769f55aa6eb5b59eabaf018402fbf4cd6ee6eb314f7`  
		Last Modified: Sat, 29 Jul 2023 09:46:15 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052fdeb0812bb14c9ff11465cfba0c6ce00187ff6f029760864c598c7a53c87d`  
		Last Modified: Sat, 29 Jul 2023 09:46:43 GMT  
		Size: 361.1 MB (361103205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2ccccdd6953ec20603736068a2f0ef6a9a8af1aa63d6f50b33628827682ee`  
		Last Modified: Sat, 29 Jul 2023 09:46:15 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aea38c3643bd58bb9bae9a884c85f60572941f3d7cd17240434e598505fe2d9`  
		Last Modified: Sat, 29 Jul 2023 09:46:15 GMT  
		Size: 10.7 KB (10713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2265318c8b282da392a35220244ea7dafc22f602be3ba16057ceeccc1dc9bae`  
		Last Modified: Sat, 29 Jul 2023 09:46:18 GMT  
		Size: 11.2 MB (11178853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta-java17` - linux; s390x

```console
$ docker pull open-liberty@sha256:29efadc44322acb5dcfa9234992ad5e79f566c2c4118f2b54bf687bfa40f7894
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 MB (467126562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13860487687637f3cf259df308a4bd1ac6b1f33252a8ca01987622173c8f93c4`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 09:23:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Aug 2023 09:23:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:27:48 GMT
ENV JAVA_VERSION=jdk-17.0.7+7_openj9-0.38.0
# Wed, 16 Aug 2023 09:29:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='601dba428fe9d9b5a883aaccbdd37f88c1fb0da2e5b5de65b40cf0a4a0e5fccb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_aarch64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='dee6b87258ceba918543956dddf97291cbc2735ffa0288d25239a07c7766d567';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_ppc64le_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ffda41aa8390d14edbce1775d652f0e4e779df025ac1404c1970802697963aab';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_x64_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        s390x)          ESUM='ee08d6830990562fcc45bec336748390d15357028d3ca0cf4a78bcea7bdfaefe';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.7%2B7_openj9-0.38.0/ibm-semeru-open-jre_s390x_linux_17.0.7_7_openj9-0.38.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 16 Aug 2023 09:29:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 09:29:09 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 16 Aug 2023 09:29:43 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 16 Aug 2023 17:46:09 GMT
USER root
# Wed, 16 Aug 2023 17:46:09 GMT
ARG LIBERTY_VERSION=23.0.0.8-beta
# Wed, 16 Aug 2023 17:46:09 GMT
ARG LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4
# Wed, 16 Aug 2023 17:46:09 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip
# Wed, 16 Aug 2023 17:46:10 GMT
ARG LIBERTY_BUILD_LABEL=cl230720230710-1201
# Wed, 16 Aug 2023 17:46:10 GMT
ARG OPENJ9_SCC=true
# Wed, 16 Aug 2023 17:46:10 GMT
ARG VERBOSE=false
# Wed, 16 Aug 2023 17:46:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230720230710-1201 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=23.0.0.8-beta
# Wed, 16 Aug 2023 17:46:10 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 16 Aug 2023 17:46:10 GMT
COPY dir:0c9b294d41044aadfdfa715e426d188c2e110fe670ffece13814d3dccfec754e in /opt/ol/helpers 
# Wed, 16 Aug 2023 17:46:10 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 16 Aug 2023 17:46:11 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 16 Aug 2023 17:46:31 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 16 Aug 2023 17:46:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 16 Aug 2023 17:46:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 16 Aug 2023 17:46:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 16 Aug 2023 17:46:59 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230720230710-1201 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.8-beta/openliberty-runtime-23.0.0.8-beta.zip LIBERTY_SHA=7bd9ae608dec65669dde34c56d93cee4b964cda4 LIBERTY_VERSION=23.0.0.8-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 16 Aug 2023 17:47:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 16 Aug 2023 17:47:00 GMT
USER 1001
# Wed, 16 Aug 2023 17:47:00 GMT
EXPOSE 9080 9443
# Wed, 16 Aug 2023 17:47:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 16 Aug 2023 17:47:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:de1d106061fc0332ca262e39ed7d2aa6384ae341a084b39449e21c742802df9c`  
		Last Modified: Wed, 16 Aug 2023 04:39:02 GMT  
		Size: 28.6 MB (28644373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33878ed31a5f2ae2ce7e393a139a1e3266bdd76a60af22203b6d4fcd73343dd7`  
		Last Modified: Wed, 16 Aug 2023 09:33:07 GMT  
		Size: 12.2 MB (12199840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a7c2636dc28310a3cedbcb73121064687568aef15bdba057a998869dbc4f6d`  
		Last Modified: Wed, 16 Aug 2023 09:34:45 GMT  
		Size: 47.6 MB (47567688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e629a3d024cac4080091fec593dacfc526207622578c53fca2c9e7b7c7e61b0a`  
		Last Modified: Wed, 16 Aug 2023 09:34:39 GMT  
		Size: 5.0 MB (4953592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7057bc3b7680c0d052b7547bf9cab5a2eba7bd713f8cee961913df47dc739a`  
		Last Modified: Wed, 16 Aug 2023 17:54:51 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d09745bbb95ee5e29cdd959289b4257cab450ccb0cd8fe569abf263bd4ed5e`  
		Last Modified: Wed, 16 Aug 2023 17:54:51 GMT  
		Size: 9.2 KB (9221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e56892f767c80442cf5e81c3fed61f662eb0ff08277c28f7ff5bc1e954d605`  
		Last Modified: Wed, 16 Aug 2023 17:54:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a9b00e4f5fa37e98a381685c15362208420b8949bd5fef12b0cf34ae1b46cb`  
		Last Modified: Wed, 16 Aug 2023 17:54:49 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e6c1968988cc0f54a2aa90db40bae9d08dd5d9e09dbd593913b4bba75629a2`  
		Last Modified: Wed, 16 Aug 2023 17:55:05 GMT  
		Size: 361.1 MB (361102820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ddf734ecef3abcca112a7be513bc699135c3c82ea1124ba590da44dd07f95f`  
		Last Modified: Wed, 16 Aug 2023 17:54:50 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ecebf71d7d41c48e1a46573eb41c4517db64c7a0674d849f595793ab2471d5`  
		Last Modified: Wed, 16 Aug 2023 17:54:50 GMT  
		Size: 10.7 KB (10688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3550d38322b712e8740c7db79366d4a5b9175c71642de862579fe937b73a22`  
		Last Modified: Wed, 16 Aug 2023 17:54:51 GMT  
		Size: 12.6 MB (12602698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
