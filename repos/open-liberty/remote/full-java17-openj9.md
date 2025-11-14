## `open-liberty:full-java17-openj9`

```console
$ docker pull open-liberty@sha256:d23b20daaad0fdc3d4134fa7442cd717bd076729bf9aa58513571dc2aeda5420
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
$ docker pull open-liberty@sha256:1ccbce4490c155ee1c160648738921a7e64882db92d074d5c7e37f840d5828f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.8 MB (459798632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98108606e16f39cd596e9117abb824c5c53efb44fb58026af693ec2238adc92d`
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
# Thu, 13 Nov 2025 23:26:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:26:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:26:12 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 13 Nov 2025 23:26:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:26:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:26:15 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:26:47 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 14 Nov 2025 00:31:28 GMT
USER root
# Fri, 14 Nov 2025 00:31:28 GMT
ARG LIBERTY_VERSION=25.0.0.11
# Fri, 14 Nov 2025 00:31:28 GMT
ARG LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f
# Fri, 14 Nov 2025 00:31:28 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip
# Fri, 14 Nov 2025 00:31:28 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 00:31:28 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:31:28 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 00:31:28 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.11 liberty.version=25.0.0.11 io.openliberty.version=25.0.0.11
# Fri, 14 Nov 2025 00:31:28 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 14 Nov 2025 00:31:28 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 14 Nov 2025 00:31:28 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 14 Nov 2025 00:31:29 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 14 Nov 2025 00:31:46 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 14 Nov 2025 00:31:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:31:46 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 00:31:47 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 00:32:07 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 14 Nov 2025 00:32:07 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 14 Nov 2025 00:32:07 GMT
USER 1001
# Fri, 14 Nov 2025 00:32:07 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 00:32:07 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 00:32:07 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed758cc5553a37ce8cad94f4b107e110a36e826b5877bddfb2f3c141f783dfa`  
		Last Modified: Thu, 13 Nov 2025 23:27:08 GMT  
		Size: 12.2 MB (12171706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b84bbca0fa33b311d0fb6c24ada2d6cbe1ecc53dfa141d8ef7fc04019138145`  
		Last Modified: Thu, 13 Nov 2025 23:27:17 GMT  
		Size: 55.2 MB (55190794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7aec9a786568cfd3ea9f2580ed8a458a099ef0e8d833b422f82ab29971be740`  
		Last Modified: Thu, 13 Nov 2025 23:27:07 GMT  
		Size: 5.1 MB (5093596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a77bb7933bd20d072a70790902c641a7707aebbfa8ddf7726f164df1b97491`  
		Last Modified: Fri, 14 Nov 2025 00:32:45 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a739e791e08e9fa945cbcd38e3b06fd6e341b38e1b77340bd528422efc20551e`  
		Last Modified: Fri, 14 Nov 2025 00:32:45 GMT  
		Size: 12.3 KB (12287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cb189748685dcec235e3a8377f96bd95f64d33e730353715864be85e85e9fc`  
		Last Modified: Fri, 14 Nov 2025 00:32:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ecaab18c15722a181adde7a93eb9abe15929d863a860d10bada032fa289322`  
		Last Modified: Fri, 14 Nov 2025 00:32:42 GMT  
		Size: 31.7 KB (31749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76e6a69765714fcfe500e2dfa56236ffbcb34798c61385b1d6a9a1e041c5a4`  
		Last Modified: Fri, 14 Nov 2025 03:53:55 GMT  
		Size: 343.9 MB (343938261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c6a078793c52b718e0171adbcc7b29a119f4b2964a6c3064d59f65ab3e4472`  
		Last Modified: Fri, 14 Nov 2025 00:32:45 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0f2c684d3f67974ac98086545e467b774b32c50b99aa501652aa9f6963523a`  
		Last Modified: Fri, 14 Nov 2025 00:32:45 GMT  
		Size: 13.7 KB (13727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a98cd58430562269b3f6e7ac2654f0fb1b3a6acfdb9ca6695f650a13f78ef64`  
		Last Modified: Fri, 14 Nov 2025 00:32:47 GMT  
		Size: 13.8 MB (13807367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:75d4633cafc1eb8f0b8c84f1212e668b237620583b1be3c5bad59a0706275af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5740356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97e28aacdfa15a5f908840c8e742183c0a1564efb05d0fc4b144271780c59a0`

```dockerfile
```

-	Layers:
	-	`sha256:a6026a3799f81a15c7ee0891bd072a2832ff154ac871887e9a791bab072db1f4`  
		Last Modified: Fri, 14 Nov 2025 03:52:17 GMT  
		Size: 5.7 MB (5700987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc7292f4e77254d327d797556a27ad8ac14ecf810e92a18da1032f511306fdc`  
		Last Modified: Fri, 14 Nov 2025 03:52:17 GMT  
		Size: 39.4 KB (39369 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:88a41f5983630a5c6eab514cf1214484f7e0b1c4af27fe1b8c5f131c60d776d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.2 MB (455179216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1110f8273ad3046d7da52cad5b67f8648dccabdef0ecfb08bbdb8f58d95586a9`
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
# Thu, 13 Nov 2025 23:26:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:26:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:26:04 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 13 Nov 2025 23:26:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:26:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:26:07 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:26:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 14 Nov 2025 00:31:57 GMT
USER root
# Fri, 14 Nov 2025 00:31:57 GMT
ARG LIBERTY_VERSION=25.0.0.11
# Fri, 14 Nov 2025 00:31:57 GMT
ARG LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f
# Fri, 14 Nov 2025 00:31:57 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip
# Fri, 14 Nov 2025 00:31:57 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 00:31:57 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:31:57 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 00:31:57 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.11 liberty.version=25.0.0.11 io.openliberty.version=25.0.0.11
# Fri, 14 Nov 2025 00:31:57 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 14 Nov 2025 00:31:57 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 14 Nov 2025 00:31:57 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 14 Nov 2025 00:31:57 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 14 Nov 2025 00:32:18 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 14 Nov 2025 00:32:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:32:18 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 00:32:18 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 00:32:40 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 14 Nov 2025 00:32:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 14 Nov 2025 00:32:40 GMT
USER 1001
# Fri, 14 Nov 2025 00:32:40 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 00:32:40 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 00:32:40 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4de0508d820199870bd9526fb7971ba639e12c5e59240c4d7b46465d9d9e77e`  
		Last Modified: Thu, 13 Nov 2025 23:26:59 GMT  
		Size: 12.1 MB (12130079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dbbc93653a34e268180a5212893ca6e44b9fa969e008d682881a08cf5abf94`  
		Last Modified: Thu, 13 Nov 2025 23:27:03 GMT  
		Size: 53.5 MB (53468115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9b00cfd87167f3c6d245a23ce981920902247b97461fa0cda28922bda8c871`  
		Last Modified: Thu, 13 Nov 2025 23:26:58 GMT  
		Size: 4.8 MB (4847896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282109cd658bce3fc92af69f1dd3387dd613b1ed2db93715af57bd38c8cc4e48`  
		Last Modified: Fri, 14 Nov 2025 00:33:19 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d53d698b1b96434726b39f7c3493359c153e8ba42711de41e7addbacbd60a14`  
		Last Modified: Fri, 14 Nov 2025 00:33:19 GMT  
		Size: 12.3 KB (12285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d733a026391b74d7faf7060456c44c6a8a6b7f545118e0e9688956e1bc83463e`  
		Last Modified: Fri, 14 Nov 2025 00:33:19 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b06bf38063bd21fa06b0d689c64c439202d3d3808f95e9688f7189fa8c20813`  
		Last Modified: Fri, 14 Nov 2025 00:33:19 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a64a0dd479f1c119d36aa618d4df5daa6bf8bf177e48e8c24e57410b6286b7`  
		Last Modified: Fri, 14 Nov 2025 00:33:12 GMT  
		Size: 343.9 MB (343938391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d661f701f119196e5a03d6e13af1e411700978d4560a543077a5b7fc887470c8`  
		Last Modified: Fri, 14 Nov 2025 00:33:19 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d0f59fcb2d8b8074796b66ceb37f788c99e85866de0de2ad1b5d2a94a20c`  
		Last Modified: Fri, 14 Nov 2025 00:33:19 GMT  
		Size: 13.7 KB (13722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b202bd1959b205d9a27e543553c779ea80c62d6f849553d4cfa3e342a805d22`  
		Last Modified: Fri, 14 Nov 2025 00:33:20 GMT  
		Size: 13.3 MB (13340182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:8a28da28c125c2f1c4c2933f83aecd1ba8de2422a81a6976ae1116dfa10e00e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5738843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef06e7f486b19a33672bed4f1c2d8aaa1c68ef11e0de4477a514ca1ff5b7898a`

```dockerfile
```

-	Layers:
	-	`sha256:bff242d247546ca86a088b2552d19b7d3392556ea9d631ff51cca98a31896458`  
		Last Modified: Fri, 14 Nov 2025 03:52:24 GMT  
		Size: 5.7 MB (5699347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9023a861fa62f907a62a4a8877c2fb4d4ad19c8c997c77d2ed4b806deeaec016`  
		Last Modified: Fri, 14 Nov 2025 03:52:25 GMT  
		Size: 39.5 KB (39496 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:84f348ad4b2e6d67d16c5e948b1b0d24f93d7cbb75035348264ba557f440d84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.3 MB (464335520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41cc1f430629137bc65c83ae1b1727aa0bbea9c3932e2863eeb3b926ea2eec9`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 18:52:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Oct 2025 18:52:43 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 18:52:43 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 30 Oct 2025 19:07:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Oct 2025 19:07:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 19:07:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 30 Oct 2025 19:07:36 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 30 Oct 2025 19:34:42 GMT
USER root
# Thu, 30 Oct 2025 19:34:42 GMT
ARG LIBERTY_VERSION=25.0.0.11
# Thu, 30 Oct 2025 19:34:42 GMT
ARG LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f
# Thu, 30 Oct 2025 19:34:42 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip
# Thu, 30 Oct 2025 19:34:42 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Thu, 30 Oct 2025 19:34:42 GMT
ARG OPENJ9_SCC=true
# Thu, 30 Oct 2025 19:34:42 GMT
ARG VERBOSE=false
# Thu, 30 Oct 2025 19:34:42 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.11 liberty.version=25.0.0.11 io.openliberty.version=25.0.0.11
# Thu, 30 Oct 2025 19:34:42 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Wed, 05 Nov 2025 05:49:49 GMT
COPY helpers /opt/ol/helpers # buildkit
# Wed, 05 Nov 2025 05:49:49 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Wed, 05 Nov 2025 06:01:36 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Wed, 05 Nov 2025 06:02:08 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Wed, 05 Nov 2025 06:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Wed, 05 Nov 2025 06:02:09 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Wed, 05 Nov 2025 06:02:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Wed, 05 Nov 2025 06:02:49 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Wed, 05 Nov 2025 06:02:49 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 05 Nov 2025 06:02:49 GMT
USER 1001
# Wed, 05 Nov 2025 06:02:49 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Wed, 05 Nov 2025 06:02:49 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Wed, 05 Nov 2025 06:02:49 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d05c427cc331d7b6dd9baffe91a10981b54840825b7525c3636088e5c3447a5`  
		Last Modified: Thu, 30 Oct 2025 18:54:22 GMT  
		Size: 12.9 MB (12893771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef928ed86375eedc62a94feb6fcf1cf8a7e5c19f50bb494965b233e2b2f61db`  
		Last Modified: Thu, 30 Oct 2025 19:08:26 GMT  
		Size: 57.0 MB (57019141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b211053be38f9412e081290294874245c906a4073ccd1b35477bb507d0b25ea6`  
		Last Modified: Thu, 30 Oct 2025 19:08:21 GMT  
		Size: 3.9 MB (3882143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c79b86a8725557d2d3c24ff6fe5e806f45cd8f97537aafbf5c702b03fadf856`  
		Last Modified: Thu, 30 Oct 2025 19:37:20 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92e253c8a9ee6a2d8cf6c2e84427b7e792e8924eda3bbc4884cd320f0e0f7d0`  
		Last Modified: Wed, 05 Nov 2025 05:52:22 GMT  
		Size: 12.3 KB (12290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f963f2c4cc38e547c57b1ab82125ace399318b63f273dabd5ee77904aac326`  
		Last Modified: Wed, 05 Nov 2025 05:52:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362b28e8f08268d981a4465f563e0b5e3a743c3fd943f7f0016c38ecf8a22b3e`  
		Last Modified: Wed, 05 Nov 2025 06:04:03 GMT  
		Size: 36.5 KB (36498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd52738f76c8f831d377fb395bcd1a093e77000d0ff209670190e91c96b14bb`  
		Last Modified: Wed, 05 Nov 2025 16:34:34 GMT  
		Size: 343.9 MB (343938575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce0cfb1806197c5676d950c211f3f322726193f5466a6b5992628cfc36d3f10`  
		Last Modified: Wed, 05 Nov 2025 06:04:03 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04832242fb50dea28a8a0cca446b2cc5e761b1fc1322dd0be7dc67b382f82d86`  
		Last Modified: Wed, 05 Nov 2025 06:04:03 GMT  
		Size: 13.7 KB (13748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c38ef92322289f3755df44b5e4c90e338d7a4a7cad80a75dade8f94e5579c09`  
		Last Modified: Wed, 05 Nov 2025 06:04:04 GMT  
		Size: 12.1 MB (12090208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:9164524e9e93f80124c83857c86c5e57bbc9a91d6fd8a14c2147f324f310cb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5745011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee9f5dc59b3e87e38816e7859f30ee6d44b4a735a35d5da2ba02f6f44eb633d`

```dockerfile
```

-	Layers:
	-	`sha256:30e64fea10efcce7c7098d39a162a0e7c6896851c732ae073061b70bb7815a6a`  
		Last Modified: Wed, 05 Nov 2025 06:46:50 GMT  
		Size: 5.7 MB (5705608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e111ba71a44f8b3e1269ea03985ee7901177991521912f617b622b30bfd202e`  
		Last Modified: Wed, 05 Nov 2025 06:46:51 GMT  
		Size: 39.4 KB (39403 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java17-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:7207e8f5ff1b23b29e205f11ecf08e25332358107b9d41d9b486d23c92db8f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.7 MB (457681598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893967e0c8a1b0fa3c6eff18101102e613a2eb2899c8fe6ebbcac96d548c8bf0`
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
# Thu, 13 Nov 2025 23:13:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:13:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:13:26 GMT
ENV JAVA_VERSION=jdk-17.0.17+10_openj9-0.56.0
# Thu, 13 Nov 2025 23:17:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='56f11335a3c67f96f0dc8ca4ebe02239fa300fd871ab46de27103666998b2aec';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_aarch64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='5cc9ac62b665c1c61860dbfe8d06f2f30d1f0439f1e93f6ae09770ca91949feb';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_ppc64le_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        amd64|x86_64)          ESUM='13c8bbbb9ffa57b33a48ca018fd281e69dd6fdbb4e96ca7df72a49db614d899c';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_x64_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        s390x)          ESUM='bc147228dc80b3add4a64b441cf3fe69e06b0b8ad3cd86444d7de2fd7c0fea86';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.17%2B10_openj9-0.56.0/ibm-semeru-open-jre_s390x_linux_17.0.17_10_openj9-0.56.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 13 Nov 2025 23:17:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:17:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 13 Nov 2025 23:17:34 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="2a955d97c6ed7d01fbf0392f3e2920129bcd541b259e894f441e411bac3bbe65576bcb3a314f06d624c9d70040828d26aa8a2c4f39d225d73f6a3db7523aa3ba";     TOMCAT_VERSION="9.0.111";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Fri, 14 Nov 2025 00:23:59 GMT
USER root
# Fri, 14 Nov 2025 00:23:59 GMT
ARG LIBERTY_VERSION=25.0.0.11
# Fri, 14 Nov 2025 00:23:59 GMT
ARG LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f
# Fri, 14 Nov 2025 00:23:59 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip
# Fri, 14 Nov 2025 00:23:59 GMT
ARG LIBERTY_BUILD_LABEL=cl251120251020-0302
# Fri, 14 Nov 2025 00:23:59 GMT
ARG OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:23:59 GMT
ARG VERBOSE=false
# Fri, 14 Nov 2025 00:23:59 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl251120251020-0302 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.11 liberty.version=25.0.0.11 io.openliberty.version=25.0.0.11
# Fri, 14 Nov 2025 00:23:59 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Fri, 14 Nov 2025 00:23:59 GMT
COPY helpers /opt/ol/helpers # buildkit
# Fri, 14 Nov 2025 00:23:59 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Fri, 14 Nov 2025 00:25:45 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Fri, 14 Nov 2025 00:25:58 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Fri, 14 Nov 2025 00:25:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/liberty/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Fri, 14 Nov 2025 00:25:58 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Fri, 14 Nov 2025 00:25:58 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml     && ln -s /logs /liberty/logs     && mkdir /serviceability     && chown -R 1001:0 /serviceability     && chmod -R g+rw /serviceability # buildkit
# Fri, 14 Nov 2025 00:26:24 GMT
# ARGS: LIBERTY_VERSION=25.0.0.11 LIBERTY_SHA=baf4c6a66207ec55f69aebc17e300067351e479f LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.11/openliberty-runtime-25.0.0.11.zip LIBERTY_BUILD_LABEL=cl251120251020-0302 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Fri, 14 Nov 2025 00:26:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 14 Nov 2025 00:26:24 GMT
USER 1001
# Fri, 14 Nov 2025 00:26:24 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Fri, 14 Nov 2025 00:26:24 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Fri, 14 Nov 2025 00:26:24 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d15824160d0d57e05338a0838871eb3f72224cf5de518ea6af54ba25e7e9c4da`  
		Last Modified: Thu, 13 Nov 2025 23:02:52 GMT  
		Size: 28.0 MB (28003285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ebf2f3fd42b59c867dbc8ee4d6fb881babedba503d35eec208ade18e4a3820`  
		Last Modified: Thu, 13 Nov 2025 23:14:34 GMT  
		Size: 12.2 MB (12219661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643db97244a4b9ad00c155561851c5bf7707bc724245c4e578ee9b8832a3bb3b`  
		Last Modified: Thu, 13 Nov 2025 23:18:04 GMT  
		Size: 54.2 MB (54201914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36379231f1f7cacfe784fdcb94367c6d6edd366528b4f5fcae5d3164a89bbca`  
		Last Modified: Thu, 13 Nov 2025 23:18:01 GMT  
		Size: 5.2 MB (5197553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24848187883f0192c6fdcc13ec9f0187bfe46e44b1067d46b6a7387333c77c6c`  
		Last Modified: Fri, 14 Nov 2025 00:25:23 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c0c80974e77ffc5b7d1b574b9f5d6048ac7fd5fea4a612139316c4731ae2c3`  
		Last Modified: Fri, 14 Nov 2025 00:25:23 GMT  
		Size: 12.3 KB (12280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b36b94909a7a67110b2a44f45916573f2916132ffdf12c46ae9c7cf0d06e210`  
		Last Modified: Fri, 14 Nov 2025 00:25:23 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba32a1fdb62dc250b6682f44c7c2509b74c048f416f4a5b73f0e634f21b3d76`  
		Last Modified: Fri, 14 Nov 2025 00:27:08 GMT  
		Size: 33.1 KB (33110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e196e5da05b9626b474e059d2e152645d19f4bad97739f49fa3549d2eb29e2e8`  
		Last Modified: Fri, 14 Nov 2025 00:27:03 GMT  
		Size: 343.9 MB (343937925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587156b840d9765ff94dcb9e156861e2a7438b722aba840e231df245bd06a3e1`  
		Last Modified: Fri, 14 Nov 2025 00:27:08 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af9552c048ee05c9bbaa3a0786c9db9ea78903d568a0d0e770127b659f45111`  
		Last Modified: Fri, 14 Nov 2025 00:27:08 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d516d902539ffa039bcd6943d578dab198319e5c0802c20de9d4de94836a2e5`  
		Last Modified: Fri, 14 Nov 2025 00:27:10 GMT  
		Size: 14.1 MB (14059801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java17-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:b10e918b9e0e673dbc5bf8d6a06b09de94912e991b6ede942d7d743d3e5616e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5741373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5ca131fd408cc81c8f8390130787143167cbfe14444384d983b51e8d5c9b3`

```dockerfile
```

-	Layers:
	-	`sha256:2c71a34eb51d44cab7a482d7cdbc3f650cf43122f46350bcff9a5353aba47272`  
		Last Modified: Fri, 14 Nov 2025 03:52:35 GMT  
		Size: 5.7 MB (5702004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074dc0f2f389baaf68d5af20179d2e1dce80a0183803ce5d8fa7622fac6508e6`  
		Last Modified: Fri, 14 Nov 2025 03:52:36 GMT  
		Size: 39.4 KB (39369 bytes)  
		MIME: application/vnd.in-toto+json
