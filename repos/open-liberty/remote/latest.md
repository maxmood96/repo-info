## `open-liberty:latest`

```console
$ docker pull open-liberty@sha256:61fbaa547c498d456469cbd5e5b4bcac58fec5378b8a7d6e9c0f5ffac34ad127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:latest` - linux; amd64

```console
$ docker pull open-liberty@sha256:43e3b28043879f046d0c9814d71b3a2494f6321658cb35e9c950f3712023bb28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428523787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7f3499f18613b9513c27a7d713170b0ffb01e241b875bfa315129f58c4c6e6`
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
# Wed, 23 Aug 2023 23:45:09 GMT
ARG LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f
# Wed, 23 Aug 2023 23:45:09 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip
# Wed, 23 Aug 2023 23:45:09 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:45:09 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:45:09 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:45:09 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:45:09 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:45:09 GMT
COPY dir:d1e0aedd7e0c7189fe544a9d4e41542551f8aabdfbf96c4604a6d4c4af871d38 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:45:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:45:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:45:24 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:45:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:45:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:45:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:45:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:45:48 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:45:48 GMT
USER 1001
# Wed, 23 Aug 2023 23:45:48 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:45:48 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:45:48 GMT
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
	-	`sha256:33310168a9d52a51161c1494ad0f72622137af68d4bbb9ff9822af310a9b8f97`  
		Last Modified: Wed, 23 Aug 2023 23:50:11 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20cc20a75c71f4965c95eb1c82a2b12fe77174a11c9e0f61b2c2fe29dddd495`  
		Last Modified: Wed, 23 Aug 2023 23:50:11 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a154b5278f76dc819e8d798869f94ba2f8fc7752eb82a0ed30e0eb0220ad82`  
		Last Modified: Wed, 23 Aug 2023 23:50:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd146b4dba61ba760020d7a7df3c698bc1ee280885e12aa95faf6932438c48e`  
		Last Modified: Wed, 23 Aug 2023 23:50:09 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f2431b9f2f159a399bf0ed6c2ff67ee962a939b1900e6cc456ae630775a299`  
		Last Modified: Wed, 23 Aug 2023 23:50:26 GMT  
		Size: 319.1 MB (319067869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032006fe30f5ba178e9b1c815c374cb326adecc352444c7117d1f2089ae6ab5b`  
		Last Modified: Wed, 23 Aug 2023 23:50:09 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606e94d414c6ff2d51590842a5b07a74d895c8d2700d792479497080a6430179`  
		Last Modified: Wed, 23 Aug 2023 23:50:09 GMT  
		Size: 10.8 KB (10850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df109cf125cd72ed516e0fc1cb3cf553536a49f183bcc8a1b703d32305f409`  
		Last Modified: Wed, 23 Aug 2023 23:50:11 GMT  
		Size: 12.3 MB (12296103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:latest` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:4c0a13dbaf62df50340e0b6449cac9ffaedf274ee788b0cd5cd105d671017c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423956898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1f96bd84b92baf0c48a7d92ed3126eba8e5b67f7148a23026cd793f4d59e2c`
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
# Wed, 23 Aug 2023 23:57:55 GMT
ARG LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f
# Wed, 23 Aug 2023 23:57:55 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip
# Wed, 23 Aug 2023 23:57:55 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:57:55 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:57:55 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:57:55 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:57:55 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:57:55 GMT
COPY dir:d1e0aedd7e0c7189fe544a9d4e41542551f8aabdfbf96c4604a6d4c4af871d38 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:57:55 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:57:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:58:09 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:58:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:58:12 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:58:13 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:58:31 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:58:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:58:32 GMT
USER 1001
# Wed, 23 Aug 2023 23:58:32 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:58:32 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:58:32 GMT
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
	-	`sha256:05782a38c47920bc69e1aff61290409ff0812d8181c64f67f4c252f86090aaf5`  
		Last Modified: Thu, 24 Aug 2023 00:02:24 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c3524142bb0cda7c88cd6b6615d110375578b695e9cfa7abf1b3971a9ca36f`  
		Last Modified: Thu, 24 Aug 2023 00:02:24 GMT  
		Size: 9.4 KB (9394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2761c46428a490f94a801b65e4bc417fb7f34bc920c69969eadb7b78d60b1960`  
		Last Modified: Thu, 24 Aug 2023 00:02:24 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce3d298106bc4689c70d68e3cc32c31af16f320fe82d5e507c9c5175d374427`  
		Last Modified: Thu, 24 Aug 2023 00:02:22 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0124c8bfe5280a4ce664ceefb5176fbe8abc0cd7ca3f7a136ff80bc965c61fff`  
		Last Modified: Thu, 24 Aug 2023 00:02:37 GMT  
		Size: 319.1 MB (319069428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d6a71ff1936894bc3823c6b3371cbdebfeae36840abb7140f19071b3b7942c`  
		Last Modified: Thu, 24 Aug 2023 00:02:22 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8134881295b9461098aa6f66d99d90a81d4b21552f4794d0f75fb3a1d3799cba`  
		Last Modified: Thu, 24 Aug 2023 00:02:22 GMT  
		Size: 10.9 KB (10862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a69e546be586a40a7668472e0b944224a1b8a0573280a16959619e162051398`  
		Last Modified: Thu, 24 Aug 2023 00:02:23 GMT  
		Size: 11.8 MB (11796073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:latest` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:637c8d52daa0a1268552356a90e7b1bb818a38929b762661caf309eeffb509ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.2 MB (433194624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253e38448e88b5086f3d8529c49751f02f7cbf065003f8ed2d8d9a4bf2450978`
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
# Wed, 23 Aug 2023 23:48:39 GMT
ARG LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f
# Wed, 23 Aug 2023 23:48:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip
# Wed, 23 Aug 2023 23:48:40 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:48:40 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:48:41 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:48:42 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:48:42 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:48:42 GMT
COPY dir:d1e0aedd7e0c7189fe544a9d4e41542551f8aabdfbf96c4604a6d4c4af871d38 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:48:43 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:48:46 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:49:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:49:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:49:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:49:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:50:25 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:50:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:50:27 GMT
USER 1001
# Wed, 23 Aug 2023 23:50:28 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:50:28 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:50:28 GMT
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
	-	`sha256:b37c05b0fe31f8501ac92d0047436382931e1ad78e65e16ee3808a40a51122a4`  
		Last Modified: Wed, 23 Aug 2023 23:58:02 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d4bd55cd65d03b0e7e10030b18d2fab608bc3e52f92507e33c0089b3ce8b90`  
		Last Modified: Wed, 23 Aug 2023 23:58:02 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb5510f5be12096f3923830f5322c37b857436a9e026363bf249e7e2e710383`  
		Last Modified: Wed, 23 Aug 2023 23:58:01 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb0501f3b85e409765bfbc7fa15fca946125d1a4a5dcb17af8edc27c5c1e28c`  
		Last Modified: Wed, 23 Aug 2023 23:57:59 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453d02ce50f7af4721144f45dc2fc199192fca4b66df0f606cacbc4f7aa7cfc`  
		Last Modified: Wed, 23 Aug 2023 23:58:25 GMT  
		Size: 319.1 MB (319068532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b27f6fd0d8b28635b720ef0b83fadd700546c09532394998728cb7ad64fa368`  
		Last Modified: Wed, 23 Aug 2023 23:57:59 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76747c66eed212c7321d4d68c333a96807f689a21d341b5fabc2be5d8a3ffa16`  
		Last Modified: Wed, 23 Aug 2023 23:57:59 GMT  
		Size: 10.9 KB (10878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bc1fe1518795b8b0cde9bc02dd6e32e8a583ca331b24e3d4485e9c965039e1`  
		Last Modified: Wed, 23 Aug 2023 23:58:02 GMT  
		Size: 11.1 MB (11094169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:latest` - linux; s390x

```console
$ docker pull open-liberty@sha256:7b2f34effb0d4c0e353f3ba7de2b3e7d60680ef057d01e228d0fc7672436b282
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.8 MB (426813648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffa4632959b24ae32ec42ef6124d8e33c74e5404975ca98be04001f708ad89e`
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
# Wed, 23 Aug 2023 23:47:07 GMT
ARG LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f
# Wed, 23 Aug 2023 23:47:07 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip
# Wed, 23 Aug 2023 23:47:07 GMT
ARG LIBERTY_BUILD_LABEL=cl230820230807-0401
# Wed, 23 Aug 2023 23:47:07 GMT
ARG OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:47:07 GMT
ARG VERBOSE=false
# Wed, 23 Aug 2023 23:47:07 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl230820230807-0401 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=23.0.0.8
# Wed, 23 Aug 2023 23:47:07 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Wed, 23 Aug 2023 23:47:08 GMT
COPY dir:d1e0aedd7e0c7189fe544a9d4e41542551f8aabdfbf96c4604a6d4c4af871d38 in /opt/ol/helpers 
# Wed, 23 Aug 2023 23:47:08 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Wed, 23 Aug 2023 23:47:08 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Wed, 23 Aug 2023 23:47:29 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Wed, 23 Aug 2023 23:47:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 23 Aug 2023 23:47:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Wed, 23 Aug 2023 23:47:38 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Wed, 23 Aug 2023 23:47:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl230820230807-0401 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/23.0.0.8/openliberty-runtime-23.0.0.8.zip LIBERTY_SHA=857c7878a03110fc019c91f3357d7d2ea6e8720f LIBERTY_VERSION=23.0.0.8 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Wed, 23 Aug 2023 23:47:58 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 23 Aug 2023 23:47:58 GMT
USER 1001
# Wed, 23 Aug 2023 23:47:58 GMT
EXPOSE 9080 9443
# Wed, 23 Aug 2023 23:47:58 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 23 Aug 2023 23:47:58 GMT
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
	-	`sha256:d85181c65dbba16c9aafc2da244c2a055b77b9c8a7863f25396cc8229de6f33f`  
		Last Modified: Wed, 23 Aug 2023 23:53:45 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ec3ecad3b91462f880655499231a878fa098b19e26d78a7debdbc3129f4209`  
		Last Modified: Wed, 23 Aug 2023 23:53:45 GMT  
		Size: 9.4 KB (9393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe74eb43541be09c49febea2a8e52dc9e81eb3450037d597d975c6f22f052178`  
		Last Modified: Wed, 23 Aug 2023 23:53:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bf042ba13fcfe65d5346e671ac8ab107ef59b8ab9252f815c835626d11f7cf`  
		Last Modified: Wed, 23 Aug 2023 23:53:44 GMT  
		Size: 33.1 KB (33115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11285859d065c3f736f52d3de9566c2ed81d42073b8db456925d607dc616a989`  
		Last Modified: Wed, 23 Aug 2023 23:53:58 GMT  
		Size: 319.1 MB (319068073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37100a460731431f573ab1b9d8b123eb9a692b9147e0dbcc97d42c66abddfb0`  
		Last Modified: Wed, 23 Aug 2023 23:53:44 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e1e03be44005b7828b94d0abaa39f03ca17a2a68a766d00e1fba02539a341e`  
		Last Modified: Wed, 23 Aug 2023 23:53:44 GMT  
		Size: 10.9 KB (10857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7a0680df4d150d70a02ea576615fb0e469e49d617eae833a316d1436c5a3cb`  
		Last Modified: Wed, 23 Aug 2023 23:53:46 GMT  
		Size: 12.3 MB (12315911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
