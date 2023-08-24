## `open-liberty:kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:69e6cdf583737faa7c377adddf479862231d35251fb78cc632d05df528d86266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:68cf32c9cc87237173a4fdfcb73f272f1be2ce30b3a0dd47e04bd8f4bb1a4290
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113933172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241549004527a1f4fd6bc6d72cf195f6d3a2d9efac268058aa7c97a6ecd0fcb1`
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
# Wed, 23 Aug 2023 20:38:29 GMT
ENV JAVA_VERSION=jdk8u382-b05_openj9-0.40.0
# Wed, 23 Aug 2023 20:41:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='8ec1bda269e5c9fa273e7a66339dd6f8ad275e1698280757e1c8c7c88042a169';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_aarch64_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='506a02193548ac410294ec33b8bf0b10be727708820f72d3c01b726c109241e9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_ppc64le_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ccfb3e4e261830ba1f3f485c4b5e0a05731b3c83d338dca17fe3b382fa2bdaff';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_x64_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        s390x)          ESUM='da32fea00275c0462e32becced06ffab8e2259640acd448c1a1663cfca442cb5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_s390x_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 23 Aug 2023 20:41:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 20:41:00 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Aug 2023 20:41:35 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 23 Aug 2023 22:54:54 GMT
USER root
# Wed, 23 Aug 2023 23:44:07 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:44:08 GMT
ARG LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a
# Wed, 23 Aug 2023 23:44:08 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip
# Wed, 23 Aug 2023 23:44:08 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:44:08 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:44:08 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:44:08 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:44:08 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:44:08 GMT
COPY dir:a51a46b81cfa5e03910d4f938a784aacd5cb102fab83ec37bb694f14e7486355 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:44:08 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:44:09 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:44:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:44:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:44:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:44:18 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:44:22 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:44:22 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:44:22 GMT
USER 1001
# Wed, 23 Aug 2023 23:44:22 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:44:22 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:44:22 GMT
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
	-	`sha256:65bad2966a634351e7dbc2bc590ff1ce3573244247aba6c52f89b29053103659`  
		Last Modified: Wed, 23 Aug 2023 21:01:10 GMT  
		Size: 50.3 MB (50327476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea318766a2a89608a4d1fc48d7e11b762fa00597b219fbe3a9a21e8598b43c0`  
		Last Modified: Wed, 23 Aug 2023 21:01:05 GMT  
		Size: 4.2 MB (4184017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a554c0ddecbeabfd000fe04dfeb075b9c2d72312e44444accdac01acc0dae8`  
		Last Modified: Wed, 23 Aug 2023 23:49:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4355b845cfc3e63f23f3056c237f6c2a9c08c3ec30f4abe2584e65d27fb5ced4`  
		Last Modified: Wed, 23 Aug 2023 23:49:45 GMT  
		Size: 8.9 KB (8940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f1ae3807955131162343b15ed066ba671e2bb74ed1f5c76cc028545387a89d`  
		Last Modified: Wed, 23 Aug 2023 23:49:45 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b71bff03978d4f6f24c02664671c6a04d83235f48f94715c061ebded736ccc`  
		Last Modified: Wed, 23 Aug 2023 23:49:44 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a052b5796208cbee797ac4047751d4d423ec90c31140f342312e8768dbdf23d0`  
		Last Modified: Wed, 23 Aug 2023 23:49:45 GMT  
		Size: 14.2 MB (14218477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3dc8f72baa5d10b999175e5681e98af7febc563f346ae026b5dcdedd508ba0`  
		Last Modified: Wed, 23 Aug 2023 23:49:44 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014af60310ec88befde081754765563c93d05e0e3b403ba5ab62ecd62152f6ed`  
		Last Modified: Wed, 23 Aug 2023 23:49:44 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cca5ec05baab8e7776d8934626ee01d226cba038de25658e077df6cbf88615a`  
		Last Modified: Wed, 23 Aug 2023 23:49:44 GMT  
		Size: 2.6 MB (2556476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:259b0829809596d00e2d52463099f4425f796de3403a082cb1537d5ac0aa5221
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109904958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185f45b9fc23fe4388d0829f7764114482efb7316ef4f326920cdd27ce9ae514`
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
# Wed, 23 Aug 2023 19:54:26 GMT
ENV JAVA_VERSION=jdk8u382-b05_openj9-0.40.0
# Wed, 23 Aug 2023 19:57:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='8ec1bda269e5c9fa273e7a66339dd6f8ad275e1698280757e1c8c7c88042a169';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_aarch64_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='506a02193548ac410294ec33b8bf0b10be727708820f72d3c01b726c109241e9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_ppc64le_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ccfb3e4e261830ba1f3f485c4b5e0a05731b3c83d338dca17fe3b382fa2bdaff';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_x64_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        s390x)          ESUM='da32fea00275c0462e32becced06ffab8e2259640acd448c1a1663cfca442cb5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_s390x_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 23 Aug 2023 19:57:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 19:57:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Aug 2023 19:57:46 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 23 Aug 2023 21:24:15 GMT
USER root
# Wed, 23 Aug 2023 23:57:06 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:57:06 GMT
ARG LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a
# Wed, 23 Aug 2023 23:57:06 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip
# Wed, 23 Aug 2023 23:57:06 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:57:06 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:57:06 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:57:06 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:57:06 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:57:06 GMT
COPY dir:a51a46b81cfa5e03910d4f938a784aacd5cb102fab83ec37bb694f14e7486355 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:57:06 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:57:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:57:13 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:57:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:57:14 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:57:14 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:57:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:57:19 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:57:19 GMT
USER 1001
# Wed, 23 Aug 2023 23:57:19 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:57:19 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:57:19 GMT
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
	-	`sha256:a37f34e5be858e41da87a910b5e03fe65c2905ca1184db27fa290434b2ce256f`  
		Last Modified: Wed, 23 Aug 2023 20:17:03 GMT  
		Size: 48.5 MB (48489166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c6df7feaeede73e8755afa12ec8f400257ac8a7fbed1bbe55020700f4bc6c2`  
		Last Modified: Wed, 23 Aug 2023 20:16:59 GMT  
		Size: 4.0 MB (4031765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d3f841417e73577988d219e61a3169514d72b1208f44713eab98e697cca359`  
		Last Modified: Thu, 24 Aug 2023 00:01:58 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372ce51e6b58bb4954a8a0207eac724360ffc38b4baf392cfbac233f19a97f32`  
		Last Modified: Thu, 24 Aug 2023 00:01:57 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece2a6d6c58837536557201ec4494ff4881c315e1c0a521288c826b11e04d082`  
		Last Modified: Thu, 24 Aug 2023 00:01:57 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce2b6e6f4ed2bce85464f5d89974ae6d2cf8c6f54329b1f2888cc96bba71e66`  
		Last Modified: Thu, 24 Aug 2023 00:01:55 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e17886d4ea3bb8ae81b8480f46061f14f75f6880367cb147f1db42a17275d0`  
		Last Modified: Thu, 24 Aug 2023 00:01:56 GMT  
		Size: 14.2 MB (14219329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47211c56ceabf780b7dedf1e28f15aa7a96ca623d55f5daa78d10333367bd632`  
		Last Modified: Thu, 24 Aug 2023 00:01:55 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b06360be452106bd77d74c53048ce1a5b62073a0d092069f3caef2eb439aa`  
		Last Modified: Thu, 24 Aug 2023 00:01:58 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0681606f2017dbeeccb2c2ad3fa5df609e9ff8004b2258ca7c52ef7dd265e5`  
		Last Modified: Thu, 24 Aug 2023 00:01:56 GMT  
		Size: 2.6 MB (2595859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:ea29da8f021d1bda1124dcc64bc38168104c4f41122edee8dc0767fff87f4298
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119808529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77912baa9cd9632cc2636eb09da9d052ee97540ba821dae8c188ce9b8c9e9196`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 07:53:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Aug 2023 07:53:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Aug 2023 20:17:50 GMT
ENV JAVA_VERSION=jdk8u382-b05_openj9-0.40.0
# Wed, 23 Aug 2023 20:20:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='8ec1bda269e5c9fa273e7a66339dd6f8ad275e1698280757e1c8c7c88042a169';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_aarch64_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='506a02193548ac410294ec33b8bf0b10be727708820f72d3c01b726c109241e9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_ppc64le_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ccfb3e4e261830ba1f3f485c4b5e0a05731b3c83d338dca17fe3b382fa2bdaff';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_x64_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        s390x)          ESUM='da32fea00275c0462e32becced06ffab8e2259640acd448c1a1663cfca442cb5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_s390x_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 23 Aug 2023 20:20:58 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 20:20:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Aug 2023 20:21:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 23 Aug 2023 21:12:40 GMT
USER root
# Wed, 23 Aug 2023 23:46:02 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:46:02 GMT
ARG LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a
# Wed, 23 Aug 2023 23:46:03 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip
# Wed, 23 Aug 2023 23:46:04 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:46:04 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:46:05 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:46:05 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:46:05 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:46:06 GMT
COPY dir:a51a46b81cfa5e03910d4f938a784aacd5cb102fab83ec37bb694f14e7486355 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:46:06 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:46:09 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:46:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:46:28 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:46:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:46:39 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:46:39 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:46:40 GMT
USER 1001
# Wed, 23 Aug 2023 23:46:40 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:46:41 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:46:41 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:09f4821f68917c7929419fff8bc583c406640180ea7d58eea03a95e463b8fb21`  
		Last Modified: Wed, 16 Aug 2023 02:15:01 GMT  
		Size: 35.7 MB (35712693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e0b5ceb7dfda582574a06a918e899d7d9019dd9005b084e06b6d57c5a53131`  
		Last Modified: Thu, 17 Aug 2023 08:04:07 GMT  
		Size: 12.9 MB (12895032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5101c5171272a8ea17512f02abbe9ebc6257f4fdc192860e0290962a2f65e243`  
		Last Modified: Wed, 23 Aug 2023 20:45:55 GMT  
		Size: 50.8 MB (50806417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7e71092b91a0e33854df21a2e9603ac34c70cd189245a0b35ef081f93afc55`  
		Last Modified: Wed, 23 Aug 2023 20:45:46 GMT  
		Size: 3.6 MB (3558466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e1c189c3fb916706883134830578ecbfbe0f82e1504daa4f957b239b42ce67`  
		Last Modified: Wed, 23 Aug 2023 23:57:27 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8749d14d63452cfc7876c3d08438e58e5b2708ece4aeca8a95e3b38b74e9a766`  
		Last Modified: Wed, 23 Aug 2023 23:57:27 GMT  
		Size: 8.9 KB (8939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cceebed5d93a63191d4d25c24529e4dbb6feb2c9cd47d166e43cf4b56838d18`  
		Last Modified: Wed, 23 Aug 2023 23:57:27 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c822e4f44ed6b83e0bac30e0e142e8068a6df6ad53e3300440ffe17f1973c5`  
		Last Modified: Wed, 23 Aug 2023 23:57:25 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7208fd68c36fb39efff5c597945ea21be093774601fc8f324ae666f48ea7278`  
		Last Modified: Wed, 23 Aug 2023 23:57:26 GMT  
		Size: 14.2 MB (14218909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ce8de62e61e205764975b4b723ee19e0c67573ce0c02ba84465badc4ac2ce0`  
		Last Modified: Wed, 23 Aug 2023 23:57:25 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be530a65a3881171214e1b9314fa44c2390c0e34da470c17b42e69397e9d4ab`  
		Last Modified: Wed, 23 Aug 2023 23:57:25 GMT  
		Size: 10.0 KB (10040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa398c07553e9d34ef99598428a1bbedcb57c3506c4fde37a5e52a129b8c495`  
		Last Modified: Wed, 23 Aug 2023 23:57:25 GMT  
		Size: 2.6 MB (2559322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:8cb46aef81de627a8822402298ffed4a223eae5dab801ecab69498f95608c9b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112281752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654e0132bd2c1571e8279c6d19c3eee097e4d978b7c5a31b9808744d08f6809d`
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
# Wed, 23 Aug 2023 19:58:41 GMT
ENV JAVA_VERSION=jdk8u382-b05_openj9-0.40.0
# Wed, 23 Aug 2023 20:00:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='8ec1bda269e5c9fa273e7a66339dd6f8ad275e1698280757e1c8c7c88042a169';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_aarch64_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='506a02193548ac410294ec33b8bf0b10be727708820f72d3c01b726c109241e9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_ppc64le_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        amd64|x86_64)          ESUM='ccfb3e4e261830ba1f3f485c4b5e0a05731b3c83d338dca17fe3b382fa2bdaff';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_x64_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        s390x)          ESUM='da32fea00275c0462e32becced06ffab8e2259640acd448c1a1663cfca442cb5';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u382-b05_openj9-0.40.0/ibm-semeru-open-jre_s390x_linux_8u382b05_openj9-0.40.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 23 Aug 2023 20:00:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Aug 2023 20:00:27 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 23 Aug 2023 20:01:05 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 23 Aug 2023 21:36:36 GMT
USER root
# Wed, 23 Aug 2023 23:46:07 GMT
ARG LIBERTY_VERSION=23.0.0.8
# Wed, 23 Aug 2023 23:46:07 GMT
ARG LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a
# Wed, 23 Aug 2023 23:46:07 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip
# Wed, 23 Aug 2023 23:46:07 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:46:07 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:46:07 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:46:08 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:46:08 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:46:08 GMT
COPY dir:a51a46b81cfa5e03910d4f938a784aacd5cb102fab83ec37bb694f14e7486355 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:46:08 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:46:09 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:46:14 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:46:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:46:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:46:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:46:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/23.0.0.8/openliberty-kernel-23.0.0.8.zip LIBERTY_SHA=5c8becbc9e0c96b8413e0113bf86b40af140201a LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:46:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:46:20 GMT
USER 1001
# Wed, 23 Aug 2023 23:46:20 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:46:20 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:46:20 GMT
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
	-	`sha256:a4d3e1a69ebdc88234b176def9ed78fd2afa8d2255ff353b4b65b6aa13f762e2`  
		Last Modified: Wed, 23 Aug 2023 20:13:38 GMT  
		Size: 50.2 MB (50218454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7c940477f972d07f95ccac5913f01b53f8b1b1e14692a9f31ad46f8d02f1b7`  
		Last Modified: Wed, 23 Aug 2023 20:13:33 GMT  
		Size: 4.3 MB (4311106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c368bfb349862a4df48a4a76e973a401c7e1b048d0760e0e2e993f631ffcf20`  
		Last Modified: Wed, 23 Aug 2023 23:53:30 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bd0f9dc6b4968b54b2086d363705e376afbf38d820f8448983f7beda08df01`  
		Last Modified: Wed, 23 Aug 2023 23:53:30 GMT  
		Size: 8.9 KB (8937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca830e7fbccb165aa0ace158b8a33e4691861315a028be62e42d7810b6bf1ee`  
		Last Modified: Wed, 23 Aug 2023 23:53:30 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7443cdfe983c208af8c5cf231d14b077988f763b072a481ba0fd1d2e2e1e959c`  
		Last Modified: Wed, 23 Aug 2023 23:53:29 GMT  
		Size: 33.1 KB (33114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c522368a42682b4cdfcc9e9b22255907c06a7bad30f8c436aec70007311a161`  
		Last Modified: Wed, 23 Aug 2023 23:53:30 GMT  
		Size: 14.2 MB (14218541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a1ad6f00cd8019ad6b9d2c69bab8ce63c23bacbf00511dc4f3333e27a0f8c`  
		Last Modified: Wed, 23 Aug 2023 23:53:29 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25a04e6fe9247276c3c5a70b313a63b1cc46d292fa1ef606c43ac6260a80840`  
		Last Modified: Wed, 23 Aug 2023 23:53:29 GMT  
		Size: 10.0 KB (10017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2f60bd249e10c7824a1f7ba791392d01b6323954432d5afef6164806b8e2a2`  
		Last Modified: Wed, 23 Aug 2023 23:53:29 GMT  
		Size: 2.6 MB (2635165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
