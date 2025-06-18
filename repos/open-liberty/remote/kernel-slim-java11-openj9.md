## `open-liberty:kernel-slim-java11-openj9`

```console
$ docker pull open-liberty@sha256:8d61540ea349bc9a2bd7c7fdd4e90203ecbfb011f1069837186ae383fedea129
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

### `open-liberty:kernel-slim-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:2931c19464649337cdffa73119a21b5c758d575b6054e8f3be81439fd28ceb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116241746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7722b4f42294a7b6c1401cb663e572787a3d97ebc332e8c4b67cae303e67aea2`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
USER root
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_VERSION=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.6 liberty.version=25.0.0.6 io.openliberty.version=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Jun 2025 15:25:00 GMT
USER 1001
# Tue, 17 Jun 2025 15:25:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Jun 2025 15:25:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Jun 2025 15:25:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473154fee0b11bc4d722e43c237f237b69136a24301983502078bc9dc527d0bb`  
		Last Modified: Tue, 17 Jun 2025 17:12:24 GMT  
		Size: 12.2 MB (12172067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb6ba5b52910f78ab9354ac0ad75ba2f1a919068cd8106ef806ea4bc865d2f3`  
		Last Modified: Tue, 17 Jun 2025 17:12:26 GMT  
		Size: 52.5 MB (52456010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3b6884b3df4e65f651464ae3b2df0d53a464c4c7a76e9bcb1b39223e674f69`  
		Last Modified: Tue, 17 Jun 2025 17:12:22 GMT  
		Size: 4.4 MB (4407179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803f5ca76433b475d31a85033862174a399adb3de7bbad168ae536368d5e7055`  
		Last Modified: Tue, 17 Jun 2025 22:33:54 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ef516b01d0806e57090ddbad763487a9b250cf82a61e686381b0bfad289519`  
		Last Modified: Tue, 17 Jun 2025 22:33:55 GMT  
		Size: 12.0 KB (11995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740ffdb7839bb07c5400b7db4aee20b181cd36fccc57177444d4a930cc54ba12`  
		Last Modified: Tue, 17 Jun 2025 22:33:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fd8bb693d823cf97b15a9fdbb8eca4d1e5706a5a6add2daa46b50805ed0034`  
		Last Modified: Tue, 17 Jun 2025 22:33:56 GMT  
		Size: 31.7 KB (31745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dec46a5ef8b975166933f82379d6ab8733772133184ee5fa5831f3f493ece8`  
		Last Modified: Tue, 17 Jun 2025 22:33:57 GMT  
		Size: 14.8 MB (14778030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becaae4e9aa85baf8c9130ad97f8d55c57ca944a4a5fdb1c3fa60ea5d99f8c7f`  
		Last Modified: Tue, 17 Jun 2025 22:33:56 GMT  
		Size: 736.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec0813a9320ead3d6cb37b8bbc94024946950dce8936ad8987aa530af01b576`  
		Last Modified: Tue, 17 Jun 2025 22:33:56 GMT  
		Size: 13.1 KB (13056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33a5eb542fcfc2f0a715663b8c4131964d9518572e1d10ce47fb91a6b32b94`  
		Last Modified: Tue, 17 Jun 2025 22:33:57 GMT  
		Size: 2.8 MB (2836638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:838e4baad3dbf6cc97329a4dcd2dba103561c6ba07ed10aa283a69938b47e8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891e49314b0517d3cb0eabca0c95a936dc0b23ffcd9b75653b64e7dc4b41e83b`

```dockerfile
```

-	Layers:
	-	`sha256:75a9329da25d9079e0846f40e88aa8c0de873ef64240e2ad9b8be22704509056`  
		Last Modified: Tue, 17 Jun 2025 23:46:50 GMT  
		Size: 3.9 MB (3879191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3ce7bb1be42132fed8510e1a255c992f8a791d44990b6245a6fc482bc02581`  
		Last Modified: Tue, 17 Jun 2025 23:46:51 GMT  
		Size: 38.9 KB (38942 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:d223b2a2fd1f7481384e3a0df14b52296a414b21cc95ff56071b1f5794de8599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110146057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d6c6cfd330cb776caa9d1176c2e32f66301af39dd7cc8096966d1fbfc671b5`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
USER root
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_VERSION=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.6 liberty.version=25.0.0.6 io.openliberty.version=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Jun 2025 15:25:00 GMT
USER 1001
# Tue, 17 Jun 2025 15:25:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Jun 2025 15:25:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Jun 2025 15:25:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbff14187feb7082a330fc6604f5d950114fba77a27a3564014bdeb0c0a7e399`  
		Last Modified: Tue, 17 Jun 2025 17:39:17 GMT  
		Size: 12.1 MB (12129302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79aed8751db549046792bc777edcca525eedc89ebe93460c37e203404f05870`  
		Last Modified: Tue, 17 Jun 2025 17:46:33 GMT  
		Size: 48.9 MB (48888727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a052f878cd6890586d100378a6682fad252e4a82b6954453d38c3f7e738bc00`  
		Last Modified: Tue, 17 Jun 2025 17:46:30 GMT  
		Size: 4.2 MB (4197882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29485922ff1806c83b91387fae36be97ab585e1085f1c552adb0b08d97ccac7`  
		Last Modified: Tue, 17 Jun 2025 18:24:30 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e37a049ca62470bd2c063aa96b25c6c8eece4ce41ccf63a2fbceb28828cefe`  
		Last Modified: Tue, 17 Jun 2025 22:39:28 GMT  
		Size: 12.0 KB (11999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0412c98dc89edf5141c725944ea260eacf29a5eb8efa9411dc6d081b05332c9`  
		Last Modified: Tue, 17 Jun 2025 22:39:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4334db577d619043fb7f198dd69cde3a725dec6d42efbfbe2fea30443cefa4`  
		Last Modified: Tue, 17 Jun 2025 22:39:28 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf92807972e99b5b5a83de286668c84d707de0480a3b5534ba920811110207`  
		Last Modified: Tue, 17 Jun 2025 22:39:34 GMT  
		Size: 14.8 MB (14778147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da1d85b4b0164a10828c7cd638dc29039668c27870f4c816945f22e770105b3`  
		Last Modified: Tue, 17 Jun 2025 22:39:29 GMT  
		Size: 739.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d747db74cc1701050791692920155ae0bda56f2291375b709523c5e9168d5209`  
		Last Modified: Tue, 17 Jun 2025 22:39:29 GMT  
		Size: 13.1 KB (13061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efac1a76cfc3fa3d9e93e337b40069b9afd80118bc5df9b41e67a4093b85aa2`  
		Last Modified: Tue, 17 Jun 2025 22:39:31 GMT  
		Size: 2.7 MB (2727003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:a8bb31de767091ab5c2f9f3b4b734640cf0ba1da47596034a4e8c2ab69e1bb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3911619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc30d8e03bb664d6d7d84b34c38391ce2fa639bac8b175d3d58989ae20c17d9`

```dockerfile
```

-	Layers:
	-	`sha256:9f69a77915d76a886f8910eb520f0c1e4cd849db0d89e349fba21472670c9aa0`  
		Last Modified: Tue, 17 Jun 2025 23:46:55 GMT  
		Size: 3.9 MB (3872537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e3c2b4204125217c8cf9dc1e057b15c72f615cd5c72fa4d0891e8dd0398601`  
		Last Modified: Tue, 17 Jun 2025 23:46:56 GMT  
		Size: 39.1 KB (39082 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:8906eee9bead52cc803b64926c77dd0d98d0727300aa6c231564c579fb10f9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122385731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16e28792e2800fd1e648f1d93747aeafbc686e027182326d286820a432ec731`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
USER root
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_VERSION=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.6 liberty.version=25.0.0.6 io.openliberty.version=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Jun 2025 15:25:00 GMT
USER 1001
# Tue, 17 Jun 2025 15:25:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Jun 2025 15:25:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Jun 2025 15:25:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c0a1fca7ea07c8c5a127826c7981b2bbb00fab8901f776e93777f6b6e7e19f`  
		Last Modified: Tue, 17 Jun 2025 17:55:19 GMT  
		Size: 12.9 MB (12893311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe643e2c62ba3b29b36e85d1c1b3ad4b19b8525dc1c11534591b5a897b87108`  
		Last Modified: Tue, 17 Jun 2025 18:04:01 GMT  
		Size: 54.1 MB (54102703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff5d8745a02d7d1739003a9cbb478252421dfc67060330461e18b9750223855`  
		Last Modified: Tue, 17 Jun 2025 18:03:48 GMT  
		Size: 3.5 MB (3464435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ff96f0a3d789c145c525b7d8eb13902eff9ab290b249dccf6b5833aa5f1ba6`  
		Last Modified: Tue, 17 Jun 2025 19:16:52 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496a55e4a38a593df6fd0665cb860b203439c68caa385a1b0e9bc43cb214d40e`  
		Last Modified: Tue, 17 Jun 2025 22:43:16 GMT  
		Size: 12.0 KB (12002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b8c6af921552bb28fba68defceb7d66777c073638467de4eb767f27818a13f`  
		Last Modified: Tue, 17 Jun 2025 22:43:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b72436e1b62a27cbc9c7ec6b88a656e52e29a4c7f7b96afbe00739bab3aa54`  
		Last Modified: Tue, 17 Jun 2025 22:43:16 GMT  
		Size: 36.5 KB (36495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2791688782f568d27ef5844e50499644655b66cb55f9f5f0d5f597e269ad9427`  
		Last Modified: Tue, 17 Jun 2025 22:43:17 GMT  
		Size: 14.8 MB (14778297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7c193045e2920904e03ad546ebbb80e3de42364db3819e0bba598a7737ad52`  
		Last Modified: Tue, 17 Jun 2025 22:43:16 GMT  
		Size: 746.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f860b3aa228a27fbb42632db8e7d88fb9d4b31946edc9234fc3afc8cd89a12`  
		Last Modified: Tue, 17 Jun 2025 22:43:16 GMT  
		Size: 13.1 KB (13086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dacaa03b14b6e775568a833a58a03bb295b6901af331cd394dbd4394481074`  
		Last Modified: Tue, 17 Jun 2025 22:43:17 GMT  
		Size: 2.6 MB (2643003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:0fc01295668d4019dcd8995699e85710d87eac61595abf6f3cb0a5b0b9b78adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3922799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226473de6ffe7c2e9ccefdff54c03c458d9fc83c5541fda7c7169474e42bca8a`

```dockerfile
```

-	Layers:
	-	`sha256:35c2095e577af3209352ba10e33c3d626c4b41b991b16068e7e319b2ef877b48`  
		Last Modified: Tue, 17 Jun 2025 23:47:06 GMT  
		Size: 3.9 MB (3883818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda4d14c77f36337d12a158f6fd8fe742e2db5b6b9a7dfff064db4379df8bed2`  
		Last Modified: Tue, 17 Jun 2025 23:47:07 GMT  
		Size: 39.0 KB (38981 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:kernel-slim-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:9fe0821e5bceb0f0f05132c6f36357d8b46fabd3aa294980e65af6c5eaa5ff88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113760463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bc5378b40506ec9e99a0fbf0f8eaf48f898425fdd604662e226b32442a87ef`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 30 May 2025 22:31:10 GMT
ARG RELEASE
# Fri, 30 May 2025 22:31:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:31:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:31:10 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:31:12 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Fri, 30 May 2025 22:31:12 GMT
CMD ["/bin/bash"]
# Tue, 17 Jun 2025 14:26:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Jun 2025 14:26:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_VERSION=jdk-11.0.27+6_openj9-0.51.0
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7aa093df03eb825d62a72a64a60e238e9fde2d36ed18f6e5418e07318ad155a2';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_aarch64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='81c7c9ee709939cc66d5122f096cd36a4d1630851d275881799746b8f9d050da';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_ppc64le_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        amd64|x86_64)          ESUM='73b79ace5c4e01cf5b0c002799185a5db4a601b3158c690cb204e3b618ad7b6e';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_x64_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        s390x)          ESUM='1225935c404b2d3f788da9c7df81250a4519a3eb8b7fc39ddc8efe5845a02051';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.27%2B6_openj9-0.51.0/ibm-semeru-open-jre_s390x_linux_11.0.27_6_openj9-0.51.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Jun 2025 14:26:50 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Jun 2025 14:26:50 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956";     TOMCAT_VERSION="9.0.105";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
USER root
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_VERSION=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip
# Tue, 17 Jun 2025 15:25:00 GMT
ARG LIBERTY_BUILD_LABEL=cl250620250602-1102
# Tue, 17 Jun 2025 15:25:00 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
ARG VERBOSE=false
# Tue, 17 Jun 2025 15:25:00 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250620250602-1102 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.6 liberty.version=25.0.0.6 io.openliberty.version=25.0.0.6
# Tue, 17 Jun 2025 15:25:00 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
# ARGS: LIBERTY_VERSION=25.0.0.6 LIBERTY_SHA=de41ad8ec018c12178e4339908626bcc6b89fdaa LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-kernel/25.0.0.6/openliberty-kernel-25.0.0.6.zip LIBERTY_BUILD_LABEL=cl250620250602-1102 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache /output/workarea     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Jun 2025 15:25:00 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Jun 2025 15:25:00 GMT
USER 1001
# Tue, 17 Jun 2025 15:25:00 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Jun 2025 15:25:00 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Jun 2025 15:25:00 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a592dff2b7023a1eb4d0588791417d7ab44efe41ce34295948fbb1653b7e87`  
		Last Modified: Tue, 17 Jun 2025 21:00:33 GMT  
		Size: 12.2 MB (12219457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae0bc1b527924c0ace1e0d04d6fd3c57ee65b1970ba12cd17e99e38e1cc6712`  
		Last Modified: Tue, 17 Jun 2025 18:19:08 GMT  
		Size: 51.3 MB (51349445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6724620859c92111104b1ce73e900908380d478be466a4911b4227f1035d41`  
		Last Modified: Tue, 17 Jun 2025 18:19:03 GMT  
		Size: 4.6 MB (4583329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c4b2f3b8fdbec42967fb1b6ba6c42e2d5dfd5f38ffb662fb727abc31367dbd`  
		Last Modified: Tue, 17 Jun 2025 19:24:13 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d77b789a38197f383e77f451bd27492d8af4428ee9d4daaaf1efa228f26455`  
		Last Modified: Tue, 17 Jun 2025 22:39:55 GMT  
		Size: 12.0 KB (12004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f58b0229ca048cb499eee7ec2552efe97a59ec87077a64faaf4d4e179f1af7f`  
		Last Modified: Tue, 17 Jun 2025 22:39:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3b1d9e15aafc2bf657a63d9b3dbffd4ee23d5db4e2dc8976fc715c2982c53c`  
		Last Modified: Tue, 17 Jun 2025 22:39:55 GMT  
		Size: 33.1 KB (33112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d919cefa68589a8a2799bc008181ae6d0bdd6c05ecc57a7365582634c1c690`  
		Last Modified: Tue, 17 Jun 2025 22:39:58 GMT  
		Size: 14.8 MB (14777719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3fca049fd1cb3ddf0e8b9410753cf4435bcf9873d36b2ee7e8e28f2de30ba5`  
		Last Modified: Tue, 17 Jun 2025 22:39:56 GMT  
		Size: 744.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052464275eeb333133fbe7fef2d24c500d11eb47155db4355dd7cc814df0e4c4`  
		Last Modified: Tue, 17 Jun 2025 22:39:56 GMT  
		Size: 13.1 KB (13072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73b785071b2cd2ead7bc56e9079a6901ea988ba99aa54eb955adb3280bca8e5`  
		Last Modified: Tue, 17 Jun 2025 22:39:57 GMT  
		Size: 2.8 MB (2769688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:kernel-slim-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:7a13756909744a000dd3814c27f59c7043813704d7338d6770343bfd8923d5d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c2df60ee27212837dad2c61d2551f90f5dc493a65647b1173f82823c81b76c`

```dockerfile
```

-	Layers:
	-	`sha256:0269fa992e8099e32099b457bb96650fa63d6c6f89fe35d8b3e3832d8fda457c`  
		Last Modified: Tue, 17 Jun 2025 23:47:12 GMT  
		Size: 3.9 MB (3880208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae38e8f7966cec8dbca3c9807b92ac4853a1db1ca1eb85b136302267fd69a42`  
		Last Modified: Tue, 17 Jun 2025 23:47:13 GMT  
		Size: 38.9 KB (38942 bytes)  
		MIME: application/vnd.in-toto+json
