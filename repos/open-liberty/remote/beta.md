## `open-liberty:beta`

```console
$ docker pull open-liberty@sha256:f1cf6a1459ede2acdcf7d04a90282d7510f7dc316bcb25c1fedc57a203353fec
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
$ docker pull open-liberty@sha256:6e0599f938fbf604bc0bf94de24d49b128ccc970e50108bca7f640d5566fa91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.2 MB (482229985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb15d3db505d82f3e94b9dcb5b6bf1dd798f2a6c1d447b207ba2d5788081bff`
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
# Mon, 01 Dec 2025 23:45:20 GMT
USER root
# Mon, 01 Dec 2025 23:45:20 GMT
ARG LIBERTY_VERSION=25.0.0.12-beta
# Mon, 01 Dec 2025 23:45:20 GMT
ARG LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5
# Mon, 01 Dec 2025 23:45:20 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip
# Mon, 01 Dec 2025 23:45:20 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Mon, 01 Dec 2025 23:45:20 GMT
ARG OPENJ9_SCC=true
# Mon, 01 Dec 2025 23:45:20 GMT
ARG VERBOSE=false
# Mon, 01 Dec 2025 23:45:20 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.12-beta liberty.version=25.0.0.12-beta io.openliberty.version=25.0.0.12-beta
# Mon, 01 Dec 2025 23:45:20 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Mon, 01 Dec 2025 23:45:20 GMT
COPY helpers /opt/ol/helpers # buildkit
# Mon, 01 Dec 2025 23:45:20 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Mon, 01 Dec 2025 23:45:20 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Mon, 01 Dec 2025 23:45:38 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Mon, 01 Dec 2025 23:45:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 01 Dec 2025 23:45:38 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Mon, 01 Dec 2025 23:45:38 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Mon, 01 Dec 2025 23:46:01 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Mon, 01 Dec 2025 23:46:01 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 01 Dec 2025 23:46:01 GMT
USER 1001
# Mon, 01 Dec 2025 23:46:01 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Mon, 01 Dec 2025 23:46:01 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 01 Dec 2025 23:46:01 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
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
	-	`sha256:4de87def56c05ffe071b73e0851c24f24f7b637be96af382bd4aa305005cd24e`  
		Last Modified: Mon, 01 Dec 2025 23:46:55 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a626b429de22cf5079c913b6db1c2405c206681864727683632b6cc4952104a7`  
		Last Modified: Mon, 01 Dec 2025 23:46:55 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf140148a3b3d8813aa2ef547f2f3ffdaadf73cb0fde13e96ca23f0645029b44`  
		Last Modified: Mon, 01 Dec 2025 23:46:56 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706dbd39fb3f7dc39fecce3c179d5af7f3ea7b7a1d8aff717a42a37f5a339a0e`  
		Last Modified: Mon, 01 Dec 2025 23:46:56 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d065d409629308d2536eb062ce6e44991ea974a61c2158b805a5844ae76f7857`  
		Last Modified: Tue, 02 Dec 2025 09:00:47 GMT  
		Size: 368.0 MB (367995173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfd528e0bb06c490e90e5bc2ccbe26c76e483c9f1c81d4908ba74b5f41cfb9b`  
		Last Modified: Mon, 01 Dec 2025 23:46:56 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1326a0bede2278fb77bd692423097881e624d4518e970a6aa9592aac82803505`  
		Last Modified: Mon, 01 Dec 2025 23:46:56 GMT  
		Size: 13.7 KB (13721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784a9dbd1754f5203d010dba0780f2374301b9335b8a646751bb815775e96115`  
		Last Modified: Mon, 01 Dec 2025 23:46:57 GMT  
		Size: 14.4 MB (14420858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:6c51d76bd065dfb48d3a9596331924efbbb15d716c57128d8d30c82f6296af9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae9039e89a633ce7802fa6781c1d7da549df6a836bf7e4c01822f752ed21bfa`

```dockerfile
```

-	Layers:
	-	`sha256:81ffb45c8f0e0c20794ac39aa3c4ca3ae3f158c3460d9e33a7c80108e12a5a0d`  
		Last Modified: Tue, 02 Dec 2025 00:53:06 GMT  
		Size: 5.8 MB (5819732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ba6944abce97f92cdeb6767a057376b44a4ee23786986754eb087c58314b5ed`  
		Last Modified: Tue, 02 Dec 2025 00:53:07 GMT  
		Size: 39.5 KB (39460 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:df80dee69094cb10b2901ceaff62b20df4b5ff5ab64f62c3e30c9ccda4816f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.1 MB (479106499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b2b52636a18ede4daa8703b1c31e7972461e582b504bbacd83b2fe7d719423`
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
# Mon, 01 Dec 2025 22:11:45 GMT
USER root
# Mon, 01 Dec 2025 22:11:45 GMT
ARG LIBERTY_VERSION=25.0.0.12-beta
# Mon, 01 Dec 2025 22:11:45 GMT
ARG LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5
# Mon, 01 Dec 2025 22:11:45 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip
# Mon, 01 Dec 2025 22:11:45 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Mon, 01 Dec 2025 22:11:45 GMT
ARG OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:11:45 GMT
ARG VERBOSE=false
# Mon, 01 Dec 2025 22:11:45 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.12-beta liberty.version=25.0.0.12-beta io.openliberty.version=25.0.0.12-beta
# Mon, 01 Dec 2025 22:11:45 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Mon, 01 Dec 2025 22:11:46 GMT
COPY helpers /opt/ol/helpers # buildkit
# Mon, 01 Dec 2025 22:11:46 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Mon, 01 Dec 2025 22:11:46 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Mon, 01 Dec 2025 22:12:05 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Mon, 01 Dec 2025 22:12:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:12:06 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Mon, 01 Dec 2025 22:12:06 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Mon, 01 Dec 2025 22:12:31 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Mon, 01 Dec 2025 22:12:31 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 01 Dec 2025 22:12:31 GMT
USER 1001
# Mon, 01 Dec 2025 22:12:31 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Mon, 01 Dec 2025 22:12:31 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 01 Dec 2025 22:12:31 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
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
	-	`sha256:50bbaf57dadc7f0bf7a7d94aaf1c110dccc4e14ce5d6568346d909326f860b9b`  
		Last Modified: Mon, 01 Dec 2025 22:13:16 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a8add42d3d6552b05171217fa9cd3d1ff74571f78e47b0f5a4ceac152f25a4`  
		Last Modified: Mon, 01 Dec 2025 22:13:16 GMT  
		Size: 12.3 KB (12286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc4a1571c21d781b9ba6f33bf7de649b6ce7b63213ecd2c554be84d9eac18e9`  
		Last Modified: Mon, 01 Dec 2025 22:13:16 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91b12391e8947a9cc08f7d79ca3634d64f60594788414d22463d67a1ca4334`  
		Last Modified: Mon, 01 Dec 2025 22:13:16 GMT  
		Size: 42.3 KB (42324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38382c9431ce1b81595c6422dd0349d7151f4f9b53a52ce330b208a6c75363b`  
		Last Modified: Mon, 01 Dec 2025 22:13:06 GMT  
		Size: 368.0 MB (367995267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffee1f82f3b6af32b90f2819897e1095eacd6e6962f7af7e6fa3aa88d8293c0c`  
		Last Modified: Mon, 01 Dec 2025 22:13:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7839d3a27020db3b03e052ec648c34f2fb3bc592261f51438f816707d42af85b`  
		Last Modified: Mon, 01 Dec 2025 22:13:17 GMT  
		Size: 13.7 KB (13725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1ad1dd0ddf6ae07126dad2b69751398cfdfb94d00737aaa75aea9d651a2909`  
		Last Modified: Mon, 01 Dec 2025 22:13:21 GMT  
		Size: 14.0 MB (13959082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:e552a407ad4836f68aabdda74fad9aacf936c4ad0abfdb59a4b4be87fc49b6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b746db3ee6c0e059e6d9dbf287be15159f84c9111a38111ebbf4feab8f8e001`

```dockerfile
```

-	Layers:
	-	`sha256:a3d78b2146024a986dd78cb69d9ec5b229531ce49a586add0167ab31a6778430`  
		Last Modified: Wed, 03 Dec 2025 00:32:58 GMT  
		Size: 5.8 MB (5819528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efb93e5fe1d2e32cc8b5d6e1d7ae8cb6c5f16318ebd745a884812fe53d0be115`  
		Last Modified: Wed, 03 Dec 2025 00:32:58 GMT  
		Size: 39.6 KB (39587 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:e7f19771158c1be48c48df7e1cf0c8fad8118dd0c80882824ef1764433e1dd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.1 MB (487064106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747bc6a0ba6240e4d5e7fd613c2e184602506ccb9b75cbdf150ee8062aa1c0a9`
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
ARG LIBERTY_VERSION=25.0.0.12-beta
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip
# Mon, 01 Dec 2025 22:15:13 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Mon, 01 Dec 2025 22:15:13 GMT
ARG OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:15:13 GMT
ARG VERBOSE=false
# Mon, 01 Dec 2025 22:15:13 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.12-beta liberty.version=25.0.0.12-beta io.openliberty.version=25.0.0.12-beta
# Mon, 01 Dec 2025 22:15:13 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Mon, 01 Dec 2025 22:15:14 GMT
COPY helpers /opt/ol/helpers # buildkit
# Mon, 01 Dec 2025 22:15:14 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Mon, 01 Dec 2025 22:15:16 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Mon, 01 Dec 2025 22:15:51 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Mon, 01 Dec 2025 22:15:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:15:53 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Mon, 01 Dec 2025 22:15:55 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Mon, 01 Dec 2025 22:16:33 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Mon, 01 Dec 2025 22:16:33 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 01 Dec 2025 22:16:33 GMT
USER 1001
# Mon, 01 Dec 2025 22:16:33 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Mon, 01 Dec 2025 22:16:33 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 01 Dec 2025 22:16:33 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
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
	-	`sha256:e6067f850bd61492c49e891f8d774d2abd66d131ead3f5d3070e1a7c9799a731`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 36.5 KB (36499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e5ed4b8a83510ed86dec505d940d1c0f01e7f0113fc6e0ff760062316bd91f`  
		Last Modified: Mon, 01 Dec 2025 22:17:55 GMT  
		Size: 368.0 MB (367995614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6cdf9fe3dd72d2f51c97bc93f22637e5c50076eba3484a27d8f388a6e96679`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a27fe30a74a0e631914c8a908a54b998d9c23b900348885ce98833e4a22136`  
		Last Modified: Mon, 01 Dec 2025 22:18:00 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeb53edd1431e00bd77b3c96d12a2535b1e27f4b635557b445bfd30df222466`  
		Last Modified: Mon, 01 Dec 2025 22:18:01 GMT  
		Size: 12.8 MB (12849789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:447d75ea1b2d632288dd469bbf6f6902901fe8308c06da9ef401cac72b83f3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5864017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a1418a300432a70ac17ca8e83312f4961fadffd964f84e858a12652f67768`

```dockerfile
```

-	Layers:
	-	`sha256:24eb30a1c16ef4d905ea6e3d5903ba0b491c64b3d4414ca31d9f46169cf4678d`  
		Last Modified: Mon, 01 Dec 2025 22:17:46 GMT  
		Size: 5.8 MB (5824523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a22cf2cc4bdde73236ce1b414f26c83cf3c94a3eadbfe6b7aebdbc0dc8f9f3`  
		Last Modified: Mon, 01 Dec 2025 22:17:45 GMT  
		Size: 39.5 KB (39494 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta` - linux; s390x

```console
$ docker pull open-liberty@sha256:99fa2d0296c1a27dd447b1d91838449b7a10448288baceca986d1355353261d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.7 MB (480675678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8697501cc058a32101e2f962e4cca269d650711d1b92fe65b62b31c7bb32df95`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:42 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:42 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:44 GMT
ADD file:3d940f8d55eafd405ad4e9fa11689b18e385411a264e560df2a7b1b1fd1c45ea in / 
# Mon, 13 Oct 2025 17:23:44 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 21:53:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 01 Dec 2025 21:53:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 21:53:32 GMT
ENV JAVA_VERSION=jdk8u472-b08_openj9-0.56.0
# Mon, 01 Dec 2025 21:53:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='e9f04c51ace0cc724a7b3e54e58ad1823d899c77c2a141ab28efb226c3c7bb97';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='995b091e78fe2e0fb201e3c06272d9bef018594e3205c0a981152bc3f537eda9';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='5babd67d884af6251b504932e2cdce2e5a969075efa856c91087ecc6f3933fc6';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='0225084f7067a8ccf5131b7656ea5ac62d6a68fbab71dc52aac24ab02299ee7a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u472-b08_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_8u472b08_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Mon, 01 Dec 2025 21:53:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 21:53:39 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 01 Dec 2025 21:54:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="fc55589f28bf6659928167461c741649b6005b64285dd81df05bb5ee40f4c6de59b8ee3af84ff756ae1513fc47f5f73070e29313b555e27f096f25881c69841d";     TOMCAT_VERSION="9.0.112";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Mon, 01 Dec 2025 22:11:11 GMT
USER root
# Mon, 01 Dec 2025 22:11:11 GMT
ARG LIBERTY_VERSION=25.0.0.12-beta
# Mon, 01 Dec 2025 22:11:11 GMT
ARG LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5
# Mon, 01 Dec 2025 22:11:11 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip
# Mon, 01 Dec 2025 22:11:11 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Mon, 01 Dec 2025 22:11:11 GMT
ARG OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:11:11 GMT
ARG VERBOSE=false
# Mon, 01 Dec 2025 22:11:11 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 8 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.12-beta liberty.version=25.0.0.12-beta io.openliberty.version=25.0.0.12-beta
# Mon, 01 Dec 2025 22:11:11 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Mon, 01 Dec 2025 22:11:12 GMT
COPY helpers /opt/ol/helpers # buildkit
# Mon, 01 Dec 2025 22:11:12 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Mon, 01 Dec 2025 22:11:13 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Mon, 01 Dec 2025 22:11:36 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Mon, 01 Dec 2025 22:11:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Mon, 01 Dec 2025 22:11:37 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Mon, 01 Dec 2025 22:11:38 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Mon, 01 Dec 2025 22:12:17 GMT
# ARGS: LIBERTY_VERSION=25.0.0.12-beta LIBERTY_SHA=5f19d7897a951a26f1b6784e790a3f72b49fa8b5 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.12-beta/openliberty-runtime-25.0.0.12-beta.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Mon, 01 Dec 2025 22:12:17 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 01 Dec 2025 22:12:17 GMT
USER 1001
# Mon, 01 Dec 2025 22:12:17 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Mon, 01 Dec 2025 22:12:17 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Mon, 01 Dec 2025 22:12:17 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729344b6db60e029cbcc5ef912d5e5debcd7c143dafbbe8c4f8b0b91566586f`  
		Last Modified: Mon, 01 Dec 2025 21:55:05 GMT  
		Size: 12.2 MB (12219897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5326878a3e5db6ab867579dfc254ed6fe76471dfa11d3439a3096a30aad7467b`  
		Last Modified: Mon, 01 Dec 2025 21:55:18 GMT  
		Size: 53.3 MB (53319766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf294f8e97976ab7613d412f2500d56938ba76a0c4dfe47f4b13870b24a51eb`  
		Last Modified: Mon, 01 Dec 2025 21:55:04 GMT  
		Size: 4.3 MB (4332346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d32498223e642987c2555dd2313b54d2ae91313d12dc5615cd829ae40258ee3`  
		Last Modified: Mon, 01 Dec 2025 22:12:32 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7e326f30e18a4e3178f7bb35aa38bd5a0d52e6c29437a0c789ed64cabbc775`  
		Last Modified: Mon, 01 Dec 2025 22:13:21 GMT  
		Size: 12.3 KB (12290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51c3f4f78195d6ab6294e1a1b2b180e4d9cae3b959b792b40decfd4045e405`  
		Last Modified: Mon, 01 Dec 2025 22:13:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a418c490f029bc1bc0a42b50b26ecf5bda5941ff20695593d0394edc35cd82`  
		Last Modified: Mon, 01 Dec 2025 22:12:32 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f667c3f2112186a2273d810a115ed88c3ca5689d0bbea59f343ca453daf34`  
		Last Modified: Mon, 01 Dec 2025 22:13:12 GMT  
		Size: 368.0 MB (367994819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1819ee67ad58185aa19b4ecee69a8b691b4e139f730401a73ba12139438e4b`  
		Last Modified: Mon, 01 Dec 2025 22:13:21 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ccfac95d5437762ee77dce728943066b10ed21664c75e9420b67fe9c54ef2`  
		Last Modified: Mon, 01 Dec 2025 22:13:21 GMT  
		Size: 13.7 KB (13746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4503a34982f4346b8b5bf9942b7e68199fecbcaf400ec8f76817f973239e8c`  
		Last Modified: Mon, 01 Dec 2025 22:13:23 GMT  
		Size: 14.7 MB (14744065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta` - unknown; unknown

```console
$ docker pull open-liberty@sha256:2f3ea3206f09b73b0c6eb8e0503ed122668bbbb0b1ebd37a89a68cd16e3dade8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173c4cb2f5d861d239421712ce4198cffca20cdb91c6dfe7fa887df09e74ac8c`

```dockerfile
```

-	Layers:
	-	`sha256:1c8bf373aaaa4a73208f8f691e943607d618f051d4ae15b459849838028fc802`  
		Last Modified: Mon, 01 Dec 2025 22:13:07 GMT  
		Size: 5.8 MB (5820749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de191fdae49e7b2a7eaca11cd3bce1ccdf45977b48f7f2f1f288949b32399ef`  
		Last Modified: Mon, 01 Dec 2025 22:13:06 GMT  
		Size: 38.7 KB (38656 bytes)  
		MIME: application/vnd.in-toto+json
