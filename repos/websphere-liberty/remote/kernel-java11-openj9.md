## `websphere-liberty:kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:aa559af613b5016b60295f3b1ebf6e5114b9786a87e27d1977cae37f22b067c2
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
$ docker pull websphere-liberty@sha256:058bc268d64a5d469cbfe3981fd1db0b66a2c20541cc9542b4855d3588302c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118731667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13939c728a6cd2cd010b5b98088cf519ec67f27c7a79a9b675d942f8e61f5254`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 06 Nov 2024 14:57:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Nov 2024 14:57:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV JAVA_VERSION=jdk-11.0.25+9_openj9-0.48.0
# Wed, 06 Nov 2024 14:57:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ebe7dc3fc6d7a0145d8834d01ca5adda19c1812af9a4f63655bc4de463377b6';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_aarch64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='451c6da5d286af654d857c2383698c19e9f05070b8e018f73f82ab1df1c51ba3';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_ppc64le_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7d8407bbc68303e84615d1981abbdda690236edfcff5535789dc7915a3c4f629';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_x64_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        s390x)          ESUM='28c3adeefd79d0054cd8f5b5de0a95277ae19a53e1f503a15d4955c38a9e715d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.25%2B9_openj9-0.48.0/ibm-semeru-open-jre_s390x_linux_11.0.25_9_openj9-0.48.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Nov 2024 14:57:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Nov 2024 14:57:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.97/bin/apache-tomcat-9.0.97.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
USER root
# Wed, 06 Nov 2024 14:57:10 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_VERSION=24.0.0.11
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.11 org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 Nov 2024 14:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.11 BuildLabel=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_URL
# Wed, 06 Nov 2024 14:57:10 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:57:10 GMT
USER 1001
# Wed, 06 Nov 2024 14:57:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:57:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:57:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4199c8f2c5e2b0ae278966cfde14054e3ccd8774336763b3dd3def4309563`  
		Last Modified: Mon, 18 Nov 2024 19:05:55 GMT  
		Size: 12.2 MB (12175004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc2d2ffb2a260cd5dac60f3d3e71903937560fb78710bc70a17a827638d5b4c`  
		Last Modified: Mon, 18 Nov 2024 19:05:56 GMT  
		Size: 52.3 MB (52287848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c93bba8d2ba60bc13741b1c6380d8815dae95eb87f71e4bb537e02ab485dde`  
		Last Modified: Mon, 18 Nov 2024 19:05:55 GMT  
		Size: 4.4 MB (4447330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31342b6597a28be5946a862dad9c98b699cfa8c41c2d97c9421f3ee7c81ebb3a`  
		Last Modified: Mon, 18 Nov 2024 20:08:03 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8259eddd9d28aa30887ccf368a119cf3bb244e67b9c900e471fcd4eca0f228ec`  
		Last Modified: Mon, 18 Nov 2024 20:08:03 GMT  
		Size: 17.4 MB (17435276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9d53c9e890270aeb423bd773117191fa25a17f91eb5a9a95e5f12a0324e2ac`  
		Last Modified: Mon, 18 Nov 2024 20:08:03 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5e5693246c864404a4306db50958fdd22918e08947d0c6e508f3829b1133f4`  
		Last Modified: Mon, 18 Nov 2024 20:08:03 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfab7065fbadbdcf9eea4d377c69bcc8c305c3406f370d1995703c77c33eb7f7`  
		Last Modified: Mon, 18 Nov 2024 20:08:03 GMT  
		Size: 11.8 KB (11832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11248874d9d188c37f4225d5da05d5dd831290d60a1caf53dd20a908e7bf00b0`  
		Last Modified: Mon, 18 Nov 2024 20:08:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228ed2ea54658c953ff6ed4810dc0dd8e4b59064c597351797bb4a289a1820f0`  
		Last Modified: Mon, 18 Nov 2024 20:08:03 GMT  
		Size: 12.6 KB (12630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d1ef58e29c4176d7a034df7911f3f3fa58fafed359a3e3802ba7da9e3cdf43`  
		Last Modified: Mon, 18 Nov 2024 20:08:05 GMT  
		Size: 2.8 MB (2792067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:2aa8abd632ab96b5ac20f0a652957beee9da6b37cf940c1ee1d59b16b5e08eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d538ebb21dedad8741524591d740e7688eb9d0583b5ae365b11a2a802a61962f`

```dockerfile
```

-	Layers:
	-	`sha256:7cf810613f41d2f33bcd2856f0feff610958b0af48ac23f54494102d63b9ff14`  
		Last Modified: Mon, 18 Nov 2024 20:08:03 GMT  
		Size: 3.7 MB (3740265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f699a37ecf4cb50e71d410daa40c7866e7133c17a8d5a963594a027863419c3e`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 40.0 KB (39993 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull websphere-liberty@sha256:e21d8a1b8604bb3c5c1370ee6fd3be3baef7a135b17ae47380d35e0dd11ad38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112372100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b362d0e9c8e9a7842ab307f0562b3cfbd6bab2cb80a2c44e011b587118a41911`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='010e099a8e6ff4f4ed1de40dfb536b59a5a3aaddeeaae38c1f4715e6a31ae462';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='31151d3e19e58a1a2ac332e4b940009c997d6cb3cb6cb36ae80250ade6ef4e32';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='34ebbf10575043cc0c00b56115f2f5b58d3b05ec662e9a7a6ce5fa55d56d290a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='13f732437f51869a127beb2e2b2af6fdfcd2da43a38f8dc0fd377568ea679ff4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
USER root
# Wed, 06 Nov 2024 14:57:10 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_VERSION=24.0.0.11
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.11 org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 Nov 2024 14:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.11 BuildLabel=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_URL
# Wed, 06 Nov 2024 14:57:10 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:57:10 GMT
USER 1001
# Wed, 06 Nov 2024 14:57:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:57:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:57:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8db97a9b46a080a285ae7eb265ed5e64db7de26df73e85dcb3512fae3446d`  
		Last Modified: Mon, 04 Nov 2024 22:08:00 GMT  
		Size: 12.1 MB (12128492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e873822163f2bb8cbcc8caf0f990a8fe909824812433edbff0c5ba377c77a5fd`  
		Last Modified: Mon, 04 Nov 2024 22:15:31 GMT  
		Size: 48.4 MB (48417750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3210c7c8921573ce6d00998fc7723962221f97b37d3e534aa688144045136dbe`  
		Last Modified: Mon, 04 Nov 2024 22:15:30 GMT  
		Size: 4.2 MB (4179588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0333e02250dd5ab726b7030fcff6d02144bdb9b099bfd4610d84f82e33125747`  
		Last Modified: Wed, 06 Nov 2024 20:44:01 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01e700dd3fec27d640c695b71df1f6e221fac70c6e484946bdedd5b04d4a3e1`  
		Last Modified: Wed, 06 Nov 2024 20:44:02 GMT  
		Size: 17.4 MB (17435609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193842f08499f67e8416d06d2980e51b1ec928d80acab13361f6b9d977115752`  
		Last Modified: Wed, 06 Nov 2024 20:44:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f67b7c59fa96239382e828faa870c4b01c44fc2fea8d6fd55d6d0d5231488e`  
		Last Modified: Wed, 06 Nov 2024 20:44:01 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d97f2b06d88bff3077e013f759315774e37ac382b4034f3fb78e04dc3f509d2`  
		Last Modified: Wed, 06 Nov 2024 20:44:02 GMT  
		Size: 11.8 KB (11832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7ea7f0ccf563d1d3f2ca9940335f46e6cdd4707c82096dd8ff6228dda00f65`  
		Last Modified: Wed, 06 Nov 2024 20:44:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f080a79d96d1f53aefafdedb09b99ddc4baf4ff40b13f0ab90f68c5c103c14`  
		Last Modified: Wed, 06 Nov 2024 20:44:02 GMT  
		Size: 12.6 KB (12631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aec06759e7ce8a2bd8fdc89c09e1f5a53cf9979dd5283868a19fbe5cc4129a`  
		Last Modified: Wed, 06 Nov 2024 20:44:04 GMT  
		Size: 2.8 MB (2783296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:dd0183113277b6f0fbd00a5f63e6cd0d428f2636d928a381d189ca3e51c638a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3771876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaa437deec129b6bda55f19666a041ebdd13fbf90595dd53d7111d0678cf537`

```dockerfile
```

-	Layers:
	-	`sha256:8098bb3e2167998aefb8545c16281e72d718c5e0f83b902a82c550afcf325b02`  
		Last Modified: Wed, 06 Nov 2024 20:44:02 GMT  
		Size: 3.7 MB (3731742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f5a4e3d29fe48db9e0423418af228437d2e37161a6ddf80c557dcc023810e9`  
		Last Modified: Wed, 06 Nov 2024 20:44:01 GMT  
		Size: 40.1 KB (40134 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:bd126c1a29d48fd494557a25a3a579817b33b6e0bf45a82d45a2439cdb3d4f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124578910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ed29bcb3f395dc6e1584a262e58ec2dce05edd9394b88530102c79fdd84135`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='010e099a8e6ff4f4ed1de40dfb536b59a5a3aaddeeaae38c1f4715e6a31ae462';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='31151d3e19e58a1a2ac332e4b940009c997d6cb3cb6cb36ae80250ade6ef4e32';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='34ebbf10575043cc0c00b56115f2f5b58d3b05ec662e9a7a6ce5fa55d56d290a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='13f732437f51869a127beb2e2b2af6fdfcd2da43a38f8dc0fd377568ea679ff4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
USER root
# Wed, 06 Nov 2024 14:57:10 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_VERSION=24.0.0.11
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.11 org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 Nov 2024 14:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.11 BuildLabel=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_URL
# Wed, 06 Nov 2024 14:57:10 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:57:10 GMT
USER 1001
# Wed, 06 Nov 2024 14:57:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:57:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:57:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6230a31e14b4a918b32fc7a3b685fad8ecafe0901deee916736d3e6f4db6ad`  
		Last Modified: Tue, 17 Sep 2024 01:15:01 GMT  
		Size: 12.9 MB (12888132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da68ab0979079a8fb75edd7436c7ce50d10f3b1eada2a3bd11271ca1c7f51c95`  
		Last Modified: Mon, 04 Nov 2024 22:17:47 GMT  
		Size: 53.6 MB (53620084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f934c682ba51e33d01b63a5f3ec615a9c01f499550584393f4517a28595dc6a9`  
		Last Modified: Mon, 04 Nov 2024 22:17:46 GMT  
		Size: 3.4 MB (3425960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582f554337385661fce630619bc0ded6e7a41e445e43ca8b289a3bffc8e835cd`  
		Last Modified: Wed, 06 Nov 2024 21:01:05 GMT  
		Size: 36.5 KB (36500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b54b9c6391dbb0e989eef788899a6436eac0429e1e39654cd96a012c60773`  
		Last Modified: Wed, 06 Nov 2024 21:01:06 GMT  
		Size: 17.4 MB (17435854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd0d35ccc2c3164a57fce6a79a4b5d88b4306199dc78f86af5d14677c39cd6`  
		Last Modified: Wed, 06 Nov 2024 21:01:05 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed64231c5e4a6891cc360a8670ac7ecf81f6e6f86e4a1a77d32cb3831b4da3ac`  
		Last Modified: Wed, 06 Nov 2024 21:01:05 GMT  
		Size: 1.5 KB (1519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf1b1885e1dc2aaf6719e4d71587d87e10cca3e216d939b5d5f643995ff29a`  
		Last Modified: Wed, 06 Nov 2024 21:01:06 GMT  
		Size: 11.8 KB (11836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d851ab9d29673081b5803a6480c63c60c1df01c8cfa5515d46e4fab779478b48`  
		Last Modified: Wed, 06 Nov 2024 21:01:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c1cc72165b6da524a9e552ea7b222c5b6698603607c649e6055cf6536a74f`  
		Last Modified: Wed, 06 Nov 2024 21:01:06 GMT  
		Size: 12.6 KB (12642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccc597b046c55606d35292d33e5dee9df4f74b1c0f6485aecacfcce05d948c0`  
		Last Modified: Wed, 06 Nov 2024 21:01:08 GMT  
		Size: 2.7 MB (2697411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:86afce875ddb9951b1b775d3478ce33834f75610bbcb86ca7bde342b9e7e2631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3777040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6a696744bb6f73d82acbba1cc98fb25483558dde61a84244747e9aae935edb`

```dockerfile
```

-	Layers:
	-	`sha256:76f58b64d1bcdd78a607806263f8730c6df948fd9adf555f60689ab1be070aec`  
		Last Modified: Wed, 06 Nov 2024 21:01:06 GMT  
		Size: 3.7 MB (3737006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aec858fa66f147f8581d7cdca73956120a9af0bab707bffc2d517e2d7bef3316`  
		Last Modified: Wed, 06 Nov 2024 21:01:05 GMT  
		Size: 40.0 KB (40034 bytes)  
		MIME: application/vnd.in-toto+json

### `websphere-liberty:kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:c37372f7d179b5b1502d3714e67401fe29918aba0336f20a3ce7529f88007a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116004368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc71b75f3ac7c2af0be51e599bc283b335cc7b9e45e788f6fbba7b1e7eadb92`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Fri, 11 Oct 2024 15:41:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 11 Oct 2024 15:41:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8_openj9-0.46.1
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='010e099a8e6ff4f4ed1de40dfb536b59a5a3aaddeeaae38c1f4715e6a31ae462';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_aarch64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='31151d3e19e58a1a2ac332e4b940009c997d6cb3cb6cb36ae80250ade6ef4e32';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_ppc64le_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        amd64|x86_64)          ESUM='34ebbf10575043cc0c00b56115f2f5b58d3b05ec662e9a7a6ce5fa55d56d290a';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_x64_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        s390x)          ESUM='13f732437f51869a127beb2e2b2af6fdfcd2da43a38f8dc0fd377568ea679ff4';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.24%2B8_openj9-0.46.1/ibm-semeru-open-jre_s390x_linux_11.0.24_8_openj9-0.46.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 15:41:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Oct 2024 15:41:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="ef3ac81debbc3a519c43d1fdb1c88ab26a8052af424d81bceccfbd6e663050a06d7aad7960fd5d11c17849829daebbebf33d92ac1158902283d0e534514aab93";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
USER root
# Wed, 06 Nov 2024 14:57:10 GMT
ARG VERBOSE=false
# Wed, 06 Nov 2024 14:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_VERSION=24.0.0.11
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_BUILD_LABEL=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Thomas Watson, Wendy Raschke, Michal Broz org.opencontainers.image.vendor=IBM org.opencontainers.image.url=https://github.com/WASdev/ci.docker org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=24.0.0.11 org.opencontainers.image.revision=cl241120241021-1102 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://ibm.biz/wl-app-image-template org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 Nov 2024 14:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ibm/wlp/bin:/opt/ibm/helpers/build
# Wed, 06 Nov 2024 14:57:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=24.0.0.11 BuildLabel=cl241120241021-1102
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ARG LIBERTY_URL
# Wed, 06 Nov 2024 14:57:10 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml | grep -E "^\s*kernel:.*${LIBERTY_VERSION}\.zip" | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && cp -a /opt/ibm/wlp/lafiles/. /licenses/     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ibm/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY NOTICES /opt/ibm/NOTICES # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY helpers/ /opt/ibm/helpers/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
COPY fixes/ /opt/ibm/fixes/ # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm/wlp /liberty     && ln -s /opt/ibm/fixes /fixes     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
# ARGS: VERBOSE=false OPENJ9_SCC=true LIBERTY_VERSION=24.0.0.11 LIBERTY_BUILD_LABEL=cl241120241021-1102 LIBERTY_SHA=cc5790346b45f63d093cf8d6a528a7730a1dc570 LIBERTY_URL= DOWNLOAD_OPTIONS=
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output # buildkit
# Wed, 06 Nov 2024 14:57:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 06 Nov 2024 14:57:10 GMT
USER 1001
# Wed, 06 Nov 2024 14:57:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 06 Nov 2024 14:57:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 Nov 2024 14:57:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d7fcbb74a18dbda1a95a881c01c2cc4d8a0d6fe38b3b4f8b5899f281f9815e`  
		Last Modified: Tue, 17 Sep 2024 01:57:02 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1cf6d8f9bd9260e4efd3417f04f019329a2e54934d728d175a8c86be858d5b`  
		Last Modified: Mon, 04 Nov 2024 22:18:38 GMT  
		Size: 50.9 MB (50893033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e47235f4b5478e2c23e3613009d1f9f37fe175fc647cd87c4420b787a2f240d`  
		Last Modified: Mon, 04 Nov 2024 22:18:37 GMT  
		Size: 4.6 MB (4583234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec46a7050eca3b34308a2ea8a443e5cdcf4f487c46268160ef2aec3e13f8310`  
		Last Modified: Wed, 06 Nov 2024 20:53:05 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f09b14e02e1aee47aa3b234acabb9e3ae0239576386225fe45b068902951cb`  
		Last Modified: Wed, 06 Nov 2024 20:53:06 GMT  
		Size: 17.4 MB (17435503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798720451300e82d8544e7cd87f5d085fe88d4bd7185ce4e26e937562c164ec`  
		Last Modified: Wed, 06 Nov 2024 20:53:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7d29c6adc7e439319d10ab72ae84f6d8b62dce32274f125646dd67b5ed1d45`  
		Last Modified: Wed, 06 Nov 2024 20:53:05 GMT  
		Size: 1.5 KB (1521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81889d87a790b47643f5a2a5f30125b8e8a657119f115ac0aedceb9e06e69b4d`  
		Last Modified: Wed, 06 Nov 2024 20:53:06 GMT  
		Size: 11.8 KB (11833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b6e7dcc21f1e7d13d86fe3c1d4d15593fb193bd0b847edb051a079eac1654f`  
		Last Modified: Wed, 06 Nov 2024 20:53:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1af7496bb01679fe213be0808192461539c0f6528a24c106d236b213df564f`  
		Last Modified: Wed, 06 Nov 2024 20:53:06 GMT  
		Size: 12.6 KB (12640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabe36885110e2104a26e292c369a64b9d80d37bb2cebf138f48b5e10966932f`  
		Last Modified: Wed, 06 Nov 2024 20:53:07 GMT  
		Size: 2.8 MB (2827526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `websphere-liberty:kernel-java11-openj9` - unknown; unknown

```console
$ docker pull websphere-liberty@sha256:f8101fa32d3210ba7664bd85ab7f0a09a3ef939c3d492c5a7156b115988c4a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3773542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce84d99a98bc2cc4ac34d032ca78961233421a9fc6b80b7de57ad2c1c7dc542`

```dockerfile
```

-	Layers:
	-	`sha256:741cbc71a67f7ee90bb466f88a33e5c686ec795afa67ff3433cede3dd56a89d2`  
		Last Modified: Wed, 06 Nov 2024 20:53:06 GMT  
		Size: 3.7 MB (3733548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42dbddd67f486dbd3e94fe4d6d4366fddbcff2baa2e34141ec122f00bec8e8c6`  
		Last Modified: Wed, 06 Nov 2024 20:53:05 GMT  
		Size: 40.0 KB (39994 bytes)  
		MIME: application/vnd.in-toto+json
