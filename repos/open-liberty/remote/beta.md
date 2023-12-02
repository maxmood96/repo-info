## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:aa8f452a7322f041b51a960ab92c81ffd9f47ddd10e35b2e34ee4b00a19cd2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `open-liberty:beta` - linux; amd64

```console
$ docker pull open-liberty@sha256:0ac318a02ff483c28976504f6e61ed95404bae98fd23947daae22e3dbf77a11b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.1 MB (437100990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894b53d57841c77fc40a7dbea80fe4abe4884afd153cab26deffd7950667d6bb`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 02:23:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 02:24:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 02:24:18 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Sat, 02 Dec 2023 02:26:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 02 Dec 2023 02:26:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 02:26:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 02 Dec 2023 02:26:38 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 02 Dec 2023 11:27:37 GMT
USER root
# Sat, 02 Dec 2023 11:27:37 GMT
ARG LIBERTY_VERSION=23.0.0.12-beta
# Sat, 02 Dec 2023 11:27:37 GMT
ARG LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8
# Sat, 02 Dec 2023 11:27:37 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip
# Sat, 02 Dec 2023 11:27:37 GMT
ARG LIBERTY_BUILD_LABEL=cl231120231030-1102
# Sat, 02 Dec 2023 11:27:37 GMT
ARG OPENJ9_SCC=true
# Sat, 02 Dec 2023 11:27:37 GMT
ARG VERBOSE=false
# Sat, 02 Dec 2023 11:27:37 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl231120231030-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=23.0.0.12-beta
# Sat, 02 Dec 2023 11:27:37 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Sat, 02 Dec 2023 11:27:37 GMT
COPY dir:3a03be0df9fe59a90276be087434855a86a8818483ded6f49c3c57610fb6842d in /opt/ol/helpers 
# Sat, 02 Dec 2023 11:27:37 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Sat, 02 Dec 2023 11:27:38 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 02 Dec 2023 11:28:00 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Sat, 02 Dec 2023 11:28:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Sat, 02 Dec 2023 11:28:02 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Sat, 02 Dec 2023 11:28:03 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Sat, 02 Dec 2023 11:28:31 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Sat, 02 Dec 2023 11:28:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 02 Dec 2023 11:28:31 GMT
USER 1001
# Sat, 02 Dec 2023 11:28:31 GMT
EXPOSE 9080 9443
# Sat, 02 Dec 2023 11:28:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Sat, 02 Dec 2023 11:28:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a261eab81e521775977f42fd67a3196085829d7723b5ca804ff8e0e504f9526`  
		Last Modified: Sat, 02 Dec 2023 02:37:49 GMT  
		Size: 12.2 MB (12155087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67567e6a9c4f679dca2a5989ca4c7110f6377f7bd4383731c9b4a735376fa978`  
		Last Modified: Sat, 02 Dec 2023 02:38:24 GMT  
		Size: 50.2 MB (50214665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800147cf0190a1d23019372d77e9499483900914ba37e636b02627d9d537ef22`  
		Last Modified: Sat, 02 Dec 2023 02:38:19 GMT  
		Size: 4.2 MB (4189669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749acccad77fd1fe2c8f9fd1cb438723a4ef1da60668fe77292dbff5ffc71a00`  
		Last Modified: Sat, 02 Dec 2023 11:42:40 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354f2d941bf2e3c2115441ce8572c294d367c58cbdcfa07e832e611d2c898bbc`  
		Last Modified: Sat, 02 Dec 2023 11:42:40 GMT  
		Size: 9.6 KB (9581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41283d9f401c9909c21248896b87ec913924e44aa43596573325cbf7f1ee60e`  
		Last Modified: Sat, 02 Dec 2023 11:42:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2035536846512181da5497b9e58045194d78aee35726061fc9a5ef344d20102f`  
		Last Modified: Sat, 02 Dec 2023 11:42:38 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e492ec657dc332f62f7496bb5e07b7c92576518b0a668c25ffd059130e5069`  
		Last Modified: Sat, 02 Dec 2023 11:42:53 GMT  
		Size: 327.4 MB (327442449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a9eaa06ae0a0ea0ed3c0ef9806f2501e5380f7825225f560cbb17f157fb755`  
		Last Modified: Sat, 02 Dec 2023 11:42:38 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be1a642946ccca4e4adafb19219aea28be7e539341927eabfa5f4a96c01a9f`  
		Last Modified: Sat, 02 Dec 2023 11:42:38 GMT  
		Size: 11.0 KB (11037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b1d7bc6d96054e55f0906afca7998209c87c3cb03ce0a04bad031ac284657d`  
		Last Modified: Sat, 02 Dec 2023 11:42:40 GMT  
		Size: 12.6 MB (12597907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:a7f58ac72fa9899c17287636ef135700538bed3c6abf0c3bb3c626f4e4038a86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.3 MB (433283653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d058853a79db90ca28657a88d95a424e9d07860d74ee2084ed9a3a8b3838799`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 07:20:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 07:21:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 07:21:21 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Sat, 02 Dec 2023 07:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 02 Dec 2023 07:22:53 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 07:22:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 02 Dec 2023 07:23:28 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 02 Dec 2023 13:07:35 GMT
USER root
# Sat, 02 Dec 2023 13:07:35 GMT
ARG LIBERTY_VERSION=23.0.0.12-beta
# Sat, 02 Dec 2023 13:07:35 GMT
ARG LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8
# Sat, 02 Dec 2023 13:07:35 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip
# Sat, 02 Dec 2023 13:07:35 GMT
ARG LIBERTY_BUILD_LABEL=cl231120231030-1102
# Sat, 02 Dec 2023 13:07:35 GMT
ARG OPENJ9_SCC=true
# Sat, 02 Dec 2023 13:07:35 GMT
ARG VERBOSE=false
# Sat, 02 Dec 2023 13:07:35 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl231120231030-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=23.0.0.12-beta
# Sat, 02 Dec 2023 13:07:35 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Sat, 02 Dec 2023 13:07:36 GMT
COPY dir:3a03be0df9fe59a90276be087434855a86a8818483ded6f49c3c57610fb6842d in /opt/ol/helpers 
# Sat, 02 Dec 2023 13:07:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Sat, 02 Dec 2023 13:07:37 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 02 Dec 2023 13:07:58 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Sat, 02 Dec 2023 13:08:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Sat, 02 Dec 2023 13:08:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Sat, 02 Dec 2023 13:08:01 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Sat, 02 Dec 2023 13:08:27 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Sat, 02 Dec 2023 13:08:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 02 Dec 2023 13:08:27 GMT
USER 1001
# Sat, 02 Dec 2023 13:08:27 GMT
EXPOSE 9080 9443
# Sat, 02 Dec 2023 13:08:27 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Sat, 02 Dec 2023 13:08:27 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95c7df977cc051774d451b6622a7dec0910ee80283f12ed6e3d66e2fa624c39`  
		Last Modified: Sat, 02 Dec 2023 07:34:00 GMT  
		Size: 12.1 MB (12113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32545047fa21dba67c74fe7f856d15fb56311a475a5da764de5d3bd6247f265e`  
		Last Modified: Sat, 02 Dec 2023 07:34:32 GMT  
		Size: 49.0 MB (49049501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5289844a1aec2816c92a7ad5fba4ecfd00921823c37f064ed748e2d2239d90f`  
		Last Modified: Sat, 02 Dec 2023 07:34:28 GMT  
		Size: 4.1 MB (4078389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac79254fbf0defd731babde45f21b9f5db873b3d2e6c9ab0cffaacff991cad85`  
		Last Modified: Sat, 02 Dec 2023 13:20:25 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc4fa7787059d8cb153a4beb82ac12e0cd362f28ea113052bab4c5f863d5838`  
		Last Modified: Sat, 02 Dec 2023 13:20:25 GMT  
		Size: 9.6 KB (9582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f326b6059b44d0c526a1ac95ee057276b12a6452446bc5c1a91dd1db2b658e`  
		Last Modified: Sat, 02 Dec 2023 13:20:24 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff66336eb46181d4800e74a5832cf95b14c623d584c7d7bdf67db4054e164c0`  
		Last Modified: Sat, 02 Dec 2023 13:20:23 GMT  
		Size: 42.3 KB (42319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7b9527da7a4eec725fd0af6681bc933bddd898789ad948e29ed90a1c49cbfe`  
		Last Modified: Sat, 02 Dec 2023 13:20:35 GMT  
		Size: 327.4 MB (327443820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5de8a42ea65e6a698db763ddc124591e4cf98b9460af4a7365671ceac887f12`  
		Last Modified: Sat, 02 Dec 2023 13:20:23 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bb037f5eae09526d53d5250a5134cb69805017f89d56cb66aed13bc8b489a6`  
		Last Modified: Sat, 02 Dec 2023 13:20:23 GMT  
		Size: 11.0 KB (11034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e970da1a2821bb00c69bba305a31ede709b98966ebe1692d69d1916f81482984`  
		Last Modified: Sat, 02 Dec 2023 13:20:25 GMT  
		Size: 12.1 MB (12132639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:ce3435c53f60beaf299593712573352976e3d5acf727e339068961a3f26b4e3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.5 MB (441455231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e30228be5a3c112cca3a1bba19d2f0352ee20e6e44d85eac00ee9c983bdbad`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Dec 2023 08:12:00 GMT
ARG RELEASE
# Fri, 01 Dec 2023 08:12:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 08:12:00 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 08:12:03 GMT
ADD file:80047e51fa5311c19317ab688acec0517d98f1cbf74fa4c22a7105e80ebaf610 in / 
# Fri, 01 Dec 2023 08:12:04 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:43:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 05:43:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:43:54 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Sat, 02 Dec 2023 05:45:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 02 Dec 2023 05:45:49 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 05:45:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 02 Dec 2023 05:46:28 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 02 Dec 2023 06:54:51 GMT
USER root
# Sat, 02 Dec 2023 06:54:52 GMT
ARG LIBERTY_VERSION=23.0.0.12-beta
# Sat, 02 Dec 2023 06:54:52 GMT
ARG LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8
# Sat, 02 Dec 2023 06:54:52 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip
# Sat, 02 Dec 2023 06:54:53 GMT
ARG LIBERTY_BUILD_LABEL=cl231120231030-1102
# Sat, 02 Dec 2023 06:54:54 GMT
ARG OPENJ9_SCC=true
# Sat, 02 Dec 2023 06:54:54 GMT
ARG VERBOSE=false
# Sat, 02 Dec 2023 06:54:55 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl231120231030-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=23.0.0.12-beta
# Sat, 02 Dec 2023 06:54:55 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Sat, 02 Dec 2023 06:54:56 GMT
COPY dir:3a03be0df9fe59a90276be087434855a86a8818483ded6f49c3c57610fb6842d in /opt/ol/helpers 
# Sat, 02 Dec 2023 06:54:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Sat, 02 Dec 2023 06:54:59 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 02 Dec 2023 06:55:33 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Sat, 02 Dec 2023 06:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Sat, 02 Dec 2023 06:55:39 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Sat, 02 Dec 2023 06:55:41 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Sat, 02 Dec 2023 06:56:16 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Sat, 02 Dec 2023 06:56:17 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 02 Dec 2023 06:56:17 GMT
USER 1001
# Sat, 02 Dec 2023 06:56:18 GMT
EXPOSE 9080 9443
# Sat, 02 Dec 2023 06:56:18 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Sat, 02 Dec 2023 06:56:18 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:c3606768af36fe4984cee7cfc0c9d919a7adf83ac4c1849c30da06916b9ec921`  
		Last Modified: Sat, 02 Dec 2023 04:49:10 GMT  
		Size: 35.7 MB (35662741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e1289b324ba8aebce68e0b4c55bfd6dc2b19fb9e45f5002f71f6d5b2765d4`  
		Last Modified: Sat, 02 Dec 2023 05:59:13 GMT  
		Size: 12.9 MB (12891067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae6a57a5082490ef3c2c32abe4f5b200007f3fd51cb3138fabf2d57268fb03a`  
		Last Modified: Sat, 02 Dec 2023 05:59:52 GMT  
		Size: 50.7 MB (50680376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ec1a6983ee37b7a957da9b3ad1b129713303a86c26a48c47ff313fef9e5b34`  
		Last Modified: Sat, 02 Dec 2023 05:59:47 GMT  
		Size: 3.5 MB (3510198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90050433b005f236c368b59cb4ab730b31c51fc0d80c23ee02baf79498cf2173`  
		Last Modified: Sat, 02 Dec 2023 07:22:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932be413540bc0e5d53b350a29a6a078f4d08296cf21f080744877370b721365`  
		Last Modified: Sat, 02 Dec 2023 07:22:56 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecce9115ebbfb02692a3ed596c61875de1a2780934360aab8229dbcf8c5a55b7`  
		Last Modified: Sat, 02 Dec 2023 07:22:56 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cced89da9d7281c3c9f5bba115bf7972f335c3d4fe45a31d3106de9ad3980c4f`  
		Last Modified: Sat, 02 Dec 2023 07:22:53 GMT  
		Size: 36.5 KB (36494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd79efddfb00bd319fcaf147c3ad890c53a929b8fe2188e9680152b9886c4e36`  
		Last Modified: Sat, 02 Dec 2023 07:23:10 GMT  
		Size: 327.4 MB (327443020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ae901386b02203c1c78a29ded39b97bdf8da4bd52857c4267d413d6fbf9e3`  
		Last Modified: Sat, 02 Dec 2023 07:22:53 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac21082fcf756f24dd9a0b648e1885724e25d85d56d22874a18629eb680fb9e`  
		Last Modified: Sat, 02 Dec 2023 07:22:53 GMT  
		Size: 11.1 KB (11054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95635d18361eefef4c3ebbe961b5f68544b2693ac88b777dae2bf1561d5ac621`  
		Last Modified: Sat, 02 Dec 2023 07:22:55 GMT  
		Size: 11.2 MB (11208173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:a5958dec8092fba71f01cab8a88c7839b2d75e59f37fe80b8df036492a0039e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.5 MB (435482642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fe0712e324aeeaf8f188dc4ef34eb1543b730d904dc083e3e31c95680c4ca0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 01 Dec 2023 08:11:20 GMT
ARG RELEASE
# Fri, 01 Dec 2023 08:11:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 08:11:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 08:11:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 08:11:22 GMT
ADD file:1e0a0e74040ce284db152e44fa004b927dfe7ed6482ff2b6541b73de409f38e8 in / 
# Fri, 01 Dec 2023 08:11:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:26:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 05:27:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:27:13 GMT
ENV JAVA_VERSION=jdk8u392-b08_openj9-0.41.0
# Sat, 02 Dec 2023 05:29:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='17df56bf2567bcca36d78ac4e46d025aec2553ba4df0b18c89464fcfebf9bb21';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_aarch64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='3991f050a560a6ef21c1f3e08ce84302c4d41b923502667c23dac21e82706a0c';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_ppc64le_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2e771721212f403dd97a132ddcd20b4ed2d0ee95d504c299517a8ce58590690e';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_x64_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        s390x)          ESUM='5108b16f79176b501d9b5e5950bb143ffcf839da6472940bb62279db529e2630';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u392-b08_openj9-0.41.0/ibm-semeru-open-jre_s390x_linux_8u392b08_openj9-0.41.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 02 Dec 2023 05:29:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 05:29:05 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 02 Dec 2023 05:29:38 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 02 Dec 2023 06:43:22 GMT
USER root
# Sat, 02 Dec 2023 06:43:22 GMT
ARG LIBERTY_VERSION=23.0.0.12-beta
# Sat, 02 Dec 2023 06:43:22 GMT
ARG LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8
# Sat, 02 Dec 2023 06:43:22 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip
# Sat, 02 Dec 2023 06:43:22 GMT
ARG LIBERTY_BUILD_LABEL=cl231120231030-1102
# Sat, 02 Dec 2023 06:43:22 GMT
ARG OPENJ9_SCC=true
# Sat, 02 Dec 2023 06:43:23 GMT
ARG VERBOSE=false
# Sat, 02 Dec 2023 06:43:23 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl231120231030-1102 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=23.0.0.12-beta
# Sat, 02 Dec 2023 06:43:23 GMT
COPY file:b2d50545eedb1d5c43e3914a49059b907fd99eab5d731eb6d4ff519f47d88408 in /opt/ol/NOTICES 
# Sat, 02 Dec 2023 06:43:23 GMT
COPY dir:3a03be0df9fe59a90276be087434855a86a8818483ded6f49c3c57610fb6842d in /opt/ol/helpers 
# Sat, 02 Dec 2023 06:43:23 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ol/fixes/ 
# Sat, 02 Dec 2023 06:43:24 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init;
# Sat, 02 Dec 2023 06:43:49 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp
# Sat, 02 Dec 2023 06:44:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Sat, 02 Dec 2023 06:44:03 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env
# Sat, 02 Dec 2023 06:44:04 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R g+rw /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml
# Sat, 02 Dec 2023 06:44:31 GMT
# ARGS: LIBERTY_BUILD_LABEL=cl231120231030-1102 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/23.0.0.12-beta/openliberty-runtime-23.0.0.12-beta.zip LIBERTY_SHA=126f29786fcf8d59a2935586ac350becba8067b8 LIBERTY_VERSION=23.0.0.12-beta VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output
# Sat, 02 Dec 2023 06:44:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 02 Dec 2023 06:44:32 GMT
USER 1001
# Sat, 02 Dec 2023 06:44:32 GMT
EXPOSE 9080 9443
# Sat, 02 Dec 2023 06:44:32 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Sat, 02 Dec 2023 06:44:32 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6290fbaa1ba32f944c0ff7cb430d6e8728560a12504f7669623e2561c9dda197`  
		Last Modified: Sat, 02 Dec 2023 05:24:33 GMT  
		Size: 28.7 MB (28654008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6cf3e30681b513e4b63895acd24d7fd36b950b43aefb860b9517b75e3ceedb`  
		Last Modified: Sat, 02 Dec 2023 05:42:40 GMT  
		Size: 12.2 MB (12199386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925d86baf6d49f779fe4beb622aa4b3350dbb8419a8f444cac5000ac2296ec75`  
		Last Modified: Sat, 02 Dec 2023 05:43:11 GMT  
		Size: 50.1 MB (50084246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d5aa95a8f967be0c1ff84e69ab99ac13d2ce02289dac1fff502d3f152d266d`  
		Last Modified: Sat, 02 Dec 2023 05:43:06 GMT  
		Size: 4.4 MB (4360828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65ea08dfbad8cafe92ea2de3f183176eeb356e2e8dff9ac7493d2dcabd4d788`  
		Last Modified: Sat, 02 Dec 2023 07:04:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a342a4c6b38ec03c97a73c89d786087122e2eb2e5aee6201035e840c8559c128`  
		Last Modified: Sat, 02 Dec 2023 07:04:17 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ebe6f2c692b78ccab6e91806cc498516e6947402d0d7e1968a2e3f1900279c`  
		Last Modified: Sat, 02 Dec 2023 07:04:17 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa52ce9060f954d6fb32d433feebe5dc8b8bdbd917b8e1c553d913ff7d76097`  
		Last Modified: Sat, 02 Dec 2023 07:04:16 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13c8ce9780d23f819abe51bd7f12bf978e7a9fc1dc467334d755cbd14d6b7ce`  
		Last Modified: Sat, 02 Dec 2023 07:04:30 GMT  
		Size: 327.4 MB (327442671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c1fe2fcebcae4b0f9089377c783e89b466b81227e6df011955ecd65e373c72`  
		Last Modified: Sat, 02 Dec 2023 07:04:16 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e29b2bb941787e58a830e298bf0ca441bdf2afc55bb00171a2e77b3d43cdb14`  
		Last Modified: Sat, 02 Dec 2023 07:04:16 GMT  
		Size: 11.0 KB (11036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4541f60872128a99b17afe77b44954aded545f8d8919119dfbc177532eeed7`  
		Last Modified: Sat, 02 Dec 2023 07:04:17 GMT  
		Size: 12.7 MB (12685242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
