## `open-liberty:beta-java17`

```console
$ docker pull open-liberty@sha256:5d9332e0d04c23e03a08b01f42d9f33f7258994e8d90b005c48f4ded2e2660d8
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

### `open-liberty:beta-java17` - linux; amd64

```console
$ docker pull open-liberty@sha256:87cac0ebaf1f6fb8a53d883640c131358a3b86f2132d6b28bb5f51e3ac64967b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.5 MB (489451162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd32e6f1d0fd3a2eb9585159db47b4b0bbf1e55702e13e0870a6a58c9ff82725`
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
# Thu, 30 Apr 2026 23:46:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:46:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:46:10 GMT
ENV JAVA_VERSION=17.0.19.0
# Thu, 30 Apr 2026 23:46:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:46:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:46:12 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:47:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:10:41 GMT
USER root
# Fri, 01 May 2026 00:10:41 GMT
ARG LIBERTY_VERSION=26.0.0.4-beta
# Fri, 01 May 2026 00:10:41 GMT
ARG LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e
# Fri, 01 May 2026 00:10:41 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip
# Fri, 01 May 2026 00:10:41 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:10:41 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:10:41 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:10:41 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.4-beta liberty.version=26.0.0.4-beta io.openliberty.version=26.0.0.4-beta
# Fri, 01 May 2026 00:10:41 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 01 May 2026 00:10:41 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 01 May 2026 00:10:41 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 01 May 2026 00:10:42 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:11:00 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 01 May 2026 00:11:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 May 2026 00:11:01 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:11:01 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:11:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 01 May 2026 00:11:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:11:24 GMT
USER 1001
# Fri, 01 May 2026 00:11:24 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:11:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:11:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cd737a8b9091e9a2bcd6d0afc1e4c62a0f2c266c8566bc302804b9c46de824`  
		Last Modified: Thu, 30 Apr 2026 23:47:27 GMT  
		Size: 12.8 MB (12805392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61a0132dbaf5c7b1e692be574dafc2896e1e40a6f082923cfc06208aed92d15`  
		Last Modified: Thu, 30 Apr 2026 23:47:28 GMT  
		Size: 56.1 MB (56093691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb25686fef712ae235cec141ed46c4ba20ec8f2d118c3a936bcb1c531472734`  
		Last Modified: Thu, 30 Apr 2026 23:47:27 GMT  
		Size: 5.0 MB (5007826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c49f0ce61b5a3bb77071c6f4e3a31d031d870216476c816e28c5f5610e1ed6`  
		Last Modified: Fri, 01 May 2026 00:11:48 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ad8981741ea625739472ad35a84cb3fa18b4efc84119ba3238b2d3662275d2`  
		Last Modified: Fri, 01 May 2026 00:11:48 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366d8a498a26d3f27b10e42cbb8f7e52c5a95c21554ca36e0dba301f2deb9ed3`  
		Last Modified: Fri, 01 May 2026 00:11:48 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f2791803b21aabd2ef52ac8b51cba5338ec937ab44eac38095942ca0278476`  
		Last Modified: Fri, 01 May 2026 00:11:48 GMT  
		Size: 31.8 KB (31751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c53fdc56060604ebd6b58bd4c4d2c9cebaca317c874539d69d9628ec586206`  
		Last Modified: Fri, 01 May 2026 00:11:58 GMT  
		Size: 371.2 MB (371164473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf392fca38fe1c6e6aa35fc0cf23f7ae40bfa819802f9dcd2941b9449fa6e870`  
		Last Modified: Fri, 01 May 2026 00:11:49 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2569ea8e647eda7192dc80e99d00cebbd289597649d1eb0aa59866af6020c17e`  
		Last Modified: Fri, 01 May 2026 00:11:49 GMT  
		Size: 13.7 KB (13726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186e573440b4a6665d7e66eed998676a7f72033d679992699a54c168ebba294`  
		Last Modified: Fri, 01 May 2026 00:11:50 GMT  
		Size: 14.6 MB (14586692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:dcc2ea11effa7ef49a6f07be22f4d1e1b8f2d1a502632fbbff9e3feefbdb47ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bcc0623f721da3033501281ba14c384306f7c68d9eec9b2f2f133de42d554e`

```dockerfile
```

-	Layers:
	-	`sha256:6a2637cabfb9cc87b6bc271e738572e12e9dfe4f50d247715cd47247caee1a50`  
		Last Modified: Fri, 01 May 2026 00:11:48 GMT  
		Size: 5.2 MB (5241671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68c147bc18ecd69d364ba372c809d2cc92691710f79c18504394720483ce7d9`  
		Last Modified: Fri, 01 May 2026 00:11:48 GMT  
		Size: 39.4 KB (39377 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:dc88826db7eb1d5d7bed8af7c486320556f4f7aa6b0b384a436f9679d3a9e80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.1 MB (486099227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cd90b07ab8d4072f19b4606e40cb4afb29b52ed2b893561b4ba621871fbc66`
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
# Thu, 30 Apr 2026 23:46:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:46:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:46:28 GMT
ENV JAVA_VERSION=17.0.19.0
# Thu, 30 Apr 2026 23:46:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:46:30 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:46:30 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:47:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:09:50 GMT
USER root
# Fri, 01 May 2026 00:09:50 GMT
ARG LIBERTY_VERSION=26.0.0.4-beta
# Fri, 01 May 2026 00:09:50 GMT
ARG LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e
# Fri, 01 May 2026 00:09:50 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip
# Fri, 01 May 2026 00:09:50 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:09:50 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:09:50 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:09:50 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.4-beta liberty.version=26.0.0.4-beta io.openliberty.version=26.0.0.4-beta
# Fri, 01 May 2026 00:09:50 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 01 May 2026 00:09:50 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 01 May 2026 00:09:50 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 01 May 2026 00:09:51 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:10:11 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 01 May 2026 00:10:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 May 2026 00:10:11 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:10:11 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:10:38 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 01 May 2026 00:10:38 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:10:38 GMT
USER 1001
# Fri, 01 May 2026 00:10:38 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:10:38 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:10:38 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58682390813eb4e99e41d3b95e0549a0d76691a908f1899a748b1fe6152e74e2`  
		Last Modified: Thu, 30 Apr 2026 23:47:46 GMT  
		Size: 12.8 MB (12837805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a2eeae307beb04671a80776bebbd5db9864e5e0f572ad0325c4cd7ec0dd3ae`  
		Last Modified: Thu, 30 Apr 2026 23:47:47 GMT  
		Size: 54.0 MB (54002667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9bde1a0155156418897c9c3cce40d2e977a72ffd8afb2c2d01bec210a475b6`  
		Last Modified: Thu, 30 Apr 2026 23:47:46 GMT  
		Size: 4.8 MB (4778048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac47745851c8c7d02c91317614cfcdcef2abf17a05b817685c16c58b7a5380`  
		Last Modified: Fri, 01 May 2026 00:11:05 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1c84241ffab2973137d68d4c021ebc03718fb78ac8c970471746b321919cd1`  
		Last Modified: Fri, 01 May 2026 00:11:05 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9558f58732f66d6faf4fe12fdd4bf613810989da75c1ca94a011b1c50769afe`  
		Last Modified: Fri, 01 May 2026 00:11:05 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f788e9e0c03a5922af0acb6ea54a2efe55b2d269ae3d22a30f7f7b626d2c0e6`  
		Last Modified: Fri, 01 May 2026 00:11:05 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9862af3279c6df54bd02e177593d038c1b3bc5783d301219e61f7b195cda4a51`  
		Last Modified: Fri, 01 May 2026 00:11:16 GMT  
		Size: 371.2 MB (371164660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622346443c012e894d1328b3c934a51351bc6df2060b3e50403f8e72d5c5e8e3`  
		Last Modified: Fri, 01 May 2026 00:11:07 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cfbc657e180dff07427334e434f5cf33790788cb39fd290fdaa6c243613138`  
		Last Modified: Fri, 01 May 2026 00:11:07 GMT  
		Size: 13.7 KB (13720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a304d6b8f4657d6ede35931bf36897eef7edae76c596422808f9eb078e7aef03`  
		Last Modified: Fri, 01 May 2026 00:11:08 GMT  
		Size: 14.4 MB (14369585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:3694ecf719dc1666539de8e98a1483b9e65bc89347745d8062c81249cf2cc8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28a89b56b24692f877931a7815a89860668709eb9335c9c3c65353e6db7778f`

```dockerfile
```

-	Layers:
	-	`sha256:1087891a901f17b0b553ec823a69b55d30be0f197b431e31276e23091fe4fc7d`  
		Last Modified: Fri, 01 May 2026 00:11:06 GMT  
		Size: 5.2 MB (5240201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de824696b93b5116ebcc039f0fcb6cc645559a577e8be666f24f0e7cdf7bfaf`  
		Last Modified: Fri, 01 May 2026 00:11:05 GMT  
		Size: 39.5 KB (39505 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:87f55fa6e70e8f24c64a90161a8c596201e5e5d3df8adb42fe575fea42b92e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.2 MB (494212459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b2867229143a0ff011576a2796bf49d2c7a75b9ad18aff3772c4c35ad55777`
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
ENV JAVA_VERSION=17.0.19.0
# Fri, 01 May 2026 04:55:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 May 2026 04:55:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 04:55:38 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 May 2026 04:56:47 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 05:09:30 GMT
USER root
# Fri, 01 May 2026 05:09:30 GMT
ARG LIBERTY_VERSION=26.0.0.4-beta
# Fri, 01 May 2026 05:09:30 GMT
ARG LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e
# Fri, 01 May 2026 05:09:30 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip
# Fri, 01 May 2026 05:09:30 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 05:09:30 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 05:09:30 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 05:09:30 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.4-beta liberty.version=26.0.0.4-beta io.openliberty.version=26.0.0.4-beta
# Fri, 01 May 2026 05:09:30 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 01 May 2026 05:09:31 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 01 May 2026 05:09:31 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 01 May 2026 05:09:32 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 05:09:55 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 01 May 2026 05:09:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 May 2026 05:09:56 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 05:09:57 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 05:10:39 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 01 May 2026 05:10:39 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 05:10:39 GMT
USER 1001
# Fri, 01 May 2026 05:10:39 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 05:10:39 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 05:10:39 GMT
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
	-	`sha256:73189a25a3352c3753e616453541d65053722fa055f7ae16f6917a7d066a8012`  
		Last Modified: Fri, 01 May 2026 04:57:18 GMT  
		Size: 58.0 MB (58022967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffab9d03b1a173697b85dcf6367cd0b90155bc06c2fcd0935ad95b1c0130bd88`  
		Last Modified: Fri, 01 May 2026 04:57:16 GMT  
		Size: 3.9 MB (3866922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf4d1ef6e2736ea7a97d63a35e2003992d857860cbc79b78040e09827a62b4c`  
		Last Modified: Fri, 01 May 2026 05:10:26 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02847293888fdbd4bb5bb5eec4a42257f1f07c4d0c356a5c608831843f1fc3d3`  
		Last Modified: Fri, 01 May 2026 05:11:34 GMT  
		Size: 12.3 KB (12282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d07c08b03c8f2d3264cb03492a7464cea7aaa24ff513a3745b3e03687335a`  
		Last Modified: Fri, 01 May 2026 05:11:34 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bce31537e0f3c16f1435b09a813ae8b552d25d9ff63224f4b0b37eb993675f`  
		Last Modified: Fri, 01 May 2026 05:10:26 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b689ec084f2d3564cf4c822bb917ac6f239324ae1ef4c901fb5f0d6b7fa070c0`  
		Last Modified: Fri, 01 May 2026 05:11:42 GMT  
		Size: 371.2 MB (371164788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c64846693cb11792ccc42c9f01c90d9214d888a3aaecc836722d7925f6dca8`  
		Last Modified: Fri, 01 May 2026 05:11:34 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eb73a46fb3b04bf4092f22e492cc1f157174f38b106220aa121cb59a55af65`  
		Last Modified: Fri, 01 May 2026 05:11:35 GMT  
		Size: 13.7 KB (13720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a17bb9e55b7419bf5444d8410140467e02e43e0e6400af09dcf8be7765892e`  
		Last Modified: Fri, 01 May 2026 05:11:36 GMT  
		Size: 13.0 MB (12990259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:dd3c09a16d8c3959483b55121fc7b622dd521d5dc1ecdc931d8a86e402a01f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5ee7675a2c5d77258c417067dff4b71c19b160a4792ecb91918b97a1b9fb34`

```dockerfile
```

-	Layers:
	-	`sha256:a2c8fe80059f0f054f194cd7e222127f0712e982e964c44fc74a4c9394ee937a`  
		Last Modified: Fri, 01 May 2026 05:11:34 GMT  
		Size: 5.2 MB (5246293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecdb7e9a5063b04cbddcade1fd6eb72babec5852d201903ab52bbda6f7189712`  
		Last Modified: Fri, 01 May 2026 05:11:34 GMT  
		Size: 39.4 KB (39411 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; s390x

```console
$ docker pull open-liberty@sha256:d0ef4b47950fe9b7edbb5e2e029002bb92555317f11efe0267ff06b27fa684d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.9 MB (492908384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdfbfe9ecad155827e7836c5f480ee212c747f68bc6c022a785b2fcc489315f`
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
ENV JAVA_VERSION=17.0.19.0
# Thu, 30 Apr 2026 23:55:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3ce5bd7829e198408dd3e27825f096f79d19438ac1e96bc583a32d9580f1d3a6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_aarch64_linux_17.0.19.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='2dc4cfb4256642cfbea7fbe0edc30e79f995e7f1e01408876b88517b52cae4ad';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_ppc64le_linux_17.0.19.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b40a28e68e84461607a5d802fe6ddb7376e4a3d8e477b32bbe5c1cdf5638a7ed';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_x64_linux_17.0.19.0.tar.gz';          ;;        s390x)          ESUM='a9abce59480d62967ffe4a6c4b176a3e22bbef7e9ec9dd4cb58d23d5881f4d58';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.19.0/ibm-semeru-open-jre_s390x_linux_17.0.19.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:55:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:55:45 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:56:49 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:08:08 GMT
USER root
# Fri, 01 May 2026 00:08:08 GMT
ARG LIBERTY_VERSION=26.0.0.4-beta
# Fri, 01 May 2026 00:08:08 GMT
ARG LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e
# Fri, 01 May 2026 00:08:08 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip
# Fri, 01 May 2026 00:08:08 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:08:08 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:08:08 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:08:08 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.4-beta liberty.version=26.0.0.4-beta io.openliberty.version=26.0.0.4-beta
# Fri, 01 May 2026 00:08:08 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 01 May 2026 00:08:08 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 01 May 2026 00:08:09 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:08:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 01 May 2026 00:08:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 May 2026 00:08:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:08:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:08:59 GMT
# ARGS: LIBERTY_VERSION=26.0.0.4-beta LIBERTY_SHA=81b6404549e313f361d12681982c38448cf0b23e LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.4-beta/openliberty-runtime-26.0.0.4-beta.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 01 May 2026 00:08:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:08:59 GMT
USER 1001
# Fri, 01 May 2026 00:08:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:08:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:08:59 GMT
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
	-	`sha256:0701e4b840e35cb8e3275f5fb084ffb2f54db6dbd06ca8c2e453994952427a44`  
		Last Modified: Thu, 30 Apr 2026 23:57:09 GMT  
		Size: 58.3 MB (58298181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb4c2b5431d5ede0be346c9b6d7ca7e7be7d0b9eb37d9fc69df71cd8f36eab6`  
		Last Modified: Thu, 30 Apr 2026 23:57:08 GMT  
		Size: 5.2 MB (5172082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c686b2794fae054d447d3985b3afc2955cbb6ef188e7bb6154ba4d84be38ac`  
		Last Modified: Fri, 01 May 2026 00:09:38 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d500144f6ea88aaafd961c1ddcaf6572c7ca2cc7b94cfb19ad592d09f3c546`  
		Last Modified: Fri, 01 May 2026 00:09:38 GMT  
		Size: 12.3 KB (12281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b5b0e9d524fc178e90172c566dafc355dbea8abbcd6b562f4a9f7990fd09c8`  
		Last Modified: Fri, 01 May 2026 00:09:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b74a1827b4a8c14735bb810748e30b5c5c6272bc8dbed4508ff94a45908b53`  
		Last Modified: Fri, 01 May 2026 00:09:38 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f924f50616523160b686ecb9ffa0c6e529b1d3aeea16aab2a1810a7b1b17f`  
		Last Modified: Fri, 01 May 2026 00:09:47 GMT  
		Size: 371.2 MB (371164283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b312c022f1fe82bc2f5eb95e6e89eef6be4cf3773df69b5870cccc163005eb60`  
		Last Modified: Fri, 01 May 2026 00:09:39 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cc4b3e44732e5ad96f3b8f669e599be2b198a105dd0d7479cb6284dcc47e16`  
		Last Modified: Fri, 01 May 2026 00:09:39 GMT  
		Size: 13.7 KB (13718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179dad9036eb7621483cbd02fd4d9ec3c88138c7d7b374f76a108c30a70f6018`  
		Last Modified: Fri, 01 May 2026 00:09:39 GMT  
		Size: 15.2 MB (15182620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:b10db4c60b85aa206fe08cf69cdd660e99718d6494d460199c7753b8fe55cfee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b24a4514a79d0ff1239bba509752222e9890727f635e24746d47acdfae749a`

```dockerfile
```

-	Layers:
	-	`sha256:75ba5d3fbc9c0c68cf8778b2741783681fdac4962714098e5983e96929880442`  
		Last Modified: Fri, 01 May 2026 00:09:38 GMT  
		Size: 5.2 MB (5242668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1fb1f3184779b3fd959477172193a984f29258226c10b07ef43f75531047af7`  
		Last Modified: Fri, 01 May 2026 00:09:38 GMT  
		Size: 39.4 KB (39377 bytes)  
		MIME: application/vnd.in-toto+json
