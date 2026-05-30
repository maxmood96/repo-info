## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:12a84a0af75b8eac2725f51b3a7feb979d90536394e4f3a7396d8022cd812019
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

### `open-liberty:beta` - linux; amd64

```console
$ docker pull open-liberty@sha256:9b57252c0d1942a98cdbaf1cafa3acf814dd5c5cca9b1ab5912c8be2c147d46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.0 MB (486999292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf032e066b1b8eb8fc31e82b12f63c6ab092957e05f1727b7d0844530c405c3`
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
# Fri, 29 May 2026 23:03:46 GMT
USER root
# Fri, 29 May 2026 23:03:46 GMT
ARG LIBERTY_VERSION=26.0.0.6-beta
# Fri, 29 May 2026 23:03:46 GMT
ARG LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52
# Fri, 29 May 2026 23:03:46 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip
# Fri, 29 May 2026 23:03:46 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:03:46 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:03:46 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:03:46 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.6-beta liberty.version=26.0.0.6-beta io.openliberty.version=26.0.0.6-beta
# Fri, 29 May 2026 23:03:46 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:03:46 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:03:46 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:03:46 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:04:00 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:00 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:04:00 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:04:21 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:04:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:04:21 GMT
USER 1001
# Fri, 29 May 2026 23:04:21 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:04:21 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:04:21 GMT
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
	-	`sha256:b1677db79a2673752a590ad15dae7b5166848f01cb24fe0ad6946514546993bb`  
		Last Modified: Fri, 29 May 2026 23:04:47 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f26da8630e1c88f69e4f5fec7f7483f917ca0a23f3fef5540b6efa89fdba7`  
		Last Modified: Fri, 29 May 2026 23:04:47 GMT  
		Size: 12.8 KB (12778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff274bfc7d15a516e5d12398eec2893fb494b1598a9077e1a8ac4920579719f`  
		Last Modified: Fri, 29 May 2026 23:04:47 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be00f85c5a177366abe929888cbae0e6cf873ac158a6cf2277647a9187c6b864`  
		Last Modified: Fri, 29 May 2026 23:04:47 GMT  
		Size: 31.8 KB (31750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13cc2236d962552107207c7b6b92be86eb5b479ab3828300e328060623209cc`  
		Last Modified: Fri, 29 May 2026 23:04:56 GMT  
		Size: 371.4 MB (371400088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b052b2d966ba13f33b87634e7ba8ccf85a91aedbf353de8eb5dd03a34d41985`  
		Last Modified: Fri, 29 May 2026 23:04:48 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8d7f2284d636eb707f40e932320b57fb31cc66d54bcb38bc1d32308a556984`  
		Last Modified: Fri, 29 May 2026 23:04:48 GMT  
		Size: 14.2 KB (14216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5fada3eaa3725ef08903005c66de424795ff6c7df7799870e50c958c332b7d`  
		Last Modified: Fri, 29 May 2026 23:04:49 GMT  
		Size: 14.4 MB (14395362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:f41f0cdd1295be24b57a37e0388430a7fdadf77553e4b550e4f3379a5d19ab2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32530d87504952917bf5718f56096bfe57ca792d4584468c5080430589a65b5`

```dockerfile
```

-	Layers:
	-	`sha256:498e7c5466bb63d413684626d33d4d699333d7b29ce109c6b8b5e28b9db88979`  
		Last Modified: Fri, 29 May 2026 23:04:47 GMT  
		Size: 5.2 MB (5240626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b516c5efbceed5ff4c6be2db3d786bb5df51b00f41415e4e239a205b4f1e8a4`  
		Last Modified: Fri, 29 May 2026 23:04:47 GMT  
		Size: 39.4 KB (39356 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:f4d4f1634c15c536c360e6aed3d7210dfdaf74d77884fd364d799e9571577e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.1 MB (485122777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d3a6ae369121ccf0563757d52b4874b1ac10aa25e3fd46931dcc84524c79aa`
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
# Fri, 29 May 2026 23:03:43 GMT
USER root
# Fri, 29 May 2026 23:03:43 GMT
ARG LIBERTY_VERSION=26.0.0.6-beta
# Fri, 29 May 2026 23:03:43 GMT
ARG LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52
# Fri, 29 May 2026 23:03:43 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip
# Fri, 29 May 2026 23:03:43 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:03:43 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:03:43 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:03:43 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.6-beta liberty.version=26.0.0.6-beta io.openliberty.version=26.0.0.6-beta
# Fri, 29 May 2026 23:03:43 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:03:43 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:03:43 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:03:43 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:04:00 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:04:00 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:04:00 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:04:26 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:04:26 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:04:26 GMT
USER 1001
# Fri, 29 May 2026 23:04:26 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:04:26 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:04:26 GMT
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
	-	`sha256:0f0e2b467e5252926a868b14780667826eae5ce5c92b2f8baf4c236fa9496dcb`  
		Last Modified: Fri, 29 May 2026 23:04:52 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e6ee6658372f33c6ad71ccefb0b443adc42d287cb0441e3ac2afc78f1062a3`  
		Last Modified: Fri, 29 May 2026 23:04:52 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090f0bcb3fe3bb07cac0ac38c2aa9bf1e94b8b2a005dc2b6be9ac6ab1e02c65f`  
		Last Modified: Fri, 29 May 2026 23:04:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147eb97850e0c7f22287409ad158206a4af07f7f87f77b723f9b4b14e9ec49cf`  
		Last Modified: Fri, 29 May 2026 23:04:52 GMT  
		Size: 42.3 KB (42326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a3f16f384e5335ddd8a19099c887c2b7abe39e25b78489adbe82f9c1fbf7c4`  
		Last Modified: Fri, 29 May 2026 23:05:00 GMT  
		Size: 371.4 MB (371400405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2efcfbcbd48ca3da0088fe16359368556cf528869c7b02d2a2612424404cd63`  
		Last Modified: Fri, 29 May 2026 23:04:53 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcfc5c2912479686cf07caf7aeac36242e157598bf4a411f088d08635a0a826`  
		Last Modified: Fri, 29 May 2026 23:04:53 GMT  
		Size: 14.2 KB (14215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe1c2d28827f7ed90a214c9febdade50d3fe8c2e7b6998bcbc27dbffa50b43f`  
		Last Modified: Fri, 29 May 2026 23:04:54 GMT  
		Size: 14.0 MB (13984953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:fba6d878d25287a6877982e068c5bbec06b7c6ee948663d7d3417a57deb2bc97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0aee365e2bd3e3027d3e131d9ce020c4564826379a023d2ecaf704f81a1ada`

```dockerfile
```

-	Layers:
	-	`sha256:65db7483e9021ffb4afdb2f9bfd297869544c558c586ed001ba89998f6eb47d9`  
		Last Modified: Fri, 29 May 2026 23:04:52 GMT  
		Size: 5.2 MB (5241215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6722a55584cbc4f8fd194aacf2579cb18a7f33b9d3e79ffc4af288d3f2446b60`  
		Last Modified: Fri, 29 May 2026 23:04:52 GMT  
		Size: 39.5 KB (39484 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:b916c020055ed661921bd881094f15629922a1cb2895f346e5955771142777c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.0 MB (492024710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a284d9c9c8004d6adb0a932b6ef6c569bc704d341b931f43628a6febc2455f4e`
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
ARG LIBERTY_VERSION=26.0.0.6-beta
# Fri, 29 May 2026 23:02:53 GMT
ARG LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52
# Fri, 29 May 2026 23:02:53 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip
# Fri, 29 May 2026 23:02:53 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:02:53 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:02:53 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:02:53 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.6-beta liberty.version=26.0.0.6-beta io.openliberty.version=26.0.0.6-beta
# Fri, 29 May 2026 23:02:53 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:02:53 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:02:54 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:02:54 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:03:22 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:03:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:03:23 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:03:25 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:04:06 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:04:06 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:04:06 GMT
USER 1001
# Fri, 29 May 2026 23:04:06 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:04:06 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:04:06 GMT
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
	-	`sha256:77aa6c698e6e90fc1f600de10998b674b41756f743b4194105f17218d00ec610`  
		Last Modified: Fri, 29 May 2026 23:05:02 GMT  
		Size: 12.8 KB (12774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1237862956b005145c00e50a45fbd83b2c8fe6afcc08c23a5e2cf51d7f65ddb5`  
		Last Modified: Fri, 29 May 2026 23:05:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae9552e3e7e4a23fc9040633baf5dd7f1599555409d981082ece87cbde8610`  
		Last Modified: Fri, 29 May 2026 23:04:59 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e106a3a5172a6120bcaff174775becc3748ca0bf7d6a889093b64e0e0cf901`  
		Last Modified: Fri, 29 May 2026 23:05:10 GMT  
		Size: 371.4 MB (371400640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f522b1fa7fb98954f810933c6f3a3d1dcbaa6ef97a400d406e1f1361e1220e`  
		Last Modified: Fri, 29 May 2026 23:05:03 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c70ad4664bcc4305c6c87c64ddcc9ce9ec2531a187e779d4cbf15a7a990cc84`  
		Last Modified: Fri, 29 May 2026 23:05:03 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0dcb8e7f5d761c202eae43a2fd686fff592dc4fb9d8e73c5c4604ddfd481ef`  
		Last Modified: Fri, 29 May 2026 23:05:04 GMT  
		Size: 12.8 MB (12843215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:f54e3dcac18700bce3c315b2e0e6b8af561cc13f0a39fa1b2cacb3281fb5c5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8450f18f5ca701290db5f04d6618f738ead683420e2f6d2f87f1be17f13384`

```dockerfile
```

-	Layers:
	-	`sha256:db13dafbab3a804b5d7ab51256cbaebecd1fa28aaae2d411083181bc50347056`  
		Last Modified: Fri, 29 May 2026 23:05:02 GMT  
		Size: 5.2 MB (5245418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44e038b815fa802b85152666e3a2b4f457d9a29f3583a711564206798094bb3`  
		Last Modified: Fri, 29 May 2026 23:05:01 GMT  
		Size: 39.4 KB (39388 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:0cca083f5600590864cd4d1591826ba56429f59653cacb200b7d6afe09255319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.9 MB (490881194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b029760648183b14483174c749cb9469f02bd34fbbfbb35c687b15239ca45833`
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
ARG LIBERTY_VERSION=26.0.0.6-beta
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip
# Fri, 29 May 2026 23:03:04 GMT
ARG LIBERTY_BUILD_LABEL=cl260520260430-1602
# Fri, 29 May 2026 23:03:04 GMT
ARG OPENJ9_SCC=true
# Fri, 29 May 2026 23:03:04 GMT
ARG VERBOSE=false
# Fri, 29 May 2026 23:03:04 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260520260430-1602 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.6-beta liberty.version=26.0.0.6-beta io.openliberty.version=26.0.0.6-beta
# Fri, 29 May 2026 23:03:04 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 29 May 2026 23:03:04 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 29 May 2026 23:03:04 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 29 May 2026 23:03:05 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 29 May 2026 23:03:29 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 29 May 2026 23:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 29 May 2026 23:03:30 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 29 May 2026 23:03:30 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 29 May 2026 23:03:59 GMT
# ARGS: LIBERTY_VERSION=26.0.0.6-beta LIBERTY_SHA=56b9c6acd33a674d4d3a58ccad393423248b3f52 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.6-beta/openliberty-runtime-26.0.0.6-beta.zip LIBERTY_BUILD_LABEL=cl260520260430-1602 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 29 May 2026 23:03:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 29 May 2026 23:03:59 GMT
USER 1001
# Fri, 29 May 2026 23:03:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 29 May 2026 23:03:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 29 May 2026 23:03:59 GMT
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
	-	`sha256:3a19e4a0fd09b13849ae1ced44971756b6028d53f91603d256b3c79386b7872d`  
		Last Modified: Fri, 29 May 2026 23:04:38 GMT  
		Size: 12.8 KB (12775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1b516fe92b8e917020ddf7f73f9def7112d6977c61e52434b247aef5a37d1c`  
		Last Modified: Fri, 29 May 2026 23:04:38 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c057150ba73812b43e27c23c9c5ce7fe41dc13b57f34da020278a6644408571c`  
		Last Modified: Fri, 29 May 2026 23:04:38 GMT  
		Size: 33.1 KB (33113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31606983ff436ce873219ddac11631eb6c815f472d61c1e8c8da99042d950b74`  
		Last Modified: Fri, 29 May 2026 23:04:44 GMT  
		Size: 371.4 MB (371400101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a391969b2630032c7fab13e36148276c33919f4ebc70481ca2aeba1074d194fd`  
		Last Modified: Fri, 29 May 2026 23:04:39 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6036d41d10d8c2d4e712c5a5aef360143be71b2f35b5a6c709655ddf2684cf9e`  
		Last Modified: Fri, 29 May 2026 23:04:39 GMT  
		Size: 14.2 KB (14224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b333c94b6c0846efb63b6f34bc161b3dc4f0d211199153109aa93b64985f39`  
		Last Modified: Fri, 29 May 2026 23:04:40 GMT  
		Size: 14.5 MB (14458593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:7a815c13da4cec074a5cc59327ca6e77f8ef64d73b93da3eaa3b64207b2a5a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3044908c09787b33ec0ec3c57eb2e2651f2d6d38ff0bc818bb1065caefa1d0fb`

```dockerfile
```

-	Layers:
	-	`sha256:b1f16258f0c2fc741ad6d218c90377f3ca558eca5bdddd8b1cd943c6c0680b18`  
		Last Modified: Fri, 29 May 2026 23:04:38 GMT  
		Size: 5.2 MB (5242249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eace27b8552fd3519717fd247e491b242342853c072cc49b42337cbeb4f92993`  
		Last Modified: Fri, 29 May 2026 23:04:38 GMT  
		Size: 39.4 KB (39355 bytes)  
		MIME: application/vnd.in-toto+json
