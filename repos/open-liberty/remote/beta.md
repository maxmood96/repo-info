## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:a65265b75214cdc5003b4da17f263994a4cd7bc43fedeef427585d486527bfbd
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
$ docker pull open-liberty@sha256:ea714436356950afa5f944bc5f91f3e0de07820c6c93800a20fe64bb652affce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.2 MB (484205189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf98d1a2f33e9eb25845072d092d846bf7135640f4362b484b01429ea0d7eb6b`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:09:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 23:09:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:09:14 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Mon, 01 Dec 2025 23:09:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 23:09:17 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:09:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 23:09:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:47:05 GMT
USER root
# Wed, 03 Dec 2025 21:47:05 GMT
ARG LIBERTY_VERSION=26.0.0.1-beta
# Wed, 03 Dec 2025 21:47:05 GMT
ARG LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db
# Wed, 03 Dec 2025 21:47:05 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip
# Wed, 03 Dec 2025 21:47:05 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:47:05 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:05 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:47:05 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.1-beta liberty.version=26.0.0.1-beta io.openliberty.version=26.0.0.1-beta
# Wed, 03 Dec 2025 21:47:05 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 03 Dec 2025 21:47:05 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 03 Dec 2025 21:47:05 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:47:05 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:47:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:47:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:47:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:47:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:47:46 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:47:46 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:47:46 GMT
USER 1001
# Wed, 03 Dec 2025 21:47:46 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:47:46 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:47:46 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98dbe6a449def6acf0185c7dd104a13d9bf9fe553f907aeae6c49c653d60593`  
		Last Modified: Mon, 01 Dec 2025 23:10:09 GMT  
		Size: 12.2 MB (12171780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b35c8a21e781fd9a8ca6dbfd1ef68934ee13f36fb3b7ce9d47dcb00f30cdcb`  
		Last Modified: Mon, 01 Dec 2025 23:10:13 GMT  
		Size: 53.7 MB (53730424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c202eabb5a0a5d81253ae53c87e64d97aa88aed4bc1f02a83c6e41eeb4745a`  
		Last Modified: Mon, 01 Dec 2025 23:10:09 GMT  
		Size: 4.3 MB (4314853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b7f076a5cd4c82347c47840721a47fd9be1668e10622ca1890b49d91c3e2d3`  
		Last Modified: Wed, 03 Dec 2025 21:48:33 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea99ab72d137a5240bb6817db31f09a87d7d3d7f09305ddb143f89d78ae8dea`  
		Last Modified: Wed, 03 Dec 2025 21:48:33 GMT  
		Size: 12.3 KB (12287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6b4944664ed140b6062b28e155ff189283b9be8195e69cbd2378b3d1f9e81`  
		Last Modified: Wed, 03 Dec 2025 21:48:33 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e854a46bed162e4153abf29bafb151ec13a4f4275c7340ca02345331e706a94`  
		Last Modified: Wed, 03 Dec 2025 21:48:33 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b9946745e41268dbdb41939da2133cbe83d12a58ee9acf27a349142b427f5`  
		Last Modified: Fri, 05 Dec 2025 00:49:45 GMT  
		Size: 370.0 MB (370034076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807e7e4c232c04a54c42b962bc3cb93187e55fc045fc0ea798406217b5e5230e`  
		Last Modified: Wed, 03 Dec 2025 21:48:33 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ec74249f6d7a6e4a39eff34880a1a09c2ffd7b9127ccf1110456dc2a2b5097`  
		Last Modified: Wed, 03 Dec 2025 21:48:33 GMT  
		Size: 13.7 KB (13720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2430170673a8829f623b3596d38cc165665ac0dcfcf1daeefa808ac8413cb6`  
		Last Modified: Wed, 03 Dec 2025 21:48:34 GMT  
		Size: 14.4 MB (14357154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:4332bcfd7b31d48e5dd73f4349391ebff2c4b2d88b6e78aea377d03db5628925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5861872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6fd17f4bf8219d994fd56d5d3913cd479260bc0ef92d51286540b730a76021`

```dockerfile
```

-	Layers:
	-	`sha256:cd8ad0dcda23009265fc825073b2a3f4b69073c68e8e108b920eb8fd0aee4f5a`  
		Last Modified: Thu, 04 Dec 2025 00:47:23 GMT  
		Size: 5.8 MB (5822432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0071c8d8664f842fba407812671ad447cbf60b38d4946b8d94d818aa582f816`  
		Last Modified: Thu, 04 Dec 2025 00:47:24 GMT  
		Size: 39.4 KB (39440 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:7654a9a5e5384674e743e9c42fab8e3a1d0b9bfd0a74565bcac6d74c24612e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.2 MB (481236480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fdccc462a5711120abf204a041f4e065ec069fcdb6dd0a912c02bff176c954`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:54:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:54:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:54:49 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Mon, 01 Dec 2025 21:54:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:54:52 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:55:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Wed, 03 Dec 2025 21:46:12 GMT
USER root
# Wed, 03 Dec 2025 21:46:12 GMT
ARG LIBERTY_VERSION=26.0.0.1-beta
# Wed, 03 Dec 2025 21:46:12 GMT
ARG LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db
# Wed, 03 Dec 2025 21:46:12 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip
# Wed, 03 Dec 2025 21:46:12 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Wed, 03 Dec 2025 21:46:12 GMT
ARG OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:46:12 GMT
ARG VERBOSE=false
# Wed, 03 Dec 2025 21:46:12 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.1-beta liberty.version=26.0.0.1-beta io.openliberty.version=26.0.0.1-beta
# Wed, 03 Dec 2025 21:46:12 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 03 Dec 2025 21:46:12 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 03 Dec 2025 21:46:12 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:46:12 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:46:34 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:46:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:46:34 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:46:35 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:46:59 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:46:59 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:46:59 GMT
USER 1001
# Wed, 03 Dec 2025 21:46:59 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:46:59 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:46:59 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5c682422801bb14f8d688a7a6305da36e5e73d85b5178dcc1a35d8071f6bed`  
		Last Modified: Mon, 01 Dec 2025 21:55:44 GMT  
		Size: 12.1 MB (12130037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f85275d523f98b42ee443d57dfc90f3e4e4e7b51af93f6c02fd8786ab05ca`  
		Last Modified: Mon, 01 Dec 2025 21:55:53 GMT  
		Size: 53.4 MB (53440936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22511a6517e63a3495bbe6b13b9c57bfd33ea690bd2c40143b776dadcb807a20`  
		Last Modified: Mon, 01 Dec 2025 21:55:43 GMT  
		Size: 4.1 MB (4126610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f00eec0b454c2ebff7c40d63b998a6db1c0880c2c48771088798dce8c14c4c`  
		Last Modified: Wed, 03 Dec 2025 21:47:42 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618a46d84414d32e168975291e2d79ac83e56195cacf17c7bfa5088fa9202ad8`  
		Last Modified: Wed, 03 Dec 2025 21:47:42 GMT  
		Size: 12.3 KB (12287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a2d588722b68c7d9b383cebe3f4e8c406ccdc89600561e771f755f953216b1`  
		Last Modified: Wed, 03 Dec 2025 21:47:42 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3f199dc13a75e7fbfed402ba8ad433ce48a375634d867f3105230cad0274c7`  
		Last Modified: Wed, 03 Dec 2025 21:47:42 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35f04b30395ac9ba13db6dd72f208c9ef8ec34949cb16a25411671de5585c27`  
		Last Modified: Fri, 05 Dec 2025 00:49:47 GMT  
		Size: 370.0 MB (370034261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a97d9dd2df9e63d22a7c28bc01f981bc48299ada498fd3befda912a3038858`  
		Last Modified: Wed, 03 Dec 2025 21:47:42 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301197ee19aa71bf20945d2d37484ea8050fbed094f00458d3630bd8e46797c3`  
		Last Modified: Wed, 03 Dec 2025 21:47:42 GMT  
		Size: 13.7 KB (13745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40082dc586f0123ac33760ae8cd63f80c08d856021cb79ac6366bbd4f2f0741`  
		Last Modified: Wed, 03 Dec 2025 21:47:44 GMT  
		Size: 14.1 MB (14050054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:af76b08bffc74f4141d0c6a50f5af1c8a6a3514f9f932053b6252b5c3050a89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5861797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4cf2a1e2145a8743a94e64a8bf8f565a648b1e466ec21557d609dc1939926`

```dockerfile
```

-	Layers:
	-	`sha256:656d3de4af4e8d1573dde80cfa02ebb8768cf48a258a66a7fd8ac210cf058b2b`  
		Last Modified: Thu, 04 Dec 2025 00:47:29 GMT  
		Size: 5.8 MB (5822228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:785c7cedf45cf093dbf4c8e2e817a7e83f31baa4c51bd792ed3c2e4c0ccb86e5`  
		Last Modified: Thu, 04 Dec 2025 00:47:30 GMT  
		Size: 39.6 KB (39569 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:32f59592ed5994618d19720a285cbbe8e3c41da1582ffb40f2f0ebd88db8c85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.1 MB (489078800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e789136a98ca49d4f4d4829bdcfaad7efa30c01ecc73fac013a12e8f02685`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:33 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Mon, 01 Dec 2025 21:55:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:55:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:55:25 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:55:59 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 01 Dec 2025 22:15:13 GMT
USER root
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_VERSION=26.0.0.1-beta
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Mon, 01 Dec 2025 22:15:13 GMT
ARG OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:15:13 GMT
ARG VERBOSE=false
# Mon, 01 Dec 2025 22:15:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.1-beta liberty.version=26.0.0.1-beta io.openliberty.version=26.0.0.1-beta
# Mon, 01 Dec 2025 22:15:13 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Mon, 01 Dec 2025 22:15:14 GMT
COPY helpers /opt/ol/helpers # buildkit
# Mon, 01 Dec 2025 22:15:14 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 03 Dec 2025 21:45:04 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 03 Dec 2025 21:45:43 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 03 Dec 2025 21:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 03 Dec 2025 21:45:45 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 03 Dec 2025 21:45:47 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 03 Dec 2025 21:46:25 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 03 Dec 2025 21:46:25 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 03 Dec 2025 21:46:25 GMT
USER 1001
# Wed, 03 Dec 2025 21:46:25 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 03 Dec 2025 21:46:25 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 03 Dec 2025 21:46:25 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Tue, 13 Jan 2026 01:30:07 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed02c429613f0e247ffa449100a48c06fced187c5ce8d553e21c41a27e3ae784`  
		Last Modified: Mon, 01 Dec 2025 21:55:07 GMT  
		Size: 12.9 MB (12893867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a25c6a5213916040c318446523626d7ebcc1fdb6e5dfabb58c732f98ab93c1`  
		Last Modified: Mon, 01 Dec 2025 21:56:43 GMT  
		Size: 55.3 MB (55309347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385a6f4ec42048f4217220ab962943ab50c7cb278f46da5909f962c54d4d049a`  
		Last Modified: Mon, 01 Dec 2025 21:56:37 GMT  
		Size: 3.5 MB (3503887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1393d327d3844f1692f0ee241eff1d93506a83d6acdbf1cf58cbbd8c187cebaa`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94e88fdd2575995ef515f54f358579e2cdf8cfd1a79d26eb5e0bd635beb4dbc`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 12.3 KB (12282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a7f7b23a19f2f4573272f72922a1c047ca446a1d1fd3f7013ba540ebc4d88c`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8131179c52d40398f341251abf2917d16280cade6af3ab6b633d641d96178b9`  
		Last Modified: Wed, 03 Dec 2025 21:48:14 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3384c7fa756faae2da99bcc76c584551fd7e7fa4184692ec4db8bbf12713179e`  
		Last Modified: Fri, 05 Dec 2025 00:46:28 GMT  
		Size: 370.0 MB (370034703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d04abe0cc7ae66389ef892ddcf34b6e5087992651b2935234155cc3a6b3da1`  
		Last Modified: Wed, 03 Dec 2025 21:48:14 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c67ed79c36b28a8c3c68701fa8b2fbb3e1ea00e561cfc2d956a4c5829063e1`  
		Last Modified: Wed, 03 Dec 2025 21:48:14 GMT  
		Size: 13.8 KB (13763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a8d6412f1c00492fa2194cb077288d8a61f0c87f475b8b67964fde136a60d3`  
		Last Modified: Wed, 03 Dec 2025 21:48:17 GMT  
		Size: 12.8 MB (12825374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:69c71bb0ed11d8724b7e3361ee5ba7b7eaf14ac9ceed956de9b6016470208c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5866698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bf1fb29c6617c99229aa5c989b84bb6688e812cd05bc7b614fc52500f51677`

```dockerfile
```

-	Layers:
	-	`sha256:c8eff2fa43cfcc5ea13043eb0268cdfa6a1095065b689eef347b7fc5d0671915`  
		Last Modified: Thu, 04 Dec 2025 00:47:35 GMT  
		Size: 5.8 MB (5827223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb5e42aaae072f4fc3a4675681aefce744437a75fe10fa04fa063a1bfdedffe`  
		Last Modified: Thu, 04 Dec 2025 00:47:36 GMT  
		Size: 39.5 KB (39475 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:839bc97da63f1e4c58c9484b1257899df255c5d42c67dd07f3a17031f543c767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.6 MB (482570553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219cba32dde9ade9df0e740bf8c4249fb91e08ef42c0884dcecc914023d029d5`
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
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Thu, 15 Jan 2026 22:12:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 15 Jan 2026 22:12:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:12:01 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 15 Jan 2026 22:12:32 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 15 Jan 2026 22:53:36 GMT
USER root
# Thu, 15 Jan 2026 22:53:36 GMT
ARG LIBERTY_VERSION=26.0.0.1-beta
# Thu, 15 Jan 2026 22:53:36 GMT
ARG LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db
# Thu, 15 Jan 2026 22:53:36 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip
# Thu, 15 Jan 2026 22:53:36 GMT
ARG LIBERTY_BUILD_LABEL=cl251220251117-0302
# Thu, 15 Jan 2026 22:53:36 GMT
ARG OPENJ9_SCC=true
# Thu, 15 Jan 2026 22:53:36 GMT
ARG VERBOSE=false
# Thu, 15 Jan 2026 22:53:36 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251220251117-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=26.0.0.1-beta liberty.version=26.0.0.1-beta io.openliberty.version=26.0.0.1-beta
# Thu, 15 Jan 2026 22:53:36 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 15 Jan 2026 22:53:36 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 15 Jan 2026 22:53:36 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 15 Jan 2026 22:53:36 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 15 Jan 2026 22:53:49 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 15 Jan 2026 22:53:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 15 Jan 2026 22:53:49 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 15 Jan 2026 22:53:50 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Thu, 15 Jan 2026 22:54:14 GMT
# ARGS: LIBERTY_VERSION=26.0.0.1-beta LIBERTY_SHA=e2b9025050408f467eb8378eda3f9530c00913db LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/26.0.0.1-beta/openliberty-runtime-26.0.0.1-beta.zip LIBERTY_BUILD_LABEL=cl251220251117-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 15 Jan 2026 22:54:14 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 15 Jan 2026 22:54:14 GMT
USER 1001
# Thu, 15 Jan 2026 22:54:14 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 15 Jan 2026 22:54:14 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 15 Jan 2026 22:54:14 GMT
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
	-	`sha256:0c8bf3a4fc2d61dc3c4745019e51665d0f9029e7459a2c4261eb3bc08b5e8b5e`  
		Last Modified: Thu, 15 Jan 2026 22:13:04 GMT  
		Size: 53.3 MB (53319766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8f6f4138aa794e673234435372ef0886abee9c0e749446ca76b57e1afcada4`  
		Last Modified: Thu, 15 Jan 2026 22:12:59 GMT  
		Size: 4.4 MB (4418349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a088c3d8721ad81c18f9f955fb47ed77c86cd113b13423bf1e6d04da6a9c03c`  
		Last Modified: Thu, 15 Jan 2026 22:54:33 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e6a9de08d2f6f67e5cd301d6fc9e879e930e141b3c3c89ea7190dd0fef523c`  
		Last Modified: Thu, 15 Jan 2026 22:55:02 GMT  
		Size: 12.3 KB (12284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4a75e75561b532c4e60a955c4945a1838dbd2e054d87ac0debeffa52f16ae2`  
		Last Modified: Thu, 15 Jan 2026 22:55:02 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8fabfba4caf6e3ce92a4830efedbfa3397723adce45b6d31a2369c8ccea9e0`  
		Last Modified: Thu, 15 Jan 2026 22:55:02 GMT  
		Size: 33.1 KB (33109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aede2895b0b2aa6041d42a889bc64150b614b666fdc71404d8efb9abfd5c34`  
		Last Modified: Thu, 15 Jan 2026 22:55:17 GMT  
		Size: 370.0 MB (370033605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4e4ca6ce587f5c2880f7befc5020547624aec2f57913282c582f88ae1c3295`  
		Last Modified: Thu, 15 Jan 2026 22:55:02 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c698ac2bab51eab964ad7ce8333a092a0a44d57fd7c5fe9c26d0beb3a78225`  
		Last Modified: Thu, 15 Jan 2026 22:55:02 GMT  
		Size: 13.7 KB (13739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c900f4d1dcec285e0d4b72392e57f3475192948444df97bdec0de74da11424`  
		Last Modified: Thu, 15 Jan 2026 22:55:04 GMT  
		Size: 14.5 MB (14514069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:49844d5eff3b060e45d20a8c260134830047b97c7916901e1ec36906e4f68e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b95dcd40ee27e27716dc9ffba3e52fb9b568ca14590873cf50a19ef5f6d70e`

```dockerfile
```

-	Layers:
	-	`sha256:291f5a5c0b3d46f226155b1d1ab8b8607c4c741b0131f16ac5e3aa6df92ec9e7`  
		Last Modified: Fri, 16 Jan 2026 00:49:12 GMT  
		Size: 5.8 MB (5823461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80021c5a8b7d2da563b0bbcd1846709b300d8bfd57e9f65b0dd2518b8cffeb41`  
		Last Modified: Fri, 16 Jan 2026 00:49:13 GMT  
		Size: 39.4 KB (39441 bytes)  
		MIME: application/vnd.in-toto+json
