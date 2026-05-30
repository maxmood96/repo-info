## `open-liberty:latest`

```console
$ docker pull open-liberty@sha256:852d4d8c572f50103dfabccba7c848c09706feb5322cfd740bae167b4206ca9a
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

### `open-liberty:latest` - linux; amd64

```console
$ docker pull open-liberty@sha256:0b6c784a7a59eec59dd8bcc7eff8eaac3e72f0a0b974b3cc2a68c99ce2c493cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483068026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b686db50ee49be27bcd33512299cad4331724c9bc6dd05c0660d931f42fca7`
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
# Thu, 30 Apr 2026 23:44:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:44:32 GMT
ENV JAVA_VERSION=8.0.492.0
# Thu, 30 Apr 2026 23:44:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='508a88f952f432fa65772d0df61f5e0236a8e92f4dd5b3bb638c2f8d7be157b6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_aarch64_linux_8.0.492.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='787cb76565f2367534973b63b46b61387b5c1de80f26bcfbd8658af70bda3728';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_ppc64le_linux_8.0.492.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8a29af537e5d9c0814fb08d830afd074da89543a4563316e84cf1563d7f7057f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_x64_linux_8.0.492.0.tar.gz';          ;;        s390x)          ESUM='60d80f64f502d25d03edac655a8ed06676024aa9474a18ee4a304d5aef79317d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_s390x_linux_8.0.492.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:44:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:44:35 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:45:38 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 29 May 2026 23:04:37 GMT
USER root
# Fri, 29 May 2026 23:04:37 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:04:37 GMT
ARG LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c
# Fri, 29 May 2026 23:04:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip
# Fri, 29 May 2026 23:04:37 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:04:37 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:37 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:04:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.5 liberty.version=26.0.0.5 io.openliberty.version=26.0.0.5
# Fri, 29 May 2026 23:04:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:04:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:04:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:04:38 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:04:51 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:04:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:51 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:04:51 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:05:10 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:05:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:05:10 GMT
USER 1001
# Fri, 29 May 2026 23:05:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:05:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:05:10 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c09ccaa270c56c1580c62b80da8b47c3d6c019626050ce3b3dfba290a969ba7`  
		Last Modified: Thu, 30 Apr 2026 23:45:51 GMT  
		Size: 12.8 MB (12805348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4312fb03f50ecf7a79922c2d5ec2141b1e55035ad4b29c9baa0784e0b7d86a`  
		Last Modified: Thu, 30 Apr 2026 23:45:50 GMT  
		Size: 54.4 MB (54376293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ff4a9d8af67543eb7d0ba7a9028e2867696ebde6aca38d9e834a9cb77e0579`  
		Last Modified: Thu, 30 Apr 2026 23:45:51 GMT  
		Size: 4.2 MB (4228135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9e5f7e6eb0d78632b938919349b51789449cf0c0d0dca0cc0733342bda5ffe`  
		Last Modified: Fri, 29 May 2026 23:05:35 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930d9b0c84c66c4bda8e611b533c151259b8e088d96c7bdeb27dae50db2085bb`  
		Last Modified: Fri, 29 May 2026 23:05:35 GMT  
		Size: 12.4 KB (12352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011af4de78292e909c298a24a4e05fc5099be24150d03ec9e6509750c059d53b`  
		Last Modified: Fri, 29 May 2026 23:05:35 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962f7942ffa614d6cc297d50873412f03a75a19244d86167ee5217d362e50cf7`  
		Last Modified: Fri, 29 May 2026 23:05:35 GMT  
		Size: 31.8 KB (31750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532ea2b0cd91ed0d598e43fdac62556484bc1ac2ff3cdcf172a73fc00403c01`  
		Last Modified: Fri, 29 May 2026 23:05:43 GMT  
		Size: 368.4 MB (368429882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86777edfb82d27e8a2a1b2ca5af2e77f61f215275946cbccf83bdbeaf018209`  
		Last Modified: Fri, 29 May 2026 23:05:36 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7250437142c75026b3389aad34511b79a46134162a114a374450c2940b55cfc`  
		Last Modified: Fri, 29 May 2026 23:05:36 GMT  
		Size: 13.8 KB (13789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce3b2e769c26d7eaf6669ef5bdbbceeda8710729c015bdbedf0a54bfe2247aa`  
		Last Modified: Fri, 29 May 2026 23:05:37 GMT  
		Size: 13.4 MB (13435152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:latest` - unknown; unknown

```console
$ docker pull open-liberty@sha256:7927f5170483909a8535dd1e458e62cefaca780798413bac79051986aff0e385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef6e09695085c8a9e63f825b82fb60fe7a42e90851fbbab3d3ae0c8217184f`

```dockerfile
```

-	Layers:
	-	`sha256:52490d060d2a495584dac8c3c49ec8ca20bc3f22661434b27f4942fc8093ce58`  
		Last Modified: Fri, 29 May 2026 23:05:35 GMT  
		Size: 5.2 MB (5224749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773f1182153d0fe405c44f5d913e58175d5159b30c616be7ddc7e689d38704c8`  
		Last Modified: Fri, 29 May 2026 23:05:35 GMT  
		Size: 39.9 KB (39870 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:latest` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:e3646335bc4c41b01128c0b841a365307b00cf46c687fae26fa5304861a669be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.2 MB (481225032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0fe980c9914c775097807f701109a13d9ca9fba218dc19082d6f9b80254e2a`
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
# Thu, 30 Apr 2026 23:44:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:44:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:44:49 GMT
ENV JAVA_VERSION=8.0.492.0
# Thu, 30 Apr 2026 23:44:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='508a88f952f432fa65772d0df61f5e0236a8e92f4dd5b3bb638c2f8d7be157b6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_aarch64_linux_8.0.492.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='787cb76565f2367534973b63b46b61387b5c1de80f26bcfbd8658af70bda3728';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_ppc64le_linux_8.0.492.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8a29af537e5d9c0814fb08d830afd074da89543a4563316e84cf1563d7f7057f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_x64_linux_8.0.492.0.tar.gz';          ;;        s390x)          ESUM='60d80f64f502d25d03edac655a8ed06676024aa9474a18ee4a304d5aef79317d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_s390x_linux_8.0.492.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:44:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:44:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:45:54 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 29 May 2026 23:04:39 GMT
USER root
# Fri, 29 May 2026 23:04:39 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:04:39 GMT
ARG LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c
# Fri, 29 May 2026 23:04:39 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip
# Fri, 29 May 2026 23:04:39 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:04:39 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:39 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:04:39 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.5 liberty.version=26.0.0.5 io.openliberty.version=26.0.0.5
# Fri, 29 May 2026 23:04:39 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:04:39 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:04:39 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:04:39 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:04:54 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:04:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:55 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:04:55 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:05:16 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:05:16 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:05:16 GMT
USER 1001
# Fri, 29 May 2026 23:05:16 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:05:16 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:05:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b4465cb1ddee3d1a9fdfd4c1ed0fc99384f391b7617d47ab038295d53a4235`  
		Last Modified: Thu, 30 Apr 2026 23:46:07 GMT  
		Size: 12.8 MB (12837773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6914eac319e1fbf1c6fcf9172abbf57538b92a8c71c2c1cd4f14ff6c910ecc3b`  
		Last Modified: Thu, 30 Apr 2026 23:46:08 GMT  
		Size: 53.8 MB (53809096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebc29974b26209e817ee5c49b69e960f440169a157dd5b4b339a269fa88e080`  
		Last Modified: Thu, 30 Apr 2026 23:46:06 GMT  
		Size: 4.1 MB (4143098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c752dec5e8f9e319e5f879f3897e25b37e239c57ae18344cebe039091c49d08`  
		Last Modified: Fri, 29 May 2026 23:05:42 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9801fc2c1803c3958b92c811c0d111d695db0e12074132ea7e6e0637c842469e`  
		Last Modified: Fri, 29 May 2026 23:05:42 GMT  
		Size: 12.4 KB (12352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b7d726e261321e4268b7020300fbe6ccf83df8f8a2dc5a8fbe0aef3b4fa337`  
		Last Modified: Fri, 29 May 2026 23:05:42 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86564890621eee194ea6526a67fa29e500247a4857cff9389436cf01f6ee7061`  
		Last Modified: Fri, 29 May 2026 23:05:42 GMT  
		Size: 42.3 KB (42326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ff520570322c3bb3c4117c6551ef8c1c0162331639b5145e9195f82c93668`  
		Last Modified: Fri, 29 May 2026 23:05:51 GMT  
		Size: 368.4 MB (368430034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d212ceedfea54a17ed55694306c8adb3148291ed8046801ea6d8d18e040227b5`  
		Last Modified: Fri, 29 May 2026 23:05:43 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c793e5670e5b43a8651b575b2095fdb04a1c34b58eca6856e9a02f618b1ce8fd`  
		Last Modified: Fri, 29 May 2026 23:05:43 GMT  
		Size: 13.8 KB (13790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f2889a20fa4c5298ee90dd41c692445ad05c3045bc5c8b36d514519809b7f3`  
		Last Modified: Fri, 29 May 2026 23:05:44 GMT  
		Size: 13.1 MB (13058430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:latest` - unknown; unknown

```console
$ docker pull open-liberty@sha256:36daa6bf5a6ac358bc65ecd03c5fb9cf566ad4ff844a6930cd3a33d60b917089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14db6f2526024e0e6372a90bf04e95bfdeb913a077d7f16f99f0ccbdb0c0aaf`

```dockerfile
```

-	Layers:
	-	`sha256:4c6d3322330cfdf062dfb856d5dde17dddea2bdf8fb3f0bf025eb2b46f692fbe`  
		Last Modified: Fri, 29 May 2026 23:05:42 GMT  
		Size: 5.2 MB (5225362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2d3f016bfdc91c310f575285c07e2c1e28236c1863f7cb3dd8c55fb1923139`  
		Last Modified: Fri, 29 May 2026 23:05:42 GMT  
		Size: 40.0 KB (40022 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:latest` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:105ecd221c848c0fd05b3210675d901504f6cc5e047bdda763a0a7b63dd6aa7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.0 MB (488022367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8ab137dcd92f30c89fa4a5b239f0066e81df4a4ec33a97c698879575224c0c`
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
ENV JAVA_VERSION=8.0.492.0
# Thu, 30 Apr 2026 23:43:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='508a88f952f432fa65772d0df61f5e0236a8e92f4dd5b3bb638c2f8d7be157b6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_aarch64_linux_8.0.492.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='787cb76565f2367534973b63b46b61387b5c1de80f26bcfbd8658af70bda3728';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_ppc64le_linux_8.0.492.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8a29af537e5d9c0814fb08d830afd074da89543a4563316e84cf1563d7f7057f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_x64_linux_8.0.492.0.tar.gz';          ;;        s390x)          ESUM='60d80f64f502d25d03edac655a8ed06676024aa9474a18ee4a304d5aef79317d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_s390x_linux_8.0.492.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:43:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:43:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:44:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 29 May 2026 23:02:53 GMT
USER root
# Fri, 29 May 2026 23:02:53 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:02:53 GMT
ARG LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c
# Fri, 29 May 2026 23:02:53 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip
# Fri, 29 May 2026 23:02:53 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:02:53 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:02:53 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:02:53 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.5 liberty.version=26.0.0.5 io.openliberty.version=26.0.0.5
# Fri, 29 May 2026 23:02:53 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:07:45 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:07:45 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:07:46 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:08:06 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:08:06 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:08:07 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:08:43 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:08:43 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:08:43 GMT
USER 1001
# Fri, 29 May 2026 23:08:43 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:08:43 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:08:43 GMT
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
	-	`sha256:4cd70528ead2ef079425673ad137a84d60bdb6f848866ccc424172c91d41453f`  
		Last Modified: Thu, 30 Apr 2026 23:44:48 GMT  
		Size: 56.1 MB (56070302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b4575003709dc5298f930010de775d256fff9d50851d79a4ae299cc0a6796`  
		Last Modified: Thu, 30 Apr 2026 23:44:46 GMT  
		Size: 3.5 MB (3542007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7430402442e3d02c20c2b2adebd7024d5560c4e1bf57f6b8a12681d479acfdd6`  
		Last Modified: Fri, 29 May 2026 23:05:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ddc8c8a3b78bd66e2c3b83906e242551dc9edba6a62da4eff9b71feffcc55c`  
		Last Modified: Sat, 30 May 2026 03:05:58 GMT  
		Size: 12.3 KB (12350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7423c021d1a149d9d4fe590da73b0f27b0a5e04c451fa477e21b1eb6e87eee`  
		Last Modified: Sat, 30 May 2026 03:05:58 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2ab0e2bcc3aa874596267038de492dcdc7b24e8ab193778bfaab6879214caa`  
		Last Modified: Sat, 30 May 2026 03:05:58 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0777e2899ac997e7623000ca3247e292e83716eea05aa40167cc90a7f1db1a5`  
		Last Modified: Sat, 30 May 2026 03:06:06 GMT  
		Size: 368.4 MB (368430325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76872fd18697696e3374fcf68205534c4e341d3c3b2fc6de3e56672d605d535`  
		Last Modified: Sat, 30 May 2026 03:05:59 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f243c1ae98d2ae37b037796647684d933cbae770e1eb96af71d6eb60956f959a`  
		Last Modified: Sat, 30 May 2026 03:05:59 GMT  
		Size: 13.8 KB (13791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7769cc4bab7268a63c71e022aa5e76b836271b353ce623e3deb7bed4f9857d46`  
		Last Modified: Sat, 30 May 2026 03:06:00 GMT  
		Size: 11.8 MB (11812071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:latest` - unknown; unknown

```console
$ docker pull open-liberty@sha256:3d09b92d5b1f19b0709bd4be3018c3dc9ce008aadfe0bd2518e9503a8370d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692291c83d142f7557868addbd219ffc4c3ee7ee61f32f5fa0ca9b09bb7c82b1`

```dockerfile
```

-	Layers:
	-	`sha256:77e70692238361125b9387d9af913b010702bb21ef17677d8a06b9edef78a5e6`  
		Last Modified: Sat, 30 May 2026 03:05:58 GMT  
		Size: 5.2 MB (5229553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8d9adb51063e9c06e9a8fc4672c6c91f939d80fffc43166cc7ba97b0662e69`  
		Last Modified: Sat, 30 May 2026 03:05:58 GMT  
		Size: 39.9 KB (39914 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:latest` - linux; s390x

```console
$ docker pull open-liberty@sha256:ce6a4466301c062638a755852b436b4bb12fadf5afe2e0f86ab8afc10615707c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (487025866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f25ccffdf1385ca8d4e6bef82da0b087a2925ad44df0acbdda3a019faa7bf3`
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
# Wed, 15 Apr 2026 20:55:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:55:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:55:19 GMT
ENV JAVA_VERSION=8.0.492.0
# Thu, 30 Apr 2026 23:39:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='508a88f952f432fa65772d0df61f5e0236a8e92f4dd5b3bb638c2f8d7be157b6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_aarch64_linux_8.0.492.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='787cb76565f2367534973b63b46b61387b5c1de80f26bcfbd8658af70bda3728';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_ppc64le_linux_8.0.492.0.tar.gz';          ;;        amd64|x86_64)          ESUM='8a29af537e5d9c0814fb08d830afd074da89543a4563316e84cf1563d7f7057f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_x64_linux_8.0.492.0.tar.gz';          ;;        s390x)          ESUM='60d80f64f502d25d03edac655a8ed06676024aa9474a18ee4a304d5aef79317d';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk-8.0.492.0/ibm-semeru-open-jre_s390x_linux_8.0.492.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:39:14 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:39:14 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:40:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 29 May 2026 23:03:04 GMT
USER root
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_VERSION=26.0.0.5
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:03:04 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:03:04 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:03:04 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.5 liberty.version=26.0.0.5 io.openliberty.version=26.0.0.5
# Fri, 29 May 2026 23:03:04 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:05:04 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:05:04 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:05:04 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:05:21 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:05:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:05:21 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:05:22 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:05:48 GMT
# ARGS: LIBERTY_VERSION=26.0.0.5 LIBERTY_SHA=c793c3f0f2ad7bcb034a4761969aa7ac5628af2c LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.5/openliberty-runtime-26.0.0.5.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:05:48 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:05:48 GMT
USER 1001
# Fri, 29 May 2026 23:05:48 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:05:48 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:05:48 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1dca01c7f8a5c02c033ddd80e1849e4d2dce0090b72e585925cee97f083f26`  
		Last Modified: Wed, 15 Apr 2026 20:56:59 GMT  
		Size: 13.1 MB (13117391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d4d3a4269f591d9677f142ec5504047dea2e497e44cd37f94432a19ebaa4e9`  
		Last Modified: Thu, 30 Apr 2026 23:40:42 GMT  
		Size: 57.5 MB (57471591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd271415780a5eb4e94dfdb8380cc3d21723d1932c69c594b2c1180e323d5b0`  
		Last Modified: Thu, 30 Apr 2026 23:40:36 GMT  
		Size: 4.5 MB (4458912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17757315905b4b34c84352a4f219e7065316f815ee94f035de941bb79e47ca7`  
		Last Modified: Fri, 29 May 2026 23:03:38 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3d684670fef46a52f538e1b6656fc7be9a57944900c1270bfc02705511d2e8`  
		Last Modified: Fri, 29 May 2026 23:06:28 GMT  
		Size: 12.3 KB (12350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63b609d10b148797bd825d48746c8810d4b75ca7062112578ef5525da56337c`  
		Last Modified: Fri, 29 May 2026 23:06:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796d7cfd2e4b7816cd0f37c96b928c1dec0744fbac22f66fdf5d708e8b95ad7e`  
		Last Modified: Fri, 29 May 2026 23:06:28 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a846ba23df7e7a6d468c7eb28c3eacca0cdcc862f67d5a3f9fcf62da3bb24a`  
		Last Modified: Fri, 29 May 2026 23:06:34 GMT  
		Size: 368.4 MB (368429715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53fafc56f571c855132f957120362eafbcef1ea5a13c0106382ab223f3496f8`  
		Last Modified: Fri, 29 May 2026 23:06:29 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47efeb59397eba8f8eb4256226e8035bd16acfc55c94d6408a2e434df43eaee8`  
		Last Modified: Fri, 29 May 2026 23:06:29 GMT  
		Size: 13.8 KB (13793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0bde6b159b09fb51ce4a34c6a93aa87e014fd1a575fd050ef975155681aa49`  
		Last Modified: Fri, 29 May 2026 23:06:29 GMT  
		Size: 13.6 MB (13574508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:latest` - unknown; unknown

```console
$ docker pull open-liberty@sha256:4045013e79134b5bf97995db26a7e65c57567e4770d9e9c63b8d278cdc00c9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140670638aad070abc2f80b9bf294c69ec3e9fc829aa84cb144874139e9d6884`

```dockerfile
```

-	Layers:
	-	`sha256:b3d9d0b2f03b3b45dc99db60d1f72d17f99de599f09f8936535f48ea05b615e0`  
		Last Modified: Fri, 29 May 2026 23:06:28 GMT  
		Size: 5.2 MB (5226372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7a1aaf0e602814bdd74687f62f14fae433fcefcec8bfb19603558bf90c62fd`  
		Last Modified: Fri, 29 May 2026 23:06:28 GMT  
		Size: 39.9 KB (39870 bytes)  
		MIME: application/vnd.in-toto+json
