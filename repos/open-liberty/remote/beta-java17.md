## `open-liberty:beta-java17`

```console
$ docker pull open-liberty@sha256:5e47f92933128587f822c898c7219995fbbb4aa910d37369e507f2c45599e95c
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

### `open-liberty:beta-java17` - linux; amd64

```console
$ docker pull open-liberty@sha256:2d792e3b7dc31c31d47b9b759eeadb46bc1eae113c4f7b36e7e3663e6213caee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483146679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05f84c7e22e8935bb6223d80e6e629fd30919e4c6a32cc07099f96951e87f3e`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Aug 2025 13:28:10 GMT
ARG RELEASE
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Aug 2025 13:28:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 13:28:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 13:28:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f80dcecc7ea669de08fc8ac807e9360fecaa0199051d6f23ececbb5089af3fb7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d61683565e694404ba09b2104c0cbbcde50c03b97bad50cb50ed7b324a08fca7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='348de4a541d7e679e027942c4f056fa7c2151711cd3c86d0b582879add89fea8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='f9cbae653a4f93dbb249e345c0f2957ec9423a913865efb000b62282425ced5d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
USER root
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_VERSION=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_BUILD_LABEL=cl250820250727-1902
# Tue, 12 Aug 2025 13:28:10 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250820250727-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.9-beta liberty.version=25.0.0.9-beta io.openliberty.version=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 12 Aug 2025 13:28:10 GMT
USER 1001
# Tue, 12 Aug 2025 13:28:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:28:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/opt/ol/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb91f569b82e1986d947224c68395fd2fd6a0b92df317398ee6a21e7eefe3a6`  
		Last Modified: Tue, 02 Sep 2025 00:13:38 GMT  
		Size: 12.2 MB (12171866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ec546651956bb2815833c2b6d6a12079b7509f2637e7b91be9f4524ec7eb8c`  
		Last Modified: Tue, 02 Sep 2025 00:13:43 GMT  
		Size: 55.1 MB (55093189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709ce8b947539e8d91b464725ece87e7704afa1d9d7acc7d4fe1dd23c8e4b0f9`  
		Last Modified: Tue, 02 Sep 2025 00:13:37 GMT  
		Size: 5.1 MB (5137736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f00e016e2f6c8d57ad39e2e67b0415db2e9df2de4926e004212a52248c14ff7`  
		Last Modified: Tue, 02 Sep 2025 01:45:47 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f08367cf51e0db77cd717ef538ecf5097ab15a8146f43b516a785ab2c2f0a6`  
		Last Modified: Tue, 02 Sep 2025 01:45:47 GMT  
		Size: 12.5 KB (12464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338c320e7bdf3e198ec0a9a0cad020314f811fc9181a757354e081ee14a31dcc`  
		Last Modified: Tue, 02 Sep 2025 01:45:47 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4f6b2a4eff38ea67bc91881092bd54f7c1455ff4f36f77182f6454d9cbc73`  
		Last Modified: Tue, 02 Sep 2025 01:45:47 GMT  
		Size: 31.7 KB (31746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598f3aff1995320cde98d039901f57e2672d585424408dd022218e94a198e595`  
		Last Modified: Tue, 02 Sep 2025 08:08:48 GMT  
		Size: 366.8 MB (366804291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a117251227a85a405338784bbdf1a5068c054f1ed09bbfdad7e58a600e76ab`  
		Last Modified: Tue, 02 Sep 2025 01:45:47 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a39765f00e2864807ca95c3292c71011d3cedbd414d9a698f7eb29eea4172d`  
		Last Modified: Tue, 02 Sep 2025 01:45:47 GMT  
		Size: 13.9 KB (13862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ee5ca9a2659b061cfe7d551647007c97a1592e8f44d1016b2b9684501fe0fb`  
		Last Modified: Tue, 02 Sep 2025 01:45:49 GMT  
		Size: 14.3 MB (14342243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:5d2a51a4f800f6503708f4db594502cb93a286260047da8ec58c96a712df3103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc1c72ce6eedd13f27612ad5a33ca4f82882c363c85aa480a9fb2e3dad86269`

```dockerfile
```

-	Layers:
	-	`sha256:7dcc84aad6895737a6dd780453c1036497a45c748307525e938c7b509043a0cf`  
		Last Modified: Tue, 02 Sep 2025 02:48:21 GMT  
		Size: 5.8 MB (5779163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a5f4e364de5125a469c7b5374c72e26ce1cdb3edde6d64cccdb5c17b485edc`  
		Last Modified: Tue, 02 Sep 2025 02:48:22 GMT  
		Size: 38.9 KB (38940 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; arm64 variant v8

```console
$ docker pull open-liberty@sha256:b4bfe48c11728aa697b8eb029fb2da2eb8e94ff8754dd82c3fe372b80c6003c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.0 MB (477997411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ddbaee7e3f80fdc2eedab8ec082eca333e63152bb96031627edc2219ccebb0`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Aug 2025 13:28:10 GMT
ARG RELEASE
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Aug 2025 13:28:10 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 13:28:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 13:28:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f80dcecc7ea669de08fc8ac807e9360fecaa0199051d6f23ececbb5089af3fb7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d61683565e694404ba09b2104c0cbbcde50c03b97bad50cb50ed7b324a08fca7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='348de4a541d7e679e027942c4f056fa7c2151711cd3c86d0b582879add89fea8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='f9cbae653a4f93dbb249e345c0f2957ec9423a913865efb000b62282425ced5d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
USER root
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_VERSION=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_BUILD_LABEL=cl250820250727-1902
# Tue, 12 Aug 2025 13:28:10 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250820250727-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.9-beta liberty.version=25.0.0.9-beta io.openliberty.version=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 12 Aug 2025 13:28:10 GMT
USER 1001
# Tue, 12 Aug 2025 13:28:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:28:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:28:10 GMT
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
	-	`sha256:227de48431b4b1d9d30256717a6ea34ba9b470bfd0d653c338fa663dec3e08d4`  
		Last Modified: Tue, 02 Sep 2025 01:40:05 GMT  
		Size: 53.4 MB (53357599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c2ff2f1e2aae9bd8d64d49fb5cf1ab3d64e639aff36a679f6837fc289d3fbc`  
		Last Modified: Tue, 02 Sep 2025 01:39:59 GMT  
		Size: 4.9 MB (4860063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f6d085e27b0ab37cc4d6793a688f16a3f752f637f662a107e505292afbcb0`  
		Last Modified: Tue, 02 Sep 2025 05:11:44 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff4d31ff6ef0ca275ef7e74e534b477298c50a56135b77bca71008b09912132`  
		Last Modified: Tue, 02 Sep 2025 05:11:44 GMT  
		Size: 12.5 KB (12461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f165d9d0dd8f98e24723288cd5a2e72315f4e6c38811e0da7ded31bf2bd5ef`  
		Last Modified: Tue, 02 Sep 2025 05:11:44 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcee050259bf4cce71ca33f025453be704d46bfdb035dcb632af9dc860692b4`  
		Last Modified: Tue, 02 Sep 2025 05:11:44 GMT  
		Size: 42.3 KB (42322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5105b2818e41ef37d9e4967d811756052857c736f5643e7aea964e6c6bf6d7`  
		Last Modified: Wed, 03 Sep 2025 13:01:34 GMT  
		Size: 366.8 MB (366804507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36883a086129ffc00cdd9c69aa0af9eb0dee6cdfd8b2a3e3a83c595e24abb97`  
		Last Modified: Tue, 02 Sep 2025 05:11:45 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b7008bb67cc50113aa3015e3127b39d82d88ed32e9d3deb0eb93849e1d7782`  
		Last Modified: Tue, 02 Sep 2025 05:11:45 GMT  
		Size: 13.9 KB (13871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25194238297894aecd7ae74736237704327c497e8a01030988fff47773b2545`  
		Last Modified: Tue, 02 Sep 2025 05:11:46 GMT  
		Size: 13.4 MB (13412408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:1f6151834d2a25ea5ed8b05ff2d3755be0955f4c6c52abfa3f4744a90a1a1cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5816591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918ea7068172f1460bc2bf08e378d0e56680d69d3457cd1bf7b76ab6b26db630`

```dockerfile
```

-	Layers:
	-	`sha256:93577c469bfaadffcc1c8d0634c411dc631979f6c0bd3251d5bfef577ce47dba`  
		Last Modified: Tue, 02 Sep 2025 08:48:27 GMT  
		Size: 5.8 MB (5777523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0d2a5e7aeb3035ca032e4a4b0ae42684b2c59cbe170463d185fc1084d2a69f`  
		Last Modified: Tue, 02 Sep 2025 08:48:28 GMT  
		Size: 39.1 KB (39068 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; ppc64le

```console
$ docker pull open-liberty@sha256:05ef58e3ffd7c4a02a8108a1a735072ae00b963ed3f6df99714277a0c4076b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.1 MB (487098419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0810e2c69ee263b2af3dc74d367a6029a671c6cc3bdeefb0cafa19e7729c2797`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Aug 2025 13:28:10 GMT
ARG RELEASE
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Aug 2025 13:28:10 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 13:28:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 13:28:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f80dcecc7ea669de08fc8ac807e9360fecaa0199051d6f23ececbb5089af3fb7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d61683565e694404ba09b2104c0cbbcde50c03b97bad50cb50ed7b324a08fca7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='348de4a541d7e679e027942c4f056fa7c2151711cd3c86d0b582879add89fea8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='f9cbae653a4f93dbb249e345c0f2957ec9423a913865efb000b62282425ced5d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
USER root
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_VERSION=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_BUILD_LABEL=cl250820250727-1902
# Tue, 12 Aug 2025 13:28:10 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250820250727-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.9-beta liberty.version=25.0.0.9-beta io.openliberty.version=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 12 Aug 2025 13:28:10 GMT
USER 1001
# Tue, 12 Aug 2025 13:28:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:28:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:28:10 GMT
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
	-	`sha256:a0794023ee760eef22ca43493d37f23f37e7faecd83d8397f213dc9dc55653f6`  
		Last Modified: Tue, 02 Sep 2025 00:50:20 GMT  
		Size: 56.9 MB (56920769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb7ed0f763090cb5b602be8efce7dede4b10c09b79d0df7db3efbb47b042e7e`  
		Last Modified: Tue, 02 Sep 2025 00:50:14 GMT  
		Size: 3.9 MB (3858418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4580a706008fa85294cf8a253ded9b73bab2c11d1d6c21ec8c403517bd199b`  
		Last Modified: Tue, 02 Sep 2025 06:04:12 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c1d32756801fbeb3217af5802161e513aea5af0a60368188d2c47ff7861c2d`  
		Last Modified: Tue, 02 Sep 2025 06:04:11 GMT  
		Size: 12.5 KB (12465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a77d5c5a934c0f2765f20f0e8eda4c120b6782f98d68e8faf52e24a77048df`  
		Last Modified: Tue, 02 Sep 2025 06:04:11 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dfdbf330abbb548896511605356d4fd474d309c09dd79e9f6e9b874a420165`  
		Last Modified: Tue, 02 Sep 2025 06:04:11 GMT  
		Size: 36.5 KB (36492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f6b6e4dd6819798bf39f172deaa7753fbaa921059840b7879044a7c0579bbf`  
		Last Modified: Tue, 02 Sep 2025 06:04:06 GMT  
		Size: 366.8 MB (366804535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c4a593885ec00c0048ce2bf109334d31bcdb37c287ec34e14b5b7ffa38705`  
		Last Modified: Tue, 02 Sep 2025 06:04:11 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a534ee5ad93211f71bfbdaa5c499f9fdfa0572ba133b424fe99e143bacf089`  
		Last Modified: Tue, 02 Sep 2025 06:04:11 GMT  
		Size: 13.9 KB (13868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b678e2fe0fdbce3a885066ca3947985f11a6dcc9ad0673ed1168e16cffcf4898`  
		Last Modified: Tue, 02 Sep 2025 06:04:12 GMT  
		Size: 12.1 MB (12111636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:3ca093f41faa2ab818ae33dc2a82799c9295c714e6db48ec78185681196a3021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8217fa1ca1d8122354ba3ab608e31b3dadb9cceb6caffc7f2bfa746596223fd`

```dockerfile
```

-	Layers:
	-	`sha256:4063fc2a9a1b0335c05ce054f523310726a167ece3a081c65a6a6074aecefceb`  
		Last Modified: Tue, 02 Sep 2025 08:48:33 GMT  
		Size: 5.8 MB (5783784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456c9d378af1d53465fe54564b64b59e81eda18d50b93ba2133f2c2e65bbb581`  
		Last Modified: Tue, 02 Sep 2025 08:48:34 GMT  
		Size: 39.0 KB (38974 bytes)  
		MIME: application/vnd.in-toto+json

### `open-liberty:beta-java17` - linux; s390x

```console
$ docker pull open-liberty@sha256:2cc960efbf6d5211813d8928552e43a0a54d69ce8c9807b589cc2ffe91c95960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480368535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a25411989e0206660c302530c2ca8ee50b8025f15a7c5f251412cf509e7c47`
-	Entrypoint: `["\/opt\/ol\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ol\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 12 Aug 2025 13:28:10 GMT
ARG RELEASE
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Aug 2025 13:28:10 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 12 Aug 2025 13:28:10 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 13:28:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 Aug 2025 13:28:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_VERSION=jdk-17.0.16+8_openj9-0.53.0
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f80dcecc7ea669de08fc8ac807e9360fecaa0199051d6f23ececbb5089af3fb7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_aarch64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='d61683565e694404ba09b2104c0cbbcde50c03b97bad50cb50ed7b324a08fca7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_ppc64le_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        amd64|x86_64)          ESUM='348de4a541d7e679e027942c4f056fa7c2151711cd3c86d0b582879add89fea8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_x64_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        s390x)          ESUM='f9cbae653a4f93dbb249e345c0f2957ec9423a913865efb000b62282425ced5d';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.16%2B8_openj9-0.53.0/ibm-semeru-open-jre_s390x_linux_17.0.16_8_openj9-0.53.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 13:28:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 12 Aug 2025 13:28:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7";     TOMCAT_VERSION="9.0.108";     TOMCAT_FILENAME="apache-tomcat-${TOMCAT_VERSION}.tar.gz";     SUCCESS=;         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     for baseUrl in         https://dlcdn.apache.org/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin         https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin     ; do         if curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${baseUrl}/${TOMCAT_FILENAME}" && [ -s "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz ]; then             SUCCESS=1;             break;         fi;     done;     [ -n "$SUCCESS" ];     echo "${TOMCAT_CHECKSUM}  ${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
USER root
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_VERSION=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip
# Tue, 12 Aug 2025 13:28:10 GMT
ARG LIBERTY_BUILD_LABEL=cl250820250727-1902
# Tue, 12 Aug 2025 13:28:10 GMT
ARG OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
ARG VERBOSE=false
# Tue, 12 Aug 2025 13:28:10 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Melissa Lee, Thomas Watson, Michal Broz, Wendy Raschke org.opencontainers.image.vendor=Open Liberty org.opencontainers.image.url=https://openliberty.io/ org.opencontainers.image.source=https://github.com/OpenLiberty/ci.docker org.opencontainers.image.revision=cl250820250727-1902 org.opencontainers.image.description=This image contains the Open Liberty beta runtime with IBM Semeru Runtime Open Edition OpenJDK 17 with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/OpenLiberty/ci.docker#building-an-application-image org.opencontainers.image.title=Open Liberty Beta org.opencontainers.image.version=25.0.0.9-beta liberty.version=25.0.0.9-beta io.openliberty.version=25.0.0.9-beta
# Tue, 12 Aug 2025 13:28:10 GMT
COPY NOTICES /opt/ol/NOTICES # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY helpers /opt/ol/helpers # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
COPY fixes/ /opt/ol/fixes/ # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_aarch64';          DUMB_INIT_SHA256=b7d648f97154a99c539b63c55979cd29f005f88430fb383007fe3458340b795e;          ;;        amd64|x86_64)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_x86_64';          DUMB_INIT_SHA256=e874b55f3279ca41415d290c512a7ba9d08f98041b28ae7c2acb19a545f1c4df;          ;;        ppc64el|ppc64le)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_ppc64le';          DUMB_INIT_SHA256=3d15e80e29f0f4fa1fc686b00613a2220bc37e83a35283d4b4cca1fbd0a5609f;          ;;        s390x)          DUMB_INIT_URL='https://github.com/Yelp/dumb-init/releases/download/v1.2.5/dumb-init_1.2.5_s390x';          DUMB_INIT_SHA256=47e4601b152fc6dcb1891e66c30ecc62a2939fd7ffd1515a7c30f281cfec53b7;          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /usr/bin/dumb-init ${DUMB_INIT_URL};     echo "${DUMB_INIT_SHA256} */usr/bin/dumb-init" | sha256sum -c -;     chmod +x /usr/bin/dumb-init; # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip openssl wget     && wget -q $LIBERTY_DOWNLOAD_URL -U UA-Open-Liberty-Docker -O /tmp/wlp.zip     && echo "$LIBERTY_SHA  /tmp/wlp.zip" > /tmp/wlp.zip.sha1     && sha1sum -c /tmp/wlp.zip.sha1     && unzip -q /tmp/wlp.zip -d /opt/ol     && rm /tmp/wlp.zip     && rm /tmp/wlp.zip.sha1     && mkdir -p /licenses     && cp /opt/ol/wlp/LICENSE /licenses/     && apt-get remove -y unzip     && apt-get remove -y wget     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && chown -R 1001:0 /opt/ol/wlp     && chmod -R g+rw /opt/ol/wlp # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ol/wlp/bin:/opt/ol/helpers/build:/opt/ol/helpers/runtime LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ol/wlp/output WLP_SKIP_MAXPERMSIZE=true OPENJ9_SCC=true
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN /opt/ol/wlp/bin/server create --template=javaee8     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea     && rm -rf /opt/ol/wlp/usr/servers/defaultServer/server.env # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN mkdir /logs     && mkdir -p /opt/ol/wlp/usr/shared/resources/lib.index.cache     && ln -s /opt/ol/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p $WLP_OUTPUT_DIR/defaultServer     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ol/wlp/usr/servers/defaultServer /config     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && mkdir -p /config/dropins     && mkdir -p /config/apps     && ln -s /opt/ol/wlp /liberty     && ln -s /opt/ol/fixes /fixes     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /opt/ol/wlp/usr     && chmod -R g+rw /opt/ol/wlp/usr     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rw /opt/ol/wlp/output     && chown -R 1001:0 /opt/ol/helpers     && chmod -R ug+rwx /opt/ol/helpers     && chown -R 1001:0 /opt/ol/fixes     && chmod -R g+rwx /opt/ol/fixes     && mkdir /etc/wlp     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && echo "<server description=\"Default Server\"><httpEndpoint id=\"defaultHttpEndpoint\" host=\"*\" /></server>" > /config/configDropins/defaults/open-default-port.xml # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
# ARGS: LIBERTY_VERSION=25.0.0.9-beta LIBERTY_SHA=287f7133048cc72ba5c901c9818ed75eeb56bed2 LIBERTY_DOWNLOAD_URL=https://repo1.maven.org/maven2/io/openliberty/beta/openliberty-runtime/25.0.0.9-beta/openliberty-runtime-25.0.0.9-beta.zip LIBERTY_BUILD_LABEL=cl250820250727-1902 OPENJ9_SCC=true VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ol/wlp/output     && chmod -R g+rwx /opt/ol/wlp/output # buildkit
# Tue, 12 Aug 2025 13:28:10 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Tue, 12 Aug 2025 13:28:10 GMT
USER 1001
# Tue, 12 Aug 2025 13:28:10 GMT
EXPOSE map[9080/tcp:{} 9443/tcp:{}]
# Tue, 12 Aug 2025 13:28:10 GMT
ENTRYPOINT ["/opt/ol/helpers/runtime/docker-server.sh"]
# Tue, 12 Aug 2025 13:28:10 GMT
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
	-	`sha256:1b4d136e940831ab895c3b6c53353634e1d0f18ebc039d30f476f1869bc332f5`  
		Last Modified: Mon, 01 Sep 2025 23:39:02 GMT  
		Size: 54.1 MB (54108962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a37a5984e226244af29e2fc1c58a374c9a0bada0ea2468640bbd067e61d1c7`  
		Last Modified: Mon, 01 Sep 2025 23:39:00 GMT  
		Size: 5.2 MB (5186617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31483a9d767190d2c350fca7757aaf53cf092027f301ab9e2f93b4953bf6cde`  
		Last Modified: Tue, 02 Sep 2025 00:43:51 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771c184d14d3b12bd76d20187332e6f97324de853930a28d6fda0d4ff101cac2`  
		Last Modified: Tue, 02 Sep 2025 00:43:51 GMT  
		Size: 12.5 KB (12461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c54b8bfbc815ac81245491ab6add06fe1302af865307b52f919550114056a51`  
		Last Modified: Tue, 02 Sep 2025 00:43:52 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3639af4bad5d35b4d483f028c1bafc29d6108958313ab12e75505c9f87852afb`  
		Last Modified: Tue, 02 Sep 2025 00:43:53 GMT  
		Size: 33.1 KB (33109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd6d63ff2f5536adf023eea3dd7623bcb736bf2050d46f03e4da68edc34d8c9`  
		Last Modified: Tue, 02 Sep 2025 00:43:40 GMT  
		Size: 366.8 MB (366803995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d28bb0812baa107eafa082430124a52225e30be7d371e016700f280868c60fd`  
		Last Modified: Tue, 02 Sep 2025 00:43:53 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07690560c375551382b2e68dc08fa70dc52efed5c46465d175ac356f2f8cff11`  
		Last Modified: Tue, 02 Sep 2025 00:43:54 GMT  
		Size: 13.9 KB (13862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7f7515ad99c3e497842ae5d82759d35b51989f156ab467962108bb07c9bef5`  
		Last Modified: Tue, 02 Sep 2025 00:43:50 GMT  
		Size: 14.0 MB (13983535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `open-liberty:beta-java17` - unknown; unknown

```console
$ docker pull open-liberty@sha256:3d489beb17987082e26657c1d15a64db734aebe27bcc28a4b1e24061af9d6134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5819119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dea5092838650c5efce78bb431490ad0b423110aad00e4eadceed1d5941a4fd`

```dockerfile
```

-	Layers:
	-	`sha256:259b7e13b1f941906a8d4632aefd6493232ca37af69e00d84502033ae5da7201`  
		Last Modified: Tue, 02 Sep 2025 02:48:38 GMT  
		Size: 5.8 MB (5780180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283fad7347687a74e0e95436d2fceece03200b3e055d4b32067e0aee5c32e5b9`  
		Last Modified: Tue, 02 Sep 2025 02:48:39 GMT  
		Size: 38.9 KB (38939 bytes)  
		MIME: application/vnd.in-toto+json
