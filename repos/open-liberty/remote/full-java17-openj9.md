## `open-liberty:full-java17-openj9`

```console
$ docker pull open-liberty@sha256:1d4b1af3cba4a737f551b07e512ec84f669aeedc5d1157c04de26e278e5df32b
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

### `open-liberty:full-java17-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:ba4e339cc15ca52c905f799ed991468d0481a032f482eee5f77ae53075316a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.1 MB (462109243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1838d851b171f6f9f352b2e8e8a26058fd73f6e1c245539d20c54b425b02f9f6`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:27:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:27:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:27:14 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 15 Jan 2026 22:27:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:27:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:27:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:27:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 16 Jan 2026 00:45:38 GMT
USER root
# Fri, 16 Jan 2026 00:45:38 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Fri, 16 Jan 2026 00:45:38 GMT
ARG LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3
# Fri, 16 Jan 2026 00:45:38 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip
# Fri, 16 Jan 2026 00:45:38 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Fri, 16 Jan 2026 00:45:38 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jan 2026 00:45:38 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 00:45:38 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Fri, 16 Jan 2026 00:45:38 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 16 Jan 2026 00:45:38 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 16 Jan 2026 00:45:38 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 16 Jan 2026 00:45:39 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 16 Jan 2026 00:45:57 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 16 Jan 2026 00:45:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 16 Jan 2026 00:45:57 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 16 Jan 2026 00:45:58 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 16 Jan 2026 00:46:18 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 16 Jan 2026 00:46:18 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Jan 2026 00:46:18 GMT
USER 1001
# Fri, 16 Jan 2026 00:46:18 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 16 Jan 2026 00:46:18 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 16 Jan 2026 00:46:18 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad96c1dea85f86acf9252b1bd3e4d4b5cd893cdb4f8ba18a6df444afd4ea1d9`  
		Last Modified: Thu, 15 Jan 2026 22:28:11 GMT  
		Size: 12.2 MB (12171783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcd7976482bebafb7cfd5d5794d319ed4d11a0cf175c3ff9cbe93e6b22a5585`  
		Last Modified: Thu, 15 Jan 2026 22:28:18 GMT  
		Size: 55.2 MB (55190779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8312ca06cf4dcf35a6056fe5f48377910aa5fe09695bbb706b8bb409a533b2b`  
		Last Modified: Thu, 15 Jan 2026 22:28:10 GMT  
		Size: 5.1 MB (5084580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6650a5e45e529318277ca14210dc2af608c1143ffe53e6c6b12a40df5c8504`  
		Last Modified: Fri, 16 Jan 2026 00:46:58 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f813d99360a5da534f7a67cd132131ace229ec2c5315cf4a1f9459aaf56141`  
		Last Modified: Fri, 16 Jan 2026 00:46:41 GMT  
		Size: 12.3 KB (12284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e38e41b15239815359fcadca945c786ac6cb94e7f50464b718b16581592e63`  
		Last Modified: Fri, 16 Jan 2026 00:46:58 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebc65cc22bf0a4ae7414654c350b6cb16ba79ca11cc08301944ecdb7ffbcb3f`  
		Last Modified: Fri, 16 Jan 2026 00:46:41 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9370db29ef242328d55783f1dee2fd67d3742e6c2245a1a1c9e13bedbd8a7bb`  
		Last Modified: Fri, 16 Jan 2026 00:46:51 GMT  
		Size: 345.9 MB (345927965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b85370383ab283d7119b14a49906060030939a77c74c29481e3b5dda3f4f67`  
		Last Modified: Fri, 16 Jan 2026 00:46:43 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869b1717a953346d190ed1290862d98db49e85e3f10a8be12f2a7119d8593191`  
		Last Modified: Fri, 16 Jan 2026 00:46:59 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd663afa7098c1f173644a6c4f3613fae58ffcb60621fa805b8cda397bbc77d`  
		Last Modified: Fri, 16 Jan 2026 00:47:11 GMT  
		Size: 14.1 MB (14137355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:880b8655f2eb5bf94be246664f8b2c40587f4f27eb13b24106c5cf7d9e2bbfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5743070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06153b01aec93f63e964b1cc6e168c27a232e594a330ca6302bf2003660cc4e0`

```dockerfile
```

-	Layers:
	-	`sha256:e925d66b2ea4d944ee173e1473caf383861c27c3dc5f3cb00559ecc850dc17b2`  
		Last Modified: Fri, 16 Jan 2026 03:50:55 GMT  
		Size: 5.7 MB (5703701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45cfd51a87ea7b0bfa2c4c13f146ce659b936a3f089969f4a14ff9473597cdd`  
		Last Modified: Fri, 16 Jan 2026 03:50:55 GMT  
		Size: 39.4 KB (39369 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:5f6c47f68fae61de972e17df1e59fedb99507b06bc4e939246f4927f6c8ea744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.3 MB (457273709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a75771343a47b0f1772bc47035ab1fc068a660c22aa699d540873931b500f6`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:29:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:29:16 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 15 Jan 2026 22:29:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:29:19 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:29:19 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:29:51 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 16 Jan 2026 00:49:11 GMT
USER root
# Fri, 16 Jan 2026 00:49:11 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Fri, 16 Jan 2026 00:49:11 GMT
ARG LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3
# Fri, 16 Jan 2026 00:49:11 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip
# Fri, 16 Jan 2026 00:49:11 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Fri, 16 Jan 2026 00:49:11 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jan 2026 00:49:11 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 00:49:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Fri, 16 Jan 2026 00:49:11 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 16 Jan 2026 00:49:11 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 16 Jan 2026 00:49:11 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 16 Jan 2026 00:49:12 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 16 Jan 2026 00:49:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 16 Jan 2026 00:49:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 16 Jan 2026 00:49:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 16 Jan 2026 00:49:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 16 Jan 2026 00:49:54 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 16 Jan 2026 00:49:54 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Jan 2026 00:49:54 GMT
USER 1001
# Fri, 16 Jan 2026 00:49:54 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 16 Jan 2026 00:49:54 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 16 Jan 2026 00:49:54 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ef9d3bfe660d622551b3c586de2f866b43b44f3ce75ef0c23b26339e6eb1eb`  
		Last Modified: Thu, 15 Jan 2026 22:30:03 GMT  
		Size: 12.1 MB (12132639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6b9251c4a9c14abe5526cdb8678e960f10ad19867712e0ad77ad7dcd436057`  
		Last Modified: Thu, 15 Jan 2026 22:30:29 GMT  
		Size: 53.5 MB (53468141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1786dbee4e241beca5a62c5c6e782ca848a0ba2d26f81700a2298991ec5385`  
		Last Modified: Thu, 15 Jan 2026 22:30:03 GMT  
		Size: 4.8 MB (4826598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2ca0d3258088095afc2be49810b3cc8e8b930012f3b51755f2744e0cf8e474`  
		Last Modified: Fri, 16 Jan 2026 00:50:19 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da061768f8b43969a75b92b2aa82f12d707a0236d3ececf6a3ef085f1a9b2293`  
		Last Modified: Fri, 16 Jan 2026 00:50:32 GMT  
		Size: 12.3 KB (12289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f7428a5069625993ada9c1a92635e6693e2c9cfab367566a0ea5f3a05b9e8e`  
		Last Modified: Fri, 16 Jan 2026 00:50:32 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137b966744be4bfda0ad4f255c79f6bdd76e12a1edf75c8139402c0f609f97c4`  
		Last Modified: Fri, 16 Jan 2026 00:50:19 GMT  
		Size: 42.3 KB (42321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03632b6606410556ac76c589df3e3b55f308cb0bbffabdfe4f058268e20a43fd`  
		Last Modified: Fri, 16 Jan 2026 00:50:55 GMT  
		Size: 345.9 MB (345928075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95bc586f369d1192040c6140fa24211da22d39a90fbf66e52b3abbaff37462f`  
		Last Modified: Fri, 16 Jan 2026 00:50:32 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c1d560687dcf1e79eb82a46241bf172f2b072a615f5e21dff1c15673f7f35`  
		Last Modified: Fri, 16 Jan 2026 00:50:32 GMT  
		Size: 13.7 KB (13721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c3319c4875fba5b56be98fc2d15af08fc1284ade76615ca7783a05983d9fc3`  
		Last Modified: Fri, 16 Jan 2026 00:50:21 GMT  
		Size: 13.5 MB (13464080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:b412f43f66c68777262de983a03a880b2c9c30fc803f9325a784f40103573ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52833d7d3e8cb4b054773d61282734be428e72a2dcd32957b1e5528b90da9c3`

```dockerfile
```

-	Layers:
	-	`sha256:3ed4c2f5d22c1c10da6dafc1ba27ba01fb827362b5dcce554f0e2c4b41b41802`  
		Last Modified: Fri, 16 Jan 2026 03:51:02 GMT  
		Size: 5.7 MB (5702061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39dfdfa747388fd2e81de74a7b2c92ea26beb6f59545228c98e0c0521f9010f7`  
		Last Modified: Fri, 16 Jan 2026 00:50:19 GMT  
		Size: 39.5 KB (39497 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:aad830771f94bf65df575392aa3392987204db38aee42aedfadfd4e0b5b661a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.3 MB (466310247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed04f4dc33e28f0b095d55b6726d4582af545985c900c8909f4637971cd5876`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:26:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:26:55 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:26:55 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 15 Jan 2026 22:37:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:37:32 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:37:32 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:38:07 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 16 Jan 2026 01:24:45 GMT
USER root
# Fri, 16 Jan 2026 01:24:45 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Fri, 16 Jan 2026 01:24:45 GMT
ARG LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3
# Fri, 16 Jan 2026 01:24:45 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip
# Fri, 16 Jan 2026 01:24:45 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Fri, 16 Jan 2026 01:24:45 GMT
ARG OPENJ9_SCC=true
# Fri, 16 Jan 2026 01:24:45 GMT
ARG VERBOSE=false
# Fri, 16 Jan 2026 01:24:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Fri, 16 Jan 2026 01:24:45 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 16 Jan 2026 01:24:45 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 16 Jan 2026 01:24:46 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 16 Jan 2026 01:33:11 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 16 Jan 2026 01:33:43 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 16 Jan 2026 01:33:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 16 Jan 2026 01:33:45 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 16 Jan 2026 01:33:46 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 16 Jan 2026 01:34:26 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 16 Jan 2026 01:34:26 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 16 Jan 2026 01:34:26 GMT
USER 1001
# Fri, 16 Jan 2026 01:34:26 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 16 Jan 2026 01:34:26 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 16 Jan 2026 01:34:26 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd5d12a160f6d8dea2246e7b85a8df4b10ff68fb7e41da962d3021f6326151b`  
		Last Modified: Thu, 15 Jan 2026 22:28:33 GMT  
		Size: 12.9 MB (12893562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b3fcc0cb045357a148effdc87bd7c18ed2d44c685f9b4f77dd618a6fdef968`  
		Last Modified: Thu, 15 Jan 2026 22:39:07 GMT  
		Size: 57.0 MB (57019141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e391e4bb4d5182a64a63e4a0db567601465acda7995b4fafe8335622e6e3a00`  
		Last Modified: Thu, 15 Jan 2026 22:38:46 GMT  
		Size: 3.9 MB (3859939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421eeefb4d0b332384a531e93c43087953e45012a3ed5847971a9d966285023a`  
		Last Modified: Fri, 16 Jan 2026 01:26:57 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd1a04ac74eb0df0be0a77e86c52ab5de7ba295b69de0414449a2a9a26b67fc`  
		Last Modified: Fri, 16 Jan 2026 01:27:14 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a517d8b9db394cccb3d460828d5a5182e6b3761811af15bda5ac5e0443ce9d2c`  
		Last Modified: Fri, 16 Jan 2026 01:27:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d5ef81a7e5bab2e659968b29f89752f593475ce38daece755b7274e243f346`  
		Last Modified: Fri, 16 Jan 2026 01:35:52 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefbf04b1248c66ec8aa2f6af2211df8dc692aac2bbb43652980b677bcfbdb57`  
		Last Modified: Fri, 16 Jan 2026 01:35:45 GMT  
		Size: 345.9 MB (345928306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7857c243e485400994eec9a374d9852ac7d534621a9898fa51cc2742082dee24`  
		Last Modified: Fri, 16 Jan 2026 01:35:22 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f211dc70453674c07aef287387970668402941b81029190e009f98cdc00f55db`  
		Last Modified: Fri, 16 Jan 2026 01:35:53 GMT  
		Size: 13.8 KB (13754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f2a14502ec0fb7b3428908c5e5ea492db1b7f09cc2526eb630211c8736e3a2`  
		Last Modified: Fri, 16 Jan 2026 01:35:26 GMT  
		Size: 12.1 MB (12097447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:b582fd7a96bf416b1796e7b2bb5d50ecf6232949d8eddc3471f0ba73674e35cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5747725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aaa1c8207e1dc2adeddcf16de1f958d3fa199a39fb95ce226ec3d88bd75be1`

```dockerfile
```

-	Layers:
	-	`sha256:8bd53f2d6fe7e38a06f226a9ace59606b1d5834ae105ec7f84f102636a3e4913`  
		Last Modified: Fri, 16 Jan 2026 03:51:13 GMT  
		Size: 5.7 MB (5708322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36f2bacc4b0083de06b5763ee75884b8cde3e24e68548f3be5a15cbfcebaba5`  
		Last Modified: Fri, 16 Jan 2026 03:51:14 GMT  
		Size: 39.4 KB (39403 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:08d9304451674aebd19da8eabf2e9d338d6a315e2ff259c4ac503d8724596e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459636798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9f060960b0724bcd747ee4e332a47d950d5188a0386ff88b28791562f745dc`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:11:59 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 15 Jan 2026 22:15:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:15:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:15:00 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:15:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 15 Jan 2026 23:49:09 GMT
USER root
# Thu, 15 Jan 2026 23:49:09 GMT
ARG LIBERTY_VERSION=25.0.0.12
# Thu, 15 Jan 2026 23:49:09 GMT
ARG LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3
# Thu, 15 Jan 2026 23:49:09 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip
# Thu, 15 Jan 2026 23:49:09 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Thu, 15 Jan 2026 23:49:09 GMT
ARG OPENJ9_SCC=true
# Thu, 15 Jan 2026 23:49:09 GMT
ARG VERBOSE=false
# Thu, 15 Jan 2026 23:49:09 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.12 liberty.version=25.0.0.12 io.openliberty.version=25.0.0.12
# Thu, 15 Jan 2026 23:49:09 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 15 Jan 2026 23:49:09 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 15 Jan 2026 23:49:09 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 15 Jan 2026 23:49:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 15 Jan 2026 23:49:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 15 Jan 2026 23:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 15 Jan 2026 23:49:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 15 Jan 2026 23:49:23 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 15 Jan 2026 23:49:48 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12 LIBERTY_SHA=a76719b59fe26af24e2ee34b3462028746d878c3 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.12/openliberty-runtime-25.0.0.12.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 15 Jan 2026 23:49:48 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 15 Jan 2026 23:49:48 GMT
USER 1001
# Thu, 15 Jan 2026 23:49:48 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 15 Jan 2026 23:49:48 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 15 Jan 2026 23:49:48 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Thu, 15 Jan 2026 21:43:58 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1421ff1e62d1ac76e2d8a34fa67faf578cf114b64b34c9d5c7c3a05835f2924`  
		Last Modified: Thu, 15 Jan 2026 22:13:00 GMT  
		Size: 12.2 MB (12220151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef92bf2e1b5d43e6698078060d355356215e7242584485701fd3d0a6ac2dfce`  
		Last Modified: Thu, 15 Jan 2026 22:16:04 GMT  
		Size: 54.2 MB (54201865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d0c0eb1496269256c130258e30b475a6ea4f784ccf3d0d77d73239046eff9`  
		Last Modified: Thu, 15 Jan 2026 22:15:51 GMT  
		Size: 5.2 MB (5230921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709b3ff304e1091cec3f8543cd8432885927d8f59833b4e63be79b377fb07f61`  
		Last Modified: Thu, 15 Jan 2026 23:50:39 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad6b1ae9f23880741295cbd59fb2e5963e84edec15bffc325324bba17c8aa89`  
		Last Modified: Thu, 15 Jan 2026 23:50:35 GMT  
		Size: 12.3 KB (12284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb2f79f018de466efbf5421ed3a96be9c101cf5b48cbc4a432369b3700480be`  
		Last Modified: Thu, 15 Jan 2026 23:50:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7825e38d2be0bee9d2af7bf9aecb9f3aead6fa4c81fd7a22ae10aea5949194`  
		Last Modified: Thu, 15 Jan 2026 23:50:24 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca35c66cb417a258469b0df81ee7ba712140fc2d1314ac10118315a7c1c35f1`  
		Last Modified: Thu, 15 Jan 2026 23:51:02 GMT  
		Size: 345.9 MB (345927594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e970311110bfba34068c03dd7262501857adeccb830fa50e5ab0e1b0a9dbd440`  
		Last Modified: Thu, 15 Jan 2026 23:50:36 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cba0bc894d34675872e10057fac9ea9da7c20fb8cf6146e6644ed47174f20d`  
		Last Modified: Thu, 15 Jan 2026 23:50:35 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78119f08c0cdbffd3691d785ae69927a67aaab62532ded2902f09611e6b4dbc`  
		Last Modified: Thu, 15 Jan 2026 23:50:37 GMT  
		Size: 14.0 MB (13991665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:c87f7e94ff25c0d6a4bcf82b4f5124f7068084b5acd679004d3c0a8b85bd5a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5744087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991b2790403f4b84752c0e7337a45177f8d0ddb35418b3cc99921e4319c8d1c7`

```dockerfile
```

-	Layers:
	-	`sha256:99d636de24d9ea9a3ffc4f3176df4a7407931141034852c8c237865ec2a7d517`  
		Last Modified: Thu, 15 Jan 2026 23:50:24 GMT  
		Size: 5.7 MB (5704718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a120036431e837adb3bd0901b0672d534a6aba48361b083c79ac6f54da1932ad`  
		Last Modified: Fri, 16 Jan 2026 00:49:43 GMT  
		Size: 39.4 KB (39369 bytes)  
		MIME: application/vnd.in-toto+json
