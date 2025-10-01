## `open-liberty:full-java11-openj9`

```console
$ docker pull open-liberty@sha256:ac48b8910cf1ac84fabd6cb54055cba34594baf539ed210680bb0c1645e699cc
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

### `open-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull open-liberty@sha256:8496863d4fb0c7e4c3033e9ffd56707e82ead4107c1ef5064c9ba6eb513ecdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.7 MB (458735408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d699a001f78918c3193c73449ee773bf0977240baeef05dcf712eab03bb42c7`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 16:09:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Sep 2025 16:09:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Thu, 11 Sep 2025 16:09:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Sep 2025 16:09:27 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 11 Sep 2025 16:09:27 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7";     TOMCAT_VERSION="9.0.109";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
USER root
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_VERSION=25.0.0.9
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_BUILD_LABEL=cl250920250821-1629
# Thu, 11 Sep 2025 16:09:27 GMT
ARG OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:09:27 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:09:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250920250821-1629 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.9 liberty.version=25.0.0.9 io.openliberty.version=25.0.0.9
# Thu, 11 Sep 2025 16:09:27 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 11 Sep 2025 16:09:27 GMT
USER 1001
# Thu, 11 Sep 2025 16:09:27 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 11 Sep 2025 16:09:27 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 11 Sep 2025 16:09:27 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b873419fc0b2d4f4451227a4a2ba55f57f9661c84d1b7df21f525e661bc6132`  
		Last Modified: Tue, 30 Sep 2025 18:05:35 GMT  
		Size: 12.2 MB (12171722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a018259d434c97002211cfebb38bd45ba594bbaf5069af0eb9146e76bba795`  
		Last Modified: Tue, 30 Sep 2025 18:05:39 GMT  
		Size: 55.8 MB (55756702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8380a34b46833487ad21d80ecccaef99ce0b50c4c2ead64bc20b5dd701b345c9`  
		Last Modified: Tue, 30 Sep 2025 18:05:34 GMT  
		Size: 4.4 MB (4441544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e61dfb8385b9688625c4150aa31ed3831a77fad530f434adb8640dfae124210`  
		Last Modified: Tue, 30 Sep 2025 21:21:07 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52388d27c7ffbfa9df77a1693fab682808fe2921ed88e6d403511023c13151e4`  
		Last Modified: Tue, 30 Sep 2025 21:22:04 GMT  
		Size: 12.5 KB (12460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5e08d4289b78d6f8482b5a4c03b37ef79389c9c8a3287b77404a88a39911c8`  
		Last Modified: Tue, 30 Sep 2025 21:22:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d0ee7ebda66b4588abe113381ed9dcad61b856eb8704b1d2c809312240e43c`  
		Last Modified: Tue, 30 Sep 2025 21:22:04 GMT  
		Size: 31.7 KB (31747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500d303652549b3b60cb1982e1abfb286959202e44e2d5bbbd0023b8e22235f8`  
		Last Modified: Wed, 01 Oct 2025 15:15:53 GMT  
		Size: 343.4 MB (343352234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d63946f1044af7d249b52ffaad39946228a29d7a73063c4da080b4706060a2d`  
		Last Modified: Tue, 30 Sep 2025 21:22:04 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02300ff28a2c16cd4a2e0e3ae0ec7ffd720eaa49a1789f79e2f8cd5329ca6539`  
		Last Modified: Tue, 30 Sep 2025 21:22:04 GMT  
		Size: 13.9 KB (13866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd42f478a1f134a2ec520e7434589fa6a55897a5fc8f8b674afed51b6a6cfae0`  
		Last Modified: Tue, 30 Sep 2025 21:22:05 GMT  
		Size: 13.4 MB (13415854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:65bde8b9cbc17068350b916dacb85236ba3f36a7e77a4393e07c85d7bcdde84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89b5deec651ee122602f3212853bb1ebdbf902d4fba97b847120fffac67cdc8`

```dockerfile
```

-	Layers:
	-	`sha256:a1f5d3a4da0e451dcdb05e427ac5fbf065a0a8a21ea1d98b83dcaf22ea10f7ad`  
		Last Modified: Wed, 01 Oct 2025 15:16:04 GMT  
		Size: 5.7 MB (5716258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe483439a1743cf67aa1383201e0169f2f46bb216d5219cfe1a9e17f157577d`  
		Last Modified: Wed, 01 Oct 2025 15:16:06 GMT  
		Size: 38.8 KB (38818 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:941de4dce4e9780084aecbd8aab7c8ff4ddc16492316633a9afe0f056ff6dead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.5 MB (454481488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe78bcf8679a7d9b1908373ba0a86728dae1576a3d2c1d2956d07268c326d87`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
USER root
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_VERSION=25.0.0.9
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_BUILD_LABEL=cl250920250821-1629
# Thu, 11 Sep 2025 16:09:27 GMT
ARG OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:09:27 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:09:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250920250821-1629 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.9 liberty.version=25.0.0.9 io.openliberty.version=25.0.0.9
# Thu, 11 Sep 2025 16:09:27 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 11 Sep 2025 16:09:27 GMT
USER 1001
# Thu, 11 Sep 2025 16:09:27 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 11 Sep 2025 16:09:27 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 11 Sep 2025 16:09:27 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ae624de3eeb0edb3e4a120905423464cf816ca0d11b0b199c055f29c2e6609`  
		Last Modified: Tue, 02 Sep 2025 01:29:48 GMT  
		Size: 12.1 MB (12130364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f476b0a9b46a567ec6ac2f3ca3531c161fb736e6f16e7f71e0b9224d64c1b0`  
		Last Modified: Tue, 02 Sep 2025 01:35:52 GMT  
		Size: 54.0 MB (54012643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac97f82108888e43ccadfb43f296c6e547e0318b241744c4db85e4b5ccd1eb6`  
		Last Modified: Tue, 02 Sep 2025 01:35:49 GMT  
		Size: 4.3 MB (4254857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fb0c78eedc1d4f9f8f4b34ebd9d07f1ce5d153cb6a58ec21fd366316bd43f5`  
		Last Modified: Thu, 11 Sep 2025 17:55:53 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd4784ca18f873403282d323b19c881a77139c0178fda5495ebf47043fdbe57`  
		Last Modified: Thu, 11 Sep 2025 17:55:53 GMT  
		Size: 12.5 KB (12462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142e1ac175c4483a75d5d061757cc5a623ab0134fdd7feb0153eddfb047643af`  
		Last Modified: Thu, 11 Sep 2025 17:55:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbf3b03c10163ca99c5db0f67e1bf4f8943016b3567fe18b0fbb5ad658e4915`  
		Last Modified: Thu, 11 Sep 2025 17:55:54 GMT  
		Size: 42.3 KB (42323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef42dd74f3dc0cc1ee2b04be8313db0abf0d2f6074bda38689abeff86521a8a`  
		Last Modified: Thu, 11 Sep 2025 21:15:58 GMT  
		Size: 343.4 MB (343352467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3641b1fe15e6ed57f43681a1a50be20649df4bf31f0487bbf77e698163f302b2`  
		Last Modified: Thu, 11 Sep 2025 17:55:52 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2ef774745096539ef6024aaaaf3c23670d67ac16e2d599271ace6b43c65f2d`  
		Last Modified: Thu, 11 Sep 2025 17:55:54 GMT  
		Size: 13.9 KB (13856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a4894ea74782a7dedd6d35abd48faa1dbb7bfb24d67509270a76c2a412d1f0`  
		Last Modified: Thu, 11 Sep 2025 21:15:46 GMT  
		Size: 13.3 MB (13298704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:78558eed9e2a8846e6645b154e1ee62dd91d4ba0152933a1fe64ad8c1fe33eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5750054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eed3527b414749725035f8ec547bcd9ec0fce067b9c8c81946fe0607329a568`

```dockerfile
```

-	Layers:
	-	`sha256:77f744f7b76bb43ceb8923d91302b4f773f13318b9c6e473d4e877e8cdec8858`  
		Last Modified: Thu, 11 Sep 2025 20:48:00 GMT  
		Size: 5.7 MB (5711109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f205af7c08a79aa7e0d6cde21e9d3dbdbae5aacb9624628360eac4e5e6914c8a`  
		Last Modified: Thu, 11 Sep 2025 20:48:01 GMT  
		Size: 38.9 KB (38945 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:7fdebcca3255bb5d4e0df1e15151507add892912a5ee2578d12493a32903155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463804668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c787106120961714105e518f25a5f677cef12aa34e2269464cd418975ed808`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
USER root
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_VERSION=25.0.0.9
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_BUILD_LABEL=cl250920250821-1629
# Thu, 11 Sep 2025 16:09:27 GMT
ARG OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:09:27 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:09:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250920250821-1629 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.9 liberty.version=25.0.0.9 io.openliberty.version=25.0.0.9
# Thu, 11 Sep 2025 16:09:27 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 11 Sep 2025 16:09:27 GMT
USER 1001
# Thu, 11 Sep 2025 16:09:27 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 11 Sep 2025 16:09:27 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 11 Sep 2025 16:09:27 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd05e0384f89e87f39bbca5882dc09e12e30daf4c6b9267897a05fc765378ae`  
		Last Modified: Tue, 02 Sep 2025 00:35:06 GMT  
		Size: 12.9 MB (12894660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ec2c99ca76967222d47b87ab651022c177583d30b6ba6e52d9d053a13b1acd`  
		Last Modified: Tue, 02 Sep 2025 00:44:06 GMT  
		Size: 57.6 MB (57604774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d287cf69b9554d2cfdbfc670598312ba27a69c49097f699dcdf54f605938086b`  
		Last Modified: Tue, 02 Sep 2025 00:43:59 GMT  
		Size: 3.5 MB (3511616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcb43d3f9998a0ed62c66ece989f439e8c06e98c1ed9984c730bd328cfb1b5d`  
		Last Modified: Tue, 02 Sep 2025 06:01:08 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ae6bf1ecc2e8db38d969e2c2b95eff4c261ea7a9779b21f002388a97bfc0e7`  
		Last Modified: Tue, 02 Sep 2025 06:01:08 GMT  
		Size: 12.5 KB (12460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a045ee766f7856c5a80abfb389601fe4edb90e238149266a085733bacfa5e258`  
		Last Modified: Tue, 02 Sep 2025 06:01:08 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14fd1d4263129fc6d1000d07877b870a527ac1205b126f08c2d555134a90a1f`  
		Last Modified: Thu, 11 Sep 2025 18:14:56 GMT  
		Size: 36.5 KB (36496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f3bf932e6d3fc42a0dde9e3c4ff68d1f0fd377a499738556bd031eae1101b5`  
		Last Modified: Thu, 11 Sep 2025 21:16:14 GMT  
		Size: 343.4 MB (343352748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0fade4918401e8a7490ab942571c7a7794ac169638b163631a15b3775f716d`  
		Last Modified: Thu, 11 Sep 2025 18:14:56 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba66deedc16ec74e3fc6e0ae9c315c180ba495d28dc94bb5e8d7e54da57dee`  
		Last Modified: Thu, 11 Sep 2025 18:14:56 GMT  
		Size: 13.9 KB (13880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91aa4bf88a83fb636a9b095304b67ac48bf6ec9fcf3ee608b46a4a500de6bc5`  
		Last Modified: Thu, 11 Sep 2025 18:14:58 GMT  
		Size: 11.9 MB (11932456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:2e05687e11bb87a930b1f799a0b6b6d53a2903bb0aa41f24948bb9f956e97285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f9ee79175d2d2bac8d7bdd1fa338e982e3d645920c3e723d1b71189d14d969`

```dockerfile
```

-	Layers:
	-	`sha256:2db1790411e4e101f041cbf9a19793500fa29275537feab9e45b9156d1553f7e`  
		Last Modified: Thu, 11 Sep 2025 20:48:06 GMT  
		Size: 5.7 MB (5717370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdee80792ca4d6820b454b8202612307238abf3442d59f8496d0ee944bbee32`  
		Last Modified: Thu, 11 Sep 2025 20:48:07 GMT  
		Size: 38.9 KB (38852 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull open-liberty@sha256:6998e7688295ac67784ced97d853091c3c993ddc39188b53d4d57786cea3f420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.3 MB (456340285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dca8bbfeefecd3f1d86184fed4e5b959b724ab3796771ac40e516271cf2839f`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Wed, 13 Aug 2025 16:09:03 GMT
ARG RELEASE
# Wed, 13 Aug 2025 16:09:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 16:09:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 13 Aug 2025 16:09:03 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Wed, 13 Aug 2025 16:09:03 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 16:09:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 13 Aug 2025 16:09:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_VERSION=jdk-11.0.28+6_openj9-0.53.0
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4f4fe23f89ff85bf3715ec5fed8ef7e93699308ee57297bd8934cfa6675b14c9';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36670add16de97abf89151d8adeea0990c4148bf36ea130e5bf97fb6d1020247';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='690d72d2662eba4a6c1ad04a99d1557e36d86d58e9a5cba60597ae393ba8ef26';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='a7d40e586d08746a4373ba77b72344c4122cf30ed1b3a792d33d6cf6e5c96aee';          BINARY_URL='https://github.com/ibmruntimes/semeru11-binaries/releases/download/jdk-11.0.28%2B6_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_11.0.28_6_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Aug 2025 16:09:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 13 Aug 2025 16:09:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
USER root
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_VERSION=25.0.0.9
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip
# Thu, 11 Sep 2025 16:09:27 GMT
ARG LIBERTY_BUILD_LABEL=cl250920250821-1629
# Thu, 11 Sep 2025 16:09:27 GMT
ARG OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:09:27 GMT
ARG VERBOSE=false
# Thu, 11 Sep 2025 16:09:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250920250821-1629 org.opencontainers.image.description=This image contains the Open Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty org.opencontainers.image.version=25.0.0.9 liberty.version=25.0.0.9 io.openliberty.version=25.0.0.9
# Thu, 11 Sep 2025 16:09:27 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
COPY helpers /opt/ol/helpers # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9 LIBERTY_SHA=951b549b9f2bf42e9ddf753a089524d2e4d24276 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/openliberty-runtime/25.0.0.9/openliberty-runtime-25.0.0.9.zip LIBERTY_BUILD_LABEL=cl250920250821-1629 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Thu, 11 Sep 2025 16:09:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 11 Sep 2025 16:09:27 GMT
USER 1001
# Thu, 11 Sep 2025 16:09:27 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Thu, 11 Sep 2025 16:09:27 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Thu, 11 Sep 2025 16:09:27 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69dd744c6ce11f9bcc42b570d4944d0ecf9b125f3d1c222308ced56deb59072`  
		Last Modified: Mon, 01 Sep 2025 23:24:49 GMT  
		Size: 12.2 MB (12219976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f642f9167f61ba7b21e62a718d8c297bcf9e48728dcd239c5c9a7019e06704ca`  
		Last Modified: Mon, 01 Sep 2025 23:33:46 GMT  
		Size: 54.3 MB (54330700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611ab9bf5fc6a77b653a681f0f3b8a631253a3064c83f66011df823e04531ab`  
		Last Modified: Mon, 01 Sep 2025 23:33:42 GMT  
		Size: 4.6 MB (4606409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00624cac97e69b034e34c6a603ba633ade2a2f8226996e2e09ae580c95dda8`  
		Last Modified: Thu, 11 Sep 2025 18:17:02 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0e33589bae1a96779e9d8b82b9ab6148c7ffd601bc8b947234b39a36d6a504`  
		Last Modified: Thu, 11 Sep 2025 17:36:28 GMT  
		Size: 12.5 KB (12460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6718976fcc137f041f73aa5b25eeafb3c8d5b5212ff0b0118c1801529d422f`  
		Last Modified: Thu, 11 Sep 2025 17:36:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fedb75eae93957819ba3e6670c694c294fecfe1ae10cb971122585f9822383`  
		Last Modified: Thu, 11 Sep 2025 18:34:47 GMT  
		Size: 33.1 KB (33111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d986d360383a163c09d338d8596d32a898c12c4ffb6c12d1c053f668ef9890`  
		Last Modified: Thu, 11 Sep 2025 20:46:12 GMT  
		Size: 343.4 MB (343351974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0fac44749539e6d1884db17680032f339cff75e6cb6206053c73fc714ce987`  
		Last Modified: Thu, 11 Sep 2025 18:34:46 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbaba1d5f368186f4249dca964539ad2bd0474d4492679742ba59e269f05152`  
		Last Modified: Thu, 11 Sep 2025 18:34:48 GMT  
		Size: 13.9 KB (13871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18c3f36018bf6a31f8ea158b7d1638e93068a8ac7f3d3b0967294c3320563a7`  
		Last Modified: Thu, 11 Sep 2025 20:45:52 GMT  
		Size: 13.8 MB (13765768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:full-java11-openj9` - unknown; unknown

```console
$ docker pull open-liberty@sha256:3a2421cbb8fe54f27d7de8ec57c539b328b1d40b9aba8de928a6cc86261678dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e223be6585f3fbcff4882c909e0140a611c0ad4a2d13f78ed0fccf3af1e71627`

```dockerfile
```

-	Layers:
	-	`sha256:faa4faa0590c4e36ba909120e06ef9bd9e90eb479e63d994b850991b41ed8777`  
		Last Modified: Thu, 11 Sep 2025 21:16:53 GMT  
		Size: 5.7 MB (5713766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229e8acdab1eaf3d1e5825f784ba97afc69a5df1a367d7eec01c27bbd20039d7`  
		Last Modified: Thu, 11 Sep 2025 21:16:55 GMT  
		Size: 38.8 KB (38817 bytes)  
		MIME: application/vnd.in-toto+json
