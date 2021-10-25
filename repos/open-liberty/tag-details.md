<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `open-liberty`

-	[`open-liberty:21.0.0.10-full-java11-openj9`](#open-liberty210010-full-java11-openj9)
-	[`open-liberty:21.0.0.10-full-java8-openj9`](#open-liberty210010-full-java8-openj9)
-	[`open-liberty:21.0.0.10-kernel-slim-java11-openj9`](#open-liberty210010-kernel-slim-java11-openj9)
-	[`open-liberty:21.0.0.10-kernel-slim-java8-openj9`](#open-liberty210010-kernel-slim-java8-openj9)
-	[`open-liberty:21.0.0.6-full-java11-openj9`](#open-liberty21006-full-java11-openj9)
-	[`open-liberty:21.0.0.6-full-java8-openj9`](#open-liberty21006-full-java8-openj9)
-	[`open-liberty:21.0.0.6-kernel-slim-java11-openj9`](#open-liberty21006-kernel-slim-java11-openj9)
-	[`open-liberty:21.0.0.6-kernel-slim-java8-openj9`](#open-liberty21006-kernel-slim-java8-openj9)
-	[`open-liberty:21.0.0.9-full-java11-openj9`](#open-liberty21009-full-java11-openj9)
-	[`open-liberty:21.0.0.9-full-java8-openj9`](#open-liberty21009-full-java8-openj9)
-	[`open-liberty:21.0.0.9-kernel-slim-java11-openj9`](#open-liberty21009-kernel-slim-java11-openj9)
-	[`open-liberty:21.0.0.9-kernel-slim-java8-openj9`](#open-liberty21009-kernel-slim-java8-openj9)
-	[`open-liberty:beta`](#open-libertybeta)
-	[`open-liberty:beta-java11`](#open-libertybeta-java11)
-	[`open-liberty:full`](#open-libertyfull)
-	[`open-liberty:full-java11-openj9`](#open-libertyfull-java11-openj9)
-	[`open-liberty:full-java8-openj9`](#open-libertyfull-java8-openj9)
-	[`open-liberty:kernel-slim`](#open-libertykernel-slim)
-	[`open-liberty:kernel-slim-java11-openj9`](#open-libertykernel-slim-java11-openj9)
-	[`open-liberty:kernel-slim-java8-openj9`](#open-libertykernel-slim-java8-openj9)
-	[`open-liberty:latest`](#open-libertylatest)

## `open-liberty:21.0.0.10-full-java11-openj9`

```console
$ docker pull open-liberty@sha256:18ade53b9bb479a28ea0ec8edf335cf0fb9a3b538ec3bdfd1d5ac42cdb2c8928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; s390x

### `open-liberty:21.0.0.10-full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:205b65b739c0a8c727e03b56944152c3046bca1bb0e0592e12d658511a7561ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288770133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5846840154a9a91544098819e60d165c89785e2cb7bd41064c001a27a021365`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:33 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:46:46 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:46:46 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:46:46 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:46:46 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:46:46 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:46:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:47:00 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:47:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:47:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:47:24 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:47:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:47:24 GMT
USER 1001
# Mon, 25 Oct 2021 21:47:24 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:47:25 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:47:25 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8124847c3d3a4fc8a36afa327d390084543a32726a22362c42bd2d19c5ef63c8`  
		Last Modified: Mon, 25 Oct 2021 21:54:12 GMT  
		Size: 8.6 KB (8553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6aefa1a20c5156363a19d38ee873ddfdb646511399b82e69ee5e5b92fb9fe5d`  
		Last Modified: Mon, 25 Oct 2021 21:54:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f649aafd4597a1ab1adafb6706bd52a78d1da20dcbd36645a7c4d26c3d2ba8`  
		Last Modified: Mon, 25 Oct 2021 21:54:19 GMT  
		Size: 185.2 MB (185168480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf85ba74c69e45298027c8ee38dd695f7072d3d94bd4d8d07ba46fd9f47f6ee9`  
		Last Modified: Mon, 25 Oct 2021 21:54:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace210521e2fb01bdbe08fcbff6d705107b5f799e13603a324970f55ba84a56`  
		Last Modified: Mon, 25 Oct 2021 21:54:11 GMT  
		Size: 10.0 KB (10039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9ec737f89ab005e35b631f2c29a0b495c2a9fc0c33ab969a4f02bb06a613dc`  
		Last Modified: Mon, 25 Oct 2021 21:54:13 GMT  
		Size: 13.1 MB (13145435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.10-full-java8-openj9`

```console
$ docker pull open-liberty@sha256:311838991be429f48e965d3dbae69fce875f3c2eed434545d9d50bfa5960ab88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; s390x

### `open-liberty:21.0.0.10-full-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:2f3ab64a31db098c609d95705017615d6009423940e97a5dedd486c04e756db1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291780673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf7411b5e6c96f094adab004b3e241498114fdc2dbea18b790fe2c7df61ed06`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:57 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:57 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:57 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:57 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:58 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:58 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:46:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:46:14 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:46:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:46:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:46:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:46:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:46:35 GMT
USER 1001
# Mon, 25 Oct 2021 21:46:35 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:46:35 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:46:35 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe4bf612a292a411455e4db7024f1fb1bac92ab7ef206436a15aa8293e62a2`  
		Last Modified: Mon, 25 Oct 2021 21:53:55 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c5943e5e87b26ebb1312db484cfc931302cbea3604e82aab88b8d529be7cef`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f78318a0320256dac4eb5702c2bff0615a5bea5661fb0b5a797a28513074b10`  
		Last Modified: Mon, 25 Oct 2021 21:54:01 GMT  
		Size: 185.2 MB (185168476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32cd122dc8e75095ad0a6ce27422c754815614825acf3ea5fa984b1682c2575`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f732eec10818b415067f0854ce1829e5147a04ef91f673e12fda5031832bc39a`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 10.0 KB (10045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d9add8f18e2677ef67b834b2a8c717032332d9b88adc07ad455f329d99f2b0`  
		Last Modified: Mon, 25 Oct 2021 21:53:55 GMT  
		Size: 10.7 MB (10730333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.10-kernel-slim-java11-openj9`

```console
$ docker pull open-liberty@sha256:b18f0e90827056b4805860e0c94795a0a3b49d044c304aef8a177b85a2a35f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; s390x

### `open-liberty:21.0.0.10-kernel-slim-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:231f02999d50ad0ab33f0bb275d62d1b3a47b04a230f99bd0db0bf1d3e64275e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104651047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171d07da0525fe515b735591b016a57d149843dfb97850cd843fa6115968fdf7`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:33 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:33 GMT
ARG LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af
# Mon, 25 Oct 2021 21:45:33 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:34 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:34 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:34 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:35 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:35 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:35 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:36 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:45:41 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:45:42 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:45:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:45:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:45:49 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:45:49 GMT
USER 1001
# Mon, 25 Oct 2021 21:45:50 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:45:50 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:45:50 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec76c8b07a8a35285c2524fd76139cdadd8850ccba033b45ea00917a27459f8d`  
		Last Modified: Mon, 25 Oct 2021 21:53:48 GMT  
		Size: 8.1 KB (8112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb0774c4b567cf5d1a7248d7d06a2a598718bd59ca6b06cf10a050e78fac8f`  
		Last Modified: Mon, 25 Oct 2021 21:53:47 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fe5b77d17a7b3c1e555aa766240e510cf55e0daf702cc1b99faa8075fc6c8d`  
		Last Modified: Mon, 25 Oct 2021 21:53:48 GMT  
		Size: 11.8 MB (11786097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f5f040f7bbd59796baab5963cdb84537c1a85d9fde8804cdd0da8decc1aa66`  
		Last Modified: Mon, 25 Oct 2021 21:53:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175124c11857f7835c72353f388987a22dad13d051424f3da97e60a40584111b`  
		Last Modified: Mon, 25 Oct 2021 21:53:47 GMT  
		Size: 9.2 KB (9218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53bd4f0cb8774be028ddadacb21bd3a653d2344acb39c18ba05a8f5e3ae4362`  
		Last Modified: Mon, 25 Oct 2021 21:53:47 GMT  
		Size: 2.4 MB (2410309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.10-kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:c22a5fd43ddf7078046175e0df97b9d90121449e27f8dfa30d6ef0d86af7bdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; s390x

### `open-liberty:21.0.0.10-kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:85d93a89be886bcfab89ce28491baff004cbdefd76061bad08a88215b409376c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109872436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec451c7cd54b3219c83acb577d49406e9cd89440ac8b0b7a3be789c67d4749d5`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:13 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:13 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:13 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:13 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:13 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:45:18 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:45:18 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:45:20 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:45:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:45:26 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:45:26 GMT
USER 1001
# Mon, 25 Oct 2021 21:45:26 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:45:26 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:45:26 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b1ad1b31bd01a80fa85db59606256029eca2d393e89251041211546d1a5a21`  
		Last Modified: Mon, 25 Oct 2021 21:53:40 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdf2a3f92a2ad7565c633127b41e7401f8c7dd3ad63dd12221f07a4b4f26f12`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05105f34fb305c8ba555f9e2bdeb844c0326dff5b4b22b66aad4d06d333e29`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 11.8 MB (11786095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bf0fcf5391cc8ded7c49089974ffb18c71b18a7ffce6109bc0b7eb9d02d2d9`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62004e8bc5c2bf69149404446b3b7549896e021fc6e8d6fb44d3749915b2722f`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 9.2 KB (9213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9a5dcf6e2ab7c858bd9fdbeb37c699275d91617f047a5cbadf49136899e3a2`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 2.2 MB (2206062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.6-full-java11-openj9`

```console
$ docker pull open-liberty@sha256:71418c9d31e37127c756cbe159adaa09ccd6240393f41a3e88f10c8f971f1992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:21.0.0.6-full-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:935149da22f848dc3af8e74449c29c5304cc677cd543a81df80da652c3015e3a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 MB (290626916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3af3741ab45ec92b212e74c5b26dd7fd6c3f7a55e04e7fbc06f891cad41d55b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:28:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 01 Oct 2021 03:29:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:30:22 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:44:37 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Fri, 01 Oct 2021 08:45:50 GMT
ARG LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0
# Fri, 01 Oct 2021 08:45:50 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Fri, 01 Oct 2021 08:45:50 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip
# Fri, 01 Oct 2021 08:45:50 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:45:50 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:45:51 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:45:51 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:45:51 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Fri, 01 Oct 2021 08:45:51 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:45:51 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:46:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:46:01 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:46:03 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:46:03 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:46:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:46:36 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:46:36 GMT
USER 1001
# Fri, 01 Oct 2021 08:46:36 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:46:36 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:46:37 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec736696f208ef0ec33b06d703a533976c7a35abe201ae6ee68f6405bc58ed`  
		Last Modified: Fri, 01 Oct 2021 03:39:56 GMT  
		Size: 44.4 MB (44382131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a366c184fa8e3539f73433cd4c7e09a1df30ee1e2ed35e509f090ab08dd34813`  
		Last Modified: Fri, 01 Oct 2021 03:39:50 GMT  
		Size: 4.1 MB (4138880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc3918c27db5075418b414735fea315af72060ee8768de8ee994d8e3d695658`  
		Last Modified: Fri, 01 Oct 2021 08:49:29 GMT  
		Size: 8.5 KB (8548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c6282f6d1b7431f7e297f8dc3fb85699036aa03c7248b7c816567d841bb12`  
		Last Modified: Fri, 01 Oct 2021 08:49:27 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c1d359588ea4f50ec885cbac523a8e65e317b078a68440a6286b7facaa02a0`  
		Last Modified: Fri, 01 Oct 2021 08:49:36 GMT  
		Size: 183.7 MB (183659194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9dbd47fdb56ee97c9228768cba3142cae0b9e9a459063c2d2b9436ddc9e46e`  
		Last Modified: Fri, 01 Oct 2021 08:49:27 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc8b0bde3cfcedb99c5e55951c5f3cbade3e127be157d6affd9e358bc992466`  
		Last Modified: Fri, 01 Oct 2021 08:49:27 GMT  
		Size: 10.0 KB (10039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a65577530c34e997a57640e5eb369176db0978c41abdf72a6b5ed879b6357`  
		Last Modified: Fri, 01 Oct 2021 08:49:29 GMT  
		Size: 13.8 MB (13823709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.6-full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:f4988a8639f7305aafaf369b2b64431bb9fdc6c5747d647f45d9e81a43fe753e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294682908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8761e1de759d3e988ddc68f0d8ecca543d5e6f7db6f90b6f7f185f7e21edf85f`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:12:53 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 06 Oct 2021 17:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:15:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:16:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:47:30 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Thu, 07 Oct 2021 09:52:34 GMT
ARG LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0
# Thu, 07 Oct 2021 09:52:38 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Thu, 07 Oct 2021 09:52:41 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip
# Thu, 07 Oct 2021 09:52:49 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:52:59 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:53:13 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:53:17 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:53:22 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Thu, 07 Oct 2021 09:53:26 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:53:29 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:54:08 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:54:15 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:54:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:54:41 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:55:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:55:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:55:52 GMT
USER 1001
# Thu, 07 Oct 2021 09:55:57 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:56:02 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:56:05 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a1310fddd70f7d129e09b08a85ca9a02ec9984d9e11434200a57a656453fa`  
		Last Modified: Wed, 06 Oct 2021 17:31:09 GMT  
		Size: 45.1 MB (45104806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b2a8e4fb8f2ea78e7be40e998ec639e4a7c6ee4a536b67cf4aebb4c1a25fe6`  
		Last Modified: Wed, 06 Oct 2021 17:31:01 GMT  
		Size: 3.3 MB (3294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fbb07d008f4c92354252d8287039b4c46b8ed5f551a7ffee3c35786b98ba9e`  
		Last Modified: Thu, 07 Oct 2021 10:00:42 GMT  
		Size: 8.6 KB (8553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc26237c30dfd7789ef8ab96a9808a1b4587fdb873e0e131ae3ca5ee70ea5709`  
		Last Modified: Thu, 07 Oct 2021 10:00:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cde1d987f9fad6a5bb7c9e9b1bdf9c43470bbb16336c4c2467995a2dfdedf8a`  
		Last Modified: Thu, 07 Oct 2021 10:00:55 GMT  
		Size: 183.7 MB (183659589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a9c2fc561f8cba0749566154eeaa75e2de6c89bfae9881d5a90eb6bd5b0e67`  
		Last Modified: Thu, 07 Oct 2021 10:00:39 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6099a1befad485828e43fa31cc098d163700ea5729d3d02cf37b09b7f06f649`  
		Last Modified: Thu, 07 Oct 2021 10:00:39 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741f27bc8e368fa9341b256fca97f4e6e48143b35d98287e631b77e204fb0ddf`  
		Last Modified: Thu, 07 Oct 2021 10:00:42 GMT  
		Size: 12.1 MB (12102097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.6-full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:9167a9495d3e37be6783c9036a315be2bf33a125b7ec7e2faf04912d74151389
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287271782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4434925c02e5789ef4e8a4526ea39feddea6e26c2f2ec7478ba5af91f56d64f0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:50:28 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Mon, 25 Oct 2021 21:51:28 GMT
ARG LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0
# Mon, 25 Oct 2021 21:51:28 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Mon, 25 Oct 2021 21:51:28 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip
# Mon, 25 Oct 2021 21:51:28 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:51:28 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:51:29 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:51:29 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:51:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Mon, 25 Oct 2021 21:51:29 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:51:29 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:51:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:51:43 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:51:44 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:51:45 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:52:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:52:08 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:52:08 GMT
USER 1001
# Mon, 25 Oct 2021 21:52:08 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:52:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:52:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec91eb295874dbf2129c2d74f316240b48118a8c715f3a44c78b9e3f7d57314`  
		Last Modified: Mon, 25 Oct 2021 21:55:35 GMT  
		Size: 8.5 KB (8549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf492d2b545a12cce747e8d6e43d449eab3723933c42ddc64cf711f1baaa9862`  
		Last Modified: Mon, 25 Oct 2021 21:55:34 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c78ba5832d0a39f42255a5edc1a373b19f803a64bf836d2e44e3b1f38559a48`  
		Last Modified: Mon, 25 Oct 2021 21:55:42 GMT  
		Size: 183.7 MB (183657834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee80eea7680066a47c48dc5cf1317932b38772e488ef2f9bed6411d969ec7c2`  
		Last Modified: Mon, 25 Oct 2021 21:55:34 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c29681315130f5898040c68b08efbb283d9f14e7d25441491e1ee34c3091909`  
		Last Modified: Mon, 25 Oct 2021 21:55:34 GMT  
		Size: 10.0 KB (10039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef7b88ecfa193d84e4b3aa6da203afd599e75305493ad7f8f0aadebcc287c11`  
		Last Modified: Mon, 25 Oct 2021 21:55:36 GMT  
		Size: 13.2 MB (13157726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.6-full-java8-openj9`

```console
$ docker pull open-liberty@sha256:9e4ab0f5f6f6ee711b3d17985e13aec3c43699cbe7bd0f6e365ee9289b200d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:21.0.0.6-full-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:cb70fbe2e48105090a471fe42569279939d0c554b6f8ba6282477c5cc639233c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295658100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab16c081e2fd638762d0234cd9e17767a955931a7fb41cba44f2a468d0c312b0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:44:15 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Fri, 01 Oct 2021 08:44:58 GMT
ARG LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0
# Fri, 01 Oct 2021 08:44:58 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Fri, 01 Oct 2021 08:44:59 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip
# Fri, 01 Oct 2021 08:44:59 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:44:59 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:44:59 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:44:59 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:45:00 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Fri, 01 Oct 2021 08:45:00 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:45:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:45:12 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:45:13 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:45:14 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:45:14 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:45:44 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:45:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:45:45 GMT
USER 1001
# Fri, 01 Oct 2021 08:45:45 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:45:45 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:45:45 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eac5ae2e1485f8b11ed60b02d44110aa244641165b84d2a145a25fa01954c6c`  
		Last Modified: Fri, 01 Oct 2021 08:49:13 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ed909f08a6d9ae8d99770c0572c2c55c24c470a5abe6bee8ad00b825e518c`  
		Last Modified: Fri, 01 Oct 2021 08:49:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba229567766d8273e9ba5a8221e3728736227d1335854b8f5af7f9b0ea3a0a8f`  
		Last Modified: Fri, 01 Oct 2021 08:49:20 GMT  
		Size: 183.7 MB (183659199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12719baa22b2d7da211b202d7d70ece5899a6974a7eb1567e954fa05d46fb708`  
		Last Modified: Fri, 01 Oct 2021 08:49:10 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1e114067be4a8dda9dc452c62faa25d735e3dd0ab88c5a18582ef85a8fa15c`  
		Last Modified: Fri, 01 Oct 2021 08:49:11 GMT  
		Size: 10.0 KB (10043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b245c030b9476d0e6a9f5155f949b59d6305738ff870effb191ea80bed173`  
		Last Modified: Fri, 01 Oct 2021 08:49:13 GMT  
		Size: 13.4 MB (13374887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.6-full-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:4682bc54926288bc070cefbb7f7094b1fc07b60763265f9b8c36c40a1a82f311
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300069757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9922440f7542904d7c2c273dc3af631f2300267a6fadc6079a5a0d22f28802`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:45:13 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Thu, 07 Oct 2021 09:49:37 GMT
ARG LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0
# Thu, 07 Oct 2021 09:49:40 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Thu, 07 Oct 2021 09:49:43 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip
# Thu, 07 Oct 2021 09:49:46 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:49:48 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:49:51 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:49:54 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:49:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Thu, 07 Oct 2021 09:50:00 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:50:01 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:50:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:50:46 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:50:52 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:51:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:51:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:51:55 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:52:03 GMT
USER 1001
# Thu, 07 Oct 2021 09:52:09 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:52:15 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:52:21 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b3fc96e9669a78210e50857b4e8d6d7d3be6acbb41496cac67bfa5de5d0c2e`  
		Last Modified: Thu, 07 Oct 2021 10:00:16 GMT  
		Size: 8.6 KB (8553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c57d2e89db565a30a21a6a82a60fc3082d94bcd95e38778d8daa2791d259b2`  
		Last Modified: Thu, 07 Oct 2021 10:00:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb302dfa83beeb016561393c7006c1dbe1911b74b788b5b319689284d7541e73`  
		Last Modified: Thu, 07 Oct 2021 10:00:29 GMT  
		Size: 183.7 MB (183659613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737b9517371f467cdc40cec4af5f6e4817287fc2b06b21aa01647cb1d5867572`  
		Last Modified: Thu, 07 Oct 2021 10:00:13 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e72a9dc505d131b46a6597f20a2da8c19ae6cdf62c13faa6b8eea8c8c16c3`  
		Last Modified: Thu, 07 Oct 2021 10:00:13 GMT  
		Size: 10.1 KB (10067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4d4990ea21999ae32c38994a1685d020ed330efb0af5c9a52c88cb6c785af7`  
		Last Modified: Thu, 07 Oct 2021 10:00:15 GMT  
		Size: 11.9 MB (11888119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.6-full-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:55b0a47e0497bdc488cff0f300fdc831878a42ebcaa166e18aa2980b7d4e4a27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1f12bf925d50bb2b70ec58cd101f16c480187c97114333dfab8830687722bb`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:50:09 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Mon, 25 Oct 2021 21:50:46 GMT
ARG LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0
# Mon, 25 Oct 2021 21:50:46 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Mon, 25 Oct 2021 21:50:46 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip
# Mon, 25 Oct 2021 21:50:46 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:50:46 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:50:46 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:50:46 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:50:46 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Mon, 25 Oct 2021 21:50:47 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:50:47 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:50:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:51:01 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:51:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:51:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:51:21 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.6/openliberty-runtime-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=7889471c63088e0eed6984c503c06ae49a1f43c0 LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:51:22 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:51:22 GMT
USER 1001
# Mon, 25 Oct 2021 21:51:22 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:51:22 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:51:22 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2f630b2f56e10ed9aee4f6e542f34bd6bbe42594aaf844cd1eab7b02530976`  
		Last Modified: Mon, 25 Oct 2021 21:55:22 GMT  
		Size: 8.6 KB (8551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6de5bd941b9d32c56e95e5279080e5b99486f92a73e2d4066f076536a16b3d`  
		Last Modified: Mon, 25 Oct 2021 21:55:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dd12b9265876b36df7f305c4700464d3102d9caaf54d59c12dbc4c23a4051d`  
		Last Modified: Mon, 25 Oct 2021 21:55:28 GMT  
		Size: 183.7 MB (183657801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d222d0f194f0cf44aedc5f107e45e79ad52b1d8a3adff2be9639f7f756ab5`  
		Last Modified: Mon, 25 Oct 2021 21:55:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19748b5b0d6fc51b22b14638701be2648c4ad4169173398ec0b7c8e5d26f7ff6`  
		Last Modified: Mon, 25 Oct 2021 21:55:21 GMT  
		Size: 10.0 KB (10043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91322960a3fb415ff135b0b66d05d46b1c876306f3aac459aec81b9387261ced`  
		Last Modified: Mon, 25 Oct 2021 21:55:22 GMT  
		Size: 10.7 MB (10691754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.6-kernel-slim-java11-openj9`

```console
$ docker pull open-liberty@sha256:7b371c2e26335a489767d2ac04b3119d156846093dd714264ee199e309ad7f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:21.0.0.6-kernel-slim-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:b41f090a7826542799f90010d6c12a6bfbeb525e51409e252ca520696fda443e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107419430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7d1b08aacb99970e49acdc74a90b9ab8b92f69076958d400b67b9a82db431e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:28:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 01 Oct 2021 03:29:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:30:22 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:44:37 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Fri, 01 Oct 2021 08:44:37 GMT
ARG LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d
# Fri, 01 Oct 2021 08:44:37 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Fri, 01 Oct 2021 08:44:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip
# Fri, 01 Oct 2021 08:44:37 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:44:38 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:44:38 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:44:38 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:44:38 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Fri, 01 Oct 2021 08:44:38 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:44:39 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:44:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:44:44 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:44:45 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:44:46 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:44:53 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:44:54 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:44:54 GMT
USER 1001
# Fri, 01 Oct 2021 08:44:54 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:44:54 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:44:54 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec736696f208ef0ec33b06d703a533976c7a35abe201ae6ee68f6405bc58ed`  
		Last Modified: Fri, 01 Oct 2021 03:39:56 GMT  
		Size: 44.4 MB (44382131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a366c184fa8e3539f73433cd4c7e09a1df30ee1e2ed35e509f090ab08dd34813`  
		Last Modified: Fri, 01 Oct 2021 03:39:50 GMT  
		Size: 4.1 MB (4138880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca31b40c234e4b44f37e01e5b5dcf9e08a34397b1d930b84f7f20825036dfde`  
		Last Modified: Fri, 01 Oct 2021 08:49:04 GMT  
		Size: 8.1 KB (8110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24517ea8eac00e075e3aa0855689e96e3def63ae1ecc50e26f93ab26d0da0140`  
		Last Modified: Fri, 01 Oct 2021 08:49:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9184673bc3ee3b5e806bccf653e4e65f68340a1fb8f8a258a3da3092c730c65`  
		Last Modified: Fri, 01 Oct 2021 08:49:03 GMT  
		Size: 11.8 MB (11777521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3294c980ad42a663ac26212795aa7032ef669477d13b55e01f234990459c05e`  
		Last Modified: Fri, 01 Oct 2021 08:49:02 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62177ae13cd02e9eb921b0b9114292fe12aa3a354cda5fdcd272fdbd92a455e`  
		Last Modified: Fri, 01 Oct 2021 08:49:02 GMT  
		Size: 9.2 KB (9219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54ad7525d53e32a9d727d62be03c1a822cea8998f746a94c58dc81e6b7d2a0e`  
		Last Modified: Fri, 01 Oct 2021 08:49:03 GMT  
		Size: 2.5 MB (2499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.6-kernel-slim-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:83295c4d028ba10584e3008c9ad2022cdc90c49562db489c0e6189673dc268a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113117676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08a3f16cdec0d5b832144267d7b9351d4cee37f60cb5fff178942b375181083`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:12:53 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 06 Oct 2021 17:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:15:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:16:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:47:30 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Thu, 07 Oct 2021 09:47:35 GMT
ARG LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d
# Thu, 07 Oct 2021 09:47:37 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Thu, 07 Oct 2021 09:47:39 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip
# Thu, 07 Oct 2021 09:47:42 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:47:47 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:47:55 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:47:58 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:48:00 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Thu, 07 Oct 2021 09:48:01 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:48:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:48:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:48:28 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:48:40 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:48:52 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:49:06 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:49:08 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:49:10 GMT
USER 1001
# Thu, 07 Oct 2021 09:49:13 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:49:15 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:49:19 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a1310fddd70f7d129e09b08a85ca9a02ec9984d9e11434200a57a656453fa`  
		Last Modified: Wed, 06 Oct 2021 17:31:09 GMT  
		Size: 45.1 MB (45104806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b2a8e4fb8f2ea78e7be40e998ec639e4a7c6ee4a536b67cf4aebb4c1a25fe6`  
		Last Modified: Wed, 06 Oct 2021 17:31:01 GMT  
		Size: 3.3 MB (3294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf61c874ce536c0ba33f8fa880a996eee1109ecf16a4ce6bda457796a87e27d2`  
		Last Modified: Thu, 07 Oct 2021 10:00:02 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa791273689a3db5a5dc30cb0072f64382faccae8a2a47c21e9b114c9c10da80`  
		Last Modified: Thu, 07 Oct 2021 10:00:00 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a78c9c367f7e3eedfe6f10d5312334d58548f56b7fbf28dd8735ee62e3e8267`  
		Last Modified: Thu, 07 Oct 2021 10:00:01 GMT  
		Size: 11.8 MB (11777958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3712d3c60b6ea27deedc4eccc62e140728181172903d10275399532cb8f146a0`  
		Last Modified: Thu, 07 Oct 2021 10:00:00 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fba9e42fc4b740b69b9ad527f67afac52bd87f53179418c9002aebc84ad03b4`  
		Last Modified: Thu, 07 Oct 2021 10:00:00 GMT  
		Size: 9.2 KB (9234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9053a605879a5086f69ce41979458ac512330c3f2defed73125035be899de771`  
		Last Modified: Thu, 07 Oct 2021 10:00:00 GMT  
		Size: 2.4 MB (2420091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.6-kernel-slim-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:257b219a4b7d30945a84d3203db680a45a1279f369f47ee747a28eb72c5be5c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104633283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc3fd36b0bec88ce2dbaebf39c24ff2f6e966a15c5d25b00e7cecbe0f3c3f80`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:50:28 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Mon, 25 Oct 2021 21:50:28 GMT
ARG LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d
# Mon, 25 Oct 2021 21:50:28 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Mon, 25 Oct 2021 21:50:28 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip
# Mon, 25 Oct 2021 21:50:28 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:50:28 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:50:28 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:50:29 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:50:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Mon, 25 Oct 2021 21:50:29 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:50:29 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:50:33 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:50:33 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:50:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:50:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:50:39 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:50:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:50:40 GMT
USER 1001
# Mon, 25 Oct 2021 21:50:40 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:50:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:50:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2367657e9b28a7aa71d3799b605215db31fa5b392e8d6c2f5a60d3e0f3fde8`  
		Last Modified: Mon, 25 Oct 2021 21:55:16 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a737afe2c44c8529116eccdd8e8a3e2c47d0ffd882892eb1f1a533306638209`  
		Last Modified: Mon, 25 Oct 2021 21:55:15 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d225f6c390db4ddee22a73f2c87fb5541e5e85a5e37f8931f2aa4c641c1e3cb3`  
		Last Modified: Mon, 25 Oct 2021 21:55:16 GMT  
		Size: 11.8 MB (11776254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe5da4d03a32db12d634b24ae899f031ff729d9e0cbce15613f5d190b19d4a1`  
		Last Modified: Mon, 25 Oct 2021 21:55:15 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a4a956b4385573078aa40c85f9e89f57bf798e65a37d3023d293eaa1692142`  
		Last Modified: Mon, 25 Oct 2021 21:55:15 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975a6a391ea50f9e521d961cc061e3e8ac7a17795cce21cdf88ca2cf865800be`  
		Last Modified: Mon, 25 Oct 2021 21:55:15 GMT  
		Size: 2.4 MB (2402396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.6-kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:57f112379dab9f22b507df4fe33c4bb04debc0fe70915be2f77e8d57803d85e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:21.0.0.6-kernel-slim-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:34dfdc814d5b465aab72c1c24b74a4b9160e3a0e9c558aa4d643f93151c4dfb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112863275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18815f1f32817f85d5299ab3d3ffd177ad07b1337b922452178c0432bc797e3c`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:44:15 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Fri, 01 Oct 2021 08:44:15 GMT
ARG LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d
# Fri, 01 Oct 2021 08:44:15 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Fri, 01 Oct 2021 08:44:16 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip
# Fri, 01 Oct 2021 08:44:16 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:44:16 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:44:16 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:44:16 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:44:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Fri, 01 Oct 2021 08:44:17 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:44:17 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:44:22 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:44:22 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:44:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:44:24 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:44:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:44:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:44:31 GMT
USER 1001
# Fri, 01 Oct 2021 08:44:31 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:44:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:44:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c38e0eec092c5d07ecf915f52da4a42e78647532043b5f3102cb27fafee155`  
		Last Modified: Fri, 01 Oct 2021 08:48:55 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a18468a2c127ba872cab72713948f2014a565d01d349e3d44f9361b994d9b7b`  
		Last Modified: Fri, 01 Oct 2021 08:48:53 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa31f1f7751510c4bcfe6b2d882a7735e626e057f123d7008425c78cc3387b81`  
		Last Modified: Fri, 01 Oct 2021 08:48:54 GMT  
		Size: 11.8 MB (11777527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4fbb933d66afb74a46ac7c5e6f2ae111de17de28849b5d9da52c83e1275e14`  
		Last Modified: Fri, 01 Oct 2021 08:48:53 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab53ea548546f48cc4c3bea497f5fc07ace1cde97b916f34c3046198039eda0`  
		Last Modified: Fri, 01 Oct 2021 08:48:53 GMT  
		Size: 9.2 KB (9213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e3b1806721e981eb7b04ddb40a3afe381b0bd414bcd6471628c8eba48b23f4`  
		Last Modified: Fri, 01 Oct 2021 08:48:54 GMT  
		Size: 2.5 MB (2463328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.6-kernel-slim-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:6f07138c59bf1877fbd26b49451bca383c6522a133fc6a60e39d64d2269bc897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118688962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c9f8fc88ce54fdd9fdf53e3962e7f29c93f06d3cb993d9a8fd891634149a7f`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:45:13 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Thu, 07 Oct 2021 09:45:18 GMT
ARG LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d
# Thu, 07 Oct 2021 09:45:20 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Thu, 07 Oct 2021 09:45:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip
# Thu, 07 Oct 2021 09:45:27 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:45:30 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:45:35 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:45:40 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:45:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Thu, 07 Oct 2021 09:45:43 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:45:44 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:46:04 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:46:08 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:46:14 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:46:25 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:46:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:46:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:47:05 GMT
USER 1001
# Thu, 07 Oct 2021 09:47:09 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:47:14 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:47:16 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a1077ca42e86466ccc635115f533ba2ccd07e24a6e93e5d3453f2f6bee2b33`  
		Last Modified: Thu, 07 Oct 2021 09:59:51 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3f77d89cbd196e7b43b365dcb4ca4506a9e2069da73fea6b87622b89243c26`  
		Last Modified: Thu, 07 Oct 2021 09:59:48 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cccf43ea527805479cd691df0a23db9216edba89eaa42818b29c6178eeeb5a2`  
		Last Modified: Thu, 07 Oct 2021 09:59:50 GMT  
		Size: 11.8 MB (11777985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1731fd2c0188a98b4342dfe5fb22b0be93b7ad9f27c3a248a8a5e10d79da72`  
		Last Modified: Thu, 07 Oct 2021 09:59:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e8466217b82fd679108c9a1864861296e4b239240ad0acbe1a574a82b38a4c`  
		Last Modified: Thu, 07 Oct 2021 09:59:48 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b884cdbd47ae5346553188430bd1fc187ca743b21ff741b20aedec5a3705fc`  
		Last Modified: Thu, 07 Oct 2021 09:59:49 GMT  
		Size: 2.4 MB (2390547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.6-kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:1fa84223c2c1067e512eef6967cfbff7babf82f6a30691458a90c02bfee0ec8c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109888420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9762406dbe5f6e5821df467049c21e412ba02e067541aaa8003560eb19cd0c`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:50:09 GMT
ARG LIBERTY_VERSION=21.0.0.6
# Mon, 25 Oct 2021 21:50:10 GMT
ARG LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d
# Mon, 25 Oct 2021 21:50:10 GMT
ARG LIBERTY_BUILD_LABEL=cl210620210527-1900
# Mon, 25 Oct 2021 21:50:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip
# Mon, 25 Oct 2021 21:50:10 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:50:10 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:50:10 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:50:10 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:50:10 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.6
# Mon, 25 Oct 2021 21:50:11 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:50:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:50:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:50:15 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:50:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:50:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:50:21 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210620210527-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.6/openliberty-kernel-21.0.0.6.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=8e84896e5c09c188d3ac0e25b5bb3759b954411d LIBERTY_VERSION=21.0.0.6 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:50:22 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:50:22 GMT
USER 1001
# Mon, 25 Oct 2021 21:50:22 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:50:22 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:50:22 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99e8de65bd9c6cf85d8f0bf4d06ed4c3a55bbda6210be21ecc807008be1b7b2`  
		Last Modified: Mon, 25 Oct 2021 21:55:10 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be36580dba830233943ddbaac1cb30575e670cd6a822c8cb9ba499582e06c21`  
		Last Modified: Mon, 25 Oct 2021 21:55:09 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b4f6a63cf154fbc72af1fc2363d1aa325eec43710c93d3a75aed55fafda0fb`  
		Last Modified: Mon, 25 Oct 2021 21:55:10 GMT  
		Size: 11.8 MB (11776283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e413edd2108011e27a2fe5bfcce3ef3def2da7e2685076c8ddafb3bf2230c30`  
		Last Modified: Mon, 25 Oct 2021 21:55:09 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decd024034d080742bbf2efddae794cfdc4277e9dd1b1ea192a535939aaaba77`  
		Last Modified: Mon, 25 Oct 2021 21:55:09 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00be50598935e6bb066c442eead4cbe2d5d0cb6d655e4419e6309f9cb7040c28`  
		Last Modified: Mon, 25 Oct 2021 21:55:09 GMT  
		Size: 2.2 MB (2231865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.9-full-java11-openj9`

```console
$ docker pull open-liberty@sha256:79c214188f9ae3b96415c8b4c9b67f9bec5cef74316663ffeb142341773b68db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:21.0.0.9-full-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:ad6683c36d46d14ac4abb1a582d3d2e7069f5b4005d26761b496b4719998612a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291986030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a615a8621f694363a4bc939334f5e96fa74023ef5a5233acebf1b8d38fef3d6b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:28:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 01 Oct 2021 03:29:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:30:22 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:43:14 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Fri, 01 Oct 2021 08:43:14 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:43:14 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Fri, 01 Oct 2021 08:43:14 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:43:15 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:43:15 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:43:15 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:43:15 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:43:15 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:43:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:43:25 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:43:26 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:43:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:43:28 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:44:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:44:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:44:01 GMT
USER 1001
# Fri, 01 Oct 2021 08:44:01 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:44:01 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:44:01 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec736696f208ef0ec33b06d703a533976c7a35abe201ae6ee68f6405bc58ed`  
		Last Modified: Fri, 01 Oct 2021 03:39:56 GMT  
		Size: 44.4 MB (44382131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a366c184fa8e3539f73433cd4c7e09a1df30ee1e2ed35e509f090ab08dd34813`  
		Last Modified: Fri, 01 Oct 2021 03:39:50 GMT  
		Size: 4.1 MB (4138880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b11e4c50c1b02b9a8706b186dfbe76f4278043ca6101c5a8792ff97ed3e435`  
		Last Modified: Fri, 01 Oct 2021 08:48:28 GMT  
		Size: 8.6 KB (8550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67df32056e1c2b9c176bdb4270f98a8e281e1f217b9068a394179c26e74c5b68`  
		Last Modified: Fri, 01 Oct 2021 08:48:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac59e11cab494c2d4b273f52f6453fff0f5560ea9d3440a886c186a7eb113e8`  
		Last Modified: Fri, 01 Oct 2021 08:48:35 GMT  
		Size: 185.1 MB (185116257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d094d2326011485c88ab379bbbcb38507e819ab3a2cc268704eae112fefc768d`  
		Last Modified: Fri, 01 Oct 2021 08:48:26 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950372e3490412fa753e90d15f40555bdc459d3465dafd590d7d5a47a01607d7`  
		Last Modified: Fri, 01 Oct 2021 08:48:26 GMT  
		Size: 10.1 KB (10050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7946107fa3dbb996f07c021bb28d3e710b91eefd6218b1032c9663d03dfc654`  
		Last Modified: Fri, 01 Oct 2021 08:48:28 GMT  
		Size: 13.7 MB (13725741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.9-full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:d77beeb050d34bd616d5dc116494788b79d4d627b3b4538aedec046d2fc17c07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296116248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a4eb54c4fc7bdfe65042d5ad425721637a538ff18fdded4a47050465222426`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:12:53 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 06 Oct 2021 17:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:15:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:16:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:36:47 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:42:12 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Thu, 07 Oct 2021 09:42:15 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:42:19 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Thu, 07 Oct 2021 09:42:23 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:42:29 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:42:32 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:42:36 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:42:39 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:42:40 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:42:41 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:43:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:43:30 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:43:38 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:43:45 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:44:32 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:44:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:44:39 GMT
USER 1001
# Thu, 07 Oct 2021 09:44:41 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:44:44 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:44:46 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a1310fddd70f7d129e09b08a85ca9a02ec9984d9e11434200a57a656453fa`  
		Last Modified: Wed, 06 Oct 2021 17:31:09 GMT  
		Size: 45.1 MB (45104806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b2a8e4fb8f2ea78e7be40e998ec639e4a7c6ee4a536b67cf4aebb4c1a25fe6`  
		Last Modified: Wed, 06 Oct 2021 17:31:01 GMT  
		Size: 3.3 MB (3294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff059797ed1f184c8aac6e5256dcfb7fd8ebb286356e28d2353578470fb8e4a3`  
		Last Modified: Thu, 07 Oct 2021 09:59:12 GMT  
		Size: 8.6 KB (8555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f508ea2c10cfd383e8a262339c7a7ed13a6d4d6fcd5e60990889f576298946`  
		Last Modified: Thu, 07 Oct 2021 09:59:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dcec252deb51906965be50afea11c90e822016bf7f98c93dc5124b215bd75e`  
		Last Modified: Thu, 07 Oct 2021 09:59:26 GMT  
		Size: 185.1 MB (185116709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af8c16719d8ad457ecc0a06726d664da4247a6c6286100686cc32da3274fff`  
		Last Modified: Thu, 07 Oct 2021 09:59:10 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094df81cde1ef780ca6632039745748f94d48e33058b662fbaf512040703d38`  
		Last Modified: Thu, 07 Oct 2021 09:59:10 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e8f891aead6727972c39846183eaf2713f9b5f8d743cad8c33d710b482567`  
		Last Modified: Thu, 07 Oct 2021 09:59:12 GMT  
		Size: 12.1 MB (12078324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.9-full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:b2e6622ef4f4e167f6e7c266a9bcde00fce9b4241bb355cf643017b8aaea37c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288617306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2241c22de863e2e284b4f35a1709bb2ec4ddd8deabb83d3df66e96541d6ea8`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:48:14 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Mon, 25 Oct 2021 21:49:21 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Mon, 25 Oct 2021 21:49:21 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Mon, 25 Oct 2021 21:49:21 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Mon, 25 Oct 2021 21:49:21 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:49:21 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:49:21 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:49:22 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:49:22 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Mon, 25 Oct 2021 21:49:22 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:49:22 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:49:32 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:49:36 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:49:36 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:49:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:49:59 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:50:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:50:00 GMT
USER 1001
# Mon, 25 Oct 2021 21:50:00 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:50:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:50:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704d9d055235a3584bb483fa0eb0c441a81208ee5d0ea27ca47fcee08f28420`  
		Last Modified: Mon, 25 Oct 2021 21:54:56 GMT  
		Size: 8.6 KB (8550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d182ccf22da7088398b99606860f8491c15b9c6e51ee299461bc77c5d68401e`  
		Last Modified: Mon, 25 Oct 2021 21:54:55 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0545891eb3c9dc2db28c7853f2b4b829ece857ec000ef5131bb81d541b4b9b28`  
		Last Modified: Mon, 25 Oct 2021 21:55:04 GMT  
		Size: 185.1 MB (185115052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c43342e1518d0675c5d02e63ac85085157d466f163e2b674564d0ffe4eba92`  
		Last Modified: Mon, 25 Oct 2021 21:54:55 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2dcc71a2ee93d7692a80df36b04511b4e3208e0a1ec525fe60cc52ac5f36b2`  
		Last Modified: Mon, 25 Oct 2021 21:54:55 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2e6fa527e4914b6efeb8239c1ff2712a3e2c1052f12c9d97485c2a81a026a5`  
		Last Modified: Mon, 25 Oct 2021 21:54:57 GMT  
		Size: 13.0 MB (13046028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.9-full-java8-openj9`

```console
$ docker pull open-liberty@sha256:eb044197ffde551060f52b1af1558d1a2b990465ffc4d6ce70e07c642a2956e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:21.0.0.9-full-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:11332203189a2473abc6b01619fa6f3900eedd17c71cd587d390a0943b8a429e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297155113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc833487bd0e5c53b41f16e6f5290cfbf405d8aacd93d73e2193fc88e53ecb9`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:42:23 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Fri, 01 Oct 2021 08:42:23 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:42:24 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:24 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:42:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:42:25 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:42:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:42:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:42:35 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:42:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:43:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:43:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:43:08 GMT
USER 1001
# Fri, 01 Oct 2021 08:43:08 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:43:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:43:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09679318c11692d08f483aac1e7a8d344749aa9b9ef495d0c0d581925d5fbf`  
		Last Modified: Fri, 01 Oct 2021 08:48:06 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f515bcbf2cee10d004afc0f02659f37d3d73159d551e065ad7f3e27c3c846c`  
		Last Modified: Fri, 01 Oct 2021 08:48:05 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23662dd8572b0c37fa42fc96f4da78cdfa818d709f83236844890e3f10f0d92d`  
		Last Modified: Fri, 01 Oct 2021 08:48:13 GMT  
		Size: 185.1 MB (185116246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e334ab7e07d9250054a58457a3153053eb46e9a08e9db80984f622e6e84b61`  
		Last Modified: Fri, 01 Oct 2021 08:48:04 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f22529ca6d49cb869d4f0a455c10dc84d966c4d0922244e452a79893ccea623`  
		Last Modified: Fri, 01 Oct 2021 08:48:04 GMT  
		Size: 10.0 KB (10043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9024c9b4674915436af1db7e8dbd20208fbdc716c9eacef5c76aab2b380fa9fd`  
		Last Modified: Fri, 01 Oct 2021 08:48:06 GMT  
		Size: 13.4 MB (13414860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.9-full-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:794d918ef4ab904c026742fee33b3cfd956e82f0c691b2dfba495f681834ca52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301578145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14426d0b0a72ec4d2872543ca1caff24d41513e71fa69e3e241b21664f1479de`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:34:23 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:38:59 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Thu, 07 Oct 2021 09:39:02 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:39:04 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Thu, 07 Oct 2021 09:39:11 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:39:13 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:39:14 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:39:19 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:39:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:39:45 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:39:52 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:40:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:40:30 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:40:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:40:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:41:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:41:47 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:41:49 GMT
USER 1001
# Thu, 07 Oct 2021 09:41:55 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:41:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:42:02 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaeab81cf835a89f1f403c833945d3b554a82588d98c3a010f7a3c7a44fb7d3`  
		Last Modified: Thu, 07 Oct 2021 09:58:40 GMT  
		Size: 8.6 KB (8551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3597446a2d59ddb34b461f023cc3db1ac1723905a3519e42869034df823998df`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ad0e3fe0fa97901df249fb8016cd38c70de162a82c3df588fdc2bf6abbd43d`  
		Last Modified: Thu, 07 Oct 2021 09:58:54 GMT  
		Size: 185.1 MB (185116681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dba658c8a8e6fe991c93dbf05105bd9f2544f66bbda7ad4c47403fd2a06b087`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92bb1230ea89c90a826b0b9b6170dc57b42b86e1852d2aff7baed7c06e5aec4`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa3b298a46f54f3c87de572f3e9128bddd47b4c59cb136ca93f36e6ae0d13a2`  
		Last Modified: Thu, 07 Oct 2021 09:58:40 GMT  
		Size: 11.9 MB (11939449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.9-full-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:a26868b350067c9dcd6444e384ab5c96fc0b98aae3d8b1fe4c08bed8519af19d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291706501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04432693cc50eb5bc0cd3a8deb21bf6098d8ea6a63f06881a7fff17913d8932d`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:47:55 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Mon, 25 Oct 2021 21:48:32 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Mon, 25 Oct 2021 21:48:32 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Mon, 25 Oct 2021 21:48:32 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Mon, 25 Oct 2021 21:48:32 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:48:32 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:48:32 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:48:33 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:48:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Mon, 25 Oct 2021 21:48:33 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:48:33 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:48:46 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:48:49 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:48:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:48:51 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:49:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:49:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:49:11 GMT
USER 1001
# Mon, 25 Oct 2021 21:49:11 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:49:11 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:49:11 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e732975672746f683bf54875cd104ca1ddfc3ad3612dbdc55dc24bd0629c1`  
		Last Modified: Mon, 25 Oct 2021 21:54:43 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe94bac9e12ec03d1dba1f328e9eebc2e7754bcca4d0fed20f2fde57bbc573`  
		Last Modified: Mon, 25 Oct 2021 21:54:42 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77655ac57420a1e4009ea96221bf5c0e653a11b5e8771a288860fdc56db80fcb`  
		Last Modified: Mon, 25 Oct 2021 21:54:50 GMT  
		Size: 185.1 MB (185115026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b41d4eaff13b8287a413a522e80c9f976bb58100e4f7e053fc6349c21ac669`  
		Last Modified: Mon, 25 Oct 2021 21:54:42 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e090182b4a37886938249e4b15b9d3b7664847e5c9c7caae6c6d3570dc2398ab`  
		Last Modified: Mon, 25 Oct 2021 21:54:43 GMT  
		Size: 10.0 KB (10041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4110dccb50296e8a4d6d8a158139f1ac2c257dfde689d1c7c9e3b133152d3fef`  
		Last Modified: Mon, 25 Oct 2021 21:54:43 GMT  
		Size: 10.7 MB (10709608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.9-kernel-slim-java11-openj9`

```console
$ docker pull open-liberty@sha256:98f0b44c691319a3f33b6ec140063b68815f842026c34dce626206f6132589aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:21.0.0.9-kernel-slim-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:fd85ed9965d69066ba5f500e16305d52b079810453ece0a7fdcf69d57be34082
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107354289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d5bb2ed9b99ad255d097dfe891ddab7cd3578d2842346360546f40cc74e909`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:28:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 01 Oct 2021 03:29:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:30:22 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:42:03 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:42:03 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:03 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:42:03 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:42:03 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:42:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:42:08 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:42:09 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:42:11 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:42:18 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:42:18 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:42:19 GMT
USER 1001
# Fri, 01 Oct 2021 08:42:19 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:42:19 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:42:19 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec736696f208ef0ec33b06d703a533976c7a35abe201ae6ee68f6405bc58ed`  
		Last Modified: Fri, 01 Oct 2021 03:39:56 GMT  
		Size: 44.4 MB (44382131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a366c184fa8e3539f73433cd4c7e09a1df30ee1e2ed35e509f090ab08dd34813`  
		Last Modified: Fri, 01 Oct 2021 03:39:50 GMT  
		Size: 4.1 MB (4138880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df8db31bcb70d33d52014722f3dcb73c9622591e9076cb39ba938b7ba40812`  
		Last Modified: Fri, 01 Oct 2021 08:47:58 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07f5fec8291be9e6554efcdc0fc907de763ce4e8fb711e16c2a072a2022600a`  
		Last Modified: Fri, 01 Oct 2021 08:47:55 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643224f731958d64ac998dc6f3d79b64fba58f9210a3d3aa4f833d2fa935e1df`  
		Last Modified: Fri, 01 Oct 2021 08:47:57 GMT  
		Size: 11.8 MB (11771793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79d569b0b62fca5e541213788e001cf2e12cf14c34c6617f463f0ade3e63fba`  
		Last Modified: Fri, 01 Oct 2021 08:47:56 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc508143cd1ab9fe48e3c4e5f354e794557feb6922b28babf79374cb2c396e0a`  
		Last Modified: Fri, 01 Oct 2021 08:47:56 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106d16a667cffec2e90c489e959831a4f39b11b1ee80c29b1bc9d199df637315`  
		Last Modified: Fri, 01 Oct 2021 08:47:56 GMT  
		Size: 2.4 MB (2440063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.9-kernel-slim-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:37a52cea31a7e54bc5aee1a232e8fb71f16a53146aa7b13854e917ee8ffe0c1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113119683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ca8c72763a32f21981bd9276369cb8339960c5e768993648f0ae040307efb8`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:12:53 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 06 Oct 2021 17:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:15:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:16:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:36:47 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:36:50 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Thu, 07 Oct 2021 09:36:52 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:36:57 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Thu, 07 Oct 2021 09:37:02 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:37:07 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:37:09 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:37:12 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:37:16 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:37:19 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:37:21 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:37:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:37:45 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:37:54 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:38:05 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:38:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:38:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:38:31 GMT
USER 1001
# Thu, 07 Oct 2021 09:38:39 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:38:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:38:42 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a1310fddd70f7d129e09b08a85ca9a02ec9984d9e11434200a57a656453fa`  
		Last Modified: Wed, 06 Oct 2021 17:31:09 GMT  
		Size: 45.1 MB (45104806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b2a8e4fb8f2ea78e7be40e998ec639e4a7c6ee4a536b67cf4aebb4c1a25fe6`  
		Last Modified: Wed, 06 Oct 2021 17:31:01 GMT  
		Size: 3.3 MB (3294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77a776270f036e23a394e0f196fa6617071bd8916f2b3fdc7d2149cee88d128`  
		Last Modified: Thu, 07 Oct 2021 09:58:30 GMT  
		Size: 8.1 KB (8112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9370437329e3e0991c6fe3d2d7c47f693f0020d00a89c0389d39741827108693`  
		Last Modified: Thu, 07 Oct 2021 09:58:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e805c18cccc0ae65f71e6f7fc618b990f1b2b3f8330ecc8822d5c7c5cdf15f30`  
		Last Modified: Thu, 07 Oct 2021 09:58:29 GMT  
		Size: 11.8 MB (11772211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dbd5c72767e0e80a5d56871d6f74fb823a892b48cf43a29344e8bb4ee380ab`  
		Last Modified: Thu, 07 Oct 2021 09:58:27 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac807dcf69663fd62af1f830fda7fecc96ed8097f82cc8841f75e1ed03597507`  
		Last Modified: Thu, 07 Oct 2021 09:58:28 GMT  
		Size: 9.2 KB (9241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453045ef5698149ef343f00461510678878f2c950fa57fb622d7ed9a0cc7363f`  
		Last Modified: Thu, 07 Oct 2021 09:58:28 GMT  
		Size: 2.4 MB (2427834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.9-kernel-slim-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:756f8a623fa595cb721e0cf3de692022ee4bf8c205a5ba05b8dce87b012db4dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104671197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4332dc3229f3b41ba293dc3c449c3a9c8818dda0e4cb415a585a4d66c43c192e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:48:14 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Mon, 25 Oct 2021 21:48:14 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Mon, 25 Oct 2021 21:48:14 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Mon, 25 Oct 2021 21:48:14 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Mon, 25 Oct 2021 21:48:14 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:48:14 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:48:15 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:48:15 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:48:15 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Mon, 25 Oct 2021 21:48:15 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:48:15 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:48:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:48:19 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:48:20 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:48:21 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:48:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:48:26 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:48:26 GMT
USER 1001
# Mon, 25 Oct 2021 21:48:26 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:48:26 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:48:26 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571787375cdf44ee06253ae70db154229efc5f925549de9d64dc64c4a7103d15`  
		Last Modified: Mon, 25 Oct 2021 21:54:38 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b072ec44165f79a7db2a5d3151868ebf72353eff2cc2dbe54a4a392cf1b7ce6c`  
		Last Modified: Mon, 25 Oct 2021 21:54:37 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9f8c47d2b76df2c72635e684e6ae3017f587c90a137d5ff99170579ba75a6b`  
		Last Modified: Mon, 25 Oct 2021 21:54:38 GMT  
		Size: 11.8 MB (11770454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d779e68b9b783be2970119d8741bacae6def2a8a048e26b8f0da92062330a9e`  
		Last Modified: Mon, 25 Oct 2021 21:54:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c633dbbed1c07460e3a8a2f55cb032d58fcef5363e8277163385de0583aca13`  
		Last Modified: Mon, 25 Oct 2021 21:54:37 GMT  
		Size: 9.2 KB (9211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0126d8c6d5483311a1ff5f818fa029640e2603522122acd1e4746145997b9759`  
		Last Modified: Mon, 25 Oct 2021 21:54:37 GMT  
		Size: 2.4 MB (2446111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:21.0.0.9-kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:68d4c25ba698422d2b931cc17c10c81697d457e06fd10b6421ffbbca640de034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:21.0.0.9-kernel-slim-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:e7e1cb59246d5412b2b5c2ccf514a142a73ac5f57491b47a1f1aa3ea9f18f13c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112840329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f9d185e9909ff1674d56fb2fc23702c7aba9694d195a55d95e0f385402546b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:41:41 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:41:41 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:41:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:41:42 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:41:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:41:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:41:47 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:41:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:41:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:41:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:41:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:41:56 GMT
USER 1001
# Fri, 01 Oct 2021 08:41:56 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:41:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:41:57 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0ae796f4836b5f61b9aa848be42ff8c010742f1183fede70339ee6d5363056`  
		Last Modified: Fri, 01 Oct 2021 08:47:46 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a782210c14eb408be16a6dd870450ac7962c1c855fd026933d71982ceb97a3`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a9309342ea7db909e49c2c6e022b38124d7a7cff9c7dcedb07a05a83dc7bbc`  
		Last Modified: Fri, 01 Oct 2021 08:47:45 GMT  
		Size: 11.8 MB (11771780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bf73ce7052cc36f343b1e0d6523854786cde30bd46602f3790fb905dfa9b68`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515b760e142528245cda1f9337ee0d1a9297ee8dfa917b613f76c6eecbd2b785`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785be3dbd33ddbc5649bf8fb4133032536c5eb7c057a6e41d22b0ea44d340378`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 2.4 MB (2446128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.9-kernel-slim-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:f0e627ede0a607110ca4a1062efa7e54a9585463a3d49fa5391b00a8cdc7597e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118689273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1ff8a934cf5c14e9d4bd54238534d001bc10cb54752b9625be75e207d778f0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:34:23 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:34:26 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Thu, 07 Oct 2021 09:34:32 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:34:34 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Thu, 07 Oct 2021 09:34:38 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:34:42 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:34:48 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:34:59 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:35:20 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:35:23 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:35:24 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:35:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:35:51 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:35:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:36:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:36:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:36:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:36:23 GMT
USER 1001
# Thu, 07 Oct 2021 09:36:26 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:36:29 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:36:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8fcad744ae0980e75b77fb152e6ce10b74804f80a668ba6571ac0562860d11`  
		Last Modified: Thu, 07 Oct 2021 09:58:16 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e168461c24e61bc28ee8905378d885d7f005301ec359c83ce94dfc327c5a307`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a476834273820d5a68f6861d11066f3d20a668196757e3cb2e03b30a309d6f`  
		Last Modified: Thu, 07 Oct 2021 09:58:15 GMT  
		Size: 11.8 MB (11772194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48fe193bf272ae89b6ebc75ed6f6457a453460c5f842f9afbe384e3f658c051`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159e19e78489d46b8c64c53d34ec39d3efebe1e04c65aa8ab17d4e79dd71aac2`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b102b0708c189940c1783b0d3df4160111df477dc49727ec75a7f36e4ed059`  
		Last Modified: Thu, 07 Oct 2021 09:58:14 GMT  
		Size: 2.4 MB (2396653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:21.0.0.9-kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:312dc06e56f6deca8a58a03f4dc1b52d6757d0009dbe472204c39913543578d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109857100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85aba34ee000e7f8ab08f46ac67fd5955e54e131ccb6049273fe13b478b85d7`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:47:55 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Mon, 25 Oct 2021 21:47:55 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Mon, 25 Oct 2021 21:47:55 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Mon, 25 Oct 2021 21:47:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Mon, 25 Oct 2021 21:47:56 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:47:56 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:47:56 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:47:56 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:47:56 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Mon, 25 Oct 2021 21:47:56 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:47:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:48:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:48:01 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:48:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:48:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:48:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:48:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:48:08 GMT
USER 1001
# Mon, 25 Oct 2021 21:48:08 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:48:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:48:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dc066f06062f4d52adcece707d2ecbb5869714675f1afd84d797357b7c0658`  
		Last Modified: Mon, 25 Oct 2021 21:54:32 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12096cc970b56dd5810e08afbfcb51061e16e09abb5415a0cc4c610203f77c3`  
		Last Modified: Mon, 25 Oct 2021 21:54:31 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445f529351a58707ea6355505c53a1ce3c6924369ee890c1e899577e15c19b79`  
		Last Modified: Mon, 25 Oct 2021 21:54:32 GMT  
		Size: 11.8 MB (11770499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cbab8b919c7fcd26d47d7189917f045c7ac3510f16fb3fd39a1dba82a9bf2f`  
		Last Modified: Mon, 25 Oct 2021 21:54:31 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3b0c4b09a230ac75c0a8b674f2de5bbc11fa047b66215b5a01e85a04ffc24b`  
		Last Modified: Mon, 25 Oct 2021 21:54:31 GMT  
		Size: 9.2 KB (9218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c2e08f06a4e511be3d51c94f1f7a1570b92b9b3155d6f998d74f0e953e44cb`  
		Last Modified: Mon, 25 Oct 2021 21:54:31 GMT  
		Size: 2.2 MB (2206325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:8ca40f8ac1563f064e154aacdfdf65ed92dcd304e51ee60a57c3554c5ab91d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:beta` - linux; amd64

```console
$ docker pull open-liberty@sha256:eb0cfce1d9a882948524b8a83b539b64c6d8d16a8397aa59d56e75d80e999783
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396042524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b8b99daaeb6d5f825372579ac62adf39569af61a9df47cbcb6300fe0f04b5e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:39:40 GMT
ARG LIBERTY_VERSION=21.0.0.10-beta
# Fri, 01 Oct 2021 08:39:40 GMT
ARG LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499
# Fri, 01 Oct 2021 08:39:40 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:39:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip
# Fri, 01 Oct 2021 08:39:40 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:39:40 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:39:41 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:39:41 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:39:41 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with AdoptOpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.10-beta
# Fri, 01 Oct 2021 08:39:41 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:39:41 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:39:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:39:59 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:40:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:40:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:40:31 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:40:32 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:40:32 GMT
USER 1001
# Fri, 01 Oct 2021 08:40:32 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:40:32 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:40:32 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd9ae859c05c2b06537fca3c997aa300912ed66fddbae0b9309958282fed5f6`  
		Last Modified: Fri, 01 Oct 2021 08:47:04 GMT  
		Size: 8.6 KB (8553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3992c1f54e2ea92450e222880960d60532df603f06878d444f256b25787102`  
		Last Modified: Fri, 01 Oct 2021 08:47:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cf69bf8172c0d74cee13fcc045603f90752a3d4ca81986e5b95237e13e2a9b`  
		Last Modified: Fri, 01 Oct 2021 08:47:16 GMT  
		Size: 284.0 MB (284003397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4d7af6db27f0e3a27a14ba24bacdabab6cea41fd44799fbfa3c9033d942678`  
		Last Modified: Fri, 01 Oct 2021 08:47:02 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eb75d4177bf237dbe27bd09e87f233db97a6ce33298e7800041fdce72b0ba5`  
		Last Modified: Fri, 01 Oct 2021 08:47:02 GMT  
		Size: 10.0 KB (10047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb455154b01cec27ae66375e8248aac89e9fea9009a18d6da1e8b1127c229b7`  
		Last Modified: Fri, 01 Oct 2021 08:47:04 GMT  
		Size: 13.4 MB (13415111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:1511ef728c4cc377f175b3f97a7e565f1752bd92422665755feb5a2a2fa35cb2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400496706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e7cb2c2617af0233361f28260c0b082375ff1c5fdca895abca6bc0f492281b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:27:40 GMT
ARG LIBERTY_VERSION=21.0.0.10-beta
# Thu, 07 Oct 2021 09:27:43 GMT
ARG LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499
# Thu, 07 Oct 2021 09:27:46 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:27:51 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip
# Thu, 07 Oct 2021 09:27:54 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:27:56 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:27:58 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:28:03 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:28:05 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with AdoptOpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.10-beta
# Thu, 07 Oct 2021 09:28:07 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:28:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:28:53 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:29:04 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:29:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:29:32 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:30:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:30:32 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:30:34 GMT
USER 1001
# Thu, 07 Oct 2021 09:30:36 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:30:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:30:43 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1890ee9c5e297442795c13046e6f50e1322c9b4c1ed162c2e04b9d67ec7f21c6`  
		Last Modified: Thu, 07 Oct 2021 09:57:10 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5565a3e5e6e60babc00ecdbf5701a01b15710393a101a1e8859fd98ad5a2f9f`  
		Last Modified: Thu, 07 Oct 2021 09:57:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6656bc455bdd8057e95889df626421b11d9c5d8ca3e359f61b2ac23923f341ad`  
		Last Modified: Thu, 07 Oct 2021 09:57:30 GMT  
		Size: 284.0 MB (284003914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809d81f5b8cec5708897cc1e9ba4dd9956e99f800a86563fb13c12d01ed25ad4`  
		Last Modified: Thu, 07 Oct 2021 09:57:06 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c1efa82877f78c495ec06c4eac85d229cd346ae246f4f2526230ef1b608136`  
		Last Modified: Thu, 07 Oct 2021 09:57:06 GMT  
		Size: 10.1 KB (10067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4bc9e4a804dabe3aa63ba135e902ff882efd4a3294a97328cca1f33d6cdd5b`  
		Last Modified: Thu, 07 Oct 2021 09:57:08 GMT  
		Size: 12.0 MB (11970770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:6651b709cdb41e2dfa4a13d29f2d9ce148fbac1ed2f9ed80e56a7b3ed7b40b95
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 MB (390877443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074cd69feeecd0125bdfcbbc5df71e66bfd1324fee5b29ef514473b1bc11ea47`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:43:25 GMT
ARG LIBERTY_VERSION=21.0.0.11-beta
# Mon, 25 Oct 2021 21:43:25 GMT
ARG LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132
# Mon, 25 Oct 2021 21:43:25 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:43:26 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip
# Mon, 25 Oct 2021 21:43:26 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:43:26 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:43:26 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:43:26 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:43:26 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.11-beta
# Mon, 25 Oct 2021 21:43:26 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:43:27 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:43:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132 LIBERTY_VERSION=21.0.0.11-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:43:48 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:43:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132 LIBERTY_VERSION=21.0.0.11-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:43:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132 LIBERTY_VERSION=21.0.0.11-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:44:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132 LIBERTY_VERSION=21.0.0.11-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:44:08 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:44:08 GMT
USER 1001
# Mon, 25 Oct 2021 21:44:08 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:44:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:44:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9522b3e5f79b96f30c0be01bc046bfab9fd1e808c4217771a3062474818d0e52`  
		Last Modified: Mon, 25 Oct 2021 21:53:03 GMT  
		Size: 8.5 KB (8549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fbd037bd8da6c0712811bc51c6e6812e27a5216a28e63846d92014eee051a4a`  
		Last Modified: Mon, 25 Oct 2021 21:53:02 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7ff1fe436e8dc94d489f39f4d19094214c97b824864f7072aae1e296b449f7`  
		Last Modified: Mon, 25 Oct 2021 21:53:13 GMT  
		Size: 284.3 MB (284254418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5278d9ce4dd2b4399fcebace92b2045b3897323f59e204ebd1ed033c19c9542`  
		Last Modified: Mon, 25 Oct 2021 21:53:02 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad866473a8e3dc444cbf650042f83b425621be5d687c789f1e627a7007210692`  
		Last Modified: Mon, 25 Oct 2021 21:53:02 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f88cd00aa177ea8413e4293d8de8d3b2bdd524af85a0d0eb17b0bbb914ab58`  
		Last Modified: Mon, 25 Oct 2021 21:53:03 GMT  
		Size: 10.7 MB (10741164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:beta-java11`

```console
$ docker pull open-liberty@sha256:8c81b9851845b92102604bc15d1025f9f5e1079e2565447924fa944bdb7001e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:beta-java11` - linux; amd64

```console
$ docker pull open-liberty@sha256:921594dc83d9d03c7ea94770da716881175ee77f4fb43606671118a49d1e098a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.1 MB (391128823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1101535e8072894f28ade7bcba8fdcabbdb9376963630789a2e0aff0a0f18d6b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:28:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 01 Oct 2021 03:29:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:30:22 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:40:40 GMT
ARG LIBERTY_VERSION=21.0.0.10-beta
# Fri, 01 Oct 2021 08:40:40 GMT
ARG LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499
# Fri, 01 Oct 2021 08:40:40 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:40:40 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip
# Fri, 01 Oct 2021 08:40:40 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:40:41 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:40:41 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:40:41 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:40:41 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with AdoptOpenJDK 11 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.10-beta
# Fri, 01 Oct 2021 08:40:41 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:40:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:40:54 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:40:55 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:40:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:40:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:41:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:41:30 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:41:31 GMT
USER 1001
# Fri, 01 Oct 2021 08:41:31 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:41:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:41:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec736696f208ef0ec33b06d703a533976c7a35abe201ae6ee68f6405bc58ed`  
		Last Modified: Fri, 01 Oct 2021 03:39:56 GMT  
		Size: 44.4 MB (44382131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a366c184fa8e3539f73433cd4c7e09a1df30ee1e2ed35e509f090ab08dd34813`  
		Last Modified: Fri, 01 Oct 2021 03:39:50 GMT  
		Size: 4.1 MB (4138880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ae7b548b8b8d5c03b5ccaf884b11d9b7c982d17f3b0ee8ed3c901353464bd6`  
		Last Modified: Fri, 01 Oct 2021 08:47:25 GMT  
		Size: 8.6 KB (8551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce1adc26effa43bd9b17ed8c529bbae4de9bdf5921c8f2efd4dbce133438e85`  
		Last Modified: Fri, 01 Oct 2021 08:47:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691a8615b6b5b5dbbde8ce25701aed85f1c6c374fd96f6d17db89ee32f8855cf`  
		Last Modified: Fri, 01 Oct 2021 08:47:36 GMT  
		Size: 284.0 MB (284003432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335694323efe1ed0b4056d02879f8026bbe6b9a7439569cc2ce2f82b85fcd881`  
		Last Modified: Fri, 01 Oct 2021 08:47:23 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd9cdf24adf10b4ff48ee1e1b4448cb6c9284084a5702f521a800213c3e894b`  
		Last Modified: Fri, 01 Oct 2021 08:47:23 GMT  
		Size: 10.1 KB (10052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41dde2a6e43331e41bdb72ae8c3b8a9802cf820816f810c1c8a083e8bc25ccf`  
		Last Modified: Fri, 01 Oct 2021 08:47:25 GMT  
		Size: 14.0 MB (13981357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta-java11` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:a3400ae6143282204771adeeccd6cb7cee46379773bc3e9c2938177de86c9de3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (395035907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca76b20d704674062d7f6bfccebc5e678121de99f7a31877ab6ba64e58f72f07`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:12:53 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 06 Oct 2021 17:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:15:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:16:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:30:55 GMT
ARG LIBERTY_VERSION=21.0.0.10-beta
# Thu, 07 Oct 2021 09:30:58 GMT
ARG LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499
# Thu, 07 Oct 2021 09:31:01 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:31:03 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip
# Thu, 07 Oct 2021 09:31:07 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:31:08 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:31:12 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:31:13 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:31:15 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with AdoptOpenJDK 11 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.10-beta
# Thu, 07 Oct 2021 09:31:17 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:31:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:31:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:32:05 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:32:29 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:32:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:33:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.10-beta/openliberty-runtime-21.0.0.10-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=1b88de47994986c4b069884a982cfbdd588c8499 LIBERTY_VERSION=21.0.0.10-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:33:34 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:33:46 GMT
USER 1001
# Thu, 07 Oct 2021 09:33:53 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:33:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:34:05 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a1310fddd70f7d129e09b08a85ca9a02ec9984d9e11434200a57a656453fa`  
		Last Modified: Wed, 06 Oct 2021 17:31:09 GMT  
		Size: 45.1 MB (45104806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b2a8e4fb8f2ea78e7be40e998ec639e4a7c6ee4a536b67cf4aebb4c1a25fe6`  
		Last Modified: Wed, 06 Oct 2021 17:31:01 GMT  
		Size: 3.3 MB (3294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8363be36af5fc94553f61e2174dd3a7db1968e85f245f8d8921e83288dc6ecc2`  
		Last Modified: Thu, 07 Oct 2021 09:57:44 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509feb54e74fc76cd69c1f98b700a80c697040b64e071f0722a0615962789c3a`  
		Last Modified: Thu, 07 Oct 2021 09:57:40 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec9140325ce5d1e80bd5348f345126afbad1279f80c5a5107dd490cebbd7d32`  
		Last Modified: Thu, 07 Oct 2021 09:58:04 GMT  
		Size: 284.0 MB (284003915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289f66e1e2145c64bc2aa4125ea4797b9e82e47111ba90172b0cf6d7277e0e06`  
		Last Modified: Thu, 07 Oct 2021 09:57:40 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a57a6a34e40d955552fbe0ef63cb049dba2de38605062b8206e113240b6e62e`  
		Last Modified: Thu, 07 Oct 2021 09:57:40 GMT  
		Size: 10.1 KB (10069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc71ea379070413124a40252cfd925456d4d0f7006db5db08f9e243ee2dee07`  
		Last Modified: Thu, 07 Oct 2021 09:57:42 GMT  
		Size: 12.1 MB (12110769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta-java11` - linux; s390x

```console
$ docker pull open-liberty@sha256:d39f8c5898ac204faf93082c43e2241942fa04557e6b6b73de7614253a6b8c97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387911008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76b27cc6dcb6d9f2f67b82117e6106c9324e6e7eea8071d143ae8f6c3b53683`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:44:14 GMT
ARG LIBERTY_VERSION=21.0.0.11-beta
# Mon, 25 Oct 2021 21:44:14 GMT
ARG LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132
# Mon, 25 Oct 2021 21:44:14 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:44:14 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip
# Mon, 25 Oct 2021 21:44:14 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:44:15 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:44:15 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:44:15 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:44:15 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 11 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=21.0.0.11-beta
# Mon, 25 Oct 2021 21:44:15 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:44:15 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:44:30 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132 LIBERTY_VERSION=21.0.0.11-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:44:35 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:44:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132 LIBERTY_VERSION=21.0.0.11-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:44:36 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132 LIBERTY_VERSION=21.0.0.11-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:44:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/21.0.0.11-beta/openliberty-runtime-21.0.0.11-beta.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=584995eb472d1d5e5379dc179aa58060eafae132 LIBERTY_VERSION=21.0.0.11-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:44:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:44:59 GMT
USER 1001
# Mon, 25 Oct 2021 21:44:59 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:45:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:45:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c492c3082ac6cdb9b6d76e9a5f5ab90ce19fa21d974ae4bbae0e87dc9534f5d4`  
		Last Modified: Mon, 25 Oct 2021 21:53:22 GMT  
		Size: 8.5 KB (8548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecaf5b218f7106df0c9b1e34f506629c2674f868e81f4c54c3d6e084a080da3`  
		Last Modified: Mon, 25 Oct 2021 21:53:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d6c6e2fd2c8c1f0257ee809c9313ebc0f00ba3e0920c55ba694c2e35ce22db`  
		Last Modified: Mon, 25 Oct 2021 21:53:32 GMT  
		Size: 284.3 MB (284254396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed8e6ccb1da56ec1d13613d3028e162a52bf99e747b9760047928e02f1626a8`  
		Last Modified: Mon, 25 Oct 2021 21:53:21 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322e8e556b3d1ed53323ecb602321b75d2ddfde50d6394eb9d277749fdaaced1`  
		Last Modified: Mon, 25 Oct 2021 21:53:22 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367e11a1231e97e6d5b8369bba2e2f86aed3148b11ac61ab17f0fbc970aaa916`  
		Last Modified: Mon, 25 Oct 2021 21:53:23 GMT  
		Size: 13.2 MB (13200381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:full`

```console
$ docker pull open-liberty@sha256:3aa4d8fb143cb4e7925182c0ab962bd27d3f3f79ef18d2ce9c23b1a38b351693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:full` - linux; amd64

```console
$ docker pull open-liberty@sha256:11332203189a2473abc6b01619fa6f3900eedd17c71cd587d390a0943b8a429e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297155113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc833487bd0e5c53b41f16e6f5290cfbf405d8aacd93d73e2193fc88e53ecb9`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:42:23 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Fri, 01 Oct 2021 08:42:23 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:42:24 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:24 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:42:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:42:25 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:42:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:42:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:42:35 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:42:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:43:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:43:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:43:08 GMT
USER 1001
# Fri, 01 Oct 2021 08:43:08 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:43:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:43:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09679318c11692d08f483aac1e7a8d344749aa9b9ef495d0c0d581925d5fbf`  
		Last Modified: Fri, 01 Oct 2021 08:48:06 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f515bcbf2cee10d004afc0f02659f37d3d73159d551e065ad7f3e27c3c846c`  
		Last Modified: Fri, 01 Oct 2021 08:48:05 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23662dd8572b0c37fa42fc96f4da78cdfa818d709f83236844890e3f10f0d92d`  
		Last Modified: Fri, 01 Oct 2021 08:48:13 GMT  
		Size: 185.1 MB (185116246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e334ab7e07d9250054a58457a3153053eb46e9a08e9db80984f622e6e84b61`  
		Last Modified: Fri, 01 Oct 2021 08:48:04 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f22529ca6d49cb869d4f0a455c10dc84d966c4d0922244e452a79893ccea623`  
		Last Modified: Fri, 01 Oct 2021 08:48:04 GMT  
		Size: 10.0 KB (10043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9024c9b4674915436af1db7e8dbd20208fbdc716c9eacef5c76aab2b380fa9fd`  
		Last Modified: Fri, 01 Oct 2021 08:48:06 GMT  
		Size: 13.4 MB (13414860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:794d918ef4ab904c026742fee33b3cfd956e82f0c691b2dfba495f681834ca52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301578145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14426d0b0a72ec4d2872543ca1caff24d41513e71fa69e3e241b21664f1479de`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:34:23 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:38:59 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Thu, 07 Oct 2021 09:39:02 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:39:04 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Thu, 07 Oct 2021 09:39:11 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:39:13 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:39:14 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:39:19 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:39:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:39:45 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:39:52 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:40:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:40:30 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:40:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:40:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:41:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:41:47 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:41:49 GMT
USER 1001
# Thu, 07 Oct 2021 09:41:55 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:41:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:42:02 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaeab81cf835a89f1f403c833945d3b554a82588d98c3a010f7a3c7a44fb7d3`  
		Last Modified: Thu, 07 Oct 2021 09:58:40 GMT  
		Size: 8.6 KB (8551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3597446a2d59ddb34b461f023cc3db1ac1723905a3519e42869034df823998df`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ad0e3fe0fa97901df249fb8016cd38c70de162a82c3df588fdc2bf6abbd43d`  
		Last Modified: Thu, 07 Oct 2021 09:58:54 GMT  
		Size: 185.1 MB (185116681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dba658c8a8e6fe991c93dbf05105bd9f2544f66bbda7ad4c47403fd2a06b087`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92bb1230ea89c90a826b0b9b6170dc57b42b86e1852d2aff7baed7c06e5aec4`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa3b298a46f54f3c87de572f3e9128bddd47b4c59cb136ca93f36e6ae0d13a2`  
		Last Modified: Thu, 07 Oct 2021 09:58:40 GMT  
		Size: 11.9 MB (11939449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full` - linux; s390x

```console
$ docker pull open-liberty@sha256:2f3ab64a31db098c609d95705017615d6009423940e97a5dedd486c04e756db1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291780673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf7411b5e6c96f094adab004b3e241498114fdc2dbea18b790fe2c7df61ed06`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:57 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:57 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:57 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:57 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:58 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:58 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:46:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:46:14 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:46:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:46:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:46:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:46:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:46:35 GMT
USER 1001
# Mon, 25 Oct 2021 21:46:35 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:46:35 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:46:35 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe4bf612a292a411455e4db7024f1fb1bac92ab7ef206436a15aa8293e62a2`  
		Last Modified: Mon, 25 Oct 2021 21:53:55 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c5943e5e87b26ebb1312db484cfc931302cbea3604e82aab88b8d529be7cef`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f78318a0320256dac4eb5702c2bff0615a5bea5661fb0b5a797a28513074b10`  
		Last Modified: Mon, 25 Oct 2021 21:54:01 GMT  
		Size: 185.2 MB (185168476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32cd122dc8e75095ad0a6ce27422c754815614825acf3ea5fa984b1682c2575`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f732eec10818b415067f0854ce1829e5147a04ef91f673e12fda5031832bc39a`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 10.0 KB (10045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d9add8f18e2677ef67b834b2a8c717032332d9b88adc07ad455f329d99f2b0`  
		Last Modified: Mon, 25 Oct 2021 21:53:55 GMT  
		Size: 10.7 MB (10730333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:full-java11-openj9`

```console
$ docker pull open-liberty@sha256:2206a74886bf05f8b91625b000874d9a4569318611cd3faac0fea8cae56a34f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:ad6683c36d46d14ac4abb1a582d3d2e7069f5b4005d26761b496b4719998612a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291986030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a615a8621f694363a4bc939334f5e96fa74023ef5a5233acebf1b8d38fef3d6b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:28:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 01 Oct 2021 03:29:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:30:22 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:43:14 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Fri, 01 Oct 2021 08:43:14 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:43:14 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Fri, 01 Oct 2021 08:43:14 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:43:15 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:43:15 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:43:15 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:43:15 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:43:15 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:43:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:43:25 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:43:26 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:43:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:43:28 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:44:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:44:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:44:01 GMT
USER 1001
# Fri, 01 Oct 2021 08:44:01 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:44:01 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:44:01 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec736696f208ef0ec33b06d703a533976c7a35abe201ae6ee68f6405bc58ed`  
		Last Modified: Fri, 01 Oct 2021 03:39:56 GMT  
		Size: 44.4 MB (44382131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a366c184fa8e3539f73433cd4c7e09a1df30ee1e2ed35e509f090ab08dd34813`  
		Last Modified: Fri, 01 Oct 2021 03:39:50 GMT  
		Size: 4.1 MB (4138880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b11e4c50c1b02b9a8706b186dfbe76f4278043ca6101c5a8792ff97ed3e435`  
		Last Modified: Fri, 01 Oct 2021 08:48:28 GMT  
		Size: 8.6 KB (8550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67df32056e1c2b9c176bdb4270f98a8e281e1f217b9068a394179c26e74c5b68`  
		Last Modified: Fri, 01 Oct 2021 08:48:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac59e11cab494c2d4b273f52f6453fff0f5560ea9d3440a886c186a7eb113e8`  
		Last Modified: Fri, 01 Oct 2021 08:48:35 GMT  
		Size: 185.1 MB (185116257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d094d2326011485c88ab379bbbcb38507e819ab3a2cc268704eae112fefc768d`  
		Last Modified: Fri, 01 Oct 2021 08:48:26 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950372e3490412fa753e90d15f40555bdc459d3465dafd590d7d5a47a01607d7`  
		Last Modified: Fri, 01 Oct 2021 08:48:26 GMT  
		Size: 10.1 KB (10050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7946107fa3dbb996f07c021bb28d3e710b91eefd6218b1032c9663d03dfc654`  
		Last Modified: Fri, 01 Oct 2021 08:48:28 GMT  
		Size: 13.7 MB (13725741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:d77beeb050d34bd616d5dc116494788b79d4d627b3b4538aedec046d2fc17c07
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296116248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a4eb54c4fc7bdfe65042d5ad425721637a538ff18fdded4a47050465222426`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:12:53 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 06 Oct 2021 17:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:15:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:16:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:36:47 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:42:12 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Thu, 07 Oct 2021 09:42:15 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:42:19 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Thu, 07 Oct 2021 09:42:23 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:42:29 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:42:32 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:42:36 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:42:39 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:42:40 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:42:41 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:43:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:43:30 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:43:38 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:43:45 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:44:32 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:44:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:44:39 GMT
USER 1001
# Thu, 07 Oct 2021 09:44:41 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:44:44 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:44:46 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a1310fddd70f7d129e09b08a85ca9a02ec9984d9e11434200a57a656453fa`  
		Last Modified: Wed, 06 Oct 2021 17:31:09 GMT  
		Size: 45.1 MB (45104806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b2a8e4fb8f2ea78e7be40e998ec639e4a7c6ee4a536b67cf4aebb4c1a25fe6`  
		Last Modified: Wed, 06 Oct 2021 17:31:01 GMT  
		Size: 3.3 MB (3294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff059797ed1f184c8aac6e5256dcfb7fd8ebb286356e28d2353578470fb8e4a3`  
		Last Modified: Thu, 07 Oct 2021 09:59:12 GMT  
		Size: 8.6 KB (8555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f508ea2c10cfd383e8a262339c7a7ed13a6d4d6fcd5e60990889f576298946`  
		Last Modified: Thu, 07 Oct 2021 09:59:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dcec252deb51906965be50afea11c90e822016bf7f98c93dc5124b215bd75e`  
		Last Modified: Thu, 07 Oct 2021 09:59:26 GMT  
		Size: 185.1 MB (185116709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af8c16719d8ad457ecc0a06726d664da4247a6c6286100686cc32da3274fff`  
		Last Modified: Thu, 07 Oct 2021 09:59:10 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094df81cde1ef780ca6632039745748f94d48e33058b662fbaf512040703d38`  
		Last Modified: Thu, 07 Oct 2021 09:59:10 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e8f891aead6727972c39846183eaf2713f9b5f8d743cad8c33d710b482567`  
		Last Modified: Thu, 07 Oct 2021 09:59:12 GMT  
		Size: 12.1 MB (12078324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:205b65b739c0a8c727e03b56944152c3046bca1bb0e0592e12d658511a7561ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288770133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5846840154a9a91544098819e60d165c89785e2cb7bd41064c001a27a021365`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:33 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:46:45 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:46:46 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:46:46 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:46:46 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:46:46 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:46:46 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:46:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:47:00 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:47:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:47:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:47:24 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:47:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:47:24 GMT
USER 1001
# Mon, 25 Oct 2021 21:47:24 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:47:25 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:47:25 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8124847c3d3a4fc8a36afa327d390084543a32726a22362c42bd2d19c5ef63c8`  
		Last Modified: Mon, 25 Oct 2021 21:54:12 GMT  
		Size: 8.6 KB (8553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6aefa1a20c5156363a19d38ee873ddfdb646511399b82e69ee5e5b92fb9fe5d`  
		Last Modified: Mon, 25 Oct 2021 21:54:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f649aafd4597a1ab1adafb6706bd52a78d1da20dcbd36645a7c4d26c3d2ba8`  
		Last Modified: Mon, 25 Oct 2021 21:54:19 GMT  
		Size: 185.2 MB (185168480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf85ba74c69e45298027c8ee38dd695f7072d3d94bd4d8d07ba46fd9f47f6ee9`  
		Last Modified: Mon, 25 Oct 2021 21:54:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace210521e2fb01bdbe08fcbff6d705107b5f799e13603a324970f55ba84a56`  
		Last Modified: Mon, 25 Oct 2021 21:54:11 GMT  
		Size: 10.0 KB (10039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9ec737f89ab005e35b631f2c29a0b495c2a9fc0c33ab969a4f02bb06a613dc`  
		Last Modified: Mon, 25 Oct 2021 21:54:13 GMT  
		Size: 13.1 MB (13145435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:full-java8-openj9`

```console
$ docker pull open-liberty@sha256:3aa4d8fb143cb4e7925182c0ab962bd27d3f3f79ef18d2ce9c23b1a38b351693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:full-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:11332203189a2473abc6b01619fa6f3900eedd17c71cd587d390a0943b8a429e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297155113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc833487bd0e5c53b41f16e6f5290cfbf405d8aacd93d73e2193fc88e53ecb9`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:42:23 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Fri, 01 Oct 2021 08:42:23 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:42:24 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:24 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:42:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:42:25 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:42:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:42:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:42:35 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:42:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:43:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:43:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:43:08 GMT
USER 1001
# Fri, 01 Oct 2021 08:43:08 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:43:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:43:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09679318c11692d08f483aac1e7a8d344749aa9b9ef495d0c0d581925d5fbf`  
		Last Modified: Fri, 01 Oct 2021 08:48:06 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f515bcbf2cee10d004afc0f02659f37d3d73159d551e065ad7f3e27c3c846c`  
		Last Modified: Fri, 01 Oct 2021 08:48:05 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23662dd8572b0c37fa42fc96f4da78cdfa818d709f83236844890e3f10f0d92d`  
		Last Modified: Fri, 01 Oct 2021 08:48:13 GMT  
		Size: 185.1 MB (185116246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e334ab7e07d9250054a58457a3153053eb46e9a08e9db80984f622e6e84b61`  
		Last Modified: Fri, 01 Oct 2021 08:48:04 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f22529ca6d49cb869d4f0a455c10dc84d966c4d0922244e452a79893ccea623`  
		Last Modified: Fri, 01 Oct 2021 08:48:04 GMT  
		Size: 10.0 KB (10043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9024c9b4674915436af1db7e8dbd20208fbdc716c9eacef5c76aab2b380fa9fd`  
		Last Modified: Fri, 01 Oct 2021 08:48:06 GMT  
		Size: 13.4 MB (13414860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:794d918ef4ab904c026742fee33b3cfd956e82f0c691b2dfba495f681834ca52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301578145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14426d0b0a72ec4d2872543ca1caff24d41513e71fa69e3e241b21664f1479de`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:34:23 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:38:59 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Thu, 07 Oct 2021 09:39:02 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:39:04 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Thu, 07 Oct 2021 09:39:11 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:39:13 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:39:14 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:39:19 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:39:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:39:45 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:39:52 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:40:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:40:30 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:40:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:40:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:41:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:41:47 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:41:49 GMT
USER 1001
# Thu, 07 Oct 2021 09:41:55 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:41:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:42:02 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaeab81cf835a89f1f403c833945d3b554a82588d98c3a010f7a3c7a44fb7d3`  
		Last Modified: Thu, 07 Oct 2021 09:58:40 GMT  
		Size: 8.6 KB (8551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3597446a2d59ddb34b461f023cc3db1ac1723905a3519e42869034df823998df`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ad0e3fe0fa97901df249fb8016cd38c70de162a82c3df588fdc2bf6abbd43d`  
		Last Modified: Thu, 07 Oct 2021 09:58:54 GMT  
		Size: 185.1 MB (185116681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dba658c8a8e6fe991c93dbf05105bd9f2544f66bbda7ad4c47403fd2a06b087`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92bb1230ea89c90a826b0b9b6170dc57b42b86e1852d2aff7baed7c06e5aec4`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa3b298a46f54f3c87de572f3e9128bddd47b4c59cb136ca93f36e6ae0d13a2`  
		Last Modified: Thu, 07 Oct 2021 09:58:40 GMT  
		Size: 11.9 MB (11939449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:2f3ab64a31db098c609d95705017615d6009423940e97a5dedd486c04e756db1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291780673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf7411b5e6c96f094adab004b3e241498114fdc2dbea18b790fe2c7df61ed06`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:57 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:57 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:57 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:57 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:58 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:58 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:46:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:46:14 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:46:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:46:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:46:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:46:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:46:35 GMT
USER 1001
# Mon, 25 Oct 2021 21:46:35 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:46:35 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:46:35 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe4bf612a292a411455e4db7024f1fb1bac92ab7ef206436a15aa8293e62a2`  
		Last Modified: Mon, 25 Oct 2021 21:53:55 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c5943e5e87b26ebb1312db484cfc931302cbea3604e82aab88b8d529be7cef`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f78318a0320256dac4eb5702c2bff0615a5bea5661fb0b5a797a28513074b10`  
		Last Modified: Mon, 25 Oct 2021 21:54:01 GMT  
		Size: 185.2 MB (185168476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32cd122dc8e75095ad0a6ce27422c754815614825acf3ea5fa984b1682c2575`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f732eec10818b415067f0854ce1829e5147a04ef91f673e12fda5031832bc39a`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 10.0 KB (10045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d9add8f18e2677ef67b834b2a8c717032332d9b88adc07ad455f329d99f2b0`  
		Last Modified: Mon, 25 Oct 2021 21:53:55 GMT  
		Size: 10.7 MB (10730333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:kernel-slim`

```console
$ docker pull open-liberty@sha256:03cdc2c524e5fadab5bd4128ae0a3300fcabb04b79a02fe537b0ce871cbd59a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim` - linux; amd64

```console
$ docker pull open-liberty@sha256:e7e1cb59246d5412b2b5c2ccf514a142a73ac5f57491b47a1f1aa3ea9f18f13c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112840329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f9d185e9909ff1674d56fb2fc23702c7aba9694d195a55d95e0f385402546b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:41:41 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:41:41 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:41:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:41:42 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:41:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:41:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:41:47 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:41:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:41:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:41:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:41:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:41:56 GMT
USER 1001
# Fri, 01 Oct 2021 08:41:56 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:41:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:41:57 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0ae796f4836b5f61b9aa848be42ff8c010742f1183fede70339ee6d5363056`  
		Last Modified: Fri, 01 Oct 2021 08:47:46 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a782210c14eb408be16a6dd870450ac7962c1c855fd026933d71982ceb97a3`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a9309342ea7db909e49c2c6e022b38124d7a7cff9c7dcedb07a05a83dc7bbc`  
		Last Modified: Fri, 01 Oct 2021 08:47:45 GMT  
		Size: 11.8 MB (11771780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bf73ce7052cc36f343b1e0d6523854786cde30bd46602f3790fb905dfa9b68`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515b760e142528245cda1f9337ee0d1a9297ee8dfa917b613f76c6eecbd2b785`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785be3dbd33ddbc5649bf8fb4133032536c5eb7c057a6e41d22b0ea44d340378`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 2.4 MB (2446128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:f0e627ede0a607110ca4a1062efa7e54a9585463a3d49fa5391b00a8cdc7597e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118689273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1ff8a934cf5c14e9d4bd54238534d001bc10cb54752b9625be75e207d778f0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:34:23 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:34:26 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Thu, 07 Oct 2021 09:34:32 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:34:34 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Thu, 07 Oct 2021 09:34:38 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:34:42 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:34:48 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:34:59 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:35:20 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:35:23 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:35:24 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:35:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:35:51 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:35:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:36:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:36:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:36:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:36:23 GMT
USER 1001
# Thu, 07 Oct 2021 09:36:26 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:36:29 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:36:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8fcad744ae0980e75b77fb152e6ce10b74804f80a668ba6571ac0562860d11`  
		Last Modified: Thu, 07 Oct 2021 09:58:16 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e168461c24e61bc28ee8905378d885d7f005301ec359c83ce94dfc327c5a307`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a476834273820d5a68f6861d11066f3d20a668196757e3cb2e03b30a309d6f`  
		Last Modified: Thu, 07 Oct 2021 09:58:15 GMT  
		Size: 11.8 MB (11772194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48fe193bf272ae89b6ebc75ed6f6457a453460c5f842f9afbe384e3f658c051`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159e19e78489d46b8c64c53d34ec39d3efebe1e04c65aa8ab17d4e79dd71aac2`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b102b0708c189940c1783b0d3df4160111df477dc49727ec75a7f36e4ed059`  
		Last Modified: Thu, 07 Oct 2021 09:58:14 GMT  
		Size: 2.4 MB (2396653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim` - linux; s390x

```console
$ docker pull open-liberty@sha256:85d93a89be886bcfab89ce28491baff004cbdefd76061bad08a88215b409376c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109872436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec451c7cd54b3219c83acb577d49406e9cd89440ac8b0b7a3be789c67d4749d5`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:13 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:13 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:13 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:13 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:13 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:45:18 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:45:18 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:45:20 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:45:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:45:26 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:45:26 GMT
USER 1001
# Mon, 25 Oct 2021 21:45:26 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:45:26 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:45:26 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b1ad1b31bd01a80fa85db59606256029eca2d393e89251041211546d1a5a21`  
		Last Modified: Mon, 25 Oct 2021 21:53:40 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdf2a3f92a2ad7565c633127b41e7401f8c7dd3ad63dd12221f07a4b4f26f12`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05105f34fb305c8ba555f9e2bdeb844c0326dff5b4b22b66aad4d06d333e29`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 11.8 MB (11786095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bf0fcf5391cc8ded7c49089974ffb18c71b18a7ffce6109bc0b7eb9d02d2d9`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62004e8bc5c2bf69149404446b3b7549896e021fc6e8d6fb44d3749915b2722f`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 9.2 KB (9213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9a5dcf6e2ab7c858bd9fdbeb37c699275d91617f047a5cbadf49136899e3a2`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 2.2 MB (2206062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:kernel-slim-java11-openj9`

```console
$ docker pull open-liberty@sha256:7b41b1c7c19efe526adbe585957fecd319dd0d70059bc53fd087434acf0b6984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:fd85ed9965d69066ba5f500e16305d52b079810453ece0a7fdcf69d57be34082
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107354289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d5bb2ed9b99ad255d097dfe891ddab7cd3578d2842346360546f40cc74e909`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:28:43 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 01 Oct 2021 03:29:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:30:22 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Fri, 01 Oct 2021 08:42:02 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:42:03 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:42:03 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:03 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:42:03 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:42:03 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:42:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:42:08 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:42:09 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:42:11 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:42:18 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:42:18 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:42:19 GMT
USER 1001
# Fri, 01 Oct 2021 08:42:19 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:42:19 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:42:19 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec736696f208ef0ec33b06d703a533976c7a35abe201ae6ee68f6405bc58ed`  
		Last Modified: Fri, 01 Oct 2021 03:39:56 GMT  
		Size: 44.4 MB (44382131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a366c184fa8e3539f73433cd4c7e09a1df30ee1e2ed35e509f090ab08dd34813`  
		Last Modified: Fri, 01 Oct 2021 03:39:50 GMT  
		Size: 4.1 MB (4138880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df8db31bcb70d33d52014722f3dcb73c9622591e9076cb39ba938b7ba40812`  
		Last Modified: Fri, 01 Oct 2021 08:47:58 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07f5fec8291be9e6554efcdc0fc907de763ce4e8fb711e16c2a072a2022600a`  
		Last Modified: Fri, 01 Oct 2021 08:47:55 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643224f731958d64ac998dc6f3d79b64fba58f9210a3d3aa4f833d2fa935e1df`  
		Last Modified: Fri, 01 Oct 2021 08:47:57 GMT  
		Size: 11.8 MB (11771793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79d569b0b62fca5e541213788e001cf2e12cf14c34c6617f463f0ade3e63fba`  
		Last Modified: Fri, 01 Oct 2021 08:47:56 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc508143cd1ab9fe48e3c4e5f354e794557feb6922b28babf79374cb2c396e0a`  
		Last Modified: Fri, 01 Oct 2021 08:47:56 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106d16a667cffec2e90c489e959831a4f39b11b1ee80c29b1bc9d199df637315`  
		Last Modified: Fri, 01 Oct 2021 08:47:56 GMT  
		Size: 2.4 MB (2440063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:37a52cea31a7e54bc5aee1a232e8fb71f16a53146aa7b13854e917ee8ffe0c1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113119683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ca8c72763a32f21981bd9276369cb8339960c5e768993648f0ae040307efb8`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:12:53 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 06 Oct 2021 17:15:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:15:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:16:01 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:36:47 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:36:50 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Thu, 07 Oct 2021 09:36:52 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:36:57 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Thu, 07 Oct 2021 09:37:02 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:37:07 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:37:09 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:37:12 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:37:16 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:37:19 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:37:21 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:37:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:37:45 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:37:54 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:38:05 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:38:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:38:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:38:31 GMT
USER 1001
# Thu, 07 Oct 2021 09:38:39 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:38:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:38:42 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324a1310fddd70f7d129e09b08a85ca9a02ec9984d9e11434200a57a656453fa`  
		Last Modified: Wed, 06 Oct 2021 17:31:09 GMT  
		Size: 45.1 MB (45104806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b2a8e4fb8f2ea78e7be40e998ec639e4a7c6ee4a536b67cf4aebb4c1a25fe6`  
		Last Modified: Wed, 06 Oct 2021 17:31:01 GMT  
		Size: 3.3 MB (3294158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77a776270f036e23a394e0f196fa6617071bd8916f2b3fdc7d2149cee88d128`  
		Last Modified: Thu, 07 Oct 2021 09:58:30 GMT  
		Size: 8.1 KB (8112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9370437329e3e0991c6fe3d2d7c47f693f0020d00a89c0389d39741827108693`  
		Last Modified: Thu, 07 Oct 2021 09:58:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e805c18cccc0ae65f71e6f7fc618b990f1b2b3f8330ecc8822d5c7c5cdf15f30`  
		Last Modified: Thu, 07 Oct 2021 09:58:29 GMT  
		Size: 11.8 MB (11772211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dbd5c72767e0e80a5d56871d6f74fb823a892b48cf43a29344e8bb4ee380ab`  
		Last Modified: Thu, 07 Oct 2021 09:58:27 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac807dcf69663fd62af1f830fda7fecc96ed8097f82cc8841f75e1ed03597507`  
		Last Modified: Thu, 07 Oct 2021 09:58:28 GMT  
		Size: 9.2 KB (9241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453045ef5698149ef343f00461510678878f2c950fa57fb622d7ed9a0cc7363f`  
		Last Modified: Thu, 07 Oct 2021 09:58:28 GMT  
		Size: 2.4 MB (2427834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:231f02999d50ad0ab33f0bb275d62d1b3a47b04a230f99bd0db0bf1d3e64275e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104651047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171d07da0525fe515b735591b016a57d149843dfb97850cd843fa6115968fdf7`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:43:16 GMT
ENV JAVA_VERSION=jdk-11.0.12+7_openj9-0.27.0
# Thu, 21 Oct 2021 01:44:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='285bd388a497db61408d26a9f3328f62004714ede94456718cf6440a109e25d2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='6e5829aeb37abfb122e0944e438ecb2043c56df14fcdcce39bd4e3c9a55571a8';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='f352998f6fdf0b84f63c563608be57f30aa3f14c8117c1219422dbc712ad4f81';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.12%2B7_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_11.0.12_7_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:44:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:44:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:33 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:33 GMT
ARG LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af
# Mon, 25 Oct 2021 21:45:33 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:34 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:34 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:34 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:35 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:35 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:35 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:36 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:45:41 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:45:42 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:45:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:45:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:45:49 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:45:49 GMT
USER 1001
# Mon, 25 Oct 2021 21:45:50 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:45:50 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:45:50 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a65affcfccb2dfb3a30625494a9215e7e9d4929140f9edd82b58ce6237783`  
		Last Modified: Thu, 21 Oct 2021 01:48:40 GMT  
		Size: 43.8 MB (43754137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d63f60a21502163d11d6ba8e7b74a661195aa07aec5130a4f62ae12f42fdfe`  
		Last Modified: Thu, 21 Oct 2021 01:48:35 GMT  
		Size: 3.8 MB (3819029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec76c8b07a8a35285c2524fd76139cdadd8850ccba033b45ea00917a27459f8d`  
		Last Modified: Mon, 25 Oct 2021 21:53:48 GMT  
		Size: 8.1 KB (8112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb0774c4b567cf5d1a7248d7d06a2a598718bd59ca6b06cf10a050e78fac8f`  
		Last Modified: Mon, 25 Oct 2021 21:53:47 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37fe5b77d17a7b3c1e555aa766240e510cf55e0daf702cc1b99faa8075fc6c8d`  
		Last Modified: Mon, 25 Oct 2021 21:53:48 GMT  
		Size: 11.8 MB (11786097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f5f040f7bbd59796baab5963cdb84537c1a85d9fde8804cdd0da8decc1aa66`  
		Last Modified: Mon, 25 Oct 2021 21:53:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175124c11857f7835c72353f388987a22dad13d051424f3da97e60a40584111b`  
		Last Modified: Mon, 25 Oct 2021 21:53:47 GMT  
		Size: 9.2 KB (9218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53bd4f0cb8774be028ddadacb21bd3a653d2344acb39c18ba05a8f5e3ae4362`  
		Last Modified: Mon, 25 Oct 2021 21:53:47 GMT  
		Size: 2.4 MB (2410309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:kernel-slim-java8-openj9`

```console
$ docker pull open-liberty@sha256:03cdc2c524e5fadab5bd4128ae0a3300fcabb04b79a02fe537b0ce871cbd59a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim-java8-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:e7e1cb59246d5412b2b5c2ccf514a142a73ac5f57491b47a1f1aa3ea9f18f13c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112840329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f9d185e9909ff1674d56fb2fc23702c7aba9694d195a55d95e0f385402546b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:41:41 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:41:41 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:41:41 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:41:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:41:42 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:41:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:41:47 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:41:47 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:41:48 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:41:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:41:56 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:41:56 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:41:56 GMT
USER 1001
# Fri, 01 Oct 2021 08:41:56 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:41:56 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:41:57 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0ae796f4836b5f61b9aa848be42ff8c010742f1183fede70339ee6d5363056`  
		Last Modified: Fri, 01 Oct 2021 08:47:46 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a782210c14eb408be16a6dd870450ac7962c1c855fd026933d71982ceb97a3`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a9309342ea7db909e49c2c6e022b38124d7a7cff9c7dcedb07a05a83dc7bbc`  
		Last Modified: Fri, 01 Oct 2021 08:47:45 GMT  
		Size: 11.8 MB (11771780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06bf73ce7052cc36f343b1e0d6523854786cde30bd46602f3790fb905dfa9b68`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515b760e142528245cda1f9337ee0d1a9297ee8dfa917b613f76c6eecbd2b785`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785be3dbd33ddbc5649bf8fb4133032536c5eb7c057a6e41d22b0ea44d340378`  
		Last Modified: Fri, 01 Oct 2021 08:47:44 GMT  
		Size: 2.4 MB (2446128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:f0e627ede0a607110ca4a1062efa7e54a9585463a3d49fa5391b00a8cdc7597e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118689273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1ff8a934cf5c14e9d4bd54238534d001bc10cb54752b9625be75e207d778f0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:34:23 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:34:26 GMT
ARG LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278
# Thu, 07 Oct 2021 09:34:32 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:34:34 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip
# Thu, 07 Oct 2021 09:34:38 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:34:42 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:34:48 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:34:59 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:35:20 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:35:23 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:35:24 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:35:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:35:51 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:35:57 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:36:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:36:17 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.9/openliberty-kernel-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=82894898cdb1824d173c3e87052f93230c163278 LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:36:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:36:23 GMT
USER 1001
# Thu, 07 Oct 2021 09:36:26 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:36:29 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:36:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8fcad744ae0980e75b77fb152e6ce10b74804f80a668ba6571ac0562860d11`  
		Last Modified: Thu, 07 Oct 2021 09:58:16 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e168461c24e61bc28ee8905378d885d7f005301ec359c83ce94dfc327c5a307`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a476834273820d5a68f6861d11066f3d20a668196757e3cb2e03b30a309d6f`  
		Last Modified: Thu, 07 Oct 2021 09:58:15 GMT  
		Size: 11.8 MB (11772194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48fe193bf272ae89b6ebc75ed6f6457a453460c5f842f9afbe384e3f658c051`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159e19e78489d46b8c64c53d34ec39d3efebe1e04c65aa8ab17d4e79dd71aac2`  
		Last Modified: Thu, 07 Oct 2021 09:58:13 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b102b0708c189940c1783b0d3df4160111df477dc49727ec75a7f36e4ed059`  
		Last Modified: Thu, 07 Oct 2021 09:58:14 GMT  
		Size: 2.4 MB (2396653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java8-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:85d93a89be886bcfab89ce28491baff004cbdefd76061bad08a88215b409376c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109872436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec451c7cd54b3219c83acb577d49406e9cd89440ac8b0b7a3be789c67d4749d5`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:12 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:13 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:13 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:13 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:13 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:13 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:45:18 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:45:18 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:45:20 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:45:26 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/21.0.0.10/openliberty-kernel-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=cbb3b8bea162cd3f2586d885893744b403f410af LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:45:26 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:45:26 GMT
USER 1001
# Mon, 25 Oct 2021 21:45:26 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:45:26 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:45:26 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b1ad1b31bd01a80fa85db59606256029eca2d393e89251041211546d1a5a21`  
		Last Modified: Mon, 25 Oct 2021 21:53:40 GMT  
		Size: 8.1 KB (8113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdf2a3f92a2ad7565c633127b41e7401f8c7dd3ad63dd12221f07a4b4f26f12`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05105f34fb305c8ba555f9e2bdeb844c0326dff5b4b22b66aad4d06d333e29`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 11.8 MB (11786095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bf0fcf5391cc8ded7c49089974ffb18c71b18a7ffce6109bc0b7eb9d02d2d9`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62004e8bc5c2bf69149404446b3b7549896e021fc6e8d6fb44d3749915b2722f`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 9.2 KB (9213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9a5dcf6e2ab7c858bd9fdbeb37c699275d91617f047a5cbadf49136899e3a2`  
		Last Modified: Mon, 25 Oct 2021 21:53:39 GMT  
		Size: 2.2 MB (2206062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `open-liberty:latest`

```console
$ docker pull open-liberty@sha256:3aa4d8fb143cb4e7925182c0ab962bd27d3f3f79ef18d2ce9c23b1a38b351693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:latest` - linux; amd64

```console
$ docker pull open-liberty@sha256:11332203189a2473abc6b01619fa6f3900eedd17c71cd587d390a0943b8a429e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297155113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc833487bd0e5c53b41f16e6f5290cfbf405d8aacd93d73e2193fc88e53ecb9`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:25:22 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:27:02 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Fri, 01 Oct 2021 03:27:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 03:27:57 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 01 Oct 2021 03:28:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 01 Oct 2021 08:41:40 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Fri, 01 Oct 2021 08:42:23 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Fri, 01 Oct 2021 08:42:23 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 01 Oct 2021 08:42:24 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 01 Oct 2021 08:42:24 GMT
ARG OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:24 GMT
ARG VERBOSE=false
# Fri, 01 Oct 2021 08:42:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Fri, 01 Oct 2021 08:42:25 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Fri, 01 Oct 2021 08:42:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 01 Oct 2021 08:42:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 01 Oct 2021 08:42:35 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 01 Oct 2021 08:42:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 01 Oct 2021 08:42:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 01 Oct 2021 08:43:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 01 Oct 2021 08:43:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 01 Oct 2021 08:43:08 GMT
USER 1001
# Fri, 01 Oct 2021 08:43:08 GMT
EXPOSE 9080 9443
# Fri, 01 Oct 2021 08:43:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 01 Oct 2021 08:43:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b9b9c1c443d1cd3d83fa6ecf9e3a4ae13b711dcc6b3aa34e9603c1cb8a930`  
		Last Modified: Fri, 01 Oct 2021 03:35:45 GMT  
		Size: 16.0 MB (16033975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f139188c865034df721a6ab200bd52a7e992d850ca9ddf9cba1a3f5ffaf70f`  
		Last Modified: Fri, 01 Oct 2021 03:39:12 GMT  
		Size: 49.8 MB (49849295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfec97744bb81be81a4a8707f110b6b22e687bf006d40c1a04fee18118dd49ca`  
		Last Modified: Fri, 01 Oct 2021 03:39:06 GMT  
		Size: 4.2 MB (4151706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc09679318c11692d08f483aac1e7a8d344749aa9b9ef495d0c0d581925d5fbf`  
		Last Modified: Fri, 01 Oct 2021 08:48:06 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f515bcbf2cee10d004afc0f02659f37d3d73159d551e065ad7f3e27c3c846c`  
		Last Modified: Fri, 01 Oct 2021 08:48:05 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23662dd8572b0c37fa42fc96f4da78cdfa818d709f83236844890e3f10f0d92d`  
		Last Modified: Fri, 01 Oct 2021 08:48:13 GMT  
		Size: 185.1 MB (185116246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e334ab7e07d9250054a58457a3153053eb46e9a08e9db80984f622e6e84b61`  
		Last Modified: Fri, 01 Oct 2021 08:48:04 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f22529ca6d49cb869d4f0a455c10dc84d966c4d0922244e452a79893ccea623`  
		Last Modified: Fri, 01 Oct 2021 08:48:04 GMT  
		Size: 10.0 KB (10043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9024c9b4674915436af1db7e8dbd20208fbdc716c9eacef5c76aab2b380fa9fd`  
		Last Modified: Fri, 01 Oct 2021 08:48:06 GMT  
		Size: 13.4 MB (13414860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:latest` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:794d918ef4ab904c026742fee33b3cfd956e82f0c691b2dfba495f681834ca52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301578145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14426d0b0a72ec4d2872543ca1caff24d41513e71fa69e3e241b21664f1479de`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:55 GMT
ADD file:361bb9cf514e8495ad6852f102582c401c790933bf4c44f858eeb9ac564def16 in / 
# Tue, 05 Oct 2021 11:08:00 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 12:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Oct 2021 17:02:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:09:51 GMT
ENV JAVA_VERSION=jdk8u292-b10_openj9-0.26.0
# Wed, 06 Oct 2021 17:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='b75216f7905cff08432a9200a78a2694a4074279f79d859d27f82a998ca1b1e9';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_ppc64le_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='573e72f696d584c3559799766401a0e76e4cbc81740db38cd7415d1f5f8369c0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_s390x_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='6d5b67979e0935febe893895b622647bf8a59df6093ae57074db11d2ac9373ea';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10_openj9-0.26.0/OpenJDK8U-jre_x64_linux_openj9_8u292b10_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Oct 2021 17:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Oct 2021 17:11:51 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 06 Oct 2021 17:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 07 Oct 2021 09:34:23 GMT
ARG LIBERTY_VERSION=21.0.0.9
# Thu, 07 Oct 2021 09:38:59 GMT
ARG LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa
# Thu, 07 Oct 2021 09:39:02 GMT
ARG LIBERTY_BUILD_LABEL=cl210920210824-2341
# Thu, 07 Oct 2021 09:39:04 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip
# Thu, 07 Oct 2021 09:39:11 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 07 Oct 2021 09:39:13 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 07 Oct 2021 09:39:14 GMT
ARG OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:39:19 GMT
ARG VERBOSE=false
# Thu, 07 Oct 2021 09:39:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl210920210824-2341 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.9
# Thu, 07 Oct 2021 09:39:45 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Thu, 07 Oct 2021 09:39:52 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 07 Oct 2021 09:40:23 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 07 Oct 2021 09:40:30 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 07 Oct 2021 09:40:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 07 Oct 2021 09:40:50 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 07 Oct 2021 09:41:43 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl210920210824-2341 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.9/openliberty-runtime-21.0.0.9.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=102958ae6e070c29a7b5c55b4c414953900283fa LIBERTY_VERSION=21.0.0.9 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 07 Oct 2021 09:41:47 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 07 Oct 2021 09:41:49 GMT
USER 1001
# Thu, 07 Oct 2021 09:41:55 GMT
EXPOSE 9080 9443
# Thu, 07 Oct 2021 09:41:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 07 Oct 2021 09:42:02 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:b9dff9847c4194072c728793574720028129f446ababa16785403b9835c873f3`  
		Last Modified: Tue, 05 Oct 2021 11:10:52 GMT  
		Size: 33.3 MB (33290710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529b2916d7c47d5c5430f8a98f7a2c8644de942bac99a8f5d242ce491d1a1841`  
		Last Modified: Wed, 06 Oct 2021 17:26:02 GMT  
		Size: 17.2 MB (17211393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb11e528fe121ddee96f1b0559c2dd99c7dc3f8eb7da7929c24571d7240cec`  
		Last Modified: Wed, 06 Oct 2021 17:30:05 GMT  
		Size: 50.6 MB (50556312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec4bfe3f916f4a74800bdf15be3c379dbf2776e5493a3593c965beaccd2522`  
		Last Modified: Wed, 06 Oct 2021 17:29:58 GMT  
		Size: 3.4 MB (3443457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaeab81cf835a89f1f403c833945d3b554a82588d98c3a010f7a3c7a44fb7d3`  
		Last Modified: Thu, 07 Oct 2021 09:58:40 GMT  
		Size: 8.6 KB (8551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3597446a2d59ddb34b461f023cc3db1ac1723905a3519e42869034df823998df`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ad0e3fe0fa97901df249fb8016cd38c70de162a82c3df588fdc2bf6abbd43d`  
		Last Modified: Thu, 07 Oct 2021 09:58:54 GMT  
		Size: 185.1 MB (185116681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dba658c8a8e6fe991c93dbf05105bd9f2544f66bbda7ad4c47403fd2a06b087`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92bb1230ea89c90a826b0b9b6170dc57b42b86e1852d2aff7baed7c06e5aec4`  
		Last Modified: Thu, 07 Oct 2021 09:58:37 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa3b298a46f54f3c87de572f3e9128bddd47b4c59cb136ca93f36e6ae0d13a2`  
		Last Modified: Thu, 07 Oct 2021 09:58:40 GMT  
		Size: 11.9 MB (11939449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:latest` - linux; s390x

```console
$ docker pull open-liberty@sha256:2f3ab64a31db098c609d95705017615d6009423940e97a5dedd486c04e756db1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291780673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf7411b5e6c96f094adab004b3e241498114fdc2dbea18b790fe2c7df61ed06`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 16 Oct 2021 00:41:46 GMT
ADD file:cf3b6f9c395392eaf2c629969f59c48cde60ae1c74c3dbb13886481999a7a4d5 in / 
# Sat, 16 Oct 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:58:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:58:53 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Oct 2021 01:41:32 GMT
ENV JAVA_VERSION=jdk8u302-b08_openj9-0.27.0
# Thu, 21 Oct 2021 01:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='376f3063225e8117f5b5f35ff73e9284123c377f7c5c6b6da976afd4fc51e8a9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_ppc64le_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        s390x)          ESUM='5bc792eaa0f1404f7d1cc48cad4b95bb192ccb1155fb9b45b228314b23fd71d7';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_s390x_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        amd64|x86_64)          ESUM='9d3d4234b9a579251426c6d498f407bcbed94d10ca572dfdc82c387b9fe9c158';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u302-b08_openj9-0.27.0/ibm-semeru-open-jre_x64_linux_8u302b08_openj9-0.27.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Oct 2021 01:42:33 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 21 Oct 2021 01:43:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 25 Oct 2021 21:45:11 GMT
ARG LIBERTY_VERSION=21.0.0.10
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_BUILD_LABEL=cl211020210920-1900
# Mon, 25 Oct 2021 21:45:56 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip
# Mon, 25 Oct 2021 21:45:57 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Mon, 25 Oct 2021 21:45:57 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Mon, 25 Oct 2021 21:45:57 GMT
ARG OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:45:57 GMT
ARG VERBOSE=false
# Mon, 25 Oct 2021 21:45:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl211020210920-1900 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=21.0.0.10
# Mon, 25 Oct 2021 21:45:58 GMT
COPY dir:e4ff10e677106842e92e637318ee2b51440fb46859dd7032cee783fd3955cb73 in /opt/ol/helpers 
# Mon, 25 Oct 2021 21:45:58 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Mon, 25 Oct 2021 21:46:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Mon, 25 Oct 2021 21:46:14 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 25 Oct 2021 21:46:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 25 Oct 2021 21:46:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Mon, 25 Oct 2021 21:46:34 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl211020210920-1900 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/21.0.0.10/openliberty-runtime-21.0.0.10.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=f4c3d36c31e3f2a83b2bd6acada80ac44bfc6922 LIBERTY_VERSION=21.0.0.10 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Mon, 25 Oct 2021 21:46:35 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 25 Oct 2021 21:46:35 GMT
USER 1001
# Mon, 25 Oct 2021 21:46:35 GMT
EXPOSE 9080 9443
# Mon, 25 Oct 2021 21:46:35 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 25 Oct 2021 21:46:35 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:1f0267805ccac7499fadaabf65e52d4564add2bc20ed25bcf77df24d8debb103`  
		Last Modified: Sat, 16 Oct 2021 00:42:57 GMT  
		Size: 27.1 MB (27120856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276dbe4459a060d2c186c43e5e92d98fa6f181617c55cce69da393b9d5dd6200`  
		Last Modified: Sat, 16 Oct 2021 01:01:03 GMT  
		Size: 15.7 MB (15742080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e93206007a50c4bdb4de374361ca2affa8268672753b2c38eca7a8bc8245565`  
		Last Modified: Thu, 21 Oct 2021 01:48:07 GMT  
		Size: 49.1 MB (49114259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcaf3c72ec5361de0a6aa1d2f58e6f223b73b7ea1414fec7890eb224baf6f0d`  
		Last Modified: Thu, 21 Oct 2021 01:48:03 GMT  
		Size: 3.9 MB (3884545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abe4bf612a292a411455e4db7024f1fb1bac92ab7ef206436a15aa8293e62a2`  
		Last Modified: Mon, 25 Oct 2021 21:53:55 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c5943e5e87b26ebb1312db484cfc931302cbea3604e82aab88b8d529be7cef`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f78318a0320256dac4eb5702c2bff0615a5bea5661fb0b5a797a28513074b10`  
		Last Modified: Mon, 25 Oct 2021 21:54:01 GMT  
		Size: 185.2 MB (185168476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32cd122dc8e75095ad0a6ce27422c754815614825acf3ea5fa984b1682c2575`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f732eec10818b415067f0854ce1829e5147a04ef91f673e12fda5031832bc39a`  
		Last Modified: Mon, 25 Oct 2021 21:53:54 GMT  
		Size: 10.0 KB (10045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d9add8f18e2677ef67b834b2a8c717032332d9b88adc07ad455f329d99f2b0`  
		Last Modified: Mon, 25 Oct 2021 21:53:55 GMT  
		Size: 10.7 MB (10730333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
