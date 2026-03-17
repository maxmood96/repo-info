## `open-liberty:full`

```console
$ docker pull open-liberty@sha256:98c9b74e69ad8788caabfa4bad381c94cf9ab30c37e9c6f848534f386e61ee1c
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

### `open-liberty:full` - linux; amd64

```console
$ docker pull open-liberty@sha256:12e1b997f8ecfc5164915f7b04bc4e0dbfb69454bb438e22ff4f0f724ce20da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460496269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c226bc196879b54c7d105955e7efef6b592e69fb9ac86888abcd4cfc2154f1a0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:33:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:33:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:33:44 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 17 Mar 2026 01:33:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 01:33:46 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:33:46 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 01:34:49 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 02:42:14 GMT
USER root
# Tue, 17 Mar 2026 02:42:14 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 02:42:14 GMT
ARG LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d
# Tue, 17 Mar 2026 02:42:14 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip
# Tue, 17 Mar 2026 02:42:14 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 02:42:14 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:42:14 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 02:42:14 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.2 liberty.version=26.0.0.2 io.openliberty.version=26.0.0.2
# Tue, 17 Mar 2026 02:42:14 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Mar 2026 02:42:14 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Mar 2026 02:42:14 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Mar 2026 02:42:14 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Mar 2026 02:42:33 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Mar 2026 02:42:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:42:33 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 02:42:33 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 02:42:53 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Mar 2026 02:42:53 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Mar 2026 02:42:53 GMT
USER 1001
# Tue, 17 Mar 2026 02:42:53 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 02:42:53 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 02:42:53 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059f6885c3a59396e58185af50c67086e7395194e4bdf3f9c1a6ec6d7b1140d7`  
		Last Modified: Tue, 17 Mar 2026 01:35:01 GMT  
		Size: 12.8 MB (12805219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb143f5dc096332f7a83a030ee6388fd2e95fb37cb7e0727bfc4ca68f2baff0`  
		Last Modified: Tue, 17 Mar 2026 01:35:02 GMT  
		Size: 54.0 MB (53997193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fed6933c4a2c709fdbe73e3aecf4664714bce3cd447b2bab1f029aec998bef`  
		Last Modified: Tue, 17 Mar 2026 01:35:00 GMT  
		Size: 4.3 MB (4253834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7096bbe3ba4046f5317a878113880b756c27768f5b20b6d74eed60496af89f`  
		Last Modified: Tue, 17 Mar 2026 02:43:17 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4793c52d878814c51f81b33b0d4c375c2e699298ce39c173e5ac8d4a22eb46f9`  
		Last Modified: Tue, 17 Mar 2026 02:43:18 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a3a9e9a17fe6f4cdfb6ad2b764237243fbe7abff05f6bf2adaac530cf22f1`  
		Last Modified: Tue, 17 Mar 2026 02:43:17 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb733e25d6afefd9d0f371e86f3ff93a6bd6ea9b0aa503df8641d1bb5a1c27`  
		Last Modified: Tue, 17 Mar 2026 02:43:17 GMT  
		Size: 31.7 KB (31748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8dc16f042a1e0bc17364db51fbf71d4f913522ed8b1d3d987fd1e6faca881b`  
		Last Modified: Tue, 17 Mar 2026 02:43:25 GMT  
		Size: 346.6 MB (346551655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b73e24dd84603ac6c419c0636929a9e8f2b93346979d9a6b288812c780a7db`  
		Last Modified: Tue, 17 Mar 2026 02:43:19 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e7f4cfa58eb5de440c557cfa9cf09898b421e629167b14f5587f553f54a31b`  
		Last Modified: Tue, 17 Mar 2026 02:43:19 GMT  
		Size: 13.7 KB (13720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51532e17b76149ba33dd99142eb693b31374364676da15a5777daf2a1d56e73`  
		Last Modified: Tue, 17 Mar 2026 02:43:19 GMT  
		Size: 13.1 MB (13096275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:ad12bf578a34d1162e3fc7dd809d0c12c91978ab40b7ce4bf180b8e5645a4f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d253570a7357586d5469e5496d9d8518b1cee3db8282c941a731df2249e58405`

```dockerfile
```

-	Layers:
	-	`sha256:368f77e2f70b29584db81a65450c50dee9037576dcd9a7fefc5633fa933ed2b3`  
		Last Modified: Tue, 17 Mar 2026 02:43:18 GMT  
		Size: 5.2 MB (5174047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5f34d8d8e8d63fef077c4bcf4928cb44056b0e1a9629b39d8d96e4aa5ae754`  
		Last Modified: Tue, 17 Mar 2026 02:43:17 GMT  
		Size: 40.0 KB (39965 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:6c892d378b22a7a10d18d3a03d5d05546d898e9ab83fa59dc0927fd1f17d71dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.1 MB (459116874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f802bee94f0787003dc68f67ac72035cc6e525883d20fcf69e75c520fd5acab`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:35:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:35:00 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:35:00 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 17 Mar 2026 01:35:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 01:35:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:35:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 01:36:05 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 02:46:32 GMT
USER root
# Tue, 17 Mar 2026 02:46:32 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 02:46:32 GMT
ARG LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d
# Tue, 17 Mar 2026 02:46:32 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip
# Tue, 17 Mar 2026 02:46:32 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 02:46:32 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:46:32 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 02:46:32 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.2 liberty.version=26.0.0.2 io.openliberty.version=26.0.0.2
# Tue, 17 Mar 2026 02:46:32 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Mar 2026 02:46:32 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Mar 2026 02:46:32 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Mar 2026 02:46:32 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Mar 2026 02:46:51 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Mar 2026 02:46:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Mar 2026 02:46:51 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 02:46:52 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 02:47:12 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Mar 2026 02:47:12 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Mar 2026 02:47:12 GMT
USER 1001
# Tue, 17 Mar 2026 02:47:12 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 02:47:12 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 02:47:12 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4d74baf060663279eeeb890b897566f7cd73e2daf822b7072afed2d7383943`  
		Last Modified: Tue, 17 Mar 2026 01:36:17 GMT  
		Size: 12.8 MB (12837534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48073fd700af09e12a53edcc3978bd58f433e7cc32086a2f42d97be1c9ce7b23`  
		Last Modified: Tue, 17 Mar 2026 01:36:18 GMT  
		Size: 53.7 MB (53702900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ffcd50baf446fc05677f89c76c26981f7a5b400f09f9d75e0d853c42ad43c4`  
		Last Modified: Tue, 17 Mar 2026 01:36:17 GMT  
		Size: 4.1 MB (4114825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb8251f6cf7daf8252c0db8a8e3c7a0fa17587421e4c4843e5c5e747199c529`  
		Last Modified: Tue, 17 Mar 2026 02:47:38 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a66048ab55b1802f8d7feb7f80ef3c4af02bf41c988e092f8a2f328035c5349`  
		Last Modified: Tue, 17 Mar 2026 02:47:38 GMT  
		Size: 12.3 KB (12283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbd68d8c8e1fdb32f032b9fc49fb6af350b164085432a943fc9227aa149000b`  
		Last Modified: Tue, 17 Mar 2026 02:47:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091242f4cc5918e6964033f4e86a32df8c8431fd75865ee8241641c752d0d598`  
		Last Modified: Tue, 17 Mar 2026 02:47:38 GMT  
		Size: 42.3 KB (42325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2a072165c56fc8cb9f075b313bbd4a8e54cbd03f9f7183adb652ad3d11505e`  
		Last Modified: Tue, 17 Mar 2026 02:47:46 GMT  
		Size: 346.6 MB (346551787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90090c0309a70df73e7e066ffc282486ff0a47817f0ffb07890db3df94a5b526`  
		Last Modified: Tue, 17 Mar 2026 02:47:39 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a07f3627079ad590793c0e7a30e881aca04452247bf61329abad0194e87438a`  
		Last Modified: Tue, 17 Mar 2026 02:47:39 GMT  
		Size: 13.7 KB (13747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd5f49589e3ee34bae87573978f51931541c1943dc7085df46b2e073e7788a`  
		Last Modified: Tue, 17 Mar 2026 02:47:40 GMT  
		Size: 13.0 MB (12969416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:062c751d2f74acd7a97821ba0c85c3d3f385542a98a6fd22349dd1bbbe27a55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a355fd1d47cd425601dc5d22a454f521c9f3ad57a4fc24dfc0ca3c540606470`

```dockerfile
```

-	Layers:
	-	`sha256:08a4cf705af6cbe8e71cdd236a7ca9b1d9bbbb2deb843d9d094f36585790125f`  
		Last Modified: Tue, 17 Mar 2026 02:47:38 GMT  
		Size: 5.2 MB (5174660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01949067767b36e84c011a4a04683797061f126d4203db2196b9b535c30004f`  
		Last Modified: Tue, 17 Mar 2026 02:47:38 GMT  
		Size: 40.1 KB (40116 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:1c72e3d10e112ae66d085d0813247437e12def9bcc804fcc81e519abb3888acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.6 MB (465616629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7215ab2138fe8a454161591fd8bca8292200047f7ded307e007b68fe89f71b8`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:45:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:45:44 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:45:44 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 17 Mar 2026 08:47:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 08:47:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:47:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 08:48:15 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 13:42:27 GMT
USER root
# Tue, 17 Mar 2026 13:42:27 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 13:42:27 GMT
ARG LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d
# Tue, 17 Mar 2026 13:42:27 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip
# Tue, 17 Mar 2026 13:42:27 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 13:42:27 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 13:42:27 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 13:42:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.2 liberty.version=26.0.0.2 io.openliberty.version=26.0.0.2
# Tue, 17 Mar 2026 13:42:27 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Mar 2026 13:42:28 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Mar 2026 13:42:28 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Mar 2026 13:47:39 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Mar 2026 13:48:06 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Mar 2026 13:48:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Mar 2026 13:48:07 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 13:48:09 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 13:48:47 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Mar 2026 13:48:47 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Mar 2026 13:48:47 GMT
USER 1001
# Tue, 17 Mar 2026 13:48:47 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 13:48:47 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 13:48:47 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fe6dcb8fff5ef43c62b8992539a79449cf84c229ea4dd2a5c95e478fed5d02`  
		Last Modified: Tue, 17 Mar 2026 08:47:39 GMT  
		Size: 13.8 MB (13787899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2f2cb68c895a6ee57f9db90b85f4fd5ce62683b680be1e875ab9de8ec6adea`  
		Last Modified: Tue, 17 Mar 2026 08:48:40 GMT  
		Size: 55.6 MB (55597364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ab609e7e271942902ac6ebf71cb4e22b7b940e1cbc6749da29003a2305ad1e`  
		Last Modified: Tue, 17 Mar 2026 08:48:39 GMT  
		Size: 3.5 MB (3490791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b597e410bf701d93b6fef62ca2cd277d61be67f305d57c351bea7e04313ac8`  
		Last Modified: Tue, 17 Mar 2026 13:44:42 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cf63f5f0b3df3c7bea31b2df2a4339da4676fca4e364d083da4eca8bd58428`  
		Last Modified: Tue, 17 Mar 2026 13:44:42 GMT  
		Size: 12.3 KB (12280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354595b93e0409fa79a89d8889de11efebb31028e70ff7ebb3862ece976552ef`  
		Last Modified: Tue, 17 Mar 2026 13:44:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be288a48a5c36c04ff1d1c31795f4f02c1e402e68856501d4d7d0a94ba0f1de`  
		Last Modified: Tue, 17 Mar 2026 13:49:41 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae94a1d49373240d9c8e6d4be6c942d5f2cad49e0f2c819a9b391b35b36360`  
		Last Modified: Tue, 17 Mar 2026 13:49:49 GMT  
		Size: 346.6 MB (346551838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b761cd023c95e68df5cc78b163cca359b94c27c8efb463082fd699c72be6235`  
		Last Modified: Tue, 17 Mar 2026 13:49:41 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df68e8a9f07c7cde6a1ba3ae165ca44a6f526b296cee8c2680789b4ea425f2d`  
		Last Modified: Tue, 17 Mar 2026 13:49:41 GMT  
		Size: 13.8 KB (13754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bd4e95046b4243482ea6f26ea3eb726d7a11b37443bb27b4d5eabf13c776c3`  
		Last Modified: Tue, 17 Mar 2026 13:49:43 GMT  
		Size: 11.8 MB (11813809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:5d04ca9c3d531e099e66e0d4623580beb4136e37279a6c8e6994ca9b51481f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806aa15177ede5b0154bee94c108bbe18884b1ad7469bf5a59a28f38075d5ba9`

```dockerfile
```

-	Layers:
	-	`sha256:ae35163d85da47cda800e22a31698b23ec56db22a107040abaf23f0160f2248d`  
		Last Modified: Tue, 17 Mar 2026 13:49:41 GMT  
		Size: 5.2 MB (5178851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f431751f5f9731f64b5a8d1ab444c7b7332c9fffe9c3c8d902ea53907c3e16`  
		Last Modified: Tue, 17 Mar 2026 13:49:41 GMT  
		Size: 40.0 KB (40011 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full` - linux; s390x

```console
$ docker pull open-liberty@sha256:f0af2553b17d6c500fc4936edcb9e65eeb082031417a28b3a41933e953d6cb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461019302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dcabebc72dfe94ea2f2f7ab4d340f52feed9207a7f9d815c28e3e955864ff0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:26:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:26:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:16 GMT
ENV JAVA_VERSION=jdk8u482-b08.1_openj9-0.57.0
# Tue, 17 Mar 2026 03:05:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)         ESUM='d8fcad671559ab383d55d331db6725a5957f110faffe17d766c7ca3b14e71abd';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_aarch64_linux_8.0.482.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='4b66859a60b250db44e6fe3b8bd8cb5f3908be50315bad0e946961c7ac03a59a';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_ppc64le_linux_8.0.482.1.tar.gz';          ;;        amd64|x86_64)          ESUM='0bf81e496b5fed8669fc5b624ba7fb45fe05d7b9c19485f441ab48d2edad68fe';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_x64_linux_8.0.482.1.tar.gz';          ;;        s390x)          ESUM='a91c33d74cc5a0826f56efe48aa2f1223c6e25189a6bb8a8444e6f67b2581765';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u482-b08.1_openj9-0.57.0/ibm-semeru-open-jre_s390x_linux_8.0.482.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 17 Mar 2026 03:05:54 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:54 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 17 Mar 2026 03:07:04 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     export CATALINA_PID=/opt/tomcat-home/tomcat.pid;     TOMCAT_CHECKSUM="8e6fa92883c161523269560a7dc9e8d58fd1199b29c630f681aa3ec2975b59d94674d2881331076b55f5ee0439748931d87c099c79d7bcea909303739e612e4b";     TOMCAT_VERSION="9.0.115";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 20;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     unset CATALINA_PID;     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 17 Mar 2026 07:15:15 GMT
USER root
# Tue, 17 Mar 2026 07:15:15 GMT
ARG LIBERTY_VERSION=26.0.0.2
# Tue, 17 Mar 2026 07:15:15 GMT
ARG LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d
# Tue, 17 Mar 2026 07:15:15 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip
# Tue, 17 Mar 2026 07:15:15 GMT
ARG LIBERTY_BUILD_LABEL=cl260220260207-1901
# Tue, 17 Mar 2026 07:15:15 GMT
ARG OPENJ9_SCC=true
# Tue, 17 Mar 2026 07:15:15 GMT
ARG VERBOSE=false
# Tue, 17 Mar 2026 07:15:15 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl260220260207-1901 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=26.0.0.2 liberty.version=26.0.0.2 io.openliberty.version=26.0.0.2
# Tue, 17 Mar 2026 07:15:15 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 17 Mar 2026 07:17:47 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 17 Mar 2026 07:17:48 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 17 Mar 2026 07:17:50 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 17 Mar 2026 07:18:18 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 17 Mar 2026 07:18:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 17 Mar 2026 07:18:19 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 17 Mar 2026 07:18:24 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Tue, 17 Mar 2026 07:19:08 GMT
# ARGS: LIBERTY_VERSION=26.0.0.2 LIBERTY_SHA=f2384de851755ae7b0c39b0f5876748f50053a3d LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/26.0.0.2/openliberty-runtime-26.0.0.2.zip LIBERTY_BUILD_LABEL=cl260220260207-1901 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 17 Mar 2026 07:19:08 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 17 Mar 2026 07:19:08 GMT
USER 1001
# Tue, 17 Mar 2026 07:19:08 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 17 Mar 2026 07:19:08 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 17 Mar 2026 07:19:08 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd91993ecc458a9cb74eb0484d5b3851acdd9dce8eb8f17d293bf0e1e72fb77`  
		Last Modified: Tue, 17 Mar 2026 02:27:53 GMT  
		Size: 13.1 MB (13117082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245443fca6a010988504e1f46e16f4de063ade3d5b9a452915b2f7beb55f11f3`  
		Last Modified: Tue, 17 Mar 2026 03:07:57 GMT  
		Size: 53.4 MB (53424165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48fd8dff32c7708cd6550c305da9801d5a396e45568acc25faeb267770b45b`  
		Last Modified: Tue, 17 Mar 2026 03:07:55 GMT  
		Size: 4.5 MB (4460822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4186b7b40e09db60f8dea38fb20f7620495dd217e804e80ed051f29f49b1afc`  
		Last Modified: Tue, 17 Mar 2026 07:17:16 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469d350a2610145d742e320dcd35ea54b8cc6da399b5861b0bc75a893de2d716`  
		Last Modified: Tue, 17 Mar 2026 07:20:00 GMT  
		Size: 12.3 KB (12285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bab32b1b97bcb35c007aad8031a2a5c2c1e3ce2313d091fed95a5f515c96a3`  
		Last Modified: Tue, 17 Mar 2026 07:20:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6468e1070eadf6695e08c94c189ad0f8902edfb08249398fb5542f34331106`  
		Last Modified: Tue, 17 Mar 2026 07:20:00 GMT  
		Size: 33.1 KB (33109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3867ac638c9e6ba445d102410a6de4fac497b2c1cf59f96c475a07b2faf26df`  
		Last Modified: Tue, 17 Mar 2026 07:20:07 GMT  
		Size: 346.6 MB (346551440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37780f22aba11a37f82af5e1adabb3702e5a013a7a5547a961a94aee5815c2`  
		Last Modified: Tue, 17 Mar 2026 07:20:01 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68dc9164fe8401edf4ca000972188f679c68d8ec20703bfc0b9f87e88c97d9e`  
		Last Modified: Tue, 17 Mar 2026 07:20:02 GMT  
		Size: 13.7 KB (13748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308b2cec7ae6ce328099a7fc689b02009a75e8bf7b785013b55f414a5aab1f75`  
		Last Modified: Tue, 17 Mar 2026 07:20:02 GMT  
		Size: 13.5 MB (13493916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full` - unknown; unknown

```console
$ docker pull open-liberty@sha256:fb3ae477f466ec1061eed191319165b97edd4052abcc44c34dcb65c7a92eb596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf6ce0000c3eaf34959aa5cab5b7d42df6a2ef62cda146e3bfef06c3dafd105`

```dockerfile
```

-	Layers:
	-	`sha256:2f95f7323b987043f12bd78e53cf59dd7003880dd53b13cda336c7d16f72876f`  
		Last Modified: Tue, 17 Mar 2026 07:20:01 GMT  
		Size: 5.2 MB (5175670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f31bdfb51621d16b97b9c009511dba4cce0d277447839a058b3424f1e3c0c67`  
		Last Modified: Tue, 17 Mar 2026 07:20:00 GMT  
		Size: 40.0 KB (39965 bytes)  
		MIME: application/vnd.in-toto+json
