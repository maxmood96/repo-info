## `open-liberty:kernel-slim-java11-openj9`

```console
$ docker pull open-liberty@sha256:8179e5e197b58b26b27bfa403dcebe8ce7eae5ed67915c6e9657390193f398e5
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

### `open-liberty:kernel-slim-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:7c3912708749c6ee5ddea23c5276a023488561f40cbd536cee2bc2cb052b869e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120491320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a60017c65df0fd9613a5d0a3a45880fba1997dd48181f088c4a6326faf9120`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:39:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:39:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:39:27 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Wed, 15 Apr 2026 20:39:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d11853bdda82f9246e012e3f619bbd66c46924199ff2d0f31079bc9637a406c0';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2cccbe7787838403a64fb8cad3995b1f6ba60c2925dd7f2a39e858bdb415922';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f15e9e3e11774ba2374e549870063309085dc6510437e40c1bd520dcde1739b0';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='2e81327f86adcee8811e824d6c04c3d7a3e733e6aa83408abb6c159903d2fa97';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:39:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:39:29 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 20:40:34 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 21:42:16 GMT
USER root
# Wed, 15 Apr 2026 21:42:16 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Wed, 15 Apr 2026 21:42:16 GMT
ARG LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b
# Wed, 15 Apr 2026 21:42:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip
# Wed, 15 Apr 2026 21:42:16 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Wed, 15 Apr 2026 21:42:16 GMT
ARG OPENJ9_SCC=true
# Wed, 15 Apr 2026 21:42:16 GMT
ARG VERBOSE=false
# Wed, 15 Apr 2026 21:42:16 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.3 liberty.version=26.0.0.3 io.openliberty.version=26.0.0.3
# Wed, 15 Apr 2026 21:42:16 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 15 Apr 2026 21:42:16 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 15 Apr 2026 21:42:16 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 15 Apr 2026 21:42:16 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 15 Apr 2026 21:42:26 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 15 Apr 2026 21:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 15 Apr 2026 21:42:27 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 15 Apr 2026 21:42:27 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 15 Apr 2026 21:42:30 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 15 Apr 2026 21:42:30 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 15 Apr 2026 21:42:30 GMT
USER 1001
# Wed, 15 Apr 2026 21:42:30 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 15 Apr 2026 21:42:30 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 15 Apr 2026 21:42:30 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26efc42667f34a191801e9477dd2b1efee14c37b3e438b11f7d404a849925c96`  
		Last Modified: Wed, 15 Apr 2026 20:40:49 GMT  
		Size: 12.8 MB (12805314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6df51bc4b043f667101400c7219ec3fe94fd69d84ed300016d17205552f33`  
		Last Modified: Wed, 15 Apr 2026 20:40:50 GMT  
		Size: 55.7 MB (55735839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036889be19c92e671fd65cd1a7a0b7ed08a4118b0b7c61588777b5b5e5794030`  
		Last Modified: Wed, 15 Apr 2026 20:40:48 GMT  
		Size: 4.4 MB (4428916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11b2139c9b5e6a4e9a42c25e2931c3b8a88da2fb2040e4bd4ffcc385c67801e`  
		Last Modified: Wed, 15 Apr 2026 21:42:39 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98a575974df25d0379f65765cab79f5bf0274d50099883fbfe9e85f58bba339`  
		Last Modified: Wed, 15 Apr 2026 21:42:39 GMT  
		Size: 11.8 KB (11820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47283d79edd786c4b2f6f6bf1b61158793848e348d35c5b6f02346454be090a6`  
		Last Modified: Wed, 15 Apr 2026 21:42:39 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12003de9f53a224c528992a5ab379477b961b653311e86016a626e2868c9b1a6`  
		Last Modified: Wed, 15 Apr 2026 21:42:39 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df04b9f6f4d71d36a6eb7f900a89fe7730f8a61a01281477b73fc68e02ebf366`  
		Last Modified: Wed, 15 Apr 2026 21:42:41 GMT  
		Size: 15.0 MB (15031498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbba54df508fa6260917d071992765b12952caad2f0c72b04e00eccec439e62e`  
		Last Modified: Wed, 15 Apr 2026 21:42:41 GMT  
		Size: 743.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0abfbc95737f07a2475211e8383398f4d80a258fed9aa97da9cbcd07d55d186`  
		Last Modified: Wed, 15 Apr 2026 21:42:41 GMT  
		Size: 12.9 KB (12929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9fa883f2681642e568af55cf60d7c2aa42c61b4e3aa31088c89b2c51b6a9c6`  
		Last Modified: Wed, 15 Apr 2026 21:42:41 GMT  
		Size: 2.7 MB (2698245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e70a7d8a3d0ccdc00fa198d19c53b67c1cc424a0c5243baded953dcd1e1408ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3359988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6771a24f2878773986bf201d2f8050169a18711deb666e5622f352a3c768ed47`

```dockerfile
```

-	Layers:
	-	`sha256:eee3fc813593d5d5e0bbbc4003eeb8810e2eabd69a8ae5d9bf191c1e778de065`  
		Last Modified: Wed, 15 Apr 2026 21:42:39 GMT  
		Size: 3.3 MB (3320505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b919027dd2c48639eea5cbe931468aba6c048450bb1224443ec1a6e248e0e957`  
		Last Modified: Wed, 15 Apr 2026 21:42:39 GMT  
		Size: 39.5 KB (39483 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:e3494d831571909e907ed70d1e7a43cb636537ccad1e31a2a345322f4139e114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117900990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180461d87d25c33a796b980cfc938c2eda660167ed6f79c65601de4064c899fd`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:39:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:39:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:39:54 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Wed, 15 Apr 2026 20:39:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d11853bdda82f9246e012e3f619bbd66c46924199ff2d0f31079bc9637a406c0';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2cccbe7787838403a64fb8cad3995b1f6ba60c2925dd7f2a39e858bdb415922';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f15e9e3e11774ba2374e549870063309085dc6510437e40c1bd520dcde1739b0';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='2e81327f86adcee8811e824d6c04c3d7a3e733e6aa83408abb6c159903d2fa97';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:39:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:39:56 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 15 Apr 2026 20:41:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 15 Apr 2026 21:54:12 GMT
USER root
# Wed, 15 Apr 2026 21:54:12 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Wed, 15 Apr 2026 21:54:12 GMT
ARG LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b
# Wed, 15 Apr 2026 21:54:12 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip
# Wed, 15 Apr 2026 21:54:12 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Wed, 15 Apr 2026 21:54:12 GMT
ARG OPENJ9_SCC=true
# Wed, 15 Apr 2026 21:54:12 GMT
ARG VERBOSE=false
# Wed, 15 Apr 2026 21:54:12 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.3 liberty.version=26.0.0.3 io.openliberty.version=26.0.0.3
# Wed, 15 Apr 2026 21:54:12 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 15 Apr 2026 21:54:12 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 15 Apr 2026 21:54:12 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 15 Apr 2026 21:54:13 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 15 Apr 2026 21:54:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 15 Apr 2026 21:54:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 15 Apr 2026 21:54:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 15 Apr 2026 21:54:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 15 Apr 2026 21:54:29 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 15 Apr 2026 21:54:29 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 15 Apr 2026 21:54:29 GMT
USER 1001
# Wed, 15 Apr 2026 21:54:29 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 15 Apr 2026 21:54:29 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 15 Apr 2026 21:54:29 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe4ee2b613972287b3913a1668cfc65de7536358aa0a7b1a8373fabc0c73eef`  
		Last Modified: Wed, 15 Apr 2026 20:41:14 GMT  
		Size: 12.8 MB (12837920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b73cd1e0342748456bbe00b3d842f84a4b0c410862f7b9b423c9afa95718578`  
		Last Modified: Wed, 15 Apr 2026 20:41:16 GMT  
		Size: 54.0 MB (54018882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9762ae7343caf93aacde7c32d63aaa74b814e58b9452019af1214e1ecedb473`  
		Last Modified: Wed, 15 Apr 2026 20:41:14 GMT  
		Size: 4.3 MB (4265048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a1f76bb14bf8aed1b9c457b40876823ea0723c24e34f9d8d72b580fb8d07a`  
		Last Modified: Wed, 15 Apr 2026 21:54:38 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0bd204ae7ccf040d2efd5add0b7ddab338be2f4d2907ae93359ff871d443ac`  
		Last Modified: Wed, 15 Apr 2026 21:54:38 GMT  
		Size: 11.8 KB (11817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce322befefa7e1f3ebf504215038de8c5bd5e0bf8f55d65ea681a4bb6e22a6`  
		Last Modified: Wed, 15 Apr 2026 21:54:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee81f0d132e83a809632c7b037381ed4a8d1d9d3bf054c2df7476cf50b17915`  
		Last Modified: Wed, 15 Apr 2026 21:54:38 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997d665b7b345f77c850f0c29f1ab7cef454d672e51454e913c2a5bd241c80a7`  
		Last Modified: Wed, 15 Apr 2026 21:54:39 GMT  
		Size: 15.0 MB (15031668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b708b158b9b57bd807520d86309ec96103386e4c7fa74ed275e8482b75193823`  
		Last Modified: Wed, 15 Apr 2026 21:54:39 GMT  
		Size: 736.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ac37a1b719d9a702e1ecf2d5bd9096aac0d976c4b853ee70ebaf07c28edfef`  
		Last Modified: Wed, 15 Apr 2026 21:54:39 GMT  
		Size: 12.9 KB (12913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8852c2d47af9ab203ea155d409ae421fd134d04164f1e36845cc575047b70b6`  
		Last Modified: Wed, 15 Apr 2026 21:54:39 GMT  
		Size: 2.8 MB (2802610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:524d7e1c038f9f6084d568740086fb989ef7e7253a27d1664c2a640080adff5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ddd7150c3e52b314faa3a1f2608391bd76dc67a892eb0f7426a74647bf056b`

```dockerfile
```

-	Layers:
	-	`sha256:f1c0080985b5dcd8df1ca67c4e141fb313c9b97e0b481677dd5c72315bdbee02`  
		Last Modified: Wed, 15 Apr 2026 21:54:38 GMT  
		Size: 3.3 MB (3319047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e082c80fac66c0d497627ab506b06b22261a16d55fd806af3db75cf064941b9`  
		Last Modified: Wed, 15 Apr 2026 21:54:38 GMT  
		Size: 39.6 KB (39622 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:a3c8701fddfa1440b92221a1b1efbea7c6c637c9e29f9a55500c1b093658f81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126941539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5217ef5fd07edf3eb80922e24621cc6dc1116d71578c2c28b81cbe49d30d45`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:39:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:39:02 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Thu, 16 Apr 2026 05:50:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d11853bdda82f9246e012e3f619bbd66c46924199ff2d0f31079bc9637a406c0';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2cccbe7787838403a64fb8cad3995b1f6ba60c2925dd7f2a39e858bdb415922';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f15e9e3e11774ba2374e549870063309085dc6510437e40c1bd520dcde1739b0';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='2e81327f86adcee8811e824d6c04c3d7a3e733e6aa83408abb6c159903d2fa97';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 16 Apr 2026 05:50:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 05:50:36 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 16 Apr 2026 05:51:46 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 16 Apr 2026 06:08:54 GMT
USER root
# Thu, 16 Apr 2026 06:08:54 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Thu, 16 Apr 2026 06:08:54 GMT
ARG LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b
# Thu, 16 Apr 2026 06:08:54 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip
# Thu, 16 Apr 2026 06:08:54 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Thu, 16 Apr 2026 06:08:54 GMT
ARG OPENJ9_SCC=true
# Thu, 16 Apr 2026 06:08:54 GMT
ARG VERBOSE=false
# Thu, 16 Apr 2026 06:08:54 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.3 liberty.version=26.0.0.3 io.openliberty.version=26.0.0.3
# Thu, 16 Apr 2026 06:08:54 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 16 Apr 2026 06:08:54 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 16 Apr 2026 06:08:54 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 16 Apr 2026 06:08:55 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 16 Apr 2026 06:09:11 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 16 Apr 2026 06:09:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 16 Apr 2026 06:09:17 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 16 Apr 2026 06:09:31 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 16 Apr 2026 06:09:42 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 16 Apr 2026 06:09:42 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 16 Apr 2026 06:09:42 GMT
USER 1001
# Thu, 16 Apr 2026 06:09:42 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 16 Apr 2026 06:09:42 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 16 Apr 2026 06:09:42 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccf3833ba70e5f487e107c0fc757f71c24195588839e7b794b482f819b1bf2d`  
		Last Modified: Wed, 15 Apr 2026 21:40:36 GMT  
		Size: 13.8 MB (13788494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93887e5dcc6c0ec8a0b9e61ac4748fbe5bfb30cd47f323afc59a61bbb399e60`  
		Last Modified: Thu, 16 Apr 2026 05:52:17 GMT  
		Size: 57.6 MB (57610250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab2ae418fa95230a02089ed9a6b7e175cf9ab205db24d0c96ed5ffff60c1b4`  
		Last Modified: Thu, 16 Apr 2026 05:52:15 GMT  
		Size: 3.5 MB (3462518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20490c381b6475ee165c4ae61c123757cc3ceb907b776426bcc39fcfb011e20f`  
		Last Modified: Thu, 16 Apr 2026 06:10:00 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75b1dffa8c914b84c4f7cf6a72274ff0ae7bb2578f12a87d897471494fcd3e`  
		Last Modified: Thu, 16 Apr 2026 06:10:00 GMT  
		Size: 11.8 KB (11819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6098d352af60d86e04b70c02c4505ecc5f07ad4bc6f9e08b726f828278643e`  
		Last Modified: Thu, 16 Apr 2026 06:10:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f290b931b99bf4ccdee19623d658d7fccfdaea5bb3dc5a56e8c3ceae9c5cb8a3`  
		Last Modified: Thu, 16 Apr 2026 06:10:00 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16212f2b87a573c3b4b5e0f28c7ce3eae041f7b8fdf529a137cfdc429d7f79d5`  
		Last Modified: Thu, 16 Apr 2026 06:10:02 GMT  
		Size: 15.0 MB (15031925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d3ae6b5065fb549bbd1afa7139f3d144666116c902a905c6d1843fa43fe238`  
		Last Modified: Thu, 16 Apr 2026 06:10:02 GMT  
		Size: 737.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85a434dfc6716a8caea39ec3cdd14c1b540b912eaee8df3a29a2639827507bf`  
		Last Modified: Thu, 16 Apr 2026 06:10:02 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ae11dab5a67a15c89fa6177a40d5d5cf994e2f6e177a78f95e0aa58c238d3d`  
		Last Modified: Thu, 16 Apr 2026 06:10:02 GMT  
		Size: 2.7 MB (2670899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:0b0dd48aa30463b5444d62134a89b265d2ac8e9366f96569776c3b7390bbd370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3364656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dabb852e10b5de95a8adb9a8cd571968b53a791cd6b35fc0ceb124ee7698fc2`

```dockerfile
```

-	Layers:
	-	`sha256:0146ce5a52d0e455e18beaeb45842b49ea86f18923282bbc8db555a8ee9c1839`  
		Last Modified: Thu, 16 Apr 2026 06:10:00 GMT  
		Size: 3.3 MB (3325133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:499f3706c68fa760435b3c17736ec0b3ee8aea055389a473ffd59326511d6a04`  
		Last Modified: Thu, 16 Apr 2026 06:10:00 GMT  
		Size: 39.5 KB (39523 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:527c10bd82d38583e6ef271937680b113ed916ebed5ac0bdd5e35f7ebe3a6ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120111701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b716ffc50d4b5b2ff4c7682570bc75bdd5f891e32bcfc18dc650cc5bac9b25b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:50:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:50:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:50:13 GMT
ENV JAVA_VERSION=jdk-11.0.30+7.1_openj9-0.57.0
# Thu, 16 Apr 2026 00:50:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d11853bdda82f9246e012e3f619bbd66c46924199ff2d0f31079bc9637a406c0';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_11.0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d2cccbe7787838403a64fb8cad3995b1f6ba60c2925dd7f2a39e858bdb415922';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_11.0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f15e9e3e11774ba2374e549870063309085dc6510437e40c1bd520dcde1739b0';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_11.0.30.1.tar.gz';          ;;        s390x)          ESUM='2e81327f86adcee8811e824d6c04c3d7a3e733e6aa83408abb6c159903d2fa97';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.30+7.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_11.0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 16 Apr 2026 00:50:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:50:20 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 16 Apr 2026 00:51:36 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 16 Apr 2026 01:21:33 GMT
USER root
# Thu, 16 Apr 2026 01:21:33 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Thu, 16 Apr 2026 01:21:33 GMT
ARG LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b
# Thu, 16 Apr 2026 01:21:33 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip
# Thu, 16 Apr 2026 01:21:33 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Thu, 16 Apr 2026 01:21:33 GMT
ARG OPENJ9_SCC=true
# Thu, 16 Apr 2026 01:21:33 GMT
ARG VERBOSE=false
# Thu, 16 Apr 2026 01:21:33 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.3 liberty.version=26.0.0.3 io.openliberty.version=26.0.0.3
# Thu, 16 Apr 2026 01:21:33 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 16 Apr 2026 01:21:33 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 16 Apr 2026 01:21:33 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 16 Apr 2026 01:21:33 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 16 Apr 2026 01:21:41 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 16 Apr 2026 01:21:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 16 Apr 2026 01:21:41 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 16 Apr 2026 01:21:41 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 16 Apr 2026 01:21:46 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=4ed962192d69effa30e34290a1a819469fe6e12b LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/26.0.0.3/openliberty-kernel-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 16 Apr 2026 01:21:46 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 16 Apr 2026 01:21:46 GMT
USER 1001
# Thu, 16 Apr 2026 01:21:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 16 Apr 2026 01:21:46 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 16 Apr 2026 01:21:46 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a45433edaccf5d141e572facc743118ac3f34051bab72b31c6fffae6248562`  
		Last Modified: Wed, 15 Apr 2026 20:51:45 GMT  
		Size: 13.1 MB (13117615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a2cd7f9ac71f26e84667f1baf259f81c841ce03adbe7f8a74230029efcb36b`  
		Last Modified: Thu, 16 Apr 2026 00:51:57 GMT  
		Size: 54.6 MB (54561907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4726cbe2ebe68221b5dcb6c3ce6441e1a42e2e7062b308378b21c6d841825f34`  
		Last Modified: Thu, 16 Apr 2026 00:51:56 GMT  
		Size: 4.7 MB (4657861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ce557bde6472d4cf61759ebdc91d47ece2df2e6523e6742543859872548af6`  
		Last Modified: Thu, 16 Apr 2026 01:22:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f13f4d373d617935174d63cc0e3c1264ea0d01ce6dc6cf3bff816e98db7a081`  
		Last Modified: Thu, 16 Apr 2026 01:22:01 GMT  
		Size: 11.8 KB (11820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183eff6640bfd84a9332130d28d72c33fa0cee5a4320a79b6557b08515f25650`  
		Last Modified: Thu, 16 Apr 2026 01:22:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9082d66f97b9f656d2934818282c85ff52e267217460644efa5f9cafa8876738`  
		Last Modified: Thu, 16 Apr 2026 01:22:01 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2fae5cbe0d03289924e9888983ff4e63d9e923b05628993dee321babfce95d`  
		Last Modified: Thu, 16 Apr 2026 01:22:02 GMT  
		Size: 15.0 MB (15031329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a94ab1a578c85e33cdf5aa3180365faa0aa6fbb7fb340dc7decf7dd3760dfae`  
		Last Modified: Thu, 16 Apr 2026 01:22:02 GMT  
		Size: 737.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3fc9797baea320e9e1b78086e99ff8e8cdd4c9f3b27b045a7e91978e45097`  
		Last Modified: Thu, 16 Apr 2026 01:22:02 GMT  
		Size: 12.9 KB (12924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9350a242b88cfc452a9c12d9adc6bd35e6a20729636aa943a4b35d27e5a0e6b0`  
		Last Modified: Thu, 16 Apr 2026 01:22:02 GMT  
		Size: 2.8 MB (2770956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:95997438f5ecbb9369b605b957d34e7a8815d507b011c1617b1bf8fea868c7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9f69c523ae7ccfe1dfdfdffaa51a1c5354b49afc652c565b7165fa6757f310`

```dockerfile
```

-	Layers:
	-	`sha256:7eb2b9f245d15c097363565f79e92e3b91a31a6eb1d74556a93b8cfa73efa597`  
		Last Modified: Thu, 16 Apr 2026 01:22:01 GMT  
		Size: 3.3 MB (3321502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8eac770f3b898896445f94285569649b7b200ad6075db770d7faabc8fbbf739`  
		Last Modified: Thu, 16 Apr 2026 01:22:01 GMT  
		Size: 39.5 KB (39483 bytes)  
		MIME: application/vnd.in-toto+json
