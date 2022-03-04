## `open-liberty:kernel-slim-java11-openj9`

```console
$ docker pull open-liberty@sha256:0a142711cc7576afa4258bf1e40fd9c47b3d30a60fafe92514f7212d1740975e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:kernel-slim-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:5fb15ffb3120dbfb53e2a95789f438ef172812247e3f417086958d25732e2153
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110704863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3e3cf2bc5fbce87508f28d45f619bb2ad6121959f52183679f84618fa0565a`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:57:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 07:42:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Feb 2022 19:22:44 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1_openj9-0.30.1
# Fri, 11 Feb 2022 19:24:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7c639ec9fff1e9d401b9e616bd63bf5cf046bbe6381ba89fdc1b2a2aa31c22bd';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_aarch64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f2ac9794343a450d0fcf5be392ce4d6abd5f13a6a1c9beb9e69b0d29abc0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_ppc64le_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f8debbd4326883a47c8afe8bbaabb5ed63d1cd2d82ef42b0fea2c6e2e54f74f1';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_x64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        s390x)          ESUM='c0707d8389945f144f8910314ae8eed1d99dd7a653ae3d8e2f58ce656e3c7349';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_s390x_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 11 Feb 2022 19:24:36 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 19:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Feb 2022 19:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 25 Feb 2022 02:26:10 GMT
ARG LIBERTY_VERSION=22.0.0.2
# Fri, 25 Feb 2022 02:26:11 GMT
ARG LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09
# Fri, 25 Feb 2022 02:26:11 GMT
ARG LIBERTY_BUILD_LABEL=cl220220220201-1901
# Fri, 25 Feb 2022 02:26:11 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip
# Fri, 25 Feb 2022 02:26:11 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 25 Feb 2022 02:26:11 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 25 Feb 2022 02:26:12 GMT
ARG OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:26:12 GMT
ARG VERBOSE=false
# Fri, 25 Feb 2022 02:26:12 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=22.0.0.2
# Fri, 25 Feb 2022 02:26:12 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 25 Feb 2022 02:26:12 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 25 Feb 2022 02:26:18 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 25 Feb 2022 02:26:18 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:26:19 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 25 Feb 2022 02:26:20 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 25 Feb 2022 02:26:28 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 25 Feb 2022 02:26:28 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 25 Feb 2022 02:26:28 GMT
USER 1001
# Fri, 25 Feb 2022 02:26:28 GMT
EXPOSE 9080 9443
# Fri, 25 Feb 2022 02:26:29 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 25 Feb 2022 02:26:29 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a290702f639f2b2f25c1f64f9446f34bd91f353be52bb6c67b3575d304932c8d`  
		Last Modified: Wed, 02 Feb 2022 07:50:26 GMT  
		Size: 16.0 MB (16032322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbf5de6623326de34a7d2963e4ea9b5ea718e5720d7d201ebffb5695e25f06c`  
		Last Modified: Fri, 11 Feb 2022 19:28:09 GMT  
		Size: 47.7 MB (47658309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f6f1ed16cfa548caa1ac1132c8669b1349e2423bb126867e997822e8204bd8`  
		Last Modified: Fri, 11 Feb 2022 19:28:05 GMT  
		Size: 4.2 MB (4181401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab39ca9ad8638b1ce2284cc77b285cbddc6f088f07b588ff9d7e40e0a46c6756`  
		Last Modified: Fri, 25 Feb 2022 02:32:11 GMT  
		Size: 8.1 KB (8111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224a97645fc8a7cbdc2238c436888c40d619517cde30307bd5b75cfbfef467c5`  
		Last Modified: Fri, 25 Feb 2022 02:32:09 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61561b8703d205ac32f11e956e30bb38e35ae0d9d2e7e28b355cc3266cabd55c`  
		Last Modified: Fri, 25 Feb 2022 02:32:10 GMT  
		Size: 11.8 MB (11772149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457b8074da9119733633e42b3541022c98d91845dd8674ce470acc16499c4faf`  
		Last Modified: Fri, 25 Feb 2022 02:32:09 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e41510c140e02c8b508c659e8a9bdce83e408ffffdb43d2c167c089f331cfd`  
		Last Modified: Fri, 25 Feb 2022 02:32:09 GMT  
		Size: 9.2 KB (9215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7f7b3b4e437acf80730d1b5b37f9276c6eb94c72a46f9ed7fa628a059d5439`  
		Last Modified: Fri, 25 Feb 2022 02:32:10 GMT  
		Size: 2.5 MB (2478047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:1d6f83619501c38a7d92ddf2c47f0e8c698275b5967058bdd93d8099486a7f10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116447357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7e428aa774dec84842b8dcb1bfc2bddf5cfd8b6143ed299785fce9d5e342a4`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Feb 2022 06:45:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 11 Feb 2022 19:24:06 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1_openj9-0.30.1
# Fri, 11 Feb 2022 19:27:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7c639ec9fff1e9d401b9e616bd63bf5cf046bbe6381ba89fdc1b2a2aa31c22bd';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_aarch64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f2ac9794343a450d0fcf5be392ce4d6abd5f13a6a1c9beb9e69b0d29abc0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_ppc64le_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f8debbd4326883a47c8afe8bbaabb5ed63d1cd2d82ef42b0fea2c6e2e54f74f1';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_x64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        s390x)          ESUM='c0707d8389945f144f8910314ae8eed1d99dd7a653ae3d8e2f58ce656e3c7349';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_s390x_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 11 Feb 2022 19:27:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Feb 2022 19:27:47 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 11 Feb 2022 19:28:31 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 25 Feb 2022 02:29:20 GMT
ARG LIBERTY_VERSION=22.0.0.2
# Fri, 25 Feb 2022 02:29:26 GMT
ARG LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09
# Fri, 25 Feb 2022 02:29:30 GMT
ARG LIBERTY_BUILD_LABEL=cl220220220201-1901
# Fri, 25 Feb 2022 02:29:35 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip
# Fri, 25 Feb 2022 02:29:38 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Fri, 25 Feb 2022 02:29:39 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Fri, 25 Feb 2022 02:29:43 GMT
ARG OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:29:50 GMT
ARG VERBOSE=false
# Fri, 25 Feb 2022 02:29:55 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=22.0.0.2
# Fri, 25 Feb 2022 02:29:57 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Fri, 25 Feb 2022 02:29:58 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Fri, 25 Feb 2022 02:30:24 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Fri, 25 Feb 2022 02:30:26 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 25 Feb 2022 02:30:35 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 25 Feb 2022 02:30:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Fri, 25 Feb 2022 02:31:10 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Fri, 25 Feb 2022 02:31:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 25 Feb 2022 02:31:26 GMT
USER 1001
# Fri, 25 Feb 2022 02:31:29 GMT
EXPOSE 9080 9443
# Fri, 25 Feb 2022 02:31:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 25 Feb 2022 02:31:34 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14599df444bd4d5693103d52a497e59eae6815ba1988ceb343c30d5ee76d645`  
		Last Modified: Wed, 02 Feb 2022 07:00:07 GMT  
		Size: 17.2 MB (17206879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4bd076876faf2f0233df3e5062e9079ea0e65d66b1a00b6546775ccf35a16f`  
		Last Modified: Fri, 11 Feb 2022 19:33:28 GMT  
		Size: 48.4 MB (48356013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8862a35e96ccf63d16c503c7d9874834dce679147273f8634d02e4cc45804df5`  
		Last Modified: Fri, 11 Feb 2022 19:33:20 GMT  
		Size: 3.3 MB (3340086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a37a223beb51d59e64a186c09e3bc2c52083ef2546314a28c8c17994ebfba4`  
		Last Modified: Fri, 25 Feb 2022 02:50:41 GMT  
		Size: 8.1 KB (8115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1378e41a0a49c4161825a2c88e36a0f937bb5b3a64d168389f2001010e84703`  
		Last Modified: Fri, 25 Feb 2022 02:50:38 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d3af24f635958edf6e656007aad6683c99d70643d5f2e46178ffd058274656`  
		Last Modified: Fri, 25 Feb 2022 02:50:41 GMT  
		Size: 11.8 MB (11772841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6b3b53cbd4e8ec95bf269f23ecaac64ebcd73d66c23f6f152be184ce8f4cc1`  
		Last Modified: Fri, 25 Feb 2022 02:50:37 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae571ee1984ea6b47027562b83f10f0385dd4a84302c566aea6c0bcd82628c1e`  
		Last Modified: Fri, 25 Feb 2022 02:50:38 GMT  
		Size: 9.2 KB (9237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e9746458e8ca8aa47190cc5f93008774d2cd454aac8c2c1779551c2ad08703`  
		Last Modified: Fri, 25 Feb 2022 02:50:39 GMT  
		Size: 2.5 MB (2468254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:kernel-slim-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:4fd8b5a7c4e910cf10240c30fc55555750e1f7f4d16e059c294e7055d2a1a905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108061509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b0085c7f62314e6d9609327ac825682683c5871a36d82291190016397f6124`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:52 GMT
ADD file:3162233da685a36a9f274a7fa1d99452cab76f37e3640d38851c782ca506f75b in / 
# Thu, 03 Mar 2022 19:41:53 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 19:59:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Mar 2022 20:04:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:06:17 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1_openj9-0.30.1
# Thu, 03 Mar 2022 20:07:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7c639ec9fff1e9d401b9e616bd63bf5cf046bbe6381ba89fdc1b2a2aa31c22bd';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_aarch64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7f2ac9794343a450d0fcf5be392ce4d6abd5f13a6a1c9beb9e69b0d29abc0a60';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_ppc64le_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        amd64|x86_64)          ESUM='f8debbd4326883a47c8afe8bbaabb5ed63d1cd2d82ef42b0fea2c6e2e54f74f1';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_x64_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        s390x)          ESUM='c0707d8389945f144f8910314ae8eed1d99dd7a653ae3d8e2f58ce656e3c7349';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.14.1%2B1_openj9-0.30.1/ibm-semeru-open-jre_s390x_linux_11.0.14.1_1_openj9-0.30.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 03 Mar 2022 20:07:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 20:07:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 03 Mar 2022 20:07:52 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 03 Mar 2022 22:45:53 GMT
ARG LIBERTY_VERSION=22.0.0.2
# Thu, 03 Mar 2022 22:45:53 GMT
ARG LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09
# Thu, 03 Mar 2022 22:45:54 GMT
ARG LIBERTY_BUILD_LABEL=cl220220220201-1901
# Thu, 03 Mar 2022 22:45:54 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip
# Thu, 03 Mar 2022 22:45:54 GMT
ARG LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE
# Thu, 03 Mar 2022 22:45:54 GMT
ARG LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7
# Thu, 03 Mar 2022 22:45:54 GMT
ARG OPENJ9_SCC=true
# Thu, 03 Mar 2022 22:45:54 GMT
ARG VERBOSE=false
# Thu, 03 Mar 2022 22:45:54 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Leo Christy Jesuraj org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl220220220201-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=22.0.0.2
# Thu, 03 Mar 2022 22:45:54 GMT
COPY dir:dea07490d51f53c887a4a2d6ade59fdcb72993a025bee3d76672fb9870bb0ef2 in /opt/ol/helpers 
# Thu, 03 Mar 2022 22:45:54 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Thu, 03 Mar 2022 22:46:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && rm -rf /var/lib/apt/lists/*     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && wget -q $LIBERTY_LICENSE_URL -O /licenses/LICENSE     && echo "$LIBERTY_LICENSE_SHA /licenses/LICENSE" | sha1sum -c --strict --check     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Thu, 03 Mar 2022 22:46:00 GMT
ENV PATH=/opt/ol/wlp/bin:/opt/ol/docker/:/opt/ol/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 03 Mar 2022 22:46:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 03 Mar 2022 22:46:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Thu, 03 Mar 2022 22:46:07 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl220220220201-1901 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/22.0.0.2/openliberty-kernel-22.0.0.2.zip LIBERTY_LICENSE_SHA=84f00503d6516c91190de866e78d6010899673b7 LIBERTY_LICENSE_URL=https://raw.githubusercontent.com/OpenLiberty/open-liberty/master/LICENSE LIBERTY_SHA=b4c24ef4b546055015af001a22fdbafe10216a09 LIBERTY_VERSION=22.0.0.2 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Thu, 03 Mar 2022 22:46:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 03 Mar 2022 22:46:07 GMT
USER 1001
# Thu, 03 Mar 2022 22:46:07 GMT
EXPOSE 9080 9443
# Thu, 03 Mar 2022 22:46:07 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 03 Mar 2022 22:46:07 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:ade7e68f4e34f438527a34c9761a285c3c3864e3daab0544b2c4f4163c7c3f56`  
		Last Modified: Thu, 03 Mar 2022 19:43:22 GMT  
		Size: 27.1 MB (27084671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6625b9cdb7a6f1a1f7715f9b1e2a04e2e285aa79c11778a4edeca0017ab83b5`  
		Last Modified: Thu, 03 Mar 2022 20:12:44 GMT  
		Size: 15.7 MB (15739982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706208334bd704c42d52eb92ef8018d846fd321bf5e403fde491557477c8bc8`  
		Last Modified: Thu, 03 Mar 2022 20:13:41 GMT  
		Size: 46.7 MB (46692257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eb36864da8ed2097d1a87555b6460db3184759a34200e5599c4e633bc8b11e`  
		Last Modified: Thu, 03 Mar 2022 20:13:35 GMT  
		Size: 4.3 MB (4258402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931c505e3a1406589ca62732f1987c5fc7f993fa72605af847f85173664420c0`  
		Last Modified: Thu, 03 Mar 2022 22:58:02 GMT  
		Size: 8.1 KB (8109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9729f385dd099b608b4ec62b7b853c5e4cb04b545ac1646251b3ba4c45826b10`  
		Last Modified: Thu, 03 Mar 2022 22:58:02 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fc2b852b4f4111597bbfa7090120921adc0d33dc3f55434de4752c028aceba`  
		Last Modified: Thu, 03 Mar 2022 22:58:02 GMT  
		Size: 11.8 MB (11772522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f379fcdbe7f690d1d13330ff41da3ed2cdc9230493cbdcf38fb60225e52935e6`  
		Last Modified: Thu, 03 Mar 2022 22:58:01 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfde615df016225c71703e01687304bcd18ae9bab5964394965c4e4663d33e2`  
		Last Modified: Thu, 03 Mar 2022 22:58:01 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d916ea10aee263c9281f1b0987570cbff7ae64ea6c786aac01129882a3a10fe8`  
		Last Modified: Thu, 03 Mar 2022 22:58:01 GMT  
		Size: 2.5 MB (2495147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
