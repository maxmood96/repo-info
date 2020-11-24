## `open-liberty:full-java11-openj9`

```console
$ docker pull open-liberty@sha256:c890cc586507f0f7979252cca708dc50554ff9fd656b152c4eda949998a2016c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:8ac167d3164315d4fd74bef7d9122c3532f42544ed0957056825eb49aa5cf6ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279171024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca444551af85dd00b08e3cfc5fea00b3c589831ac2e4369aa4f839c1f7a282a`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Oct 2020 17:32:33 GMT
ADD file:435d9776fdd3a1834f344fb82e459dbbb67cd50c71ab5e29b719273888d5bb7c in / 
# Fri, 23 Oct 2020 17:32:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:32:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 17:32:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:32:36 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:19:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:20:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 17:25:27 GMT
ENV JAVA_VERSION=jdk-11.0.9+11_openj9-0.23.0
# Wed, 28 Oct 2020 17:27:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b73f406dba1560dc194ac891452a1aacc2ba3b3e5e7b55e91a64559f8c2d9539';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_aarch64_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='256a01e045867dcbbc541a6dd95ed315599f737b278319c4b936ce5a8a464424';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        s390x)          ESUM='91b74f434a3d7000dac788693f0b1e5288bd99c9bc6ef345ba6e165957defcf3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        amd64|x86_64)          ESUM='54c845c167c197ba789eb6c3508faa5b1c95c9abe2ac26878123b6eecc87a111';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_x64_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 28 Oct 2020 17:27:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Oct 2020 17:27:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Wed, 28 Oct 2020 17:28:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     SCC_GEN_RUNS_COUNT=3;     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 28 Oct 2020 17:28:53 GMT
ENV OPENJ9_JAVA_OPTIONS=-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 24 Nov 2020 01:52:18 GMT
ARG LIBERTY_VERSION=20.0.0.12
# Tue, 24 Nov 2020 01:53:48 GMT
ARG LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e
# Tue, 24 Nov 2020 01:53:48 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 01:53:48 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip
# Tue, 24 Nov 2020 01:53:48 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 01:53:48 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 01:53:49 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:53:49 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 01:53:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=20.0.0.12
# Tue, 24 Nov 2020 01:53:49 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 01:53:49 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 01:54:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 01:54:01 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:54:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 01:54:03 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 01:54:42 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 01:54:42 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 01:54:43 GMT
USER 1001
# Tue, 24 Nov 2020 01:54:43 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 01:54:43 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 01:54:43 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6a5697faee43339ef8e33e3839060252392ad99325a48f7c9d7e93c22db4d4cf`  
		Last Modified: Thu, 08 Oct 2020 15:19:51 GMT  
		Size: 28.6 MB (28558714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba13d3bc422b493440f97a8f148d245e1999cb616cb05876edc3ef29e79852f2`  
		Last Modified: Fri, 23 Oct 2020 17:33:25 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a254829d9e55168306fd80a49e02eb015551facee9c444d9dce3b26d19238b82`  
		Last Modified: Fri, 23 Oct 2020 17:33:25 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03adaffd7e576f90e30e1dede0962fbbb0b58baede693e6375c2c137e506ef92`  
		Last Modified: Wed, 28 Oct 2020 17:37:00 GMT  
		Size: 16.0 MB (16031340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25c6ae47f01d1ca61746122b9b904e8cf3d3f16e048774c5c301b535c035c87`  
		Last Modified: Wed, 28 Oct 2020 17:40:51 GMT  
		Size: 42.8 MB (42770675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bffedeca141cd6b2ed75ae8a7aea20289574815afef5089ea410c4305532a8`  
		Last Modified: Wed, 28 Oct 2020 17:40:44 GMT  
		Size: 4.4 MB (4431006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26960407c3776c8b5df4a9fbf761863b267bef198b4fce4f1ef2bc52ab4a0980`  
		Last Modified: Tue, 24 Nov 2020 01:57:57 GMT  
		Size: 8.5 KB (8516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e929c87ce24fca4109057fadaf4288c2fec5fa8189f17894b1aa512ea9095776`  
		Last Modified: Tue, 24 Nov 2020 01:57:56 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830cb5582179b38d8d635e7d9596337d35fe6bf586f1079eb6a48f7ce8a3b0bd`  
		Last Modified: Tue, 24 Nov 2020 01:58:07 GMT  
		Size: 173.6 MB (173562103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9acb0edaf613f391a8ea09d433c0257d011381b422f23886f5c9840c5865a1`  
		Last Modified: Tue, 24 Nov 2020 01:57:57 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037abc0895b48f5936b240d870104a8720c29d0cd9eb9a27c614ab1643d026b6`  
		Last Modified: Tue, 24 Nov 2020 01:57:57 GMT  
		Size: 9.9 KB (9900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9db8da445ba07b490b0394018ad9883786e4b1047f183caabc203fb2b0208b`  
		Last Modified: Tue, 24 Nov 2020 01:57:59 GMT  
		Size: 13.8 MB (13796295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:ad5f1845f680d430a69059362583d8cf15e5a40857c7705624d1d46e38dc7117
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283191950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416dbec692ae7e5086385a69fbff91be75a5ed94c45dbe91e83029b74344c2ce`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Oct 2020 19:25:52 GMT
ADD file:b9c09681764b8697badc8139e82a30efeb353faf61258695d1cd3a843c4de6a8 in / 
# Fri, 23 Oct 2020 19:26:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:26:38 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:26:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:27:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:17:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:19:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 17:29:32 GMT
ENV JAVA_VERSION=jdk-11.0.9+11_openj9-0.23.0
# Wed, 28 Oct 2020 17:32:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b73f406dba1560dc194ac891452a1aacc2ba3b3e5e7b55e91a64559f8c2d9539';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_aarch64_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='256a01e045867dcbbc541a6dd95ed315599f737b278319c4b936ce5a8a464424';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        s390x)          ESUM='91b74f434a3d7000dac788693f0b1e5288bd99c9bc6ef345ba6e165957defcf3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        amd64|x86_64)          ESUM='54c845c167c197ba789eb6c3508faa5b1c95c9abe2ac26878123b6eecc87a111';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_x64_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 28 Oct 2020 17:32:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Oct 2020 17:32:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Wed, 28 Oct 2020 17:34:18 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     SCC_GEN_RUNS_COUNT=3;     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 28 Oct 2020 17:34:21 GMT
ENV OPENJ9_JAVA_OPTIONS=-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 24 Nov 2020 03:41:52 GMT
ARG LIBERTY_VERSION=20.0.0.12
# Tue, 24 Nov 2020 03:47:55 GMT
ARG LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e
# Tue, 24 Nov 2020 03:48:00 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 03:48:04 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip
# Tue, 24 Nov 2020 03:48:07 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 03:48:09 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 03:48:13 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 03:48:16 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 03:48:19 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=20.0.0.12
# Tue, 24 Nov 2020 03:48:20 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 03:48:22 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 03:48:51 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 03:48:58 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 03:49:06 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 03:49:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 03:50:44 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 03:50:50 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 03:50:53 GMT
USER 1001
# Tue, 24 Nov 2020 03:50:57 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 03:51:05 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 03:51:10 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:76ff736f6fb2d41940a6cbdeab4242e9a64ef7df99ee4f3d9fcb9ec67bfccfc6`  
		Last Modified: Mon, 12 Oct 2020 16:20:28 GMT  
		Size: 33.3 MB (33275528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3d354673d1251716a1ed9cc3460095ee31664859e23d7e616546a17d287728`  
		Last Modified: Fri, 23 Oct 2020 19:31:29 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434fabf01a92cfd54e3ae6f5e3dc7a3837ac2199999f713fbdf5cb2c800324a2`  
		Last Modified: Fri, 23 Oct 2020 19:31:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb82384b001eeabdc2ca426e902a10696a33f7e7723f24eca9f4848ebbe13a5e`  
		Last Modified: Wed, 28 Oct 2020 17:47:13 GMT  
		Size: 17.2 MB (17208276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9518fb573dc23ad650fc0ea068af5f93f07e910761dbb8b83156f14d391027`  
		Last Modified: Wed, 28 Oct 2020 17:53:00 GMT  
		Size: 43.7 MB (43650458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7e2048088ed2d44960340a046c30cd88499c7356ea5d5da70160cb9286e6de`  
		Last Modified: Wed, 28 Oct 2020 17:52:52 GMT  
		Size: 3.5 MB (3464582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ca5f33c45bc1fb66d815593bed20c1fa116c2577117135a535b975e6d0669a`  
		Last Modified: Tue, 24 Nov 2020 03:59:45 GMT  
		Size: 8.5 KB (8549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c5b1d0f1062df749fafac658321c6e09b301a3bb5b4d2d353ba2e721fbb421`  
		Last Modified: Tue, 24 Nov 2020 03:59:41 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7066a36d28eb4dc8face0f1d38076e2d893d57d601a1ae4cc766f838b906d6a`  
		Last Modified: Tue, 24 Nov 2020 03:59:59 GMT  
		Size: 173.6 MB (173562818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fb888ec1de655aefa72caec26571dc95f30b98e5b733523bf02966728c8295`  
		Last Modified: Tue, 24 Nov 2020 03:59:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ca8149a48aaf46787b9df7436786ec7c870640634a3947a72dd4e0c6b619af`  
		Last Modified: Tue, 24 Nov 2020 03:59:42 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b939e34871786a62e214174d2588eef1dbda71eb753de5aae93a05048e64d6`  
		Last Modified: Tue, 24 Nov 2020 03:59:46 GMT  
		Size: 12.0 MB (12009096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:cf8858f9efaa44ced868f90cd690c36f386073702faeff5ac20268392b385d55
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275674712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82702e38a99d995b87e8195a1b9f3bce7c6281033b881d6bffbb7bc29cff87a0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Oct 2020 19:09:19 GMT
ADD file:9b934c86e9ab1dd29cef318d8dd9cd1228b9d92124f434c50ad7d03ede1a5c76 in / 
# Fri, 23 Oct 2020 19:09:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:09:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:09:27 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:09:27 GMT
CMD ["/bin/bash"]
# Wed, 28 Oct 2020 17:41:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Oct 2020 17:41:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Oct 2020 17:47:34 GMT
ENV JAVA_VERSION=jdk-11.0.9+11_openj9-0.23.0
# Wed, 28 Oct 2020 17:49:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b73f406dba1560dc194ac891452a1aacc2ba3b3e5e7b55e91a64559f8c2d9539';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_aarch64_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='256a01e045867dcbbc541a6dd95ed315599f737b278319c4b936ce5a8a464424';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        s390x)          ESUM='91b74f434a3d7000dac788693f0b1e5288bd99c9bc6ef345ba6e165957defcf3';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        amd64|x86_64)          ESUM='54c845c167c197ba789eb6c3508faa5b1c95c9abe2ac26878123b6eecc87a111';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.9%2B11_openj9-0.23.0/OpenJDK11U-jre_x64_linux_openj9_11.0.9_11_openj9-0.23.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 28 Oct 2020 17:49:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Oct 2020 17:49:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Wed, 28 Oct 2020 17:51:11 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     SCC_GEN_RUNS_COUNT=3;     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     for i in $(seq 0 $SCC_GEN_RUNS_COUNT);     do         "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;         sleep 5;         "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh;         sleep 5;     done;         FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 28 Oct 2020 17:51:11 GMT
ENV OPENJ9_JAVA_OPTIONS=-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 24 Nov 2020 01:51:10 GMT
ARG LIBERTY_VERSION=20.0.0.12
# Tue, 24 Nov 2020 01:53:31 GMT
ARG LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e
# Tue, 24 Nov 2020 01:53:32 GMT
ARG LIBERTY_BUILD_LABEL=cl201220201111-0736
# Tue, 24 Nov 2020 01:53:33 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip
# Tue, 24 Nov 2020 01:53:33 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Tue, 24 Nov 2020 01:53:34 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Tue, 24 Nov 2020 01:53:34 GMT
ARG OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:53:35 GMT
ARG VERBOSE=false
# Tue, 24 Nov 2020 01:53:35 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the Open Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=20.0.0.12
# Tue, 24 Nov 2020 01:53:36 GMT
COPY dir:7aff51efcc7f992aebc75df1ed45eed67c8a6f2121249c7fc7b35f23cc108b3d in /opt/ol/helpers 
# Tue, 24 Nov 2020 01:53:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Tue, 24 Nov 2020 01:54:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Tue, 24 Nov 2020 01:54:10 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 24 Nov 2020 01:54:13 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Tue, 24 Nov 2020 01:54:15 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Tue, 24 Nov 2020 01:54:55 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl201220201111-0736 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/20.0.0.12/openliberty-runtime-20.0.0.12.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=18deec3a143a6a2ac46c717722a90678c524fa4e LIBERTY_VERSION=20.0.0.12 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Tue, 24 Nov 2020 01:54:57 GMT
ENV RANDFILE=/tmp/.rnd
# Tue, 24 Nov 2020 01:54:58 GMT
USER 1001
# Tue, 24 Nov 2020 01:54:58 GMT
EXPOSE 9080 9443
# Tue, 24 Nov 2020 01:54:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 24 Nov 2020 01:55:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d3e8e1a5d50716d6aabb0cef46599f9e7a722a560910d6f724737aaef0a7d6c3`  
		Last Modified: Mon, 12 Oct 2020 16:45:31 GMT  
		Size: 27.2 MB (27224393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04282efaafb3c9b53bba677fc3c06c478dc1613c1f21939bfa2c113aeef2f99c`  
		Last Modified: Fri, 23 Oct 2020 19:10:20 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6269ae100536d7559ae6ebe6606b4405ebb706c3d963926c5568b6e7fd954582`  
		Last Modified: Fri, 23 Oct 2020 19:10:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cd8065d26d8f90607b2debf915de6242befbe898f8fb305dbd99dc8df92d3a`  
		Last Modified: Wed, 28 Oct 2020 17:59:30 GMT  
		Size: 15.8 MB (15772935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85326a811af266d8284989b860fcf1e92ea12f9c383c5a2b79a622b2096ba7a7`  
		Last Modified: Wed, 28 Oct 2020 18:03:12 GMT  
		Size: 42.0 MB (42029813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426d45bc780f2843a5e6d7b59b2552d62db894ec6a13ee501d17d38dfc0046a1`  
		Last Modified: Wed, 28 Oct 2020 18:03:07 GMT  
		Size: 4.1 MB (4063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344e65c3ba5a16c5dd909c6e53eac95b33cc0a725b8742041ab132b8acdc58d7`  
		Last Modified: Tue, 24 Nov 2020 01:59:23 GMT  
		Size: 8.6 KB (8550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d222d1410cf85d1ac39c8864bb3725d32e7cc44f66c2cadd94c1ab7f96538f`  
		Last Modified: Tue, 24 Nov 2020 01:59:20 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5fbd96f805566c525d74ef696ec238f40b31d37f9c720325b6d642512420d4`  
		Last Modified: Tue, 24 Nov 2020 01:59:29 GMT  
		Size: 173.6 MB (173562229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc5fe6b35b72a7f4f16643e730bdb317016f89873f7b8554303737b8cdeed5f`  
		Last Modified: Tue, 24 Nov 2020 01:59:21 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b2ef38a3542aac1ccde9752c2ff0bedbaaa290e6bc9c6a4f27412f4b479e34`  
		Last Modified: Tue, 24 Nov 2020 01:59:21 GMT  
		Size: 10.0 KB (10040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2131ce0269b35e413ed535491ce5fbbdd0106e65c99ae0291ed716ae9643cb4`  
		Last Modified: Tue, 24 Nov 2020 01:59:22 GMT  
		Size: 13.0 MB (13000392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
