## `open-liberty:full-java11-openj9`

```console
$ docker pull open-liberty@sha256:006404cb542f4da791f745e7269f75846cb3dd135cef1573aa17643849807aee
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

### `open-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:414a8e57b580b3688f7a06be6a744b23e630589e38edb58b3736a886e91524af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463165952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75ce6f39d9e5f7652d91edf0784498e8ba18f05a7a6860369ea20ef8045f4a8`
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
# Thu, 30 Apr 2026 23:44:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:44:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:44:55 GMT
ENV JAVA_VERSION=11.0.31.0
# Thu, 30 Apr 2026 23:44:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='587138f9b489026d0e9b733f5de5fe061079b59029993f7bf99ae8c79fcbce2d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_aarch64_linux_11.0.31.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b9b997d087549d7c9f054c1b755b13017dafccd21ab18a6f53fe856e2f83f20e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_ppc64le_linux_11.0.31.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e51820d8cb2f47c57d625943d0d65c0f2d10a06d88d6626fa7fa00fe4c1ecd44';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_x64_linux_11.0.31.0.tar.gz';          ;;        s390x)          ESUM='41ebc50a449603e813320c917f9ad66b26bbbbbd3a3ff32e8985e264b9115993';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_s390x_linux_11.0.31.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:44:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:44:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:46:00 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:11:37 GMT
USER root
# Fri, 01 May 2026 00:11:37 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 01 May 2026 00:11:37 GMT
ARG LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec
# Fri, 01 May 2026 00:11:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip
# Fri, 01 May 2026 00:11:37 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:11:37 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:11:37 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:11:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.3 liberty.version=26.0.0.3 io.openliberty.version=26.0.0.3
# Fri, 01 May 2026 00:11:37 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 01 May 2026 00:11:37 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 01 May 2026 00:11:37 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 01 May 2026 00:11:38 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:11:55 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 01 May 2026 00:11:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 May 2026 00:11:55 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:11:56 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:12:14 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 01 May 2026 00:12:14 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:12:14 GMT
USER 1001
# Fri, 01 May 2026 00:12:14 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:12:14 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:12:14 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855cf1f0ba4ff0e4e5105a883ec8fbe77e3ec7cdda83d219915ac27ccad64291`  
		Last Modified: Thu, 30 Apr 2026 23:46:12 GMT  
		Size: 12.8 MB (12805328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e17f1bc1581fcccb623dd0971b6dba127d74855effcb97a2575d2c017226356`  
		Last Modified: Thu, 30 Apr 2026 23:46:13 GMT  
		Size: 56.3 MB (56280537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e7c69ca9cef45d8929a714d2bdb7abdae76f6cae19381492e5741e66ca160d`  
		Last Modified: Thu, 30 Apr 2026 23:46:12 GMT  
		Size: 4.5 MB (4450238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d721dfc0594beac8239ec84424dc4da94947faaab7771944bcc2dedb2e63927`  
		Last Modified: Fri, 01 May 2026 00:12:37 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662320234106963ba8cb829f4818d3c5e3a9a885c02e123c448040eb3e5b59a1`  
		Last Modified: Fri, 01 May 2026 00:12:37 GMT  
		Size: 12.3 KB (12280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab79d89fa6c11952cfaf1663e7781ce176ac219b21319b4c2991942217df8b4`  
		Last Modified: Fri, 01 May 2026 00:12:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49be68175c95a15b5b2ff976bd2e83b1f3b926a763e549f46ccd63f7f54fcc2b`  
		Last Modified: Fri, 01 May 2026 00:12:37 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68084595d1bfeefb319b220447ca82e8005725b4547dec37cab619d448c27dcf`  
		Last Modified: Fri, 01 May 2026 00:12:46 GMT  
		Size: 346.5 MB (346511448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce4fbbae7361b796576ec7456cef704bdd6f7f178845d7180f01e7c4b2dc01b`  
		Last Modified: Fri, 01 May 2026 00:12:38 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff5c2e33c0b551fc464b791b3ec9a2c7233434ad275e7026fa2b1be20dffc06`  
		Last Modified: Fri, 01 May 2026 00:12:38 GMT  
		Size: 13.7 KB (13749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f74d001e378fd4f8ff0e454b07f19a132c1021c89a3253c044e4bf092ebcabe`  
		Last Modified: Fri, 01 May 2026 00:12:39 GMT  
		Size: 13.3 MB (13325300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:5ee24bb3183bf0aa894f1ddc6244830b41a448b1ae8757213d355f34ff3350ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c33f47ebbbf17d6c8cf4a95fb86a9b1ba03dcc95123f14df03e923f9d1892d9`

```dockerfile
```

-	Layers:
	-	`sha256:bdefda1cae89f4bc9f9d5b0d8b774c5a40902f8f5cb0cf32388cac3f3bfaf0cf`  
		Last Modified: Fri, 01 May 2026 00:12:37 GMT  
		Size: 5.2 MB (5159534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf511567425749d2a5562f8dccedc546554f86ea724dec6aaa357cde0441086`  
		Last Modified: Fri, 01 May 2026 00:12:37 GMT  
		Size: 39.3 KB (39259 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:51560bedbd87114946859a170dfc5b73ed0196e707e32cfe7877163de0c08dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.9 MB (459907144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b2cc9f499888f1d8afe6b3a920b6c7197da06dcb214edaca2cb43e63c361de`
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
# Thu, 30 Apr 2026 23:44:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:44:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Apr 2026 23:44:51 GMT
ENV JAVA_VERSION=11.0.31.0
# Thu, 30 Apr 2026 23:44:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='587138f9b489026d0e9b733f5de5fe061079b59029993f7bf99ae8c79fcbce2d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_aarch64_linux_11.0.31.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b9b997d087549d7c9f054c1b755b13017dafccd21ab18a6f53fe856e2f83f20e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_ppc64le_linux_11.0.31.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e51820d8cb2f47c57d625943d0d65c0f2d10a06d88d6626fa7fa00fe4c1ecd44';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_x64_linux_11.0.31.0.tar.gz';          ;;        s390x)          ESUM='41ebc50a449603e813320c917f9ad66b26bbbbbd3a3ff32e8985e264b9115993';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_s390x_linux_11.0.31.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:44:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:45:56 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:11:09 GMT
USER root
# Fri, 01 May 2026 00:11:09 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 01 May 2026 00:11:09 GMT
ARG LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec
# Fri, 01 May 2026 00:11:09 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip
# Fri, 01 May 2026 00:11:09 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:11:09 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:11:09 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:11:09 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.3 liberty.version=26.0.0.3 io.openliberty.version=26.0.0.3
# Fri, 01 May 2026 00:11:09 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 01 May 2026 00:11:09 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 01 May 2026 00:11:09 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 01 May 2026 00:11:09 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:11:32 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 01 May 2026 00:11:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 May 2026 00:11:32 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:11:32 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:11:55 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 01 May 2026 00:11:55 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:11:55 GMT
USER 1001
# Fri, 01 May 2026 00:11:55 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:11:55 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:11:55 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d42e71012d312a9431aa7e2e2e34a8e7e4da5cb5839bb027d2af2f4444749`  
		Last Modified: Thu, 30 Apr 2026 23:46:10 GMT  
		Size: 12.8 MB (12837772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcc198b8f4a0775d430689bdb0c3322cb808afb1a3943368ff9af3a5444ed55`  
		Last Modified: Thu, 30 Apr 2026 23:46:11 GMT  
		Size: 54.2 MB (54232415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbb232c2a5782022573c4323506af92d11b2b941f2181fbffdb0fa3eeab80b4`  
		Last Modified: Thu, 30 Apr 2026 23:46:09 GMT  
		Size: 4.3 MB (4281113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf221870155a616c230fbe317fdec74f7da506f2e1e58c024d5d52a1f3a871ce`  
		Last Modified: Fri, 01 May 2026 00:12:19 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142c959d3e58a76ab1b59e7e6aec771b2b4afbf568cd790481e2dba9dd12e905`  
		Last Modified: Fri, 01 May 2026 00:12:19 GMT  
		Size: 12.3 KB (12281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4f86550d992d24e2aa6fe44bd36e2a0d5451d62c8b9832895e939a84b0e37b`  
		Last Modified: Fri, 01 May 2026 00:12:19 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc46fc8eb8f0ebb8aecfa633d6e36e1a68d57f7bf53be4875957155630d1f2da`  
		Last Modified: Fri, 01 May 2026 00:12:19 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1821098280e96433a69c11e16c90e8bf8509cbd33a52c7ae25bdd5832015046f`  
		Last Modified: Fri, 01 May 2026 00:12:27 GMT  
		Size: 346.5 MB (346511622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583401c48c1c887f5752c165a98c08831f35a6cf49030af89a17fcc24792e532`  
		Last Modified: Fri, 01 May 2026 00:12:21 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e74202aa2814c5e8d3799f23c5b5a012236909b9608a9de30deecef3100e734`  
		Last Modified: Fri, 01 May 2026 00:12:21 GMT  
		Size: 13.7 KB (13720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a70f12ec40375f2aff00fdba979fc1f24edee04207f9d99468cbb9d8bb555f1`  
		Last Modified: Fri, 01 May 2026 00:12:21 GMT  
		Size: 13.1 MB (13097766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:c48c25a635b89b5b0ed0c1a68b79a2e2e63fa51a59642fa2ac4a30b0480ef338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5197451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945f55d18658a34cf803503ac712bea60493d3c921476b8145f1daa583da0a11`

```dockerfile
```

-	Layers:
	-	`sha256:5b60e61dd1b241316618ec428199769eba4cf6e57ac80f7e482d9a1458a87372`  
		Last Modified: Fri, 01 May 2026 00:12:20 GMT  
		Size: 5.2 MB (5158064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36a3ce941bdd4667334c4ba7880537b433002427edf5f5e9b15202ae4f53092`  
		Last Modified: Fri, 01 May 2026 00:12:19 GMT  
		Size: 39.4 KB (39387 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:02a015984f97ac6bfdc07e6059ca6fecf100c99bef04e84284db59f0caf21aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.5 MB (468455812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ad7fa469e0de457eb7cb8a38dd14d1868bf3396ded3a610ec12f1f98baa0c1`
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
ENV JAVA_VERSION=11.0.31.0
# Thu, 30 Apr 2026 23:47:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='587138f9b489026d0e9b733f5de5fe061079b59029993f7bf99ae8c79fcbce2d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_aarch64_linux_11.0.31.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b9b997d087549d7c9f054c1b755b13017dafccd21ab18a6f53fe856e2f83f20e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_ppc64le_linux_11.0.31.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e51820d8cb2f47c57d625943d0d65c0f2d10a06d88d6626fa7fa00fe4c1ecd44';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_x64_linux_11.0.31.0.tar.gz';          ;;        s390x)          ESUM='41ebc50a449603e813320c917f9ad66b26bbbbbd3a3ff32e8985e264b9115993';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_s390x_linux_11.0.31.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Apr 2026 23:47:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:47:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Apr 2026 23:48:16 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 00:19:17 GMT
USER root
# Fri, 01 May 2026 00:19:17 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 01 May 2026 00:19:17 GMT
ARG LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec
# Fri, 01 May 2026 00:19:17 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip
# Fri, 01 May 2026 00:19:17 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 00:19:17 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 00:19:17 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 00:19:17 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.3 liberty.version=26.0.0.3 io.openliberty.version=26.0.0.3
# Fri, 01 May 2026 00:19:17 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 01 May 2026 00:19:17 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 01 May 2026 00:19:17 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 01 May 2026 00:23:59 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 00:24:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 01 May 2026 00:24:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 May 2026 00:24:25 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 00:24:26 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 00:25:07 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 01 May 2026 00:25:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 00:25:07 GMT
USER 1001
# Fri, 01 May 2026 00:25:07 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 00:25:07 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 00:25:07 GMT
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
	-	`sha256:b08a61d045a66c408bcb49853bf52b4b7081d86b2de6cf76fe6c85bb79d59857`  
		Last Modified: Thu, 30 Apr 2026 23:48:41 GMT  
		Size: 58.2 MB (58237260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0aa9d26a1cd683ff21eeadbfd0e70cf336ccf821815f62aced4a13850786e3`  
		Last Modified: Thu, 30 Apr 2026 23:48:40 GMT  
		Size: 3.5 MB (3495351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59da1e25056c2d8f7141a90f0db3edb0354bfdf5c1a5a6ad7a71a83cb803fdf1`  
		Last Modified: Fri, 01 May 2026 00:22:18 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1422cb72397d178daf22800aea53e4b177dafd81b2fc25108b54f2f63b25c31c`  
		Last Modified: Fri, 01 May 2026 00:22:18 GMT  
		Size: 12.3 KB (12280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c0479da595daeb5fe8babc856345398a27d4b164ed0bb476b0b56ac0d21707`  
		Last Modified: Fri, 01 May 2026 00:22:18 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd2dcb8eecfcd4d444dfee3e97180df4c299fdf3ec5a66c56615ed4d0efd8df`  
		Last Modified: Fri, 01 May 2026 00:26:12 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617b490312534fe81e8b2766276f7ebc1e20497e05a3640f2927062a8484ed46`  
		Last Modified: Fri, 01 May 2026 00:26:20 GMT  
		Size: 346.5 MB (346511847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6381b20bc90d33e3be005c7638ce5da568d88bab62604de5ec3cbe91bb65d5ea`  
		Last Modified: Fri, 01 May 2026 00:26:12 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44c54879b5e5c6a1db0f08d88edf08fba854fc3cd27fdee5c11f1d6d207b77`  
		Last Modified: Fri, 01 May 2026 00:26:12 GMT  
		Size: 13.7 KB (13729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba91cf246fc22cef88ece7b2cca0638124db14940be39b6d164e9c6ee01114e4`  
		Last Modified: Fri, 01 May 2026 00:26:14 GMT  
		Size: 12.0 MB (12043828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:862064f3c77dc5e50fb08003a6fcb361d4b8994ace5a2b82468849d0ef300699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0098add88161d320a7e177cde7ddfcaa3af68cf15e8773968c7d002387d83eb`

```dockerfile
```

-	Layers:
	-	`sha256:a65f2f671037196aa39435ae9289044f310e8a4acf7fb33de81d6a5719cbbac9`  
		Last Modified: Fri, 01 May 2026 00:26:12 GMT  
		Size: 5.2 MB (5164156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5e3b7ef9427e28c1644001137fadd4fc3078ad6d272d8c199e2119e3b8882c`  
		Last Modified: Fri, 01 May 2026 00:26:12 GMT  
		Size: 39.3 KB (39293 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:c4cb9103416420ccbeb80b4a3ff5b24448c6d11090f41ec0a965013ec2809670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.2 MB (466237911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e67f1cfe024bb9fcc09840d408edbffc4610b5b6e40ae19d12266fad6628f91`
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
ENV JAVA_VERSION=11.0.31.0
# Fri, 01 May 2026 04:19:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='587138f9b489026d0e9b733f5de5fe061079b59029993f7bf99ae8c79fcbce2d';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_aarch64_linux_11.0.31.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b9b997d087549d7c9f054c1b755b13017dafccd21ab18a6f53fe856e2f83f20e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_ppc64le_linux_11.0.31.0.tar.gz';          ;;        amd64|x86_64)          ESUM='e51820d8cb2f47c57d625943d0d65c0f2d10a06d88d6626fa7fa00fe4c1ecd44';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_x64_linux_11.0.31.0.tar.gz';          ;;        s390x)          ESUM='41ebc50a449603e813320c917f9ad66b26bbbbbd3a3ff32e8985e264b9115993';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.31.0/ibm-semeru-open-jre_s390x_linux_11.0.31.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 May 2026 04:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 04:19:38 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 May 2026 04:20:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="82b15278a7bfa2685c80e07963c43246df4fd742d574b608a68f5ce67c6ffde0eff3e224cc9809925cc6bf7002a190c3bf420f50c0e4052467d3e665efc84a54";     TOMCAT_VERSION="9.0.117";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 01 May 2026 05:09:18 GMT
USER root
# Fri, 01 May 2026 05:09:18 GMT
ARG LIBERTY_VERSION=26.0.0.3
# Fri, 01 May 2026 05:09:18 GMT
ARG LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec
# Fri, 01 May 2026 05:09:18 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip
# Fri, 01 May 2026 05:09:18 GMT
ARG LIBERTY_BUILD_LABEL=cl260320260309-1102
# Fri, 01 May 2026 05:09:18 GMT
ARG OPENJ9_SCC=true
# Fri, 01 May 2026 05:09:18 GMT
ARG VERBOSE=false
# Fri, 01 May 2026 05:09:18 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260320260309-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.3 liberty.version=26.0.0.3 io.openliberty.version=26.0.0.3
# Fri, 01 May 2026 05:09:18 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 01 May 2026 05:09:19 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 01 May 2026 05:09:19 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 01 May 2026 05:09:19 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 01 May 2026 05:09:37 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 01 May 2026 05:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 May 2026 05:09:38 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 01 May 2026 05:09:38 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 01 May 2026 05:10:02 GMT
# ARGS: LIBERTY_VERSION=26.0.0.3 LIBERTY_SHA=afc4c71987b5f04b13f48be172de92edba612cec LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.3/openliberty-runtime-26.0.0.3.zip LIBERTY_BUILD_LABEL=cl260320260309-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 01 May 2026 05:10:02 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 May 2026 05:10:02 GMT
USER 1001
# Fri, 01 May 2026 05:10:02 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 01 May 2026 05:10:02 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 May 2026 05:10:02 GMT
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
	-	`sha256:743013867de7f4a1fc79d77bf36472a366d9ced49e2d3eb4d0aa697c129ce394`  
		Last Modified: Fri, 01 May 2026 04:21:03 GMT  
		Size: 58.4 MB (58400840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581e218fbdbd99269133a85a10601d3fceea4860e77fe66a2c2c17adf14dbce9`  
		Last Modified: Fri, 01 May 2026 04:21:03 GMT  
		Size: 4.6 MB (4608341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87353f03ad0235507d07b9a5e1f49b292dca4d1589790ccdca4a41886ddb0f16`  
		Last Modified: Fri, 01 May 2026 05:09:51 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620a8458f65a1de05bb1111765087e2c1682e7dcf3291c7b6d2ffdb5860e2029`  
		Last Modified: Fri, 01 May 2026 05:10:36 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8b74f41b124b389426d67ed95bbd039de3892e081f0ad9f17366e23063c047`  
		Last Modified: Fri, 01 May 2026 05:10:36 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d23d799457f0c637832054d5e76e32dc4ecec0c24dbd78ea4f76ece206c43`  
		Last Modified: Fri, 01 May 2026 05:09:51 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef59b9378d01c9fad2eb07d50d351be76bd19429fb47eebb2ce471e2e82e68ca`  
		Last Modified: Fri, 01 May 2026 05:10:43 GMT  
		Size: 346.5 MB (346511326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb40ada7cbf72c62c3a2bdf09f7bd648ba423ecd7d89d4c7fbe12a8cf364d48a`  
		Last Modified: Fri, 01 May 2026 05:10:36 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af912261a568e08140dcaf4b526a41834cabf1ded1a944a4cff8dae901e0501`  
		Last Modified: Fri, 01 May 2026 05:10:37 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923ef00c5601e27086afc61a7a42de9a0acbe2031df6ce52f3714e46073bb1cf`  
		Last Modified: Fri, 01 May 2026 05:10:37 GMT  
		Size: 13.6 MB (13626398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:dd8dbd266e280aea741e940ce07230b7f3b91d639f87ca198958dcfd695bd8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6dbb8dd765e5d0940e83ef0f09dab4ecc77ddc643c6dda08213e0acd5fa23d`

```dockerfile
```

-	Layers:
	-	`sha256:c906e418a8b98d34a7490926238bd21286d698965d2205498a72ba640c5a50dc`  
		Last Modified: Fri, 01 May 2026 05:10:36 GMT  
		Size: 5.2 MB (5160531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa4c6e3f86ef6a60ca8b057926b03c07dc14bc927da27a91b5c54de7e363fbb`  
		Last Modified: Fri, 01 May 2026 05:10:36 GMT  
		Size: 38.5 KB (38455 bytes)  
		MIME: application/vnd.in-toto+json
